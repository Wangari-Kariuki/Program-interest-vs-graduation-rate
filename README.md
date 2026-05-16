#   Descriptive analysis of change of program interest and graduation rate

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
The data processing and cleaning required three major steps to filter out student information about what majors they declared interest in rom when they enroled until they graduated
First, I examined the format of the values in the three data sets provided. 
Next, I merged the students' initial interest information with their concurrent changes in major declaration. The main challenge was normalizing the varied text entries for first interests, which were raw strings (e.g., "Biology," "Biomolecular Biology," "Computer Science"), while the declared programs used program codes (e.g., "BIOL," "CS"), making comparison tedious. To address this, I used a Python library called MyFuzz, which analyzes text strings and returns a similarity ratio. Using this tool, I was able to match raw text strings to the corresponding program code format.
{inset code snippet}

For the visualizations, I used Plotly Express to generate dynamic and interactive visual representations of the program details. 


## Results
After wrangling the dater i managed to answer the following questons: 
**So how many students within 2017 and 2021 switched majors?**

After filtering out the students with major changes, I discovered that 247 (15%) out of the recorded 1628  students had switched majors at least once during their three years in college.

**Which mjors did they switch to and from?**

The third visualization shows the trend in student counts across various programs. Notably, Economics, Computer Science, and Psychology experienced the largest percentage decline(between 40% and 42%) n the number of students who switched majors.

**Of all the ones who graduated, how many actually stuck with the interests they made from first year?**

Out of 1562 graduating students, 367 chose one of their first-year academic interests as their major.
This is 23.50% of all graduated students.

This is a representation of variation in the number of programs enrolled students are interested in. 
<iframe
   src = "https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/first_visuali.html"
   width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="no">
   ></iframe>

This is a categorical bar graph representing the student count per major obtained from student enrollment information. Obtained  by mapping a list of program codes to the student information.
<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/second_visuali.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>


The visualization is a stacked bar graph representing the change in student count before and after students changed majors. It accounts for information only from students who switched majors.
Hover over each bar to see the varying student count. 

<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/third_graph.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>

Conclusion






