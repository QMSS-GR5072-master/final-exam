# Final Exam

## Instructions:

1. Your final document should be an `.md` file (GitHub-flavored markdown) knitted from an R Markdown file. Create a folder called `/final-exam` where you will add the `.md` file, and a folder called `/src` where you will  place the `.Rmd` file and any other scripts you used to create the reports.

  In answering each of the questions for the assignment please include
  - the question as a header in your R Markdown report,
  - the raw code that you used to generate your results, and
  - the top ten rows/values/elements of any resulting tibble, dataframe, vector, or list created in your results (unless a lesser amount is requested).

2. when you are done with your final `push` to this repo, submit the link to this repo on Canvas. (Make sure to `commit` your progress throughout the day, and `push` your progress at the end of each day.)


## Exam Items [`100 pts`]

Feel free to refer to any R scripts provided throughout the course to answer the following questions:

1. [`10 pts`] Web-scrape all table data from the following [webpage](http://vincentarelbundock.github.io/Rdatasets/datasets.html) and build a data frame in R.  Limit your final table to include columns for "Package", "Item", "Title", "Rows", and "Cols".  Print the first five rows of the table.

2. [`10 pts`] Web-scrape the full links to every CSV file listed in the CSV column of the web-page.  Add a new column to your data frame that includes these links.  Name the column "`csv_links`".  Print the first five rows of the table.

	Note: You may need to use string operations to recreate the full link to the csv files after they are scraped.

3. [`5 pts`] Use R code/functions to search the "Title" column to return the row of data with the title, "Violent Crime Rates by US State"

4. [`10 pts`] Import the csv file into R using the full link listed in the "`csv_links`" column for this dataset.  Create a new variable called "`violent_crime`" that adds together data for all columns in the dataset that contain violent crime data (i.e.-add data from assault, murder, and rape columns together in new column called "`violent_crime`").

5. [`10 pts`] Using one or more of the following example datasets that come preloaded in R (see `?data(state)` for more information), add state region codes, state divisions, and all of the variables from the `state.x77` dataset to your Violent Crime Rates data frame.  Print the first five lines of your new dataset.

	`state.abb`, `state.area`, `state.center`, `state.division`, `state.name`, `state.region`

	**Note 1:** state names can be extracted to new columns for joins from these datasets by using `row.names()` if needed.

	**Note 2:** Some of these state datasets may be matrix objects or lists.  Be sure to convert them to data frames before joining them if needed.

6. [`5 pts`] Calculate the average for each numeric column in the dataset.

7. [`5 pts`] Group the data by region and then calculate the average for each numeric column in the dataset per region.  Which region had the highest population (data is from the late 1970s)?  Which region had the most violent crime?

8. [`5 pts`] Group the data by division and then calculate the average for each numeric column in the dataset per division.  Which division had the highest population (data is from the late 1970s)?  Which division had the most violent crime?

9. [`5 pts`] What SQL statement would you write to return two columns denoting income and Illiteracy in your state data?

10. [`5 pts`] What SQL statement would you write to return two columns denoting income and Illiteracy in your state data and sort the data from the highest to lowest income values and limit the data to incomes at or higher than 5000?

11. [`5 pts`] What SQL statement would you write to return two columns denoting income and Illiteracy in your state data and sort the data from the highest to lowest income values and limit the data to incomes at or higher than 5000 and return the top 10 rows only?

12. [`10 pts`] Create a new data frame that includes two columns from your state data denoting state names and violent crimes.  Spread the state names to 50 unique columns with a single row that includes the violent crime data per state.  Print the first five columns of the new dataset.

13. [`10 pts`] Take the dataset from question 12 and use a function from the apply family of functions to return a named list with each name denoting a state and each value per state indicating the square root of the value for violent crimes.

14. [`5 pts`] Subset the list you created in question 13 to extract values for Texas and New York.

**That's it!  Once you submit the link to this repo on Canvas you are done!**
