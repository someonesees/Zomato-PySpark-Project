# Zomato-PySpark-Project

#### This project not only explores the capabilities of PySpark for data manipulation and analysis but also integrates advanced techniques to derive meaningful insights from the Zomato dataset. Depending on your interests and objectives, you can emphasize different aspects such as visualization, modeling, or deployment to make the project more comprehensive and impactful.

### Project Outline

#### 1. Introduction
   - Project Title: Zomato Dataset Analysis
   - Description: This project involves data loading, exploration, cleaning, and analysis of a Zomato dataset using PySpark. The goal is to derive insights and perform                          various data transformations.

#### 2. Prerequisites
   - Libraries and Tools:
   - PySpark
   - Python
   - Jupyter Notebook or Databricks environment

#### 3. **Data Exploration and Cleaning**
   - Load the Zomato dataset into a PySpark DataFrame.
   - Explore the schema and understand the data types.
   - Check for missing values, handle them appropriately (e.g., imputation or removal).
   - Convert relevant columns to appropriate data types (e.g., numeric fields).

#### 4. **Data Preparation**
   - Preprocess the data for analysis and modeling.
   - Select relevant features for the project (e.g., restaurant ID, location, cuisine, ratings).
   - Ensure categorical variables are encoded properly if needed (e.g., one-hot encoding for categorical features).

### 5. **Transformations**
##### 5.1. Flattening the nested JSON
   - Transform the nested JSON structure into a flat DataFrame to simplify data processing and analysis by converting nested fields into separate columns.
   - Utilize PySpark functions to recursively extract and flatten nested fields, ensuring that each nested field is accessible as a top-level column in the resulting               DataFrame.

##### 5.2. Broadcast Join 
    - To efficiently join two DataFrames in PySpark using broadcast join
    - Applied broadcast join to perform join for country name dataset.
    - It optimizes performance by broadcasting the smaller DataFrame to all worker nodes, reducing the amount of data shuffled across the network during the join operation.

##### 5.3. Column Selection and Renaming
   - Selected specific columns and rename them.
   - Uses the select function and alias method.

##### 5.4. Adding New Columns
   -  Created new columns based on existing data.
   -  Uses the withColumn function.

##### 5.5. Removing Duplicates
   -  Removed duplicate rows based on specific columns.
   -  Uses the dropDuplicates function.

##### 5.6 Handling Missing Values
   -  Handled missing or null values in the dataset.
   -  Uses the fillna, dropna, or replace functions.

##### 5.7. **Window Functions**
   - Applied window functions to perform calculations over partitions of the data.
   - Example window functions:
      - Calculate moving averages of ratings or votes.
      - Rank restaurants within each locality based on ratings or votes.
      - Compute top-N restaurants in each city based on specific criteria.

##### 5.8. Filter
   - Purpose is to select rows that meet certain conditions.
   - Uses the filter or where functions
     
##### 5.9. Grouping and Aggregation 
   -  Grouping data by one or more columns and perform aggregate functions like sum, count, average, etc.
   -  Uses the groupBy and agg functions

##### 5.10. Lead and Lag
   - To Access subsequent (lead) and preceding (lag) row values within a specified window, enabling advanced comparative analysis across rows, such as identifying trends           or changes in ratings over time or sequence.
   - Utilized PySpark's lead and lag functions within a Window specification to create new columns that store the next and previous ratings, respectively, facilitating             enhanced row-wise comparisons and insights.
