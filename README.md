# Program interest vs graduation rate analysis progress

# * Project update 1*
I have decided to explore my first option. So far I have obtained more than four thousand entries of enrolled students from the Institutional Research department and I will be wrangling the daa in the coming weeks. This is a personal project but I might reach out to my classmates and professor for help if necessary. Research questions:

Does switching majors affect a student's likelihood of graduating?
Which program categories do students mostly switch to or from?
How has the rate of switching majors changed over time?
In what period or year do students switch majors?
# * Project Update 2*
Obtaining and exploring available datasets

I decided to work with data from the wWhitman's institute research department, which I obtained by requesting it from the director of institute research through my professor. The dataset contains information about enrolled students, their declared academic interests, and their graduation status. This allows us to explore questions regarding the trends in the types of programs students switch to or from, the number of students who change majors, and the number of students who graduated or withdrew from college. I noticed there are inconsistencies with the data, such as missing values, mismatched dates, error codes, and duplicated values.

#  First Visualization
This is a representation of variation in number of programs enrolled students are interested in. 
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

Narrative plan: 
My plan is to have the following order of items in my data story:
1. Background and reason for this project
2. Data sourcing and procedure
3. Results and conclusion (Visual representations of my findings) 
4. Future improvement
5. Viewers/Readers  Comments
<iframe 
  src="https://Wangari-Kariuki.github.io/Program-interest-vs-graduation-rate/second_visuali.html" 
  width="100%" 
  height="600px" 
  frameborder="0" 
  scrolling="yes">
</iframe>
