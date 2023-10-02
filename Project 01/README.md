# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring Climate Data of Singapore

## Lim Zi Ming

## Problem Statement

We are a group of data scientists working for the Singapore Health Promotion Board who is responsible for developing and organising health promotion and disease prevention programmes. The Health Promotion Board aims to empower Singaporeans to attain optimal health, increase the quality and years of healthy life and prevent illness, disability and premature death.

We have been tasked by Health Promotion Board to explore if rainy seasons has a correlation with mortality rate and hospital visits. This would allow Health Promotion Board to make informed decisions and develop targeted interventions during rainy seasons to address any potential health risks. By understanding the relationship between rainy seasons and mortality rates or hospital visits, the Health Promotion Board can implement preventive measures, allocate resources effectively, and develop appropriate health promotion campaigns.

# Executive Summary

he Health Promotion Board has tasked us with exploring the correlation between rainy seasons and mortality rates, as well as hospital visits, in order to make informed decisions and develop targeted interventions. Our analysis aims to address potential health risks associated with rainy seasons and provide recommendations to the Health Promotion Board.

Through our investigation, we have found evidence suggesting a correlation between rainy seasons and adverse health outcomes. Our analysis indicates that during rainy seasons, there is an increase in mortality rates and hospital visits, potentially due to factors such as increased incidence of respiratory infections, accidents related to slippery conditions, and waterborne illnesses.

To address these findings, we recommend the following actions:

- Enhance Public Awareness: Develop and implement public awareness campaigns to educate the population about the potential health risks associated with higher PSI level periods. Focus on promoting preventive measures and safety practices to reduce the impact of adverse weather conditions.

- Strengthen Healthcare Infrastructure: Allocate resources and strengthen the healthcare infrastructure, particularly in areas prone to higher mortality rates and increased hospital visits during rainy seasons. This includes ensuring sufficient healthcare facilities, medical personnel, and necessary equipment to handle the potential surge in demand.

- Targeted Interventions: Develop targeted interventions and initiatives specifically tailored to address health risks during rainy seasons. This could involve providing information on proper hygiene practices, immunizations, and appropriate medical care for common rainy season-related illnesses.

- Collaboration with Meteorological Agencies: Establish collaborations with meteorological agencies to obtain accurate and timely weather forecasts. This will enable the Health Promotion Board to proactively plan and respond to potential health risks associated with specific weather conditions during the rainy seasons.

- Data Monitoring and Analysis: Continuously monitor and analyze data related to mortality rates and hospital visits during rainy seasons. Identify trends and patterns to gain deeper insights into the specific health risks and challenges faced during these periods. This will facilitate evidence-based decision-making and targeted interventions.

- Community Engagement: Engage with the community through outreach programs and partnerships with local organizations. Encourage community participation in health promotion activities, disaster preparedness, and response plans during rainy seasons.

- Evaluation and Continuous Improvement: Regularly evaluate the effectiveness of interventions implemented during rainy seasons. Collect feedback from healthcare professionals, the community, and other stakeholders to identify areas for improvement and make necessary adjustments to strategies and campaigns.

By implementing these recommendations, the Health Promotion Board can effectively address potential health risks during rainy seasons, enhance public health outcomes, and ensure the well-being of the population.

Our analysis provides a solid foundation for evidence-based decision-making, allowing the Health Promotion Board to take proactive measures in ensuring public health and safety during rainy seasons.


## Datasets

#### Provided Data

There are 2 datasets included in the [`data`](./data/) folder for this project. These correspond to rainfall information. 

* [`rainfall-monthly-number-of-rain-days.csv`](./data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* [`rainfall-monthly-total.csv`](./data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022
* [`Hosp_visits_monthly.csv`](./projects/project_1/data/Healthcare/Hosp_visits_monthly.csv): Hospital admissions in monthly
* [`Hospital_visits.xlsx`](./projects/project_1/data/Healthcare/Hospital_visits.xlsx): Hospital admissions in yearly
* [`Mortality_rate.xlsx`](./data/Healthcare/Mortality_rate.xlsx): Death and life expectancy of various categories
* [`historical-24-hr-psi.csv`](./data/Healthcare/historical-24-hr-psi.csv): Historical data of PSI levels at different regions in Singapore

Other relevant weather datasets from [data.gov.sg](data.gov.sg) that you can download and use are as follows:

* [Relative Humidity](https://data.gov.sg/dataset/relative-humidity-monthly-mean)
* [Monthly Maximum Daily Rainfall](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)
* [Hourly wet bulb temperature](https://data.gov.sg/dataset/wet-bulb-temperature-hourly)
* [Monthly mean sunshine hours](https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration)
* [Surface Air Temperature](https://data.gov.sg/dataset/surface-air-temperature-mean-daily-minimum)

## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|total_rain|float|rainfall-monthly-total|Total rainfall in mm| 
|no_of_rainy_days|integer|rainfall-monthly-number-of-rain|Number of rainy days on the month|
|psi|integer|historical-24-hr-psi|Mean levels of PSI at different regions per year|
|death_by_age|float|Mortality_rate|Rate of death per 1,000 residents|
|death_by_causes|integer|Mortality_rate|Total number of deaths due to respiratory diseases|
|total_visits|int|Hospital_visits|Total number of admissions per year|

## Conclusion:
In conclusion, our exploration of the correlation between rainy seasons and mortality rates, as well as hospital visits, has provided valuable insights for the Health Promotion Board. By understanding the relationship between rainy seasons and health outcomes, the Health Promotion Board can make informed decisions and develop targeted interventions to address potential health risks during these periods.

Our analysis highlights the importance of implementing preventive measures, allocating resources effectively, and developing appropriate health promotion campaigns during rainy seasons. By enhancing public awareness, strengthening healthcare infrastructure, and implementing targeted interventions, the Health Promotion Board can effectively mitigate the impact of adverse weather conditions on public health.

Overall, our findings provide a solid foundation for the Health Promotion Board to develop evidence-based strategies and interventions that will lead to improved health outcomes during rainy seasons.

## References:
* https://www.mdpi.com/2073-4433/11/1/9
* https://www.straitstimes.com/world/air-pollution-kills-6-to-7-million-prematurely-every-year-un-report
* https://reference.nlb.gov.sg/guides/sci-tech/sciences/air-pollution/
* https://ehjournal.biomedcentral.com/articles/10.1186/s12940-019-0476-4