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
