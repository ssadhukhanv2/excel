
# Concepts


## Nested If and IFS

* Nested If: `=IF([extra_runs]>0,IF([extras_type]="wides","Wide","Not Wide"),"Not Extra")`
  * check if a ball is extra ball and wide
* If you have more than one if you can use IFS


* Joins:
  * Two table
  * Figure out a common column within a table
  * Take ID from First table, secarch for the id in the second table, if you find the id, you take the row
  * We can also choose the columns we want to display


## Lookups

* HLookups: Horizontal Look up. Searches in a row
  * matches on the first row
* VLookups: Vertical Look up. Searches in a column
  * Almost equivalent to joins in SQL or Tableau
  * check if the given id of a table exist in a table, if the id exist, then check the other columns in the table
  * ID
  * Table to Search
  * Result to display
  * `=VLOOKUP(F10,A14:Q12,11)` 11 is the output column
  * `=IFERROR(VLOOKUP(F10,A14:Q12,11),"Incorrect Match Id)` supply a defult value if match can't be found
  * Limitations:  
    * VLOOKUP assumes the search column is the first column in the table.
    * VLOOKUP bydefault can only output a single column: overcome this by using multiple vlookups.
    * If we have more than one row with the same search id, it returns any one of rows.

  * **Approximate Match** Incase of numeric values `=VLOOKUP(F10,A14:Q12,11,TRUE)` this is an approx match same as `=VLOOKUP(F10,A14:Q12,11)`, returns value from lower row number if exact match doesn't exist.
    * Assumes the data is sorted
    * Try to find a number > given value
    * Output previous value for this.
    * *Always sort the data before using Exact Match*
  * **Exact Match:** Incase of numeric values `=VLOOKUP(F10,A14:Q12,11,FALSE)` this is an exact match. so if value doesn't exist returns error.

  * Incase of Numeric Approximate Match is default.
  * Incase of Strings Exact Match is default.


## Match and Index
1:12
* **Match:** takes id, search in column, gives nth row if it has the same id
  * At position in the list of column team2 comes `=MATCH("batting_team",A1:S1,FALSE)`
  * Match always gives the first occurrence only.

* **Index:** takes an index and range and gives a value.
  * `=INDEX(E1:E26,5)`

* We can use match() and index() to match a key and then return the relevant column

* First Match where Sachin Tendulkar is Man of the Match
`=INDEX(Table2[id],MATCH("SR Tendulkar",Table2[player_of_match],0))`


## Array Function
* Mathemetical operation on two array ranges `=A2:A8*B2:B8`
* Sum of product of  two array ranges `=SUM(A2:A8*B2:B8)`
* Scaler multiplication is also allowed `=A2:A8*10`
* Manipulation of string arrays are also allowed `=RIGHT(D2:D32,3)`

## Filter
* Reduce number of rows `FILTER(<columns to select>,<condition>)`
* Filter only the innings 1 `FILTER(Table8,Table8[innings]=1)`
* Spill error: if there are existing text/formatting around, this error is thrown
* Gives only the over column from innings 1 `FILTER(Table8[over],Table8[inning]=1)`
