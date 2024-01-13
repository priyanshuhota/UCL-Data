#  UCL HISTORY ANALYSIS PROJECT 
I got data from kaggle from [here.](https://www.kaggle.com/datasets/basharalkuwaiti/champions-league-era-stats)

## Pre-Processing of data
Data was very messy at first I had to apply multiple methods to clean the data and make it more usable. I used MS-Excel for preprocessing of data. Some of the cleaning I did included:
* First file was all in a single column separated by comma I used 'Text to Column' function with comma as delimiter to get a usable file.
* Club names were not consistent in every file so I used find and replace function to make all the club names consistent with first file.
* In some files there were country code while in other files there were country name so I used get data from web function in excel and created a table for country and their code from wikipedia. Which was helpful later in implementing SQL queries.
* Then I used VLOOKUP function to identify countries from their code using above table.
* I also created player id, coach id and club id tables by using first two letter of first name and first two letter of last name. For that I used space as delimiter in 'Text to columns' to split first and last name and then used 'LEFT(2, NAME)' to generate ids.
* Also I created a list of most prominent coaches and players for each club using SORT function and finding most appearances of them.
* There wasn't much of missing data so I didn't have to worry about that.
* Although there were some data which was not supposed to be negative (for ex : 'goals scored') I took care of that as well.

After preprocessing my data looked like [this.](https://docs.google.com/spreadsheets/d/1gPnB9x6OTVlWq7eYFD7xy_7K8sP125f_/edit#gid=615385692)
