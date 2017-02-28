# Python-Project-Final

In this project, we are trying to predict the analysis for donatation data which person shall we approach for more donate. 
This data has been collected from PARALYZED VETERANS OF AMERICA.

We had followed few steps for data prediction :-
1. Data Cleaning and Visualization :-
    There are 481 columns and 9999 rows of data in which there were lots of data was missing and absurd values for eg:- ZipCode 
    has negative value, gender has empty values as some people don't like mention their gender these days.
    so, we have predicted our values with all columns but we have chosen some specific columns to clean as ZipCode, Domain, Gender,
    Major and MDMAUD
    As we all know zip code divides on the basis of area, so we have converted all the negative values present in ZipCode to positive
    and then before deleting the zip column, I slicied the first column as ZIP1 as it has region code and ZIP23 as it has place code
    Domain attribute will tell us that the specific region where person is located. as it is urban, city, rural so to fill these
    empty columns of this will be filled with lowest value so that we can have better efficiency of code.
    After this we replaced all remaining folders with 0.
    checked if gender has zeroes too. so replaced the gender with "unique" value and shown it visually with count plot.
    Major column has two values X and 0. X depicts that the person has donated something in past while 0 will be minimal value for 
    those who don't. As we proceed further, the machine learning requires the data should be in numerical form. so, X has been 
    converted to 1.
    Like Major, MDMAUD has been converted to 0 and 1.

2. DATA COMPESSION AND VISUALIZATION USING PCA[PRINCIPAL COMPONENT ANALYSIS]:
    In our project we have done the data compression using the Principal Component Analysis(PCA).
    As we know that PCA reduces dimensions by focusing on the data with the most variations. This is useful for the high 
    dimensional data because PCA helps us to draw a simple XY plot.PCA is used as a technique for finding the directions 
    of maximal variance.
    Using PCA – we can represent Larger series of data in a smaller number of components meaningfully interpreted.
    We have used the principle component analysis on the 32 rows(16 Ethnicity columns and 16 Employed in various fields) and 
    finally when we obtain the 4 components after the data compression we are then converting this data to a DataFrame and merging
    it with the original data so that the data stays intact.
    
3. Data prediction:-
    We have used Logistic regression as our Target value is in 0 and 1. After compressing the data, we have eliminated the Target 
    column in another column and rest of the column in another dataframe to generate train and test dataframe with 80:20. As we have
    some columns which contained object datatype columns, we converted them to numeric value with the help of LabelEncoder class.
    With the help of Train data we fit some data in regression and predicted the binary values with accuracy of 97%.
