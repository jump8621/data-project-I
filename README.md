# Pyres of California

## Background

Our project is to evaluate and analyze California Wildfire Data based on a California Wildfire Incidents dataset between 2013 and 2019. The project will focus on factors such as resources deployed, acreage burned, structure damage, injuries, personnel involved in firefighting and related questions, as the data admits.

## Assumption

- [California wildfire incidents from 2013 to 2019]('Resources/California_Fire_Incidents_original.csv') and [list of California county]('Resources/ca_county_list.csv') will be applied in order to conduct the analysis.
- The analysis will be divided into 2 main parts, all fire incidents and major fire incidents (based on dataset).
- In each main part, the analysis will focus on resources and the damage of fire by County. 
- Personnel invloved will represent all the resources in this analysis.

## Hypothesis

- Fire incident has a time pattern of occurrence
- Burned time has relation with burned area.
- Larger area of burn or longer fire duration requires more resources
- Higher number of fire incidents lead to higher number of injuries

## Data Limitation

- Data incompletion which will be excluded might cause an inaccurate conclusion.
- The definition of major fire incident in the dataset which indicates by true/false differs from California Fire Department which states that major fire incident is more than 10 arces. The group decision was using the information based on the dataset because we counldn't find the evidence to support if the file is uncredible.

## Analysis

### Statistical Summary

Overall statistics performed for the overall data set were calculated for various critical parameters, including acres burned, injuries, equipment used, personnel involved, and structures damaged and destroyed, etc. As presented in the table, there is a wide range of values for each parameter, as reflected by the differential variance and standard deviation. Also, the histogram graph shows that the dataset is a random distribution.

**Statistical Table** | **Histogram Graph**
--------------------- | ---------------------
![SumTable](Images/table_summary.png) | ![HistGraph](Images/hist_data_plot.png)


### California Fire Summary By Year and Month

***Are there any trends in the time of year that fires are most active? Which year was the most active?***

When examining the number of fire incidents by month, for both the number of incidents and acres burned, there’s an increase for the month of July, across years 2013-2019. The year 2017 had the greatest number of fires, 438 times. The year 2018 had the greatest amount of area burned, 1,549,401 acres.

![firepattern1](Images/PatternbyMonth.png)

![firepattern2](Images/PatternbyMonth_arces.png)

### California Fire Summary By County

***Which California counties had the highest number of fires? Are there any counties that were untouched by wildfires?***

- Out of all 58 counties in California, Riverside County had the highest number of fire incidents: 146 times. Whereas, San Francisco County and Imperial County both had zero fire incidents between 2013-2019.

**Top 10 Counties** | **Bottom 10 Counties**
--------------------- | ---------------------
![top_county_no](Images/bar_top_ca_all_fire.png) | ![bottom_county_no](Images/bar_bottom_ca_all_fire.png)

- When studying only major fire incidents, another small county, Alpine County, joins the two counties mentioned above as counties that had no major fires between 2013 and 2019.

**Major Top 10 Counties** | **Major Bottom 10 Counties**
--------------------- | ---------------------
![top_county_no](Images/bar_top_ca_mj_fire.png) | ![bottom_county_no](Images/bar_bottom_ca_area all_fire.png)
---
***Which county ranked the highest in terms of area burned? Which county ranked the lowest in area burned?***

- Out of all the counties that had at least one fire incident reported between 2013-2019, Siskiyou county has the highest area burned: 367,914 acres. Whereas, San Mateo county has the lowest area burned at only 153 acres.

**Top 10 Counties: Area** | **Bottom 10 Counties: Area**
--------------------- | ---------------------
![top_county_no](Images/bar_top_ca_area_all_fire.png) | ![bottom_county_no](Images/bar_bottom_ca_area all_fire.png)

- 40 percent of all counties in California (22 counties) have lost at least 100,000 acres due to fires between 2013-2019. 

![100acres](Images/all_area_scatter_showall.png)
---

### California Fire Factor (Duration of Fire)

***What is the correlation between the time a fire incident has burned versus the size of the area burned?***

- The correlation between the size of the area burned versus the duration of time the fire burned is 0.0576, which implies that there is no relation between these factors. 

![time_area_corr](Images/day_area.png)

- The correlation between the size of the area burned versus the frequency in each county is 0.413, which implies that there is moderate relation between fire frequency and burned area.

![times_area_corr](Images/area_num.png)

### California resource deploy

***How do counties compare when measuring the severity of wildfire events, loss of life, and fire-fighting equipment deployed?***

- As seen in the figure below, Butte County had considerability higher loss of life due to wildfires than any other counties in this dataset. 

- Additional research attributed Butte County’s staggering loss of life to the 2018 Camp Fire. To date, the Camp Fire remains the deadliest and most destructive wildfire in California’s history. 

- This discovery could also be seen in the data that showed a spike in the equipment used in 2018.

![Mj_fat_inj](Images/Bar_Chart_County_Fire_Count_Injuries_Fatalities.png)

- When comparing equipment deployed for fighting wildfires from 2013-2019, Butte County and San Diego County had similar figures, despite Butte County suffering a much higher loss of life. 

![Mj_resources_deployed](Images/Bar_Chart_Equipment_Top_Five_Counties.png)

