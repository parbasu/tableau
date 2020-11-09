

**Data source:**

The source of all the data in the visualizations is the PDF file titled PCS 2019 - Police Crime Statistics Report, which is available at the Bundeskriminalamt [website](http://www.bka.de/EN). I have also uploaded it [here](https://github.com/parbasu/tableau/blob/main/crime_germany/pks2019_englisch.pdf).

I extracted the data from the PDF using [Tabula](https://tabula.technology/). The tables didn't come out nice, so I had to do a lot of cleaning up in Google Sheets. The end result of that process can be found [here](https://github.com/parbasu/tableau/blob/main/crime_germany/pcs2019_clean_raw_data.xlsx). The title of each worksheet tells you the page from which the data was extracted.

Note: The data is also available as an Excel spreadsheet but it is too detailed. Unless you know how to group together similar offence types under one category and which criminal offences to emphasize, you are only going to get confused and end up making a lot of mistakes! The report on the other hand contains the aggregated data corresponding to the different offence categories.

**Data preparation:**

The clean raw data is still unusable for Tableau. There are three reasons for this:

**1.** Different tables which contain the same type of data are not grouped together. For example, one table contains the recorded cases of street crime in different states in Germany and the same information but for violent crime is present in a different table. What we would like to see is one table which contains both information with an added offence category column. This allows us to use the category column as a filter.

**2.** Tableau works best with row-oriented data. But the data in the PDF report is column-oriented, which makes sense as it is meant to be read. For example, instead of having separate columns for the year 2019 and 2018, we would like to have a single year column. So I had to do pivot and transpose the tables to bring them into a more Tableau-friendly format.

**3.** In contrast to 1., sometimes a table contains data that really should be on a separate table. In our case, this is mainly because the data is only shown for the year 2019. For example, the recorded cases are only shown for the year 2019, but offence rate is shown for all the way back to 2012. Also, I think it is best to keep state-level and country-level data separate. 

The end result of **1.** can be found [here](https://github.com/parbasu/tableau/blob/main/crime_germany/pcs.xlsx).

For the visualizations [Crime Statistics Germany by City](https://public.tableau.com/views/CrimeStatisticsGermanybyCity/crimestatsgermanycity?:language=en-GB&:display_count=y&:origin=viz_share_link) and [Crime Statistics Germany by State](https://public.tableau.com/views/CrimeStatisticsGermanybyState/crimestatsstategermany?:language=en-GB&:display_count=y&:origin=viz_share_link), the end result of **1.**,**2.** and **3.** can be found [here](https://github.com/parbasu/tableau/blob/main/crime_germany/crime_stats_germany_city.xlsx) and [here](https://github.com/parbasu/tableau/blob/main/crime_germany/crime_stats_germany_state.xlsx) respectively.

---

**Notes on the [Police Crime Statistics Federal Republic of Germany Report 2019](https://github.com/parbasu/tableau/blob/main/crime_germany/pks2019_englisch.pdf)**

The report broadly contains the following information: 

**1.** Section 1 contains information about how the data is recorded, what type of data is not recorded, and a word of caution about making certain types of conclusions from the data.

**2.** Section 2 contains information about the total number of recorded cases (which includes attempts), the number of German and non-German suspects and the clearance rate for the year 2018 and 2019 for certain types of offences.

**3.** Section 3.1 contains information about the development of total crime and total crime excluding crimes like unauthorised entry and stay (these are called offences against foreigners' law) over the last 15 years. For certain types of offences we are given information about the percentage share of attempts for the year 2018 and 2019. The geographical distribution of crime by municipality size is also given.

**4.** Section 3.2 contains information about the total number of recorded cases, percentage share of attempts, the total number of suspects, percentage share of suspects that were either male or female, clearance rate, total number of recorded cases and offence rate by state and city for selected offence categories.

**5.** Section 4 contains information about the clearance rate, percentage share of cleared-up cases in which the suspects were  hard-drug users, clearance rate by state and city. 

**6.** Section 5 contains information about monetary loss as a result of certain offences.

**7.** Section 6 contains information about the victims, their age, their gender, their nationality, and their relationship with the suspects.

**8.** Section 7 contains information about the suspects, their age, their gender, their nationality, and percentage share of suspects that were hard drug users.

**9.** Section 8 is just the glossary. It contains information about how statistics like clearance rate and offence rate, among other things, are calculated.

---

As you can see, there is a lot of data in the report. The visualizations I created use tables only from section 3.2. I haven't provided a summary of my findings because based on the two visualizations, the type of conclusions you can make are pretty straightforward. They are interesting nonetheless. For example, the clearance rate for street crime and thefts in Berlin is extremely low at 11.8% and 22.3% respectively. So if you get pickpocketed or your bike gets stolen, you are not getting your stuff back!
