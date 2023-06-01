# Rename Columns

- [Problem](#problem)
- [Sample Dataset](#sample-dataset)
- [Sample Dataset](#rename-columns)

Problem
--------
In case the name of a generic column e.g., Column1, Column2, etc need to be updated via another human readable name the method to do it is descibed below.

Sample Dataset
----------------
For this example a manually added dummy dataset has been created in the Power BI file. However, it is possible to add a column name via DB or other datasource such as a SharePoitn list or an excel file.

Rename Columns
----------------
To rename the columns of the source table one need to have an intermediate mapping table. Then a manual step need to be added in the advanced query editor and the column data types need to be recreated manually. The code is shown below.