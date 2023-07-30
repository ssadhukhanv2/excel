# **Dashboards & Excel Capstone Intro**

1. Conceptualising Dashbaording
2. Slicers
3. Match Name creation
4. Case study



## **Concept 1: Dashboarding Concepts**

Dashboards may be used for provding the business users a view of the data(by combining multiple sheets)

### **Seasons Level Dashboard**
Assumptions: Year of the match date is the Season
Metrics:
* Season Slicer
* **Winner Team of a Season**: Who ever won the last match of the season
Find the last match of the season using pivot table, then use a VLOOKUP() to get the winner of the season.
* **Man of the Season**
* **Bowler with most wickets in a season**: Use Pivot Table Slicers
* **Batsman with Most Runs in a season:**: Use Pivot Table Slicers
* Most Strike rates
* Season Selector(Slicer)
* Display the season


### Text Join Function
* Uses Delimiter to join a specific fields 


### **Match Level Dashboard**
* Season Slicer
* Match Slicer:
  * Team 1 vs Team2 vs Date
* Winners
* Man of the Match
* Toss Winner
* Stats
  * Most Runs
  * Most Wickets
* Teams that played
* Venue


### **Pivot Table Slicer**
Filters data across multiple pivot table.
* It is similar to filters.
* However filters apply at a pvot table level but Slicers may be connected to multiple Pivot Tables.
* To Apply Slicer to an existing Pivot Table. Select the Pivot Table -> Go to Pivot Table Analysis Tab -> Insert Slicer
* Connect multiple pivot table to the same slicer. Right click on the slicer -> Report Connections -> Select the Tables there





### **Interview Pattern Questions**
* No direct questions from tools like excel or tableau
* Ask which metric will you put in a given scenario
* Ask which tool to use in a given scenario
* Understanding charts.  Like what are the different types of charts, dual axis, multiple axis, what are the metrics and when to use them?
* What happends if there us a bump or increase in your chart
* Is there a way which will make the chart from readable

* Tableu:
  * Filters(types)
  * Live vs Extract
  * LOD expressions

* Excel:
  * How lookups works
  * Pivot Tables(columns needed in the pivot tables)

* CHarts:
  * Types of chart to use
  * How to improve a chart
  * Compare two trends or data points in chart.

* Datasources
  * For Large dataset what should we use
  * Should joins be used in data visualization
  * How to speed up

* Business Accumen/Product Understanding/Visualization understanding
 
   Given a scenario 
  * what are the right metrics in a dashboard
  * right metrics or slicers to use