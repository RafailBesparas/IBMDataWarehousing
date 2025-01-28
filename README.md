# IBMDataWarehousing
As a Data Engineer for a solid waste management company in Brazil, you are building a data warehouse to generate reports on waste collection efficiency, truck fleet performance, recycling rates, operational costs, and environmental impact.

Step1: Create the Database
# The company would like to create a data warehouse so that it can create reports like:
Total waste collected per year per city
Total waste collected per month per city
Total waste collected per quarter per city
Total waste collected per year per truck type
Total waste collected per truck type per city
Total waste collected per truck type per station per city 

# Step2: Create the Dimension and Fact Tables

## MyDimDate
1. dateid
2. date
3 .day
4. month
5. year
6. monthname
7. dayofweek

## MyDimWaste
1. wasteid
2. wastetype
3. description
4. recyclable
5. wastecategory (optional)

## MyDimZone
1. zoneid
2. zonename
3. city
4. region (optional)

## MyFactTrips
1. tripid
2. dateid (foreign key to MyDimDate)
3. wasteid (foreign key to MyDimWaste)
4. zoneid (foreign key to MyDimZone)
5. waste_collected_in_tons
6. trip_number
7. collection_zone

# Step 3: Populate the Tables, Re-create them based on the Data Files
After the initial schema design, operational issues led to changes in data collection. The previous tables (MyDimDate, MyDimWaste, MyDimZone, MyFactTrips) are no longer applicable. The company now provides data in CSV files, introducing new tables: DimTruck and DimStation, reflecting the updated design.

# Step4: Execution
1. Create a Group Set
2. Create a rollup view
3. Create a cube view
4. create a materialized view








