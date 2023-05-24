# Other

- [Problem](#problem)
- [Sample Dataset](#sample-dataset)
- [Dynamic KPI Selection](#dynamic-kpi-selection)
- [Create Generic DAX Measures](#create-generic-dax-measures)
- [Consume a Generic DAX Measure](#consume-a-generic-dax-measure)

Problem
--------
In power BI tooltips you cannot scroll and need to show only the top X values and summarize the rest in Others. You also often want the others option to be at the bottom despite the fact that the total number of rows can be the largest.
![8](https://github.com/christostsiaras/Power-BI/assets/5610687/ae2c2de3-e1d1-4c9f-80bf-c2b350398b6b)


Sample Dataset
----------------
For this example the Supermarket dummy sales dataset is downloaded from [kaggle](https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales?resource=download).
The assumption for the PBIX file to work is that you save the CSV dataset at "C:\data\supermarket_sales - Sheet1.csv". Else you might edit the query and change the path.

Calculated Table with Other Option
----------------------------------
Create the table containing the Others value for a given column.In this case we will be counting number of invoices per Product line. So we need to create a table with one column containing all product lines plus the  additional value "Other"
![1](https://github.com/christostsiaras/Power-BI/assets/5610687/b051f6e0-1a9b-4969-89e4-24cbec72963e)

To do that go to the tab table tools and add a new calculated table
![2](https://github.com/christostsiaras/Power-BI/assets/5610687/978bc9bd-2530-4550-9b1d-6595bfb6148e)


Count Measures
--------------
Create in the original table the distinct count measure to calculate how many distinct invoices (keep in mind the invoice ID need to be either a number or a text) exist per product line.
![3](https://github.com/christostsiaras/Power-BI/assets/5610687/ecfb2edc-6557-446b-9c73-33c4314fbf7e)

Now create another measure in the calculated table to count the distinct number of invoices including the other category. You may also use this measure beyond tooltips where you can use filtering.
![4](https://github.com/christostsiaras/Power-BI/assets/5610687/fd6b34f7-aa15-4cb0-9e01-17890cceb608)

Create the visualization consuming the newly created columns and measure. Use a table visualization and add a filter for this visualization refering to the original product line and filter the top N values based on the original count invoices measure.
![5](https://github.com/christostsiaras/Power-BI/assets/5610687/091f43d4-0aa9-4c29-a351-788d2802ec3b)

To short and force the other option to be at the bottom you will need an additional supporting index measure. The code is shown below.
![6](https://github.com/christostsiaras/Power-BI/assets/5610687/b9cb39a6-3fe8-4f37-927c-67d5a17fb06f)

Add the Tooltip
---------------

Include the index column created above in the table visualization and short so that the Other option appers to the bottom.
![7](https://github.com/christostsiaras/Power-BI/assets/5610687/76e902eb-4b34-485a-bfef-a187696eed05)

To add the report as a tooltip create a hidden page, tick on the option Tooltips and select the page on the page option.
![8](https://github.com/christostsiaras/Power-BI/assets/5610687/63364674-735d-4c2e-9c29-13299e1d3bfd)

To consume tha page with the normal filter remove the top N filter from the visualization and add a slicer on the product line column.
![9](https://github.com/christostsiaras/Power-BI/assets/5610687/cda9fa6d-3c40-4625-87b0-9bf11500f61d)


