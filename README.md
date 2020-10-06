# Final Project
Group 6 Xuelei Zhang Mitchell Lazarz

## Script 1:

The code web-scrapped weather information of Worcester, MA from the National Weather Service website.  At the beginning, the user is asked to enter a latitude and longitude of a location. Then, a 5 day weather forecast is generated based on the input.  However, the results are hard to read. Therefore, part of the codes modified the results by converting the final output to uppercase. In addition, by using the *.replace()* function, it fixed the spacing issues with the original output, making it more readable for readers. 

Fortunately, I did not run into any major problems during coding, but I came across a few syntax errors, for example, I forgot to put a colon in a for loop. Overall, the coding process was easy. I think this script would be helpful for the future, because it can help me extract large amounts of data from websites quickly. Moreover, the data I scrapped would be easy to analyze compared to simply copy=paste them. 

## Script 2:

This script uses a survey of voters and county names in Kenya that is used to determine which county should receive resources for humanitarian work.

### Challenge 1:

The code challenge 1 of script 2 includes a function that indicates the name of the county and the number of votes that county received. In order to do so, I started by using the upload function to upload a .txt file, which contains the voting information of each individual. I then created a function called county_vote_count(county) and set the counter equals to 0. By using *strip()* and *split()* function, the outputs are split into different lines and the characters in both the left and right are removed.  Then, I used an if statement to count the votes a county received. If the name in the list equals the input county name, then the counter increased by 1. 

The process of writing challenge 1 was okay. I came across a problem where I put the ‘count’ in the wrong place. I put it outside the function and kept getting 0 as the result. I fixed it by moving it inside the function. 

### Challenge 2:

In Challenge 2, three functions were created to manipulate the imported .txt survey file.  The first function cleaned the data for interpretation, the second function checked to see if an individual voted twice, and lastly, the survey results were displayed to determine the county with the most votes.

#### Function 1: Data Munging

After importing the .txt file, two empty lists were created to hold voter names and county names after data cleaning.  The munging function stripped the survey file and split the voter name and county at every hyphen.  The *.upper* function and *.replace* functions were used to remove unnecessary spaces and convert all characters to uppercase for consistency.  After this cleanup, voter names and county names were appended to the empty lists.

#### Function 2:  Checking for repeat votes

An empty list to hold voter names was created before writing the function.  In this function, the voter name list was called and sent through a for loop.  In this loop, if the name in the voter list is not in the empty list, the name was added.  During this loop, if the voter name was already added to the list, a statement was printed stating that an individual voted twice.

#### Function 3:  Counting the vote

An empty dictionary is created to hold the results of counting the votes.  The function calls the county name list and performs a for loop where if the county in the list is not in the dictionary, it is added to the dictionary with a value of 1.  If the county name is already in the dictionary, then the value is incremented.  The results are printed with a statement showing the key, value pair of the dictionary (“County : Count”).

The function then checks for the winner.  A variable called ‘winner’ is assigned to 0 then a for loop is run for the count value in the dictionary.  If the count is greater than 0, then the ‘winner’ variable is reassigned this value until the greatest count is assigned.  Then an additional for loop is run where, if the count in the dictionary is equal to the newly assigned ‘winner’ variable, a statement is printed with the county with the most votes.


The main issues that came up in writing this code was in the differentiation between local and global variables.  I solved this by appending the names and counties in the initial function to global lists.  From there, I was able to use these lists in the last two functions.

