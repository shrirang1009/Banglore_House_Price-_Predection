Bangalore-house's-price
This notebook is for people who are looking to buy a place in Bangalore city(INDIA)
Created a model that predicts Bangalore house rate to help people to know about the prices of house in various places without the need of contacting different agents for the same.
Data shape is 13320 rows and 9 columns.
EDA
Column 'total_sqft' was provided in avergare terms i.e 1195 - 1440, converted the same to float by taking the average of the numbers.

Created a new column - 'price_per_sqft' for better analysis.

Scaled down the number of locations to 241 from 1287 since most of the location occured less than 10 times.

On an average, the ratio between total_sqrt_foot and number of BHK should always be 300, hence we removed all the entries with values lesser than 300.
![image](https://github.com/shrirang1009/Banglore_House_Price-_Predection/assets/149002149/8d91c2d8-e926-46c2-ac1b-80d3242491bc)
Here we find that min price per sqft is 267 rs/sqft whereas max is 12000000, this shows a wide variation in property prices. Removal of 2214 outliers using Mean and Standard Deviation
![image](https://github.com/shrirang1009/Banglore_House_Price-_Predection/assets/149002149/f18a8071-59e9-48ee-bc4b-70fe08f07b14)
We see that there are alot of houses with 5000/- price per square feet rate
Removal of Data where the number of bathrooms is higher than number of bhk+2
Performed One hot encoding to represent the categorical values in binary form since machine learning algorithms cannot operate on label data directly.
I also split the data into train and tests sets with a test size of 20%. Model Used:-
Multiple Linear Regression - r^2 value of 0.86
Built a function to predict the house price with location, number of Square foot area, Bathroom, and BHK.
![image](https://github.com/shrirang1009/Banglore_House_Price-_Predection/assets/149002149/928fd3b3-f6e7-4bcd-bb42-13218f8aed4e)
The prices mentioned are in Lakhs(Indian Currency)
