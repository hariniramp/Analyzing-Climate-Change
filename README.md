# Analyzing Climate Change: The Evolution and Public Opinion
# Harini Ram Prasad

## Introduction

The issue of climate change is something that has been significantly impacting the world since the early 19th century. Scientists have argued that greenhouse gas emissions could be contributing to global warming. Over the years, we've observed increases in global temperature, depletion of precious natural resources and severe damage to the environment. Solutions to these problems involve policies on green energy, conservation and education in climate change. Another observable factor is public opinion on climate change. Often, we see that policies around climate change, or lack thereof, indicate that the threat is one that people do not take seriously enough. In fact, a huge subsection of the population firmly believes that climate change is a hoax, and not a real problem whatsoever. For us to affect real impact in the realm of climate change, it is necessary to educate people on the matter, in conjunction with instituting progressive policy. A brief scientific abstract outlining the project methodology and details is available [here](https://github.com/hariniramp/data-512-final/blob/main/Scientific%20Abstract.pdf). A short slide deck with the project highlights can be found [here](https://github.com/hariniramp/Analyzing-Climate-Change/blob/main/Analyzing%20Climate%20Change_%20Summary%20Slide%20Deck.pdf).

### Motivation
**Part I:**

Part 1 of my analysis focuses on the actual phenomenon of climate change.The effects of climate change can be seen in the increase in global surface temperature, rising sea levels,increasingly frequent extreme weather events and the rapid decline in biodiversity. All the major causes of climate change point to human activities: deforestation, the use of fossil fuels, increase in greenhouse gas emissions, etc. Since climate change is something that almost entirely stems from human activities, it becomes important to increase discussion about the climate and raise awareness amongst people about this issue. The only way to combat climate change is to educate people about the realities of climate change and the serious damage we've been inflicting on our environment.

**Part II:**

This brings me to Part 2 of my analysis: people's attitudes towards climate change. A lot of people truly believe that the idea of climate change is a hoax or are in denial and this is a real problem. The only way to curb climate change is to get people to change their attitudes and transition to a more sustainable lifestyle. So, this led me to anlayze people's views about climate change.

As for the **audience**, I think ideally everyone should care about this anlaysis because it is something that impacts literally everyone. However, this analysis pertains to anyone who is interested in the weather and changing climate. My hope however, is people who don't believe in climate change explore my analysis so that I am able to lend a hand in educating those either ill-informed or with their heads in the sand.

## Dependencies

The dependencies used in analysis of this dataset are as follows:

* wget
* kaggle
* urllib
* pyramid-arima
* pandas
* numpy
* zipfile
* scipy
* matplotlib
* statsmodels
* seaborn
* os

## Research Questions and Findings

My goal with the project was to address trends and patterns in climate change as well as public opinion around it. To this end, I divided my analysis into two main questions, with subsections devoted to various analyses. I would like to answer some of the following questions concerning both climate change itself, as well as people's perceptions regarding it. A detailed account of the analysis and findings can be found on [this Jupyter notebook](https://github.com/hariniramp/data-512-final/blob/main/Analyzing_Climate_Change_The_Evolution_and_Public_Opinion_.ipynb). All the outputs and visualizations from my analysis can be found in the [Visualizations directory](https://github.com/hariniramp/data-512-final/blob/main/Visualizations).

*   **What factors influence the way people think about climate change?**
1.   Does a state's political affiliation impact the way they answer certain questions about climate change?

![Republican Voter Percentage vs. Attitudes on various Climate Change Issues](https://github.com/hariniramp/data-512-final/blob/main/Visualizations/scatter_rq1.png)

As we can see from the above visual, the general trend seems to portray that as the percentage of Republican voters in a county increases, the percentage of people in that county who wish to de-prioritize different climate change issues increases as well. With this figure and results of a hypothesis test, we can say with 95% confidence that Republican counties are more likely to vote against climate forward bills and policies than Democratic counties.

2.   Do states with higher surface temperatures perceive a greater threat from global warming?

![Statewise Effect of Temperature on Global Warming Attitudes](https://github.com/hariniramp/data-512-final/blob/main/Visualizations/scatter_rq3.png)

The above visual shows us the fairly even spread of states with different surface temperatures. We can see as supported by analysis 1 that Republican majority states tend to have greater percentages of populations opposing climate change and global warming ideologies. However, we do not see a significant relationship between surface temperature and climate change attitudes.

3.   What are the renewable energy, fossil fuel generation patterns of states that perceive global warming as a big threat versus those states that don't?

![Relationship between Renewable Energy Generation and Climate Change Attitudes](https://github.com/hariniramp/data-512-final/blob/main/Visualizations/scatter_rq2.1.png)

The above visual also shows little to no correlation between a state's renewable energy generation percentage and climate change attitudes. The scatterplot is fairly even and nonsignificant.

*   **How has surface temperature evolved over the years and what factors might have affected this evolution?**

1.   What can we project the global surface temperature to be in the next 20 years? 30 years?

Initially, I did some exploratory data analysis on the global surface temperature time series. I forecasted the temperature until 2040 as follows.

![Primary time series forecast: 2040 surface temperature](https://github.com/hariniramp/data-512-final/blob/main/Visualizations/forecast_2_rq4.png)

Although a general increase in average annual temperature was observed, this time frame was not significant enough to notice any changes in temperature. So, I increased the time frame to 150 years and projected the temperature for the year 2165 to see a sizeable difference in surface temperature.

![Time series forecast: 2165 surface temperature](https://github.com/hariniramp/data-512-final/blob/main/Visualizations/forecast_3_rq4.png)

As we can see from the black line, a very evident increase exists in the average surface temperature if things continue the way they are now. This is a very significant and concerning finding as it shows us the alarming rate at which the climate is changing.

2.   Do states that gain more energy burning fossil fuels have higher surface temperatures? 

![Renewable Energy Generation vs Surface Temperature](https://github.com/hariniramp/data-512-final/blob/main/Visualizations/scatter_rq5.png)

As the amount of renewable energy generated increases, with the blue dots we can observe a somewhat vague downward trend in surface temperatures. However, looking at the line of best fit in red, we see an increasing trend. This leaves us with an unclear conclusion and nonsignificant results regarding the effect of a state's renewable energy generation on surface temperature.

## Data and Terms of Use

The data I chose for my questions actually encompasses several datasets. The descriptions, as well as terms of use of the selected datasets are below. The full datasets can be found on the [Data directory](https://github.com/hariniramp/data-512-final/tree/main/Data) in this repository.

1. I will use data from [Yale's Climate Perception Survey Study](https://climatecommunication.yale.edu/visualizations-data/ycom-us/), which asked respondents several questions on climate change and their opinions of it, and aggregated respondents who answered 'yes' or 'no' into separate columns, as percentages of the whole survey-taking population, by US county. The limitation of this dataset is that since it has been aggregated already, I will not be able to compare answers of the same respondent to multiple questions. It would have been interesting to analyze this in greater detail. The [Data Download](https://climatecommunication.yale.edu/visualizations-data/ycom-us/) section of this link specifies that the data may be used for research or academic purposes if cited appropriately. This dataset could possibly suffer from **selection bias**, as it only contains the views of those people who the survey was made available to.

2. My second dataset of choice will be the [Berkeley Earth Climate dataset](https://www.kaggle.com/berkeleyearth/climate-change-earth-surface-temperature-data), which presents a daily progression in surface temperatures of cities, states, countries, over the past ~250 years. The drawback to this dataset is that since it goes so far back, there are a lot of missing values in the beginning and this must be dealt with. This data comes under the [CC BY-NC-SA 4.0 License](https://creativecommons.org/licenses/by-nc-sa/4.0/).

3. The third dataset I will use is the [MIT Election Lab data](https://electionlab.mit.edu/data) to determine political affiliations that US counties has had over the years. This will be used in conjunction with the 1st dataset to assess attitudes across different counties and see if they vary in relation with political attitudes. This dataset's [terms of use](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/VOQCHQ) classify it as being under public domain or CC0.

4. Additionally, I will use data from the [EIA Website](https://www.eia.gov/renewable/data.php) to further explore trends in renewable energy generation patterns. The [Terms of Use](https://www.eia.gov/about/copyrights_reuse.php) for the EIA Data certify that the data is "in the public domain and are not subject to copyright protection". It indicates that anyone is free to use, duplicate and redistribute the data so long as proper attribution with publication date is made.

## Special Considerations

* The data from the YPCCC survey on climate change attitudes might suffer from selection bias. Although there was representation from the US counties, we are assuming that the survey results speak for all natives of those US counties/states. This might not be the case and the methodology for selecting participants might also not be completely random. This could result in several biases in the source of data.

* For the energy related data from EIA, the renewable and nonrenewable sources of energy could be broken down into the individual sources of energy. However, not all possible forms of energy generation were present and this is a possible source of skewing data. We must take these figures with this consideration in mind.

* A lot of the surface temperature analysis was done by averaging the temperatures over a year for an annual average. This might not have been the best way to do this. Enough consideration should be given to outliers and uncertainties. However, this was beyond the scope of the analysis. However, a future direction might be to take the median or a cluster center measure of the temperatures.

## Reproducibility
This repository contains a [Jupyter notebook](https://github.com/hariniramp/data-512-final/blob/main/Analyzing_Climate_Change_The_Evolution_and_Public_Opinion_.ipynb) that is entirely reproducible. One can download it and run it from start to finish to reproduce it. Each code chunk is preceded by a description of what the code chunk does for added clarity. For any further questions, mail the author at hramprasad98@gmail.com

## License and Terms of Use
This project is licensed under the [MIT License](https://github.com/hariniramp/data-512-final/blob/main/LICENSE).
