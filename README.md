# pandas-challenge
## Background
You are the new Chief Data Scientist for your city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

As a first task, you've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

## Instructions
Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

## District Summary
Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:

* Total number of unique schools

* Total students

* Total budget

* Average math score

* Average reading score

* % passing math (the percentage of students who passed math)

* % passing reading (the percentage of students who passed reading)

* % overall passing (the percentage of students who passed math AND reading)

## School Summary
Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:

* School name

* School type

* Total students

* Total school budget

* Per student budget

* Average math score

* Average reading score

* % passing math (the percentage of students who passed math)

* % passing reading (the percentage of students who passed reading)

* % overall passing (the percentage of students who passed math AND reading)

### Highest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in descending order and display the top 5 rows.

Save the results in a DataFrame called "top_schools".

### Lowest-Performing Schools (by % Overall Passing)
Sort the schools by % Overall Passing in ascending order and display the top 5 rows.

Save the results in a DataFrame called "bottom_schools".

### Math Scores by Grade
Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Reading Scores by Grade
Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

### Scores by School Spending
Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

![label](https://user-images.githubusercontent.com/114199979/221949503-969c3a05-a7e7-4fbb-a4b3-8e12c3d0cde0.png)

Use pd.cut to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

![code](https://user-images.githubusercontent.com/114199979/221948660-04bf2b0b-7475-47e2-a81d-a443dd4d18f3.png)

Use the scores above to create a DataFrame called spending_summary.

Include the following metrics in the table:

* Average math score

* Average reading score

* % passing math (the percentage of students who passed math)

* % passing reading (the percentage of students who passed reading)

* % overall passing (the percentage of students who passed math AND reading)

### Scores by School Size
Use the following code to bin the per_school_summary.
![bins](https://user-images.githubusercontent.com/114199979/221949066-31d5670c-f961-4f1e-b8e3-dcec40478017.png)
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

### Scores by School Type
Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.

This new DataFrame should show school performance based on the "School Type".

# Summary of Analysis
This data is desribing 15 schools with 39170 students, containing details about the score of students in math and reading class.
In this challenge we categorized schools by different metrics such as their type, size and budget and evaluate scores of students for math, reading, overall,and the passing percentage to analyze the performance of each school.
One interesting insight which is obtained by looking at the overall passing percentage, is that all of the top performing schools are Charter schools, also smaller schools with a total budget around 1 mollion dollars, and all of the worst-performing schools are District, larger and also with a budget almost doubled!!
If we take a closer look to average scores by grade level table, we can understand that there's not much of a noticable difference between different grade levels of each school and the tolerance is mainly around 1%.
The table with spending ranges demonstrates that the relation between budget for each student and overall passing percentage is inverse, meaning the higher the budget is, the lower the performance and the average scores are.
We can also see that when the school size is larger than 2000 students the overall prformance, average scores and number of passing students has a considerable decrease.
Finally, comparing schools only by their type, we can understand that average math score and number of student that passed the math class are much lower in district schools than charter schools, this difference in reading score averages is less but still charter schools have a better overall performance.
