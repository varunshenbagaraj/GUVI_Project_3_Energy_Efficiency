## GUVI_Project_3_Energy_Efficiency
A comparison of the strongest predictors computed by Linear Regression and Random Forest in predicting the Heating &amp; Cooling Load of buidings.

### Industrial Automation - Energy Efficiency
### Problem Statement:
The effect of eight input variables (relative compactness, surface area, wall area, roof area, overall height, orientation, glazing area, glazing area distribution) on two output variables, namely heating load (HL) and cooling load (CL), of residential buildings is investigated using a statistical machine learning framework. We have to use a number of classical and non-parametric statistical analytic tools to carefully analyze the strength of each input variable's correlation with each of the output variables in order to discover the most strongly associated input variables. We need to estimate HL and CL, we can compare a traditional linear regression approach to a sophisticated state-of-the-art nonlinear non-parametric method, random forests.

### Data Set Information:
We perform energy analysis using 12 different building shapes simulated in Ecotect. The buildings differ with respect to the glazing area, the glazing area distribution, and the orientation, amongst other parameters. We simulate various settings as functions of the afore-mentioned characteristics to obtain 768 building shapes. The dataset comprises 768 samples and 8 features, aiming to predict two real valued responses. It can also be used as a multi-class classification problem if the response is rounded to the nearest integer.

### Attribute Information:
The dataset contains eight attributes (or features, denoted by X1...X8) and two responses (or outcomes, denoted by y1 and y2). The aim is to use the eight features to predict each of the two responses.
* X1 Relative Compactness
* X2 Surface Area
* X3 Wall Area
* X4 Roof Area
* X5 Overall Height
* X6 Orientation
* X7 Glazing Area
* X8 Glazing Area Distribution
* y1 Heating Load - Target
* y2 Cooling Load - Target


#### Dependencies
* Programming Language – *Python*
* Data Analysis – *Pandas*
* Data Visualization – *Matplotlib, Seaborn*
* ML Algorithms – *Linear Regression, Random Forest Regression*
* Performance Evaluation – *Accuracy Score*

#### Approach
* All the features were renamed for better readability.
* Feature extraction was performed. Floor Area was introduced into the dataset.
* EDA was performed to check for multicollinearity and eliminate the same
* The results of prediction was evaluated using accuracy score.
* The best model can be decided based on the accuracy score
* Important  features(i.e. strongest predictors) were computed from the coefficients(weights) and attributes available within the model.
* Evaluation metrics and Feature importance have been tabulated.

#### EDA Insights
* We observed that **Surface_Area = Wall_Area + 2 x Roof_Area**. We know that, **Roof_Area = Floor_Area** in buildings, a new feature Floor_Area was introduced into the dataset thus making **Surface_Area = Wall_Area + Roof_Area + Floor_Area**
* **Relative Compactness and Surface Area are inversely proportional.** Since Wall_Area (WA), Floor_Area (FA), and Roof_Area (RA) are directly proportional to Surface Area(SA), **Relative Compactness is inversely proportional to RA, WA, FA also.**
* The dependent variables **Heating_Load & Cooling_Load itself are directly proportional** to each other. Therefore, **further investigation is required whether either of them can be dropped for Linear Regression.**

#### Further Developments
* Investigation required if we can eliminate either of the regressands since they are directly proportional to each other.
* Eliminating one of them will make applying gradient descent easier by which Linear Regression can be optimized
* Industry experts to be consulted to get details about the optimum loads so that building can be modelled in a very sustainable manner to consume the right amount of electricity.
