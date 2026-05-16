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
The data processing and cleaning required three major steps to filter out student information about what majors they declared interest in during their first years, second, third, and final years.
First, I examined the major interests during their first years using pandas grouping and filtering methods. 
{insert code snippet}


Next, I merged the students' initial interest information with their concurrent changes in major declaration. The main challenge was normalizing the varied text entries for first interests, which were raw strings (e.g., "Biology," "Biomolecular Biology," "Computer Science"), while the declared programs used program codes (e.g., "BIOL," "CS"), making comparison tedious. To address this, I used a Python library called MyFuzz, which analyzes text strings and returns a similarity ratio. Using this tool, I was able to match raw text strings to the corresponding program code format.
{inset code snippet}

For the visualizations, I used Plotly Express to generate dynamic and interactive visual representations of the program details. 

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




