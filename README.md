## Understanding Business

The first step in the Data Science Life Cycle is to understand the business we are about to interperet the Data. The data itself does explain quite a bit about the business model:

* This is a small business with only nine employees.
* Employees are responsible for selling to specific regions which subset into specific territories.
* Order quantities are large and since suppliers are involved, either a specialty grocery and/or restaurant supplier.


## The Database

Northwind database--a free, open-source dataset created by Microsoft containing data from a fictional company. 

<img src='https://raw.githubusercontent.com/learn-co-curriculum/dsc-2-final-project/master/Northwind_ERD.png'>

## Data Mining

The data is provided via a SQLite database. After glancing through the tables in https://sqliteonline.com/, there are a few notes for reference:

* The tables CustomerCustomerDemo and CustomerDemographics have no information in htem. 
* While the ERD tables have all ID columns listed, they are not specifically labeled those items in the tables. Only "Id" is provided. This will mean renaming may be necessary for the purpose of joining tables(dataframes).
* Since basic SQL queries will not be efficient for the purposes of the project, we will convert the database into a pandas dataframe using sqlalchemy and pandas.

## Hypothesis Testing

### Question 1: Do discounts have a statistically significant effect on the number of products customers order? If so, at what level(s) of discount?

#### Ho = Discounts do not have a significant effect on the number of products customers order.
#### Ha = Discounts do have a significant positive effect on the number of products customers order.

After cleaning and setting the data for this experiment:

### Step 1: Run a normality test on both control and experiment datasets using Scipy's Shapiro test:

control - (0.8434571027755737, 3.803856556577728e-34) - normally distributed
experiment - (0.8673426508903503, 6.471277454941499e-26) - normally distributed

### Step 2: Run a visual probability distributions graph to see if there are differences between the means and standard deviations.

add img[pdf](pdf.png)
