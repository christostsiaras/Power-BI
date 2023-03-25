# PowerBI
Power BI standard reports e.g., Pareto charts and dynamic columns selection.
For this example the Supermarket dummy sales dataset is downloaded from https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales?resource=download. The assumption for the PBIX file to work is that you save the CSV dataset at "C:\data\supermarket_sales - Sheet1.csv".

To create the dynamic column selection fields e.g., to plot either sales or quantity 
![Create Fields](https://user-images.githubusercontent.com/5610687/227746544-12d91969-aedd-4b99-a1e7-e0312a863cbc.png)
![create selected parameter measure](https://user-images.githubusercontent.com/5610687/227746589-f81ad831-0f1a-41e4-bacd-f6fd4ade7976.png)

You might want to add the unit in the dynamic column selection. This you have to do it manually by editing the fields DAX code

![Parameter before adding Unit](https://user-images.githubusercontent.com/5610687/227746681-e051406c-f0c0-49d1-ad7e-a96a5606b98c.png)
![Parameter after adding Unit](https://user-images.githubusercontent.com/5610687/227746647-7a7d4d44-4dd4-4e1c-9ff4-364321d43105.png)

To summarize the sales and the quantity you will need to use the SWITCH function. Like that later for any additional functions using the SUM function you will no tneed to maintain futrther code, allowing you to edit the code only once.

![SUM 1](https://user-images.githubusercontent.com/5610687/227746739-6ff75afa-e7db-463e-89eb-db4996f50a8a.png)
![SUM 2](https://user-images.githubusercontent.com/5610687/227746742-74bf799f-3c7a-42f6-82c7-7875d56b3b34.png)

The cumulative function and % cumulative function to sumarize either sales or quantity is illustrated below. Observe that the relative point is adjusted if a slicer is used to filter the dates.

![CDF](https://user-images.githubusercontent.com/5610687/227746804-f8f32b7b-f8c2-494c-8025-fe0e31041580.png)
![per cent CDF](https://user-images.githubusercontent.com/5610687/227746810-90cbb055-e50e-4ef6-a92f-a555d26dfa3c.png)
