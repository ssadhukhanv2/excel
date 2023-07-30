* Functions
* Pivot Tables
* Visualization and Formatting
* Macros
* Stat Functions



## Concepts 1: Get the top n rows

### **Pivot Tables and Sort** 
Pvot Means change.
* Select the Table-> Insert-> Pivot Table
* Pivot Table has 4 components:
  * **Rows**:Drag columns to Rows for making it row in the pivot table
  * **Columns:** Drag columns to Column for making it column in the pivot table
  * **Values** For populating the values for the selected rows and columns
  * **Filters** For filtering out the data

* Helper columns: We can create additional columns for the Tables, which we can use in the Helper columns.

* Data in the pivot table is not automatically refreshed if data in the actual table is not changed. We need to actually refresh it.

* **Value Filters:** We can get the top n rows based a field within a pivot table using Value filters. Row Label-> Expand the sort option dropdown within the cell-> Value Filter

### **Pivot Charts** 
We can create charts from pivot table.
* Charts created from pivot tables are much better as pivot table automatically aggregates the data. (We can also create charts using normal table but that may have undesirable results as data in normal table are not automatically aggregated.)
* If you change your pivot table data, the data chart created from the pivot table also changes


### **Conditional formatting**
Given a range and condition we color or insert databars 
Apply formatting on conditions. 
* For example- Highlish the top 10 rows.
* 


### **Large Functions**
=LARGE(AI7:AI40,5)

## **Helper Columns**
We can create additonal helper columns to figure out things. Add a column to the pivot table using IF()
* We can use "Helper Columns" to find out what percentage of toss winners/losers were also the winners


### **Distinct Values**

* **Remove Duplicate** This removes duplcates at the row level and we can also use it for single column ranges as well. Data Tab-> Remove Duplicate

* **Unique Function** This can also be used to remove duplicate.  
* `UNIQUE(Z3:Z143,FALSE)` by row (use this always)
* `UNIQUE(Z3:Z143,TRUE)` by column

     Unique function is only available in office 365.


## **Concept 2: Macros used to records steps and run it on sheets**

* Record our steps and then we can run it on same sheets
* used to automate tasks
* **Recording Macro** View -> Macro -> Record Macro
* **Running Macro** View -> Macro -> Open Macro and run it
* Useful for automation and automate formatting
* Some times dorting doesn't work.