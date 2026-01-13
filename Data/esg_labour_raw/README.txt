Industrial Factory Group (IFG) is a multinational manufacturing company operating across Southeast Asia, including factories in Thailand, Vietnam, Indonesia, and Malaysia. The company specializes in electronics assembly, textile production, and automotive components, employing over 300 workers across its regional facilities.

In response to rising global expectations for corporate sustainability and labour rights transparency, IFG has initiated a group-wide ESG (Environmental, Social, Governance) monitoring program. This dashboard focuses on the Social pillar, specifically Labour Standards, in alignment with FTSE Russell and ILO (International Labour Organization) principles.

1. dim_factory.csv
   - factory_id: Unique ID of the factory (e.g., F001)
   - factory_name: Human-readable factory name
   - region: North, South, East, West
   - country: Country of the factory

2. dim_employee.csv
   - employee_id: Unique employee ID
   - factory_id: Links to dim_factory
   - gender: Male or Female
   - is_union_member: 1 if union member, 0 if not
   - salary: Monthly salary in local currency
   - date_of_birth: DOB
   - position_id: position id

3. dim_time.csv
   - date: Daily date from Jan to Jun 2024
   - month: Period in YYYY-MM format

4. dim_position
   - position_id
   - position_name

5. fact_labour_incident.csv
   - incident_id: Unique identifier of incident
   - employee_id: Foreign key to dim_employee
   - incident_date: Date of incident
   - incident_type: Injury, Harassment, or Discrimination
   - lost_time_days: Number of days absent due to incident

6. fact_training.csv
   - training_id: Unique ID for training event
   - employee_id: Foreign key to dim_employee
   - training_date: Date of training
   - training_topic: Labour Rights, Anti-Discrimination, or Safety
   - hours: Number of hours of training

