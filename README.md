#   Descriptive analysis of Student Program Interest and Graduation Trends

**By: Esther Kariuki**

**May 16th, 2026**


## Motivation and objective
According to a study by the Department of Education, approximately 30% of undergraduate students change their major at least once within their first three years of study. The rate of change varied by field, with students who declared STEM majors switching at a rate of 35%.More information about this can be found in <a href= "https://nces.ed.gov/pubs2018/2018434/index.asp">this article</a>
The goal of this project is to examine the rate at which students enrolled in Whitman College change majors and whether there is a reasonable correlation between that and their graduation statuses.I will explore the variation in the rate of changing majors according to the different fields of studies.  

## About the data
The data was requested from  by Whitman College Department of institution research through Professor Jordan.The dataset contained information over 1800 enrolled students between 2017 and 2021 academic years, their declared academic interests, and their graduation status.

<!--##  Research questions
Does switching majors affect a student's likelihood of graduating?

Which program categories do students mostly switch to or from?

How has the rate of changing majors changed over time based on difference in programs?
-->


## Analysis procedure
The data processing and cleaning required three major steps to filter out student information about what majors they declared interest in rom when they enroled until they graduated. 
First, I examined the format of the values in the three data sets provided. 
Next, I merged the students' initial interest information with their concurrent changes in major declaration. The main challenge was normalizing the varied text entries for first interests, which were raw strings (e.g., "Biology," "Biomolecular Biology," "Computer Science"), while the declared programs used program codes (e.g., "BIOL," "CS"), making comparison tedious. To address this, I used a Python library called MyFuzz, which analyzes text strings and returns a similarity ratio. Using this tool, I was able to match raw text strings to the corresponding program code format.
A limtation of this library for our task is that it does character matching which is inefficient hre since our analysis requires the program to identify the meanings and not just character match the strings. To create a structured and constrained pipeline to ensure maximum accuracy of our program we follow these steps:

1. Normalization
2. Creating a controlled vocabulary map
3. Passing the lists of strings through fuzzy pipeline and mapping dictionary
To determine the  number of students who switched  majors: I fitered out the student IDs of students whose program status was tagged as "changed mind". 
For the visualizations, I used Plotly Express to generate dynamic and interactive visual representations of the program details. 

This <a href= "https://github.com/Wangari-Kariuki/Program-interest-vs-graduation-rate/blob/main/final_project_report.ipynb">Google colab report </a> includes all the code and step by step procedure of my analysis
## Results
**Evaluating initial major interests**

Although this was a tangent from examining the major changes, it later became useful in evaluating the variation in the level of interest for different majors at enrollment.
<figure>
   <iframe
   src = "https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/first_visuali.html"
   width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="no">
   ></iframe>
</figure>


<figure>
<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/second_visuali.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>
   <figcaption>
      
This is a categorical bar graph representing the student count per major obtained from student enrollment information. Obtained  by mapping a list of program codes to the student information.

   </figcaption>
</figure>

Biology was the most popular major among students at enrollment, with over 6 percent of all enrolled students selecting it as their preferred area of interest. Environmental studies and mathematics and natural sciences were also highly popular among first-year students. However, humanities majors trailed behind, with minimal interest ranging between 0.3 and 1 percent. Notably, English, Economics, and Politics were also very popular within the first year of enrollment, with average percentages between 3 and 4 percent.

**How many students within 2017 and 2021 switched majors?**

After filtering out the students with major changes, I discovered that 247 (15%) out of the recorded 1628 enrolled students had switched majors at least once during their three years in college.That is approximately 1 in evey 6 undergraduate students

**Which majors did they switch to and from?**

The visualiation bellow shows the trend in student counts across various programs. Notably, Economics, Computer Science, and Psychology experienced the largest percentage decline(between 40% and 42%) in the number of students who switched majors. Meaning, students mostly switched from those majors to other programs, while I never managed to track the exact programs that each student switched from and to, because of the limitation of the data set provided. This analysis supplies enough information by tracking changes in student count per program. 

<figure>
<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/third_graph.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>
<figcaption> 
   The visualization is a stacked bar graph representing the change in student count before and after students changed majors. It accounts for information only from students who switched majors.
Hover over each bar to see the varying student count. 
</figcaption>
</figure>

**Student count per major category**
To obtain the major categories I created program group dictionary and mapped each listed program on enrollement, during sophomore and junior year and during grad year  to its respective program group. I then grouped the student IDs by the major programs an obtaine the student count for each group.
<iframe 
  src = "https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/categorical_student_count.html"
  width="100%" 
  height="500px" 
  frameborder="0" 
  scrolling="yes">
</iframe>


This is a categorical bar graph representing the student count per major obtained from student enrollment information. Obtained  by mapping a list of program codes to the student information.
**Of all the ones who graduated, how many actually stuck with the interests they made from first year?**
Out of 1562 graduating students, 23% chose one of their first-year academic interests as their major. 

With this we can infer that that the rest 15% changed their majors and majoriiry which is over 60% had their initial interests as undeclared. 

**Reflection**

Throughout this project, I have appreciated the effort it takes to clean and subset data during descriptive analysis. I have also learned how important it is to have target questions especially for this kind of analysis, because it becomes tempting to go on tangents when coming up with new insights. And also that the new insights can be useful in fulfilling the objectives. 

**Future stretch**
I wish to explore this data further by using clustering analysis to evaluate trends in  the programs by categorizing them into humanities, sciences , arts and applied fields. 

**Research resources**
- Pandas documentation: I used pandas documentation for most of data filtering algorithms
- Google Gemini: I  used gemini chat assst in google colab  debug errors
- <a href="https://plotly.com/python/plotly-express/">Plotly Express documentation</a>
- Stack OverFlow






