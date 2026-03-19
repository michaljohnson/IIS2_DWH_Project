# IIS2_DWH_Project


**DWH Project**

**Objectives**

In this project, you will create a **mini
data warehouse** (DWH) consisting of a **Staging Area** and a  **Data Mart** .

Afterward, you will conduct  **various analyses** .

The project simulates how a company builds a
DWH, including analysis,  **using multiple datasets** . This will give you a
solid practical understanding of the  **DWH concept** , which is relevant to
various businesses.

Summarize your results in a **PowerPoint
report** ( **max. 10 pages, including screenshots** ). Then,  **upload your
report and source code (KNIME workflow file + SQL files) to Moodle** . Only
one submission **per group** is required. Please **include the names of all
group** members on  **the title slide of your report** .

When  **exporting the KNIME workflows, do not
reset them (checkbox, see image** ), so that we can review the output of each
node without needing to reconstruct the corresponding tables and databases
locally.

![A close up of a text

AI-generated content may be incorrect.]()

**Details**

The practicum consists of **three** parts.
You must have completed  **Exercises 1-3 beforehand** , as this project builds
on that knowledge. Unlike the practicums, there is no step-by-step guide for
this project; instead, you will apply what you have learned. If you get stuck
at any point,  **feel free to reach out to your practicum supervisor for
guidance** .

**1. Staging
Area**

The starting point is multiple datasets from
the sample company " **Nordwind** ." All datasets are provided as
CSV files.

Your first task is to create a **Staging Area**
that consolidates all datasets. You will work with the following six tables:

* **Products**
* **Categories**
* **Customers**
* **Orders**
* **OrderDetails**
* **Employees**

**Considerations:**

* Use **KNIME**
  as the tool.
* Write
  the contents of each CSV file into a separate  **PostgreSQL table** .
* Create
  tables with  **meaningful data types** .
* Address
  **data quality issues** before storing data in PostgreSQL tables.

**Task: Handling Incorrect Entries**

* In the
  OrderDetails dataset, some discount values (Discount column) have been recorded as **negative
  numbers** (e.g., -0.15). Ensure that no negative discounts exist.

**Task: Handling Duplicates**

* The Products dataset contains duplicate entries for
  the same products.
* Identify
  how these duplicate entries differ and eliminate them so that each product
  appears **only once** in the target table.

**Task: Handling Different Date Formats**

* The Orders and Employees
  datasets contain different date formats (e.g.,  **US format MM-DD-YYYY vs.
  international format DD-MM-YYYY** ). Ensure that all tables use the  **same
  date format** .
* Decide
  how to handle  **missing (NULL) date values** .

**2. Data
Mart**

Now, you are ready to create a  **Data Mart** .
Use **at least** the six tables from the Staging Area.

To do this, you must first design a **Star
Schema** with:

* One **fact
  table**
* Several
  **dimension tables**

Describe the **Star Schema** in your
report.

**Before **designing the Data Mart,
think about **the types of questions you want to analyze** later (see
Section  **3: Analyses** ).

Then, create the corresponding tables and
populate them with data from the  **Staging Area** .

If you decide to use a  **time dimension** ,
refer to the practicum exercises for guidance.

**You do not need to generate this data using
KNIME or PostgreSQL.**

**3. Analyses**

Now, you can conduct analyses based on your
Data Mart. Identify **five interesting questions** that you would like to
explore.

You are free to be creative! Here are some
example questions for inspiration:

* **From
  which countries do the customers with the five largest orders come?**
* **What
  is the average discount for products delivered to Latin American
  countries?**
* **Which
  products have higher demand than their storage capacity?**

You are free to choose the tasks and functions
you use for these analyses. **Experiment boldly!**

**Results**

**Guidelines for the max. 10-page PowerPoint
report:**

* **Describe** the
  structure of the **Staging Area** and **Data Mart** briefly. Use **screenshots**
  to illustrate the data models and  **ETL processes** .
* **Formulate** your
  five research questions and describe your **analysis results**
  (including screenshots).
* **Important:**
  Summarize your **experiences** and **conclusions** on one slide.

**Grading**

The project is worth a total of  **8 points** ,
distributed as follows:

* **Staging
  Area:** 2 points
* **Data
  Mart:** 2 points
* **Analysis:** 2
  points
* **Report:** 2
  points
