# Zomato-PySpark-Project

#### This project involves analyzing a Zomato dataset to understand restaurant trends and customer preferences across different countries. The analysis includes data cleaning, merging datasets, performing transformations such as aggregations and feature engineering, and applying lead and lag functions for trend prediction. Key insights include average cost and rating comparisons, customer engagement levels, and service availability across countries. The lead and lag analysis further provides valuable predictions on future trends in pricing and customer satisfaction, enabling strategic decision-making for restaurant management.

### Project Outline

#### 1. Introduction
   - Project Title: Zomato Dataset Analysis
   - Description: This project involves data loading, exploration, cleaning, and analysis of a Zomato dataset using PySpark. The goal is to derive insights and perform       
                  various data transformations, including optimizing joins with broadcast joins and flattening nested JSON structures and using advance transformations like                     lead and lag.

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
     
#### 6. Visualization
   - Visualization Tools:
        - Databricks built-in visualizations.

#### 7. Conclusions
   - The average cost for two in the USA is lower compared to the UK and India. This suggests that dining out might be more affordable in the USA.
   - The average rating of restaurants is highest in the USA, indicating higher customer satisfaction compared to India and the UK.
   - The total votes show that restaurants in India receive the highest customer engagement, followed by the UK and the USA.
   - Table booking availability is highest in the UK, suggesting a preference for reserved dining experiences.
   - Online delivery services are more available in India, reflecting a higher demand for food delivery options.

##### 7.1. **Trend Prediction**:
   - The lead values for the average cost indicate that costs are expected to rise in certain countries such as the UK, while in others like the USA, they might remain stable      or decrease.
   - By analyzing lag values, we can confirm whether the historical trend matches the projected trend.

##### 7.2. **Customer Satisfaction**:
   - Lead values for ratings suggest that customer satisfaction is likely to improve in countries like India, while it might decline in the UK.
   - Lag values provide a historical perspective, helping us understand whether the changes in ratings are consistent with past trends.

##### 7.3. **Strategic Decisions**:
   - Restaurants can use these insights to make strategic decisions such as adjusting pricing or focusing on improving customer service in countries where future ratings are expected to decline.


# This Helped in understanding the Funtionality with some Advanced Transformations and Power of Apache Spark.
