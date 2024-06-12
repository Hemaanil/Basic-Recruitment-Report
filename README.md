# Basic-Recruitment-Project
Practiced DataSet
# Hiring Process Report

## Problem Statement

This Report helps one of the level 5 MNC based consultancy  understands their Hiring process better. It helps the management know if their clients are satisfied with their services. Through different ratings, they get to know their improvement area, & thus they can improve their services by identifying these areas. 


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is an excel file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : It was observed that in none of the columns errors & empty values were present 

- Step 5 : Which sources are we finding most of our candidates at?-- For this no calculations were done. jus showed the difference in Stacked Area Chart.

 ## we can see the count of position by position 

![Screenshot 2024-06-12 220419](https://github.com/Hemaanil/Hemalatha/assets/165702332/59c8e4b6-6ee2-4d54-958a-d0920a772918)

- Step 6 : In the report view, under the view tab, theme was selected.

- Step 7 :  For total interviews have been conducted for the selected time period,  Used card visual with Candidate name in the field, selected count option in data options(fields of that particular visual) -summarization used slicer, so that for selected time period we can change dates.

- Step 8 : For the selected time period (year/month/week) what is the number of the candidates in the different stages of the recruitment, did below calculation for screening comments, first round, 2nd round, 3rd round columns individually.

Screening Comments Measure = 
CALCULATE (
    COUNTROWS ( 'Recruitment Data' ),
    FILTER ( 'Recruitment Data', 'Recruitment Data'[Screening Comments] = "Good fit" )
)
Used Pie Chart and added all the 4 measures to the same field(values)


- Step 9 : How does the movement looks like from one stage to another on terms of %?
     did below calculation for screening comments, first round, 2nd round, 3rd round columns individually.

Screening Percentage = DIVIDE([Screening Comments Measure], COUNT('Recruitment data'[Candidate Name]))
 
after this to get the result in percentage format go to measure tools - format option - select percentage

Used Funnel visual and added all the 4 measures to the same field(values)

- Step 10 : what are the weekly trends for a selected month?
Take line chart and add month column from calendar to the X- axis  and candidate name to the y- axis in fields

- Step 11 : what are the monthly trends for Overall time period?
for weekly same like above process but change month column to week. and add data labels.

- Step 12 : what re the most prominent rejection reasons?
Create Tree visual and add rejection reason column in the field.....in filter field also add same column and in basic filtering remove blanks and make Top N value to 6.

- Step 13 : which postilions have been hired for selected month or week?
Create Column chart and add position column in x-axis and y-axis too.

And overall the Report looks like 


![Screenshot 2024-06-12 221041](https://github.com/Hemaanil/Hemalatha/assets/165702332/24f5b661-d3fc-4f48-9212-e372095f1b13)


  
