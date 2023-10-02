#  ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2 - Singapore Housing Data and Kaggle Challenge

![housing](images/housing.jpeg)

## Background

The rising housing prices in Singapore have become a prominent and complex issue affecting residents and the overall economy. Over the past few years, there has been a rapid surge in property values, resulting in challenges related to housing affordability and accessibility for many individuals and families. Several factors contribute to this phenomenon. First and foremost, Singapore's limited land supply and growing population put significant pressure on the housing market, leading to an increase in demand for housing units. Additionally, the country's status as a global financial hub and an attractive destination for foreign investors further fuels demand and competition in the real estate sector.

Government policies and initiatives aimed at promoting homeownership and investment in the property market also play a role in the rising prices. While these policies have helped many citizens acquire properties, they have also contributed to the surge in property values. Furthermore, economic growth, low-interest rates, and favorable financing options have encouraged property speculation and investment, further driving up housing prices. As a result, first-time homebuyers and low to middle-income families may face difficulties in purchasing their own homes.

The escalation in housing prices has led to concerns about social equity and income inequality, as well as the potential risk of a property bubble. Policymakers are grappling with the challenge of striking a balance between stimulating economic growth through the property market and ensuring housing affordability for all citizens. Addressing the issue of rising housing prices requires a comprehensive and multi-faceted approach. Policymakers, real estate experts, and stakeholders are continuously exploring various measures to regulate the market, enhance housing supply, and introduce affordability schemes to alleviate the impact on vulnerable segments of the population.

## Problem Statement

The rapid increase in housing prices in Singapore has become a major concern for residents and policymakers. To address this issue, we aim to develop a regression model that can accurately predict housing prices based on various factors such as property features, location, economic indicators, and demographic trends. By understanding the underlying patterns and drivers of housing prices, the regression model will enable us to identify key factors contributing to the soaring prices. This, in turn, will assist in formulating effective policies and strategies to manage housing affordability and create a more sustainable and balanced real estate market in Singapore. The ultimate objective is to provide valuable insights to stakeholders and policymakers, aiding in the development of evidence-based solutions to tackle the challenges posed by escalating housing costs.

Some guideline questions for this project:
- What are the factors that we can consider as input features for the regression model?
- What potential benefits can stakeholders and policymakers gain from the insights provided by the regression model?

## Findings

**Top Predictors** 
 - Flat models
 - Regions
 - Floor area sqm

**Conclusions**:

- Predictive Accuracy: The ridge regression model has shown promising results in accurately predicting housing prices in Singapore based on various factors, including property features, location, economic indicators, and demographic trends. Comparing the results of the test and train set, there is a margin of error at **<u>0.99%</u>**. 

- Significant Factors: The model has identified the key drivers of soaring housing prices, allowing policymakers to gain insights into the most influential factors contributing to the increase. From the model, we can safely assume that some features of the model like `Flat models`, `Regions` and the `Floor area sqm` are some of the strong key drivers of the housing price.

- Model Robustness: The ridge regression model's regularization parameter (alpha) has been tuned to find an optimal value, ensuring the model's stability and reducing the risk of overfitting.

- Policy Insights: The regression model's outputs have provided valuable insights into the relationships between different variables and housing prices, guiding policymakers in formulating evidence-based policies.

**Recommendations**:

- Address Supply Constraints: Based on the model's findings, policymakers should focus on increasing the supply of housing units to meet the growing demand. This could involve optimizing land use, redeveloping underutilized areas, and streamlining approval processes for new housing developments.

- Targeted Affordable Housing Initiatives: Utilize the regression model to identify areas with the greatest affordability challenges and design targeted affordable housing initiatives. These initiatives should cater to the needs of low and middle-income families, providing them with access to more affordable housing options.

- Sustainable Urban Planning: Implement sustainable urban planning practices that promote balanced growth and ensure housing affordability. This includes integrating residential, commercial, and recreational spaces to create vibrant and self-sustaining communities.

- Manage Speculation: To curb excessive speculation and stabilize the housing market, consider implementing measures such as property cooling measures or capital gains taxes on property transactions.

- Public-Private Partnerships: Foster collaborations between the public and private sectors to address housing affordability issues. Encourage developers to participate in affordable housing projects and provide incentives for creating housing units that cater to diverse income groups.

- Regular Market Monitoring: Continuously monitor the real estate market and economic indicators to detect potential bubbles or price fluctuations. Implement timely interventions to mitigate risks and maintain market stability.

- Data-Driven Policy Decisions: Leverage the predictive capabilities of the ridge regression model to make informed policy decisions. Regularly update and refine the model using new data to ensure its relevance and accuracy.

- Community Engagement: Involve residents and stakeholders in the policy development process to understand their housing needs and preferences. Engaging the community will lead to more inclusive and effective housing policies.

By adopting these recommendations and leveraging the insights from the ridge regression model, policymakers can work towards a more sustainable and balanced real estate market in Singapore, ensuring that housing remains affordable for the residents while fostering responsible growth and development in the housing sector.

## Moving Forward

While the predictive model and key features provide great insights for the investor, we are still limited to the data quality and the limited features. Regression models assume a linear relationship between the independent variables and the dependent variable. If the true relationship is non-linear, the model may not accurately capture the underlying patterns in the data. The model's predictions may also not be reliable when making predictions beyond the range of the training data (extrapolation). The model might not have enough information to accurately predict prices in unobserved scenarios.

To enchance the model and improve performance, we can consider the following:

- Include external factors like government policies, interests rates and macroeconomic indicators that may impact housing prices.
- Using other more advance forms of regression models.
- Collaborate closely with stakeholders, policymakers, and domain experts throughout the model development process. Gather feedback and insights from them to ensure that the model's recommendations align with their needs and priorities.

## Data Dictionary
https://www.kaggle.com/competitions/dsi-sg-project-2-regression-challenge-hdb-price/data

## References
https://www.eastasiaforum.org/2023/04/15/investigating-singapores-public-housing-issues/
https://www.reuters.com/breakingviews/pricey-property-is-pointy-dilemma-singapore-2023-06-28/
https://www.greenspinnaker.co.uk/the-future-of-housing/