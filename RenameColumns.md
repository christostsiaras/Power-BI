# Rename Columns

- [Problem](#problem)
- [Sample Dataset](#sample-dataset)
- [Sample Dataset](#rename-columns)
- [Download](#download)

Problem
--------
In case the name of a generic column e.g., Column1, Column2, etc need to be updated via another human readable name the method to do it is descibed below.
![image](https://github.com/christostsiaras/Power-BI/assets/5610687/de91fa24-f415-4d79-8ec7-3c8ab85dc0a4)

Sample Dataset
----------------
For this example a manually added dummy dataset has been created in the Power BI file. However, it is possible to add a column name via DB or other datasource such as a SharePoitn list or an excel file.
![image](https://github.com/christostsiaras/Power-BI/assets/5610687/393c3f12-6e1a-42de-b064-38e749b87361)


Rename Columns
----------------
To rename the columns of the source table one need to have an intermediate mapping table. 
![image](https://github.com/christostsiaras/Power-BI/assets/5610687/77d18cf1-9085-4f3b-90fc-4fbd0cfc60b9)

Then a manual step need to be added in the advanced query editor and the column data types need to be recreated manually. The code is shown below.
![image](https://github.com/christostsiaras/Power-BI/assets/5610687/a4913b94-8049-4424-bef7-f7f7783ba55e)

Download
---------
Download the file [here](https://github.com/christostsiaras/Power-BI/tree/main/Rename%20Columns)
