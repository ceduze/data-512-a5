# data-512-a6
Final Project. DATA512. Charles Duze

### Goal of this Project
For this assignment I attempt to demystifying the king county food inspection data and provide useful customizable insights.

### Abstract
Most people have to eat. If you are one of the privileged few who gets to live in this part of the world, you have choices about what and where to eat. In fact, you have so many choices it becomes a “1st world problem”. One criteria for dealing with choice is that most people, after eating, don’t want deal with food poisoning[1].

There isn’t always an easy way to know what the after-food outcome would be. Some cities have Food grade ratings in the windows. Though it may be inconvenient to get all the way to the restaurant only to be disappointed. We have Yelp reviews that help with other selection criteria but it does not yet include food safety information. It is being piloted for a few cities but not yet Seattle[2]. 

King County publishes the food inspection results, but it’s too unwieldly to be useful to the average person. King County has tried to simplify the rating system which is great[3]. However, the open data available does not include the simplified ratings.

For this project, I
* wrote some reusable code to explore the dataset 
* processed the data into a more easily consumed format.
* made the processed outputs available to download and take to your tool of choice
* made the methods and code available so you can reuse 
* shared some initial findings including visualizations
* allowed you to customize some reports for your city by changing only one word

We tested 4 hypothesis, 1 of which was rejected. In addition, to the hypothesis testing, I also provide some insightful visualizations. These visualizations are customizable for different cities.  

I invite you and the open data science committee to build upon this work.


### References
[1] https://www.hlbenefits.com/food-poisoning-causes-symptoms-treatments-recovery/ 

[2] https://www.yelpblog.com/2013/01/introducing-lives

[3] http://www.kingcounty.gov/depts/health/environmental-health/food-safety/inspection-system/search.aspx#/

### Data Sources
**Food Establishment Inspection Data**
This data set (CC-0) contains Health Department inspection results for food service establishments in King County, from 2006 to the present. However for this project, I'll only be looking at one year's worth of data from November 2016 to October 2017. Information about the dataset, schema and API can be found here: https://data.kingcounty.gov/Health/Food-Establishment-Inspection-Data/f29f-zza5

**2016 King County and Its Cities Population**
This dataset (CC-0) contains the Office of Financial Management(OFM) 2016 population estimate for cities in King County's. It is a downloadable csv, however it requires some manual processing to programmatically accessed. Additional information including the download can be found here:
http://www.kingcounty.gov/depts/executive/performance-strategy-budget/regional-planning/Demographics.aspx

### Licenses for Data Used
Both datasets were provided by King County under CC-0. Additional information is available in the links above.


### APIs
[Socrata API](https://dev.socrata.com/foundry/data.kingcounty.gov/gkhn-e8mn)  



### Output Files and Columns
#### KingCountyFoodInspectionData_Output_Establishment.csv
**business_id**  
Unique Identifier for establishments

**inspection_business_name**  
Name of establishment 

**city**  
City

**description**  
Class of establishment

**InspectTypeCnt_Consult**  
Count of Consultation/Education Inspections

**InspectTypeCnt_Routine**      
Count of Routine Inspections

**InspectTypeCnt_Return**      
Count of Return Inspections

**ViolationCnt_Blue**      
Count of Blue violations

**ViolationCnt_Red**     
Count of Red violations

**SafetyGroup**  
Safety group rating



#### KingCountyFoodInspectionData_Output_City.csv
**city**    
Name of city. (Lowercase)

**population_2016**    
2016 City Population

**NumEstablisments**    
Number of Food Establishments in the city

**NumRoutineInspections**    
Number of Routine Inspections for all restaurants in the city

**SafetyGroupCnt_High**    
Number of establishments with High rating

**SafetyGroupPcnt_High**    
Percent of establishments with High rating

**SafetyGroupCnt_Lower**    
Number of establishments with Low or Very Low rating

**SafetyGroupPcnt_Lower**  
Percent of establishments with Low or Very Low rating

#### kingcounty_food_inspection.csv
Unaltered output from the API call. For columns names please see link under Data sources above.

#### OFM-CitiesPop2016-Formatted.csv
Manually processed to enable programmatically accessed. See details in iPython notebook. For columns names please see link under Data sources above.

### Other Issues
Please see iPython Notebook for more information.

