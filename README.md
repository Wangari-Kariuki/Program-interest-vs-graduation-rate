#    Exploratory analysis of change of program interest and graduation rate

## Motivation and objective
According to a study by the Department of Education, approximately 30% of undergraduate students change their major at least once within their first three years of study. The rate of change varied by field, with students who declared STEM majors switching at a rate of 35%.More information about this can be found in <a href= "https://nces.ed.gov/pubs2018/2018434/index.asp">this article</a>
The goal of this project is to examine the rate at which students enrolled in Whitman College change majors and whether there is a reasonable correlation between that and their graduation statuses.I will explore the variation in the rate of changing majors according to the different fields of studies.  

## About the data
The data was requested from  by Whitman College Department of institution research through Professor Jordan.The dataset contained information of 2000 enrolled students between 2017 and 2021 academic years, their declared academic interests, and their graduation status.

##  Research questions
Does switching majors affect a student's likelihood of graduating?
Which program categories do students mostly switch to or from?
How has the rate of switching majors changed over time?
In what period or year do students switch majors?

## Analysis Knowledge



## Results

### First Visualization
This is a representation of variation in the number of programs enrolled students are interested in. 
<iframe
   src = "https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/first_visuali.html"
   width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="no">
   ></iframe>
# Week 14 update
After analyzing the structure of my data, cleaning and merging the data frames to contain student program interest information, I now need to compare the Program codes of declared majors with the initial academic interest. Note that the declared majors are listed as program codes and not subjects, so I needed to create a separate column that contains the list of interests as program codes. 

To do this, I created a custom function that iterates and compares each listed subject with the subject's program codes and returns the program code of the listed subject.
Pending tasks:
1. Analyze change in program codes from inital interest to, delcaration and graduation

3. Create visualization to represent this trend and variation in different groups of students
   
4. Categorize the filtered data according to Program types and represent this information in a visaulization


<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/second_visuali.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>

<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/third_graph.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>





Narrative plan: 
My plan is to have the following order of items in my data story:
1. Background and reason for this project
2. Data sourcing and procedure
3. Results and conclusion (Visual representations of my findings) 
4. Future improvement
5. Viewers/Readers  Comments



