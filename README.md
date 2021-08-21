# CRYPTOCURRENCIES

# PURPOSE
The purpose of this challenge is to help an investment bank create their new cryptocurency investment portfolio. The bank has asked to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The end result of this analysis is to divide cryptocurrencies into clusters. The features of these clusters or explaining what these clusters are is out of scope for now.

## ANALYSIS
Since we do not have a pre-defined answer here, so we'll make use of Unsupervised Machine Learning Algorithms to help us divide our data into clusters which can then be analyzed further to determine which cryptocurrencies can be added to the investment bank's portfolio.

## APPROACH

Here's the original dataset

![image](https://user-images.githubusercontent.com/82654977/130310638-fef52a2d-6094-44da-9f76-e65d1dec4b40.png)

Following steps have been taken to come up with clusters:

1. Data Preprocessing:
- Use pandas get_dummies to convert non numerical to numerical data
- Use sklearn's sklearn.preprocessing package's Standardscaler() function to scale all values in a dataset
- Reduce features such as CoinName who play no important role in our analysis.
- Consider only the cryptocurrencies that are currently being traded

2. Reduce data dimension:
- Use sklearn's sklearn.decomposition package's PCA module to reduce dimensions into three principal components

3. Create cluster using K-Means
- Used sklearn's sklearn.cluster package's KMeans function
- Find the best value for k using the Elbow Curve
- Initialize K-means module and generate predictions

4. Generate 3D scatter plot and hvplot

- Club predictions created with K-Means algorithm along with PCA values with original dataset. 

![image](https://user-images.githubusercontent.com/82654977/130310664-6fe9ff02-ea72-4478-b3b9-ad11085eff05.png)


- Create the 3D scatter plot

![newplot](https://user-images.githubusercontent.com/82654977/130310686-5276c8d3-77d2-4e0a-a707-fc43cedfb1c3.png)

- Create hvplot scatter plot using scaled values of "TotalCoinSupply" and "TotalCoinsMined"


![bokeh_plot](https://user-images.githubusercontent.com/82654977/130310750-0394f5a9-6665-4285-938b-049f1ae41b0b.png)


### RESULT

1. There are 532 cryptocurrencies that are being traded and mined.
2. These cryptocurrencies can be divided into 4 distinct clusters.



























