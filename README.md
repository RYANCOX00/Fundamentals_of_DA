# Fundamentals_of_DA
A repository for Fundamentals of Data Analysis assignments

Started the notebook for matplotlib and CAO. Inputed heading, packages, reference list. 

Started messing around with pyplot. 



# CAO note book
called in level 6, 7, 8 courses by requests package and checked if they pulled correctly. 
defined a function to search for patterns to obtain only the lines of course. 
Compiled the RE code and ran it. 
Initially I used a full match RE however it omitted approx 27 level 8 courses that did not have points asssigned at either first round or neither 1st or 2nd round. 
Called the function for level 8 and then level 6 and 7. 


## 31/10/2021
deleted the code to call 6 and 7.  Also removed the defined function to recall data as its likely only going to be used once. 2020 is on excel file and 2019 is on PDF file. 

Got an error that ISO-8859-1' didn't reckonise character '\x96' on CM002. Identified from coursework that there is an error on the server. The standard used appears to be cp1252, not ISO as stated in the webpages network. 
Count on the lines is 949. 
Attempted to split each line where there is more than 1 space and re-join them with a comma. 
And write to a CSV file. 
Problem is that there are mutliple lines where course name has more than 2 spaces. 
Going to attempt to reconfigure a full match regular expression and add a comma after each group. 