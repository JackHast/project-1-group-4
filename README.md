# project-1-group-4
Project Title: Analysis of Measures Adopted to Stop The Spread -  Covid-19 Pandemic

Group Members: Hajar, Helena, Hussam, Jack

In this study, an extensive dataset from different sources was gathered of data in an attempt to address the following.

1- What was the incidence (occurrence) of Covid-a19 pre and post vaccinations?

2- Were government mandates including face covering effective in stopping the spread of covid?

3- Compare hospital beds and the number of testing to the number of Covid-19 cases



1- What was the incidence (occurrence) of Covid-a19 pre and post vaccinations?

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


Policy Analysis:

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

0 - No policy
1 - Recommended
2 - Required in some public areas
3 - Required in all public spaces
4 - Required outside the home at all 

In the jupyter notebook ipynb file cleaning_data.ipynb these two indices are averaged for all countries (that had a recorded stringency and facemask index) over the period of 1/1/2020 to 31/12/2022. In the file policy_analysis.ipynb, we have firstly plotted these averages for the stringency index against the total cases per million (as of 31/12/2022), where it can be seen that there exists a moderate negative relationship between mean stringency index and total cases per million for upper middle and high income countries.

   Jack/images/stringency_vs_total_cases_HI.png

Initially, all 176 countries were plotted, however, it was noticed that all low income countries and almost all lower middle income countries had comparatively small total cases per million. We believe that this discrepancy between low – lower middle income and upper middle – high income countries may be due to poor reporting of infection numbers in underdeveloped and developing economies. 



