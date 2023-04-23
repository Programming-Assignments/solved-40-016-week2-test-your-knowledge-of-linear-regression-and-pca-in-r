Download Link: https://assignmentchef.com/product/solved-40-016-week2-test-your-knowledge-of-linear-regression-and-pca-in-r
<br>



<ol>

 <li>This question involves the use of simple linear regression on the Auto dataset. This dataset was taken from the StatLib library which is maintained at Carnegie Mellon University. The dataset has the following fields:</li>

</ol>

<ul>

 <li>mpg: miles per gallon</li>

 <li>cylinders: number of cylinders</li>

 <li>displacement: engine displacement (cu. inches)</li>

 <li>horsepower: engine horsepower</li>

 <li>acceleration: time to accelerate from 0 to 60 mph (sec.)</li>

 <li>year: model year (modulo 100)</li>

 <li>origin: origin of car (1. American, 2. European, 3. Japanese)</li>

 <li>name: vehicle name</li>

 <li>Perform a simple linear regression with mpg as the response and horsepower as the predictor. Comment on why you need to change the horsepower variable before performing the regression.</li>

 <li>Comment on the output by answering the following questions:

  <ul>

   <li>Is there a strong relationship between the predictor and the response?</li>

   <li>Is the relationship between the predictor and the response positive or negative?</li>

  </ul></li>

 <li>What is the predicted mpg associated with a horsepower of 98? What is the associated 99% confidence interval?</li>

</ul>

<em>Hint</em>: You can check the predict.lm function on how the confidence interval can be computed for predictions with R.

<ul>

 <li>Compute the correlation between the response and the predictor variable. How does this compare with the <em>R</em><sup>2 </sup>value?</li>

 <li>Plot the response and the predictor. Also plot the least squares regression line.</li>

 <li>First install the package ggfortify which aids plotting linear models with ggplot2. Use the following two commands in R to produce diagnostic plots of the linear regression fit:</li>

</ul>

<h1>&gt; library(ggfortify) &gt; autoplot(your model name)</h1>

Comment on the Residuals versus Fitted plot and the Normal Q-Q plot and on any problems you might see with the fit.

<ol start="2">

 <li>This question involves the use of multiple linear regression on the Auto dataset building on question 1.

  <ul>

   <li>Produce a scatterplot matrix which includes all the variables in the dataset.</li>

   <li>Compute a matrix of correlations between the variables using the function cor(). You need to exclude the name variable which is qualitative.</li>

   <li>Perform a multiple linear regression with mpg as the response and all other variables except name as the predictors. Comment on the output by answering the following questions:

    <ul>

     <li>Is there a strong relationship between the predictors and the response?</li>

     <li>Which predictors appear to have a statistically significant relationship to the response?</li>

     <li>What does the coefficient for the year variable suggest?</li>

    </ul></li>

  </ul></li>

</ol>

<ol start="3">

 <li>This problem focusses on the multicollinearity problem with simulated data.

  <ul>

   <li>Perform the following commands in R:</li>

  </ul></li>

</ol>

<h1><em>&gt; </em>set.seed(1) <em>&gt; </em>x1 <em>&lt;</em>− runif(100) <em>&gt; </em>x2 <em>&lt;</em>− 0.5*x1 + rnorm(100)/10 <em>&gt; </em>y <em>&lt;</em>− 2 + 2*x1 + 0.3*x2 + rnorm(100)</h1>

The last line corresponds to creating a linear model in which y is a function of x1 and x2. Write out the form of the linear model. What are the regression coefficients?

<ul>

 <li>What is the correlation between x1 and x2? Create a scatterplot displaying the relationship between the variables.</li>

 <li>Using the data, fit a least square regression to predict y using x1 and x2.

  <ul>

   <li>What are the estimated parameters of <em>β</em><sup>ˆ</sup><sub>0</sub>, <em>β</em><sup>ˆ</sup><sub>1 </sub>and <em>β</em><sup>ˆ</sup><sub>2</sub>? How do these relate to the true <em>β</em><sub>0</sub>, <em>β</em><sub>1 </sub>and <em>β</em><sub>2</sub>?</li>

   <li>Can you reject the null hypothesis <em>H</em><sub>0 </sub>: <em>β</em><sub>1 </sub>= 0?</li>

   <li>How about the null hypothesis <em>H</em><sub>0 </sub>: <em>β</em><sub>2 </sub>= 0?</li>

  </ul></li>

 <li>Now fit a least squares regression to predict y using only x1.

  <ul>

   <li>How does the estimated <em>β</em><sup>ˆ</sup><sub>1 </sub>relate to the true <em>β</em><sub>1</sub>?</li>

   <li>Can you reject the null hypothesis <em>H</em><sub>0 </sub>: <em>β</em><sub>1 </sub>= 0?</li>

  </ul></li>

 <li>Now fit a least squares regression to predict y using only x2.

  <ul>

   <li>How does the estimated <em>β</em><sup>ˆ</sup><sub>2 </sub>relate to the true <em>β</em><sub>2</sub>?</li>

   <li>Can you reject the null hypothesis <em>H</em><sub>0 </sub>: <em>β</em><sub>2 </sub>= 0?</li>

  </ul></li>

 <li>Provide an explanation on the results in parts (c)-(e).</li>

</ul>

<ol start="4">

 <li>This problem involves the Boston dataset. This data was part of an important paper in 1978 by Harrison and Rubinfeld titled “<strong>Hedonic housing prices and the demand for clean air</strong>” published in the <em>Journal of Environmental Economics and Management 5(1): 81-102</em>.</li>

</ol>

The dataset has the following fields:

<ul>

 <li>crim: per capita crime rate by town</li>

 <li>zn: proportion of residential land zoned for lots over 25,000 sq.ft</li>

 <li>indus: proportion of non-retail business acres per town</li>

 <li>chas: Charles River dummy variable (= 1 if tract bounds river; 0 otherwise)</li>

 <li>nox: nitrogen oxides concentration (parts per 10 million)</li>

 <li>rm: average number of rooms per dwelling</li>

 <li>age: proportion of owner-occupied units built prior to 1940</li>

 <li>dis: weighted mean of distances to five Boston employment centres</li>

 <li>rad: index of accessibility to radial highways</li>

 <li>tax: full-value property-tax rate per $10,000</li>

 <li>ptratio: pupil-teacher ratio by town</li>

 <li>black: 1000(<em>Bk </em>− 0<em>.</em>63)<sup>2 </sup>where <em>Bk </em>is the proportion of black residents by town</li>

 <li>lstat: lower status of the population (percent)</li>

 <li>medv: median value of owner-occupied homes in $1000s</li>

</ul>

We will try to predict the median house value using thirteen predictors.

<ul>

 <li>For each predictor, fit a simple linear regression model using a single variable to predict the response. In which of these models is there a statistically significant relationship between the predictor and the response? Plot the figure of relationship between medv and lstat as an example to validate your finding.</li>

 <li>Fit a multiple linear regression models to predict your response using all the predictors. Compare the adjusted <em>R</em><sup>2 </sup>from this model with the simple regression model. For which predictors, can we reject the null hypothesis <em>H</em><sub>0 </sub>: <em>β<sub>j </sub></em>= 0?</li>

 <li>Create a plot displaying the univariate regression coefficients from (a) on the X-axis and the multiple regression coefficients from (b) on the Y-axis. That is each predictor is displayed as a single point in the plot. Comment on this plot.</li>

 <li>In this question, we will check if there is evidence of non-linear association between the lstat predictor variable and the response? To answer the question, fit a model of the form</li>

</ul>

medv = <em>β</em><sub>0 </sub>+ <em>β</em><sub>1</sub>lstat + <em>β</em><sub>2</sub>lstat

You can make use of the poly() function in R. Does this help improve the fit¿ Add higher degree polynomial fits. What is the degree of the polynomial fit beyond which the terms no longer remain significant?

<ol start="5">

 <li>Orley Ashenfelter in his paper “<strong>Predicting the Quality and Price of Bordeaux Wines</strong>” published in <em>The Economic Journal </em>showed that the variability in the prices of Bordeaux wines is predicted well by the weather that created the grapes. In this question, you will validate how these results translate to a dataset for wines produced in Australia. The data is provided in the file winedata.csv. The dataset contains the following variables:

  <ul>

   <li>vintage: year the wine was made</li>

   <li>price91: 1991 auction prices for the wine in dollars</li>

   <li>price92: 1992 auction prices for the wine in dollars</li>

   <li>temp: average temperature during the growing season in degree Celsius</li>

   <li>hrain: total harvest rain in mm</li>

   <li>wrain: total winter rain in mm</li>

   <li>tempdiff: sum of the difference between the maximum and minimum temperatures during the growing season in degree Celsius</li>

  </ul></li>

</ol>

<ul>

 <li>Define two new variables age91 and age92 that captures the age of the wine (in years) at the time of the auctions. For example, a 1961 wine would have an age of 30 at the auction in 1991. What is the average price of wines that were 15 years or older at the time of the 1991 auction?</li>

 <li>What is the average price of the wines in the 1991 auction that were produced in years when both the harvest rain was below average and the temperature difference was below average?</li>

 <li>In this question, you will develop a simple linear regression model to fit the log of the price at which the wine was auctioned in 1991 with the age of the wine. To fit the model, use a training set with data for the wines up to (and including) the year 1981. What is the R-squared for this model?</li>

 <li>Find the 99% confidence interval for the estimated coefficients from the regression.</li>

 <li>Use the model to predict the log of prices for wines made from 1982 onwards and auctioned in 1991. What is the test R-squared?</li>

 <li>Which among the following options describes best the quality of fit of the model for this dataset in comparison with the Bordeaux wine dataset that was analyzed by Orley Ashenfelter?

  <ul>

   <li>The result indicates that the variation of the prices of the wines in this dataset is explained much less by the age of the wine in comparison to Bordeaux wines.</li>

   <li>The result indicates that the variation of the prices of the wines in this dataset is explained much more by the age of the wine in comparison to Bordeaux wines.</li>

   <li>The age of the wine has no predictive power on the wine prices in both the datasets.</li>

  </ul></li>

 <li>Construct a multiple regression model to fit the log of the price at which the wine was auctioned in 1991 with all the possible predictors (age91, temp, hrain, wrain, tempdiff) in the training dataset. To fit your model, use the data for wines made up to (and including) the year 1981. What is the R-squared for the model?</li>

 <li>Is this model preferred to the model with only the age variable as a predictor (use the adjusted R-squared for the model to decide on this)?</li>

 <li>Which among the following best describes the output from the fitted model?

  <ul>

   <li>The result indicates that less the temperature, the better is the price and quality of the wine</li>

   <li>The result indicates that greater the temperature difference, the better is the price and quality of wine.</li>

   <li>The result indicates that lesser the harvest rain, the better is the price and quality of the wine.</li>

   <li>The result indicates that winter rain is a very important variable in the fit of the data.</li>

  </ul></li>

 <li>Of the five variables (age91, temp, hrain, wrain, tempdiff), drop the two variables that are the least significant from the results in (g). Rerun the linear regression and write down your fitted model.</li>

 <li>Is this model preferred to the model with all variables as predictors (use the adjusted R-squared in the training set to decide on this)?</li>

 <li>Using the variables identified in (j), construct a multiple regression model to fit the log of the price at which the wine was auctioned in 1992 (remember to use age92 instead of age91). To fit your model, use the data for wines made up to (and including) the year 1981. What is the R-squared for the model?</li>

 <li>Suppose in this application, we assume that a variable is statistically significant at the 0.2 level. Would you reject the hypothesis that the coefficient for the variable hrain is zero?</li>

 <li>By separately estimating the equations for the wine prices for each auction, we can better establish the credibility of the explanatory variables because:

  <ul>

   <li>We have more data to fit our models with.</li>

   <li>The effect of the weather variables and age of the wine (sign of the estimated coefficients) can be checked for consistency across years.</li>

   <li>1991 and 1992 are the markets when the Australian wines were traded heavily.</li>

  </ul></li>

</ul>

Select the best option.

<ul>

 <li>The current fit of the linear regression using the weather variables drops all observations where any of the entries are missing. Provide a short explanation on when this might not be a reasonable approach to use.</li>

</ul>

<ol start="6">

 <li>This question involves the use of principal component analysis on the well-known iris The dataset is available in R.

  <ul>

   <li>How many observations are there in the dataset? What are the different fields/attributes in the data set?</li>

   <li>Create a new dataset data by removing the Species column and store its content as iris.sp.</li>

   <li>Compare the various pair of features using a pairwise scatterplot and find correlation coefficients between the features. Which features seem to be highly correlated?</li>

   <li>Conduct a principal component analysis on data without standardizing the data. You may use prcomp(…, scale=F).

    <ul>

     <li>How many principal components are required to explain at least 90 % of the variability in the data? Plot the cumulative percentage of variance explained by the principal components to answer this question.</li>

     <li>Plot the data along the first two principal components and color the different species separately. Does the first principal component create enough separation among the different species? To plot, you may use the function fviz pca ind or fviz pca biplot in library(factoextra). Alternatively, you may use biplot or construct a plot using ggplot2 as well.</li>

    </ul></li>

   <li>Do the same exercise as in (d) above, now after standardizing the dataset. Comment on any differences you observe.</li>

  </ul></li>

 <li>This problem involves the dataset wine italy.csv which was obtained from the University of Irvine Machine Learning Repository. These data are the results of a chemical analysis of wines grown in the same region in Italy but derived from three different <em>cultivars</em>. The analysis determined the quantities of 13 constituents found in each of the three types of wines. The first column identifies the cultivars and the next thirteen are the attributes given by:

  <ul>

   <li>alcohol: Alcohol</li>

   <li>malic: Malic acid</li>

   <li>ash: Ash</li>

   <li>alkalin: Alkalinity of ash</li>

   <li>mag: Magnesium</li>

   <li>phenols: Total phenols</li>

   <li>flavanoids: Flavanoids</li>

   <li>nonflavanoids: Nonflavanoid phenols</li>

   <li>proanth: Proanthocyanins</li>

   <li>color: Color Intensity</li>

   <li>hue: Hue</li>

   <li>od280: OD280/ OD315 of diluted wines</li>

   <li>proline: Proline</li>

  </ul></li>

</ol>

<ul>

 <li>Check the relationship between the variables by creating a pair-wise scatterplot of the thirteen attributes.</li>

 <li>Conduct a principal component analysis on the standardized data. What proportion of the total variance is explained by the first two components?</li>

 <li>Plot the data along the first two principal components and color the different cultivars separately. Also plot the loadings of the different components to show the importance of the different attributes on the first two principal components?</li>

</ul>

(i) Which two key attributes differentiate Cultivar 2 from the other two cultivars? (ii) Which two key attributes differentiate Cultivar 3 from the other two cultivars?

<ul>

 <li>Use an appropriate plot to find the number of attributes required to explain at least 80% of the total variation in the data.</li>

</ul>