# Analysis of Measures Adopted to Stop The Spread -  COVID-19 Pandemic

Group Members: Hajar, Helena, Hussam, Jack

In this study, an extensive dataset from different sources was gathered of data in an attempt to address the following.

What were the main factors that contributed to COVID-19 outcomes in 2020 to 2022?

1- What was the incidence (occurrence) of COVID-19 pre and post vaccinations?

2- Were government mandates including face covering effective in stopping the spread of covid?

3- Compare hospital beds and the number of testing to the number of COVID--19 cases

This analysis will include COVID-19 data from countries in all continents and focus on COVID-19 data recorded from the beginning of 2020 to the end of 2022.

### What was the incidence (occurrence) of COVID-19 pre and post vaccinations?

The dataset contains about 240 countries in total, with dates ranging from early 2020 to late 2022. Before conducting the analysis, the dataset was QC’ed and cleaned. The following was removed from the dataset.
- Any country without cases recoded before vaccine roll-out
- Any location without cases recorded post-vaccine roll-out
- Any locations grouped together
 - Any questionable location trend (date vs number of cases recorded before and after vaccine roll-out.

The next step was to (for each location)
- extract the vaccine roll-out date 
- calculate the ratio of the population vaccinated
- Calculate the total number of cases before and after the vaccine roll-out date
The dataset was then organized (sorted) in ascending order based on the date of vaccine roll-out. the location that adopted the vaccine earlier is considered to be among the top-performing location. The location that adopted the vaccine later is considered among the bottom performers. The top 20 locations and bottom 20 locations were then chosen for further analysis.

Top 20 Countries (analysis):

The total number of cases before and after vaccine roll-out were plotted(see figure below). The plot clearly shows the locations are in North America and South America and, Europe. Also, two distinct regions of data appear one for North and South America and one for Europe. Fitting straight lines were placed on the plot to study the behavior of each region. The rate of change for the Americas (5.37) is much higher than that for Europe (1.68). This indicates that the range of range in total number of cases for the European location is much narrower for the Americas’ range of change. The initial jump in total cases, however, after vaccine roll-out in Europe (around 450000) is higher than that for the Americas (around 27600). Although the vaccine seems to have not decreased the cases in all continents, it seems to have stabilized the situation in Europe.
Mid to high ratio of population vaccinated in all countries.

![image](https://github.com/JackHast/project-1-group-4/assets/134576485/5849ff83-fb1d-4661-9762-ef2cf26108e8)

Bottom 20 Countries (analysis)

The plot below shows that most countries are from Africa, with a very low to low ratio of population vaccinated. The plot also shows a very low number of total cases recorded before and after the vaccine roll-out. Some countries also showed a reduction in the total number of cases post-vaccine roll-out date. It could be misleading if we try to drive any conclusion from this plot before, firstly, check about the reporting system in these countries, how they define cases, and conduct tests.

![image](https://github.com/JackHast/project-1-group-4/assets/134576485/f3e53a72-d60d-44ce-aaf3-98a9fe55c860)

### Were government mandates including face covering effective in stopping the spread of covid?

For this part of the analysis two indices were used to determine the effectiveness of government mandates designed to stop the spread of covid-19. Firstly, the stringency index, which is on a scale of 0 (no policy) to 100 (strictest possible), is a measure of the severity of 9 separate categories,

-	School closures
-	Workplace closures
-	Cancellation of public events
-	Restrictions of public gatherings
-	Closures of public transport
-	Stay-at-home requirements
-	Public information campaigns
-	Restrictions of internal movements
-	International travel controls

Secondly, an index measuring 5 different levels of policy regarding the wearing of facemasks was used,

0 - No policy,
1 - Recommended,
2 - Required in some public areas,
3 - Required in all public spaces,
4 - Required outside the home at all 

In the jupyter notebook ipynb file Jack/cleaning_data.ipynb these two indices are averaged for all countries (that had a recorded stringency and facemask index) over the period of 1/1/2020 to 31/12/2022. In the file Jack/policy_analysis.ipynb, we have firstly plotted these averages for the stringency index against the total cases per million (as of 31/12/2022), where it can be seen that there exists a moderate negative relationship between mean stringency index and total cases per million for upper middle and high income countries.

   ![image](https://github.com/JackHast/project-1-group-4/assets/131254350/452cf776-247d-42b8-be23-dea74cc920a1)

Initially, all 176 countries were plotted, however, it was noticed that all low income countries and almost all lower middle income countries had comparatively small total cases per million. We believe that this discrepancy between low – lower middle income and upper middle – high income countries may be due to poor reporting of infection numbers in underdeveloped and developing economies. 

Next, we looked at the effectiveness of facemasks where we saw that Pearson coefficient for mean facemask index and total cases per million was -0.3 (weak negative correlation) however any relationship could possibly be explained by the fact that the mean facemask index has a moderate positive relationship with mean stringency index. 

![image](https://github.com/JackHast/project-1-group-4/assets/131254350/94bb3a0d-553b-4fe3-b231-4bc857bec29f)

The outliers shown above are outliers with respect to the income level that the countries were in, i.e, Sweden is an outlier with respect to the facemask index among high income countries, Tonga with respect to upper middle income countries and Belarus and China are outliers with respect to the stringency index among upper middle income countries. 

### Assessment of healthcare facilities: hospital beds and number of testing 
**Comparing hospital beds to the population of the country**

*	Lower Availability of Hospital Beds: Bolivia, Malaysia, Sweden, and South Africa have fewer hospital beds per 1000 people, indicating lower capacity to accommodate patients.
*	Moderate Availability of Hospital Beds: Countries like Canada, Denmark, United Kingdom, United States, Ireland, Spain, and others have a moderate number of hospital beds per 1000 people, suggesting a moderate capacity to handle healthcare demands.
*	Higher Availability of Hospital Beds: Countries including Slovenia, Luxembourg, Switzerland, Estonia, and others have a higher number of hospital beds per 1000 people, indicating a relatively higher capacity to handle healthcare demands.

![Hospital Beds per 1000](https://github.com/JackHast/project-1-group-4/assets/134599676/657e2ea6-f16e-4264-87c3-360870538242)
![Population Year 2020-2022](https://github.com/JackHast/project-1-group-4/assets/134599676/3973ea18-45b7-4f04-8943-04d45ac5f608)

*	Hospital beds per 1000 vs Excess mortality
*	The low R-squared indicates a weak relationship between "Hospital beds per 1000" and "Excess Mortality" rates.The availability of hospital beds per 1000 people does not have a strong influence on excess mortality.

![Excess Mortality vs Hospital Beds](https://github.com/JackHast/project-1-group-4/assets/134599676/5238f731-abdd-49e6-abe5-ab53b1b82c83)

*  GDP per capita vs Excess mortality
*  A correlation coefficient of 0.38 between "Excess Mortality" and "GDP per capita" suggests a moderate correlation between these two variables.
In summary, the data suggests weak to moderate correlations between "Excess Mortality" and the other variables: "Hospital beds per 1000" and "GDP per capita.

![Excess Mortality vs GDP per capita](https://github.com/JackHast/project-1-group-4/assets/134599676/1573850f-25d7-4e26-8855-794d14d3ca01)

**Comparing number of tests to number of COVID-19 cases**

**Understanding the data:**
Different countries publish their data according to different definitions of tests. One difference is that some countries report the number of people tested, while others report the number of tests performed. The number of tests performed can be higher if the same person is tested more than once. Our World in Data has provided documentation for each country that provided source descriptions detailing information on COVID-19 data. 

Testing data in the following section below only includes PCR and antigen tests. In addition, the actual number of COIV-19 cases were likely to be much higher than the number of confirmed cases, this is due to limited testing. 
To answer this question, the daily_tests_vs_cases.csv file was cleaned by removing all rows that had NaN values in the new_tests column and daily new confirmed cases column. Also, columns were renamed for clarity. 

Positive rate is calculated by dividing 7-day olling average of daily average of daily cases by the 7-day rolling average of daily tests. This is a good measure of how adequately countries are testing. A high positive rate suggests higher transmission of COVID-19 and is concerning. 


![image](https://github.com/JackHast/project-1-group-4/assets/130710065/ecfacb47-daac-4702-98d4-3c542a242869)

The plot above shows the share of Covid-19 tests that were positive from March 2020 to December 2022. The positive rate of five countries were compared. Australia and South Korea’s testing was adequate as evidenced by below 1% positive rate from 2020 to 2020. There is a spike in the positive rate in January 2022 which indicates inadequate testing. India and South Africa had high positive rates above 20% at several points in time between 2020 and 2022 indicating inadequate testing. 
Our World in Data and other health organisations recommend increasing testing and responding appropriately to positive tests to reduce COVID-19 transmission. The plot below contradicts this advice. 

![image](https://github.com/JackHast/project-1-group-4/assets/130710065/724f09f6-1048-4444-8b34-1623b5412898)

The plot above shows the relationship between daily confirmed cases per million and daily tests per million. This relationship was shown for a specific date i.e. 2nd February 2021. This date was chosen as it was a point in time when there were high COVID-19 cases recorded in several countries around the world. The calculated correlation coefficient of 0.36 indicates a weak positive correlation between two factors. This correlation value could be impacted by the outliers. The calculated outliers are 436.5 for daily confirmed cases and 6561 for daily tests. The points on the plot greater than the outlier values are European and Asian countries which include Slovakia, Denmark and Portugal. 










