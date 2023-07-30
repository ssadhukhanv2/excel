# Introduction to excel



* SQL -> Data Query
* Tableau -> Data Visualization
* 80% of companie uses excel
* Data Analysys by Excel - Top 10 Jobs on Linkedin
* With excel no matter whichever chart etc are created, most users will be able to use and modify excel(even if he/she doesn't understand sql, tableau, excel etc)
* Roles:
  * Data Analyst
  * Financial Analyst
  * Project Manager


## **Agenda**
Core Functions:
* Math
* Datetime
* Logical
* Text Functions
* Lookups
* Array Functions

Business use cases

Hypothesis Testing

## **Concepts**

### **Excel**
Spreadsheet program. 
* **Spreadsheet**: In the same place we can have multiple tables.
* Excel supports 1 million rows (sufficient for most business analysis where it's not big data)
* Supports Data Visulaizations

Potential issues with excel:
* With large datasets(more than 1-2 lacs row), performance issue happens.
* Excel supports csv, xls, xlsx, tsv etc
* With excel we can read JSON, connect to a SQL DB, covert pdf to excel etc

Concepts from Tableu which are relevnat to excel:
* Charts
* Filtering
* Granularity
* Table Calculation
* Pivot

Things that are easier to do with spreadsheet programs
* Data Manipulations(change small values)
* quick ordering
* simple calc
* add additional fields

Excel Versions:
* 2021
  - one time payment (12000 for lifetime)
  - offline
  - no update in future
  - one user/device
* office 365
  - 4900/yr for 1 person or 6200/Yr  for 6 people
  - online and offline
  - regular updates
  - 5 devices are supported

Excel capabilities that we will focus:
* Major Functionalities
* Prominent Functions
* Dashboarding


## Things to do
* Create a Kaggle profile


## **Question: Help FC understand why they lost**
* Final of 2020 Edition:
  * MI and DC


* Hypothesis Testing: You have some hypothesis and you check if your hypothesis is true or not.
  * Come up with Hypothesis
  * Convert hypothesis into mathemetical expression
    
    * Possible Hypothesis to mathemetical expression conversion:
      * **Toss and Pitch**: Unavailable data
      * **Openers lost quick wickets**: wickets lost in initial overs(wickets in 0-5 overs)
      * **Death overs**: runs/wickets scored in the last 5 overs
      * **low score**: sum of runs
      * **poor bowling**: runrate
      * **run rate**: number of runs score per over
      * **miss fielding**: Unavailable data
      * **extra runs**: calculate the total run per match:  Uunavailable data

  * Sheet name: MI vs DC final

    * **low score**: Total runs scored in each innings. SUM()

### **FORMULAES**
to write a formulae use `=function(start cell: end cell)`

example 
* `=SUM(J9:J131)`
* `=AVG(J9:J131)`
* `=COUNT(J9:J131)`
* `=SUMIF(range,critera,[sum_range])`
  * criteria is checked on range
  * sum is done on sum_range
  * if sum_range is not given then sum happens on range
* `=SUMIF(J9:J131, ">=200")`: only sum when condition is true, SUMIF takes a range
* `COUNTIF(J9:J131, ">=200")`: only count when condition is true
* `=SUMIF(J9:J131, 200)`: only sum when cell is equal to 200
* `COUNTIF(J9:J131, 200)`: only count when cell is equal to 200
*  `=IF(COND,value_if_true,value_if_false)` IF CONDis true VALUE1 ELSE VALUE2, if takes a cell `=IF(AP7>200,AP7,0)`
* Find values which are >=500 but less than 600, use if we have and/or conditition AND(COND1,COND2) and OR(COND1, COND2) `=IF(AND(AP7<600,AP7>=500),AP7,0) `

* Running Sum: Drag drop formulae 57:40
* $ means fixed refernecing (vertical to horizontal) till 1:05:00

### **Table Referencing**
* Each subtable can be given a name, `Format as table` 1:06:50
* When we put a table name, =SUM(M2:M817), this would be same as `SUM(Table1['result_margin'])` -> sum of all values in a column 
* How many extra runs were given to mi to dc in the second innings. `SUM(Table1['extra_runs'])`
* Total number of balls `=COUNT(Table7['ball'])`
* Extra runs by wides: `=SUMIF(Table7[extras_type],"Wides",Table_7[extra_runs])`
* Wickets lost `COUNTIF(releveant columns)`
* Run rate of DC in the initial 5 overs: Figure out the first 5 overs and calculate the total runs
* Total Over: MAX(OVER)+1 or DCOUNT()
* Max ball in last over: IF last over count the number of balls or find the max ball 1:48:00-1:53:00


### **Text Functions**
* CONCAT(U5," ",V2)
* LEFT(U5,3) if you only want the first 3 letter(N letters from the left)
* RIGHT(U5,3) if you only want the last 3 letter(N letters from the right)
* SUBSTR(U7, )
* in excel we can nest any function inside any other function
CONCAT(LEFT(U5,3)," ",RIGHT(U5,3))
* Caught C fielder b baller: `=IF(M!2="Caught",concat("C ",O12,"B ",Q12))`
* Convert any string to a number `=NUMBERVALUE(K5)`, becomes really powerful when we are using right and left
* convert 52* tp 52
  * IF(RIGHT(TABLE_25[@Runs],1)='*',NUMBERVALUE(LEFT(LEN(TABLE_25[@Runs]))-1),0)