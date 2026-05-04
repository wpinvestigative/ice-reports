# About this story

Data behind the Washington Post [story](https://www.washingtonpost.com/business/2026/05/04/ice-detention-centers-force/): Internal ICE records reveal widespread use of force in detention centers

# Methodology

The Post obtained reports on 1,460 use-of-force incidents at ICE detention centers dated Jan. 1, 2024 to Feb. 28, 2026. Reporters extracted dates, numbers of detainees involved, facility names, law enforcement agencies and whether the report indicated that oleoresin capsicum (pepper spray) was deployed. The Post is releasing a limited cut of the transformed data. 

Reporters used Google Pinpoint’s AI to help identify reports in which a detainee may have been injured, and then verified the injury descriptions manually. If an injury appeared to be caused by self-harm or a fight with another detainee, it was not counted. Some narratives included multiple dates. For the purpose of this analysis, only the first date of each narrative was counted. Incidents during the last year of President Biden occurred between January 21, 2024 and January 20, 2025. Incidents during President Trump's first year of his second term occurred between January 21, 2025 and January 20, 2026.

For facility populations, the Post used the median of Interval Average Daily Population figures [calculated](https://relevant-research.com/assets/pdf/methodology_writeup.pdf) by Relevant Research. These estimates better represent current population figures because Relevant calculates and accounts for rates of change each month, versus ICE's single rolling annual average. We limited our calculation of population change to the 98 facilities that had reported use of force.

For all tables, variables are pulled from the data source. No data dictionary was provided.


# Files of note in this repo

* **[data/ice_uof_narratives.csv](data)** - Variable names are from the data source
* **[data/ice_uof_participants.csv](data)** - Groups of participants in the "participant" column of ice_uof_participant.csv are split into rows that can be joined back to the original data frame based on the "row" and "sen_number" columns.
* **[data/ice_uof_dates.csv](data)** - Sometimes multiple dates are included in the "narrative' column of ice_uof_narrative.csv. This is a relational dataframe with a unique identifier of the row and sen number with a row for every data pulled from the narrative in chronological order and indicated with their order "date1", "date2", etc.
* **[data/ice_uof_dictionary.csv](data)** - details on variables in csvs


### Staff involved

Reporters: [Douglas MacMillan](https://www.washingtonpost.com/people/douglas-macmillan/), [Andrew Ba Tran](https://www.washingtonpost.com/people/andrew-ba-tran/)

Editors: Meghan Hoyer and Alexis Fitts
