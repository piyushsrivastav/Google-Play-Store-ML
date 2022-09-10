# Google-Play-Store-ML
The Goal is to predict the rating for an app based on the given input features like size, number of downloads etc.
While many public datasets (on Kaggle and the like) provide Apple App Store data, there are not many counterpart datasets available for Google Play Store apps anywhere on the web.On digging deeper, it can be found out that iTunes App Store page deploys a nicely indexed appendix-like structure to allow for simple and easy web scraping. On the other hand, Google Play Store uses sophisticated modern-day techniques (like dynamic page load) using JQuery making scraping more challenging.

The Play Store apps data has enormous potential to drive app-making businesses to success. Actionable insights can be drawn for developers to work on and capture the Android market!

Each app (row) has values for catergory, rating, reviews, size, installs, price, rated, last updated, and version.

Source: https://www.kaggle.com/lava18/google-play-store-apps

## CONTEXT:
The Play Store apps data has enormous potential to drive app-making businesses to success. However, many apps
are being developed every single day and only a few of them become profitable. It is important for developers to be
able to predict the success of their app and incorporate features which makes an app successful. We can collect app
data and user ratings from the app stores and use it to extract insightful information. A machine learning model can be
used to predict rating for a given app, which can be used to estimate success and scope of improvement.

## ATTRIBUTE INFORMATION:
1. App: Application name
2. Category: Category the app belongs to
3. Rating: Overall user rating of the app
4. Reviews: Number of user reviews for the app
5. Size: Size of the app
6. Installs: Number of user downloads/installs for the app
7. Type: Paid or Free
8. Price: Price of the app
9. Content Rating: Age group the app is targeted at - Children / Mature 21+ / Adult
10. Genres: An app can belong to multiple genres (apart from its main category). For eg, a musical family game
will belong to Music, Game, Family genres.
11. Last Updated: Date when the app was last updated on Play Store
12. Current Ver: Current version of the app available on Play Store
13. Android Ver: Min required Android version

### Steps to the project: [Total score: 20 points]
1. Import required libraries and read the data: [ Score: 1 point ]
- Import the required libraries and read the dataset.
- Check the first few samples, shape, info of the data and try to familiarize yourself with different features.
2. Data cleansing and Exploratory data analysis: [ Score: 10 points ]
- Check summary statistics of the dataset. List out the columns that need to be worked upon for model building.
- Check if there are any duplicate records in the dataset? if any drop them.
- Check the unique categories of the column 'Category', Is there are any invalid category? If yes drop them.
- Check if there are missing values present in the column Rating, If any? drop them and Convert ratings to high
and low categories(>3.5 is high rest low) and store it in a new column ‘Rating_category’.
- Check the distribution of the newly created column 'Rating_category' and comment on the distribution.
- Convert the column "Reviews" to numeric datatype and check the presence of outliers in the column and
handle the outliers using transformation approach.
- The column 'Size' contains alphanumeric values, handle the non numeric data and convert the column into
suitable datatype. (hint: Replace M with 1 million and K with 1 thousand, and drop/impute the entries where
size='Varies with device').
- Check the column 'Installs', handle the unwanted characters and convert the column into suitable dataype.
- Check the column 'Price', remove the unwanted characters and convert the column into suitable datatype.
3. Data Preparation for model building: [ Score: 2 points ]
- Drop the columns which you think redundant for the analysis.(suggestion: drop column 'rating', since we
created a new feature from it (i.e. rating_category) will use that as target.)
- For the target column 'Rating_category' Replace 'high' as 1 and 'low' as 0.
- Encode the categorical columns.
- Segregate the target and independent features.
- Split the dataset into train and test.
- Standardize the data, so that the values are within a particular range.
4. Model training, and testing: [ Score: 5 points ]
- Write a function to fit and print the model predictions, input parameters would be model, train, and test data.
- Use the above function and train a Decision tree, Random Forest, Bagging, Boosting, and Stacked Classifier
models and make predictions on test data and evaluate the models.
5. Conclusion and improvisation: [ Score: 2 point ]
- Compare and write your conclusions and steps to be taken in future in order to improve the accuracy of the
model.
