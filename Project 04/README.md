# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Predict Dengue Cases

# <u>Background</u>

Dengue fever is a mosquito-borne viral illness that poses a significant public health threat in Singapore. Dengue fever is endemic in Singapore, with frequent outbreaks causing considerable morbidity and occasionally even mortality. With the incidence of <u>[**dengue increasing globally**](https://www.paho.org/en/news/3-8-2023-dengue-cases-increase-globally-vector-control-community-engagement-key-prevent-spread#:~:text=During%20the%20EPI%2DWIN%20Webinar,million%20infections%20occurring%20each%20year.)</u>, it is crucial to implement effective prevention and control strategies.

As part of the <u>[**Vector Biology and Control Division (VBCD)**](https://www.nea.gov.sg/corporate-functions/who-we-are/groups-and-divisions/public-health-groups-and-divisions)</u>, we carry out research and surveillance of mosquitoes and other vectors and risk assessment of present and future vector-borne diseases that pose a public health threat to Singapore. The division continually explores and evaluates new and safe control tools, and develops novel strategies for risk intervention and management tailored to Singapore's unique urban and dense landscape.


# <u>Problem Statement</u>

The National Environmental Agency (NEA) is tasked with managing and reducing the impact of dengue in the country. Predicting dengue outbreaks is a complex task that requires taking into account a variety of factors, including environmental, social, and behavioral variables.

Project Wolbachia in Singapore aims to reduce dengue transmission by releasing mosquitoes infected with Wolbachia bacteria. However, the project has faced challenges including ecological concerns, <u>[**skepticism from the community**](https://www.todayonline.com/voices/project-wolbachia-residents-are-killing-helpful-mosquitoes-which-can-be-nuisance)</u>, <u>[**high costs**](https://journals.plos.org/globalpublichealth/article?id=10.1371/journal.pgph.0000024#:~:text=Under%20an%20assumed%20steady%2Dstate,to%202020%20under%2040%25%20intervention)</u>, <u>[**weather disruptions**](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9098883/)</u>, and integration with other control measures. Monitoring and evaluating the project's impact are essential for its success and to inform future dengue control strategies.

As part of the VBCD, we seek to develop a predictive model capable of forecasting the number of dengue cases and understanding the trends in dengue outbreaks for a subsequent period. The model would incorporate a wide range of relevant factors that influence the spread of dengue, over a period of 2012 to 2023.

Specifically, the model should include:

1. **Weather Data**: It is well-known that climatic conditions play a pivotal role in affecting mosquito behavior and the spread of dengue fever. Hence, the model will incorporate data on weather variables such as temperature, humidity, and rainfall to assess their potential influence on dengue cases.

2. **Google Search Trends**: A notable indicator of public awareness and concern regarding dengue is the volume of related search queries on Google. Therefore, the model will include Google search trends data on dengue-related terms spanning to reflect the behavioral dynamics that might contribute to the spread of the disease.

3. **Project Wolbachia Data**: Project Wolbachia, initiated to curb the transmission of dengue, involves the release of mosquitoes infected with Wolbachia bacteria, impairing their ability to transmit the virus. The model will take into account data on the timing and locations of Project Wolbachia releases to understand their potential impact on the incidence of dengue cases.

Accurate predictions from the model can have significant implications for public health in Singapore. With reliable forecasts, the VBCD can:

1. **Allocate Resources Efficiently**: By anticipating dengue outbreaks, the VBCD can allocate resources, such as mosquito control teams and public health campaigns, more efficiently to areas at higher risk.

2. **Target Prevention Measures Effectively**: With insights into the factors driving dengue outbreaks, the VBCD can tailor prevention measures, such as fogging, removal of breeding sites, and public education, to specific high-risk areas and times.

3. **Raise Public Awareness**: During periods of high predicted risk, the VBCD can increase public awareness campaigns to inform residents about the importance of mosquito control and dengue prevention measures.

4. **Assess the Impact of Project Wolbachia**: By incorporating data on Project Wolbachia, the model can provide insights into the effectiveness of the program and inform decisions on future releases of Wolbachia-infected mosquitoes.

Ultimately, the development of a robust predictive model for dengue cases in Singapore will contribute to more effective dengue management and prevention strategies, thereby reducing the impact of dengue on public health and the economy.


# <u>Data</u>

Final dataset used for modelling (before scaling):

|Feature|Type|Datasource|Description|
|---|---|---|---|
|dengue haemorrhagic fever|integer|[weekly_infectious_disease_bulletin_year_2012_2022.csv](https://www.moh.gov.sg/resources-statistics/infectious-disease-statistics/2022/weekly-infectious-diseases-bulletin)|Number of recorded cases of Dengue Fever in an epidemiological week|
|chikungunya fever|integer|[weekly_infectious_disease_bulletin_year_2012_2022.csv](https://www.moh.gov.sg/resources-statistics/infectious-disease-statistics/2022/weekly-infectious-diseases-bulletin)|Number of recorded cases of Chikungunya Fever in an epidemiological week|
|zika virus infection|integer|[weekly_infectious_disease_bulletin_year_2012_2022.csv](https://www.moh.gov.sg/resources-statistics/infectious-disease-statistics/2022/weekly-infectious-diseases-bulletin)|Number of recorded cases of Zika Virus Infections in an epidemiological week|
|Dengue fever: (Singapore)|integer|[term_google__trend_2012_2023.csv](https://trends.google.com/trends/explore?date=2012-01-01%202023-08-24&geo=SG&q=%2Fm%2F09wsg)|Numbers represent search interest relative to the highest point on the chart for the given region and time|
|Insect repellent: (Singapore)|integer|[term_google__trend_2012_2023.csv](https://trends.google.com/trends/explore?date=2012-01-01%202023-08-24&geo=SG&q=%2Fm%2F09wsg)|Numbers represent search interest relative to the highest point on the chart for the given region and time|
|weekly mean rainfall (mm)|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The weekly mean rainfall recorded at the Changi Climate Station|
|highest 30 min rainfall(mm)|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The highest 30 min rainfall for the week recorded at the Changi Climate Station|
|highest 60 min rainfall (mm)|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The highest 30 min rainfall for the week recorded at the Changi Climate Station|
|highest 120 min rainfall (mm)|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The highest 30 min rainfall for the week recorded at the Changi Climate Station|
|mean temperature|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The weekly mean air temperature recorded at the Changi Climate Station|
|maximum temperature|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The weekly maximum temperature recorded at the Changi Climate Station|
|minimumtemperature|float|[combined_data.csv](http://www.weather.gov.sg/climate-historical-daily/)|The weekly minimum temperature recorded at the Changi Climate Station|

# <u>Models MAPE scores summary</u>

|Models|MAPE Scores|
|---|---|
|ARIMA|0.20|
|SARIMA|<u>**0.13**</u>|
|ARIMAX|0.20|
|PyCaret's SARIMA|0.37|
|PyCaret's SARIMAX|0.40|

# <u>Conclusion</u>

 **Model Accuracy**: 
   - A MAPE of 0.13 indicates that the SARIMA model predictions are, on average, off by 13%. This also means that the model has an accuracy rate of 87%. In forecasting terms, accuracy is crucial, especially for predicting dengue cases.

 **Benefit to Project Wolbachia**:
   - The model can serve as a reliable tool for the **Project Wolbachia** team to anticipate dengue outbreaks, allowing them to strategize the release of Wolbachia-infected mosquitoes more effectively. By being able to predict dengue cases, the team can optimize its interventions, possibly leading to more efficient suppression of the Aedes mosquito population.
   
In conclusion, the SARIMA model, with its promising MAPE of 0.13, offers valuable insights that can significantly enhance the efficiency of dengue control initiatives like **Project Wolbachia**. By harnessing this predictive power, NEA can take a more proactive stance in its efforts to combat dengue in the region.


## Cost-Benefit Analysis

Using the MAPE (Mean Absolute Percentage Error) of 0.13, We've determined that our model's accuracy is approximately 87% (1 - MAPE). Given the steady-state costs of US$22.7M per year, and with an objective to target 80% efficiency, We used the formula to calculate the potential cost averted by our model:

```
(1-MAPE) x (Benefit Ratio) - (Steady-State Cost x Scaling Factor) 
= (1-0.13) x 55.93 - (22.7 x 1.8) 
= US$7.79 million
```

Based on this, We estimate that by implementing our model, we can potentially avert costs to the tune of US$7.79 million, showcasing the significant financial value of our model in the context of dengue prevention and strategic resource allocation. NEA can assess the trade-offs between the costs and benefits of the program. This analysis helps optimize resource allocation and maximize the benefits of the program in reducing dengue cases, healthcare costs, and productivity losses.


In conclusion, the SARIMA model, with its promising MAPE of 0.13, offers valuable insights that can significantly enhance the efficiency of dengue control initiatives like **Project Wolbachia**. By harnessing this predictive power, NEA can take a more proactive stance in its efforts to combat dengue in the region.
