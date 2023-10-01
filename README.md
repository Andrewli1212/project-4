# project-4
Selling Italian Sun(data)sets
The purpose of this project is to apply machine learning models to housing prices from a dataset collected on Italy , including number of bedrooms and bathrooms, location, region, amenities, sale prices and other relevant features. The practical uses of this analysis include assisting homebuyers, realtors, and property investors to provide valuable predictions for prices based on known property features. 

Tools and Libraries used:
Jupyter Notebook, Pandas, Matplotlib, Google Colaboratory, Machine Learning models, Tableau

Process: 

The first step was to evaluate the dataset we chose, and then preprocess the data to make it usable for purposes. The original dataset was in Italian, so this was translated in the Jupyter Notebook to English. The date column was then converted to the proper datetime format, unnecessary columns were altogether removed, and null values in the 'price', 'bedrooms', and 'bathrooms' columns were removed. We then filtered out prices that were below 1,000 and above 10,000,000, to remove obvious outliers. After viewing a boxplot of the data, we further removed outliers above the price of 727,000. We also replaced the region of those with less than 1000 properties from the original region to "Other". We also created visualizations in Tableau to assist with our data analysis.

After cleaning the data, we then developed and evaluated the performance of the models trained on the cleaned data. We initiated the model, split the data into training and testing sets, train the model, and then evaluate the performance of the model.

Analysis:


Data Limitations:
This dataset contained data on Italian properties only, so these models may not work well for other countries, with houses containing potentially a different set of common features, such as homes in the United States.  However, the same process and analysis can be applied on a different dataset, and could potentially have similar accuracy. 

Future Analyis:
In the future, with more time and resources, we could scale this project to include both rental and sale prices, look at housing prices in other countries, including the U.S., and/or could create models specifically for different types of properties (i.e. apartments, villas, lofts, single family homes, townhomes, etc.)
