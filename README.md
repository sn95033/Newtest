
## Final Project Submission

Please fill out:
* Student name: Rebecca Mih
* Student pace: full time online
* Scheduled project review date/time: September 17, 8:30 AM
* Instructor name: Victor Geislinger
* Blog post URL:


<div>
<img src="Seattle_Timeout.GIF" width="500"/>
</div


## Objectives

* The way that realtors have looked a intrinsic house values is typically based on 3 key factors:
    - Location
    - Square footage` of living space
    - Number of bedrooms and bathrooms
    
    
* The purpose of this report is to provide visualizations that may bring new perspective on a data science approach to real estate pricing


* The focus is to work on creating effective analysis and improving interpretability of Data Science analysis and models



## Definition of features provided
#
Column Names and descriptions for Kings County Data Set
* **id** - unique identified for a house
* **date** - house was sold
* **price** -  is prediction target
* **bedrooms** - # of Bedrooms/House
* **bathrooms** - # of bathrooms/bedrooms
* **sqft_living** -  square footage of the home
* **sqft_lot** -  square footage of the lot
* **floors** -  total floors (levels) in house
* **waterfront** - House which has a view to a waterfront
* **view** - Has been viewed
* **condition** - How good the condition is ( Overall )
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house apart from basement
* **sqft_basement** - square footage of the basement
* **yr_built** - Built Year
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors


# Analysis Workflow

### 1. Pre-processing the data 

1. Check data size, NaNs, and # of non-null values which are not valid data 
2. Clean up missing values by imputing values or dropping
3. Replace ? or other non-valid data by imputing values or dropping data
4. Check for duplicates and remove if appropriate
5. Change datatypes of columns as appropriate


### 2. Perform visualizations and re-shape/transform data
1. Use .describe() and .hist() histograms
    * 1a. Identify outliers (based on auto-scaling of plots)
    * 1b. Note which features are continuous and which are categorical
   
   
2. Perform Geo-spatial visualizations to help the audience understand the data scope


3. Perform 3D scatter plots visualizations on key features that stakeholders typically care about
    * 3a. Square foot living space
    * 3b. Age of house (year built)
    * 3c. Price
    * 3d. Price per Square Foot
   
   
4. Analyse the target (Sales Price)  using statistical analysis, .groupby() and .describe() and visualizations (boxplots)
    * 4a. Review the geo-spatial distribution of the data to understand whether grouped differences are meaningful
    * 4b. Perform additional univariate splits based on categorical data to see if additional data cleaning is needed
    * 4c. Outlier calculations and decision to drop or not
    * 4d. Decide whether to filter (based on analysis results) or not
   
   
5. Look at feature correlations (Pearson correlation) for those that may be co-linear


6. If feature scaling and normalization is needed (with linear regression it can improve kurtosis and skew
    * 6a. Transform non-categorical data to categoricals and perform one-hot encoding
    * 6b. Perform log transformations on continuous variables (if applicable)
    * 6c. Normalize continuous variables

### 3. Create a Multi-Linear Regression Model



1. Split into train and test data  (Treated as optional here)
2. Run the model
3. Review quality indicators for the model:  p-values, skew, kurtosis (deviation from normal) and # of datapoints ( to look for co-linearity )
4. Revise data inputs if needed to improve quality indicators 
    - by adding created features, and removing colinear features
    - by removing outliers through filters
    - through use of subject matter knowledge

### 4. Write the Report
1. Explain key business findings and recommended next steps



## Visualizations of Data Scope



<div>
<img src="map showing key zips.gif" width="300"/> <img src="kde on map 2.gif" width="300"/> 
</div



##  3D Geo-spatial visualization using the longitude and latitude data
##    

<div>
<img src="3D scatterplots.GIF" width="600"/> 
</div


## Lets look a little deeper into the Price vs Location using Boxplots
## In particular, let's try to anticipate the questions our audience (realtors) might have regarding price and location


    * 1. Is there any significant trends between zipcode and price ?
    * 2. Is there any good way to group price trends?
    * 3. What's the home price impact of having waterfront housing ?
    * 4. Is there a significant difference between houses on the peninsula versus away from the coastline ?



##  Boxplot Analysis
##    
<div>
<img src="Price vs Zip.GIF" width="600"/> 
</div

##   
