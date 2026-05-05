# My Portfolio

## About me


## Projects
Executive Summary

To develop a better understanding of current wider market conditions within insurance industry, public data must be utilized and interpreted. 

Utilising supervised models, where answers are known, linear regression can be leveraged to accurately predict market movements driven by historical data that is available. This is the basis of the Data science Project. Being able to contextualize the market conditions enhances guidelines for sustainable growth and aids in creating realistic targets/plans that can be achieved.

As a result of the analysis, public UK Insurance market data is weaker than expected. There are too few data points to create a robust model that can instill a high level of confidence in results. In order to improve the model, different data sources must be used in conjunction with one another to create a bigger and clearer picture of the previous and current market conditions to generate an accurate and trust worth prediction into the future of the market. EDA has shown that there is a decline in number of policies for majority of products. However, there are exceptions to the trend where specific products are stable across the prior years, furthermore there are also outliers which show an increasing trend over the prior years.

This project could be taken a step further by utilizing alternate methodology such as time series forecasting. Not only is this also a supervised model, it would also enable the extension of the question. Not only uncovering current and future market saturation but also uncovering when this is most likely to manifest and where the current and future trend is likely to end up.

Methodology

Insurance market is assumed to be in a softening state. The purpose of the project is to answer the following question; Can a large-scale UK insurer continue to sustainably grow in volume or is the UK insurance market saturated?

Hypothesis: Annual insurance transaction activity in the UK is flat or declining over time

Linear regression is the scientific methodology of choice. This supervised learning method is appropriate as the data is mainly numerical which fits with the continuous numerical output of the model compared to other methodologies such as logistic regression, which classifies data into binary categorical outputs such as 0 or 1, which would not be suitable for this project.

ETL:
<img width="572" height="120" alt="image" src="https://github.com/user-attachments/assets/dd27bfbb-e71f-4753-b0b9-b3cec70f7488" />

 
Figure 1: ETL Diagram
•	FCA data transformed by utilizing Excel
•	Transformed Dataset is loaded into Python ready for data science techniques to be applied

Data was extracted from FCA website. This is a trusted public data source which helps with transparency and accessibility. The data is free and easily scrutinized, which ensures that it can be of the highest standard, ready for impactful analysis.

Date cleansing and EDA are important steps to during the transformation stage of the ETL process, ensuring that data is understood as well as maintain a high level of data integrity. This will enable accurate results and analysis. At a surface level, data is explored and cleaned within Excel. Rationale for tool choice is driven by ease of access when manipulating data. Python could also be a suitable alternative to action any transformational changes necessary, however small changes may be over-complicated when using programming languages rather than accessible Graphical User Interface features available in applications such as Excel.

Python is the tool of choice for the linear regression model. There is an abundance of packages and libraries that can be leveraged to complete the linear regression model and provide useful insights. There are alternative tools such as R, SQL and Java. These have not been chosen due to accessibility of python as well as the easy-to-understand programming language. There is also a large community of data scientists who utilize Python which makes debugging easier when confronting errors as experience is shared across forums.
<img width="543" height="572" alt="image" src="https://github.com/user-attachments/assets/6ca7aec6-5b84-4175-a6c7-e82dde69db33" />

 
Figure 2: Raw data from FCA loaded in Excel

Data is transformed by cleaning and ensuring data is well structured and of high quality with no null entries as well as correct data types within fields. Useful data is also curated from the whole dataset to reduce noise in the machine learning model. 

Data context is also important to ensure data is fully understood. In this scenario, the asterisks are in place where the data has not been populated due to a low volume of submission data from firms. Essentially, these asterisks are to be treated as nulls.  
<img width="940" height="131" alt="image" src="https://github.com/user-attachments/assets/ec6bd3ca-d7f4-4132-9363-b53efc69998d" />

Figure 3: Data note included on FCA Export

When handling nulls there are two viable options, to impute or drop from the data. The dataset, although spans 3 years, is not very large. Dropping any number of rows could negatively Impact data integrity. On the other hand, imputing could reduce variance and inadvertently introduce overfitting and bias. The two options are to be weighed up in context of the data and the project question. 

Dropping the rows is the desired choice in this scenario. This will equate to <10% of the data being removed. This was chosen over imputing as it would introduce bias as there are different products within the dataset and therefore an average across all products would not be viable. Entries that are null all fall under buckets where there are multiple years of data missing therefore using any statistical imputation of average (mean, median or mode) of the specific product across the years would also not be viable.

Results

EDA:

Surface level EDA has shown across the 3 years included in the dataset, there is a general trend of decline in 2024. In some cases, there is a peak in 2023 compared to 2022, which resolved to a decline in 2024 over the prior 2 years. There are some anomalies to this general trend, where there has been a consistent trending increase over the 3 years included in the data. This highlights that there may be caveats to be included such as specific products can deviate from general market saturation in specific areas. These findings are displayed in line graphs and tables to visually communicate effectively.
<img width="464" height="249" alt="image" src="https://github.com/user-attachments/assets/e6ecfe2f-1fd4-498d-8c34-36c94d2e884f" /><img width="463" height="249" alt="image" src="https://github.com/user-attachments/assets/7effd4ca-04d8-4e8b-8996-0070c41b441b" />
<img width="499" height="262" alt="image" src="https://github.com/user-attachments/assets/db858cb1-2031-441a-a840-c28b2bdfa7cd" /><img width="441" height="261" alt="image" src="https://github.com/user-attachments/assets/4bcf5cbf-8042-4c4f-93ca-488f8c517160" />

 
Transformed dataset loaded into python as well as packages and libraries.
<img width="304" height="113" alt="image" src="https://github.com/user-attachments/assets/a9e6f19f-4830-4fd6-834e-6a24baf5968d" /><img width="371" height="140" alt="image" src="https://github.com/user-attachments/assets/f7ceda7c-d15c-4fb3-9614-4df2b0b1beb8" />


  

The data is explored further in python. Completing EDAs throughout the process ensures that the data is of high quality throughout the project.  
<img width="940" height="332" alt="image" src="https://github.com/user-attachments/assets/e1971b51-f802-4cff-82a5-503a5495cb41" />

As a result of the EDA, there is some feature engineering to take place. Column names to be changed to text to ensure there are no errors as the project is progressed, as well as manipulating the data to ensure that all columns are numerical. These text-based columns would have to be dropped if they are not manipulated, which is not preferred. Instead, each row is assigned a numerical code, and column names are altered.
<img width="792" height="349" alt="image" src="https://github.com/user-attachments/assets/420024d2-6120-4cff-961f-e019004ca397" />
 

Profile of the dataset it created to ensure full understanding of the data as well as validating earlier cleansing.   
<img width="940" height="85" alt="image" src="https://github.com/user-attachments/assets/39ed2fe9-7e5b-469d-b914-fee1a1d9044f" />
<img width="940" height="331" alt="image" src="https://github.com/user-attachments/assets/fc50085f-218d-49ad-9660-2810def206a2" />
<img width="681" height="489" alt="image" src="https://github.com/user-attachments/assets/dd4cef7a-b4fe-430f-b0f4-f9e519b566e0" />
<img width="685" height="416" alt="image" src="https://github.com/user-attachments/assets/c9666c29-5891-4c0f-99c7-22892ab02790" />
<img width="940" height="357" alt="image" src="https://github.com/user-attachments/assets/944b714d-ffb4-498b-b597-c23da136f0a4" />
   

From the profile, it can be deduced that product is not correlated with Total policies in force. There is a linear trend between the years and the total. There is also a large variance between the minimum and maximum numbers within fields. This may be a cause for concern that will require normalizing the dataset in order to scale the data correctly. This ensures that the model can perform accurately.
Data is then scaled via minmax scaler. This assigns each number a value from 0 to 1, ensuring that all values are scaled the same. This is an important step as it helps with machine learning performance as well as preventing features from skewing the model.  
<img width="940" height="260" alt="image" src="https://github.com/user-attachments/assets/4e16b34a-1c3e-485c-adea-c00b847b1338" />

Following the scaling, data is then prepared by creating a train and test split. The chosen split is 70/30 which is industry standard but this can be altered depending on the model and the data that is being used. The data is also randomised to ensure that any prior sorting on the data does not skew the results of the model. In order for predictions to be unbiased, the test data is kept from the model to ensure no bias is introduced.  
<img width="940" height="324" alt="image" src="https://github.com/user-attachments/assets/0771caae-1105-4ae6-96e2-d800b4173128" />

Brief EDA is performed on the train dataset; this ensures data is understood at every step of the model pipeline. 
<img width="702" height="556" alt="image" src="https://github.com/user-attachments/assets/3fcba981-33cc-4041-819a-a1bfb710eecc" />
 
Following EDA, field to be predicted is separated from the input variables 
<img width="849" height="465" alt="image" src="https://github.com/user-attachments/assets/a10404e1-d773-4249-b31f-83bccc79cd24" />
 
Another EDA takes place of the training dataset. The EDA highlights that the data, although scaled, is positively skewed. This could negatively impact the performance of the model.
<img width="855" height="635" alt="image" src="https://github.com/user-attachments/assets/366afbc4-0bfe-4f50-927e-21fa8556e66b" />
 

Model is then initialized
<img width="629" height="208" alt="image" src="https://github.com/user-attachments/assets/fb5d6e6c-71b0-4721-a162-fe92c8d42811" />
 
Intercepts and coefficients are presented to further understand the results of the model. These are then used to create some manual predictions.
<img width="940" height="491" alt="image" src="https://github.com/user-attachments/assets/ceb2e546-52e8-44cb-9a23-a6c5588662d0" />
 
Model is then evaluated utilising performance metrics such as R squared Score, Root Mean Squared Error (RMSE) and Mean Absolute Percentage Error (MAPE). R Squared is the proportion of variance in the dependent variable that is predictable from the independent variables. Value closer to 1 indicates a better fit. RMSE is the square root of the average of squared differences between prediction and actual observation. Value closer to 0 indicates no error. MAPE measures the accuracy of forecasting or regression models by calculating the average absolute percentage difference between predicted and actual values. Lower values are an indicator of better model performance.
<img width="711" height="672" alt="image" src="https://github.com/user-attachments/assets/eba5156a-8493-4246-a6c8-45a689c4b428" />
 

Analysis:

Upon in-depth analysis it was found that the model does not have a high level of confidence. Results show that the R Squared score, RMSE and MAPE all indicate the model being perfect. This is a highly unlikely scenario and is more likely linked to flaws within the data. Part of these flaws include a lack of data point to create predictions. Furthermore, the dataset also reduced in size when the train and test split is initialized. To link back to the question and hypothesis, it is clear from the various EDA’s performed during the project that there is an overall trend of decreasing policies in force of the 3 years that are included in the data. The model cannot be trusted in order to prove or disprove the hypothesis, however, EDA also highlights that although the market in general is declining, there are opportunities that deviate from the general trend and may pose as viable options to attack. This results in a not entirely saturated UK insurance market.

These findings have been displayed as various tables and graphs in order to paint a clear picture of the analysis and aid with the story telling of the data. Clear depictions enable quick and efficient decision making by the relevant stakeholders.



Recommendations

Findings show that there are indicators present that highlight signs of market softening, but there may still be room for growth. To better justify this, more robust datasets should be used to ensure that not only can future models perform better, but also to ensure that the market as an entirety is better represented within the results.

Issues with data proved to negatively impact the model, these could be solved by implementing further normalization techniques such as Log Transformation or Yeo-Johnson Transformation. These methods will help to minimize skewness within the data, aiding in better model performance.

Multiple data sources would also prove to better the project, not only would this provide more data for the model but would also further enhance the questions that can be answered from the study. For example, joining policies in force with UK population could enhance findings and show not only if the market is becoming saturated but also why it may be the case.

Alternative machine learning methodologies could also be used in conjunction with linear regression such as Time Series forecasting. This would further enhance the results of the project by not only confirming or denying if the UK insurance market is saturated, but also aiding in showing, visually, when the saturation will manifest.


## Work Experience

