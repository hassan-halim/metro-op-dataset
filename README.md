# metro-op-dataset
Most of files in this dataset are not official figures of Cairo metro authority, we used a summerized table of average passenger arrival
for one week and perfromed some statistical distributions to generate "hourly passenger arrival per station", "per minute passenger arrival".

The infrastructure, line plan, and timetable data are prepared after interviewing technical teams in the Cairo metro and by observations.

infrastructure and timetable data are in railML format, to know more about railML please visit "www.railML.org"
The ODM file also is generated by assuming a probablity distribution of passenger routes in line1

In the below list of the dataset files:
1- Infra_Line1.xml --> Infrastructure details of Cairo metro line 1 (toplogical data is correct but distances between stations are not)
2- CMC_railML_Infra_ex.xsd--> A custom extenstion to railML prepared by us to add needed data in our problem (e.g. station passenger capacity , and station storage capacit)
3- l1_wd_plan.json --> Line plan for metro line 1, line plans are used to determin some important operational parameters such as headway time and train frequency per hour. This line plan is prepared according to interviews with the metro technical team
4- Line_1_ODM.csv--> calculated origin-destination matrix "passenger routes"
5- SimTimetables --> Timetable files per hour ("calc_timetable_5.xml" is the timetable for 5AM hour), again these files are caclulated based on th line plan.
6- Line1 Actual Daily Figures--> A summerized report shows the average number passengers arrrives to line 1 during a week. we used this file to distribute the arrival numbers over the statoins using normal disribution.
7- Passenger Arrival Per Minute (folder) --> These figutables are estimated for the first 3 hours by a Possion process using the file mentioned in point 6.
