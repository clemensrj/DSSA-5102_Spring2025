# Broadway Shows Data Set 
## DSSA-5102 - Spring 2025

### Where is the data from? ​
This dataset was found on Kaggle.com

### How was it collected?​
The data was collected from Playbill.com which provides a variety of information about broadway performances including gross income, number of seats in theatre, etc. 

### How was it extracted?​
The user who uploaded this data set used web scraping in order to pull the show information off of playbill.com/grosses. The data would have been gathered in an unstructured format (HTML), then processed into structured data (CSV or Excel) for easier analysis.

### What program was used to clean the data?​
The data was cleaned using Python, specifically utilizing the pandas library for data manipulation and the matplotlib library for visualizations. Additional libraries such as numpy were used for numerical operations and data transformations.

### How was the data cleaned or transformed? Be specific.​
In order to clean the data all column names were made lowercase, then all special characters ($,%,*) and spaces were removed. This will make it easier to understand when utilizing this data in programs like SQL. Next, rows that did not have a Show Name for the showname column were changed to unknown for easier comprehension when reading our data. Then, duplicate rows which were completely identical were removed in order to easily plot general trends and clean up some entries that do not add any more information to the dataset. Although there were many zeros in the Potential Gross column, those were kept as they described intial performances of specific shows and held information of when shows were not performing. Finally these changes were visualized and saved into the cleaned data set for ease of use. 

### What are the units of the numeric data?​
- Potential Gross: The unit is dollars ($), representing the total revenue from ticket sales for each performance.
- Seats Sold: The unit is the number of seats sold for each performance.
- Seats in Theater: The unit is the number of seats available in the theater for each performance.
- Average Ticket: The unit is dollars ($), representing the average price of a ticket for each performance.
- Previews: The unit is number of preview performances before the official opening.

### What were the formulas used in column creation?​
Since all columns were provided in the original data set, no formulas were used. However, there are some potential calculations which might have contributed to the original data set. Below are listed some possible calculations which may have helped create the data set. 

- Potential Gross = Seats Sold * Average Ticket Price
- Average Ticket = Potential Gross / Seats Sold
- Capacity = (Seats Sold / Seats in Theater) * 100
- Difference in Capacity = Capacity - (previous Capacity)


### How is the data validated to ensure consistency?​
Cleaning the column names listed above, handling missing values, and determining how to handle zero values within the data all contributed to making sure the dataset was consistent. The data was also visualized as a data frame and through a few test plots in order to determine the consistency within the cleaned data. 

### What are the definitions for the column names? Include all columns in your dataset.​
- Year: The year of the performance. Includes day and month for each week signified in row of data.
- Show_name: The name of the Broadway show.
- Potential_Gross: The total gross revenue from ticket sales for the performance.
- Difference: The difference between the potential gross and actual gross (if applicable).
- Average_ticket: The average price of a ticket for that performance.
- Seats_Sold: The number of seats sold for the performance.
- Seats_in_theater: The total number of seats available in the theater.
- Previews: The number of preview performances before the official opening.
- %cap: The percentage of seating capacity that was sold.
- diff_cap: The difference in seating capacity percentage compared to a benchmark (if applicable).

### What are the regulations to using the data?
Since this dataset comes from Kaggle and was scraped from Playbill.com, it is essential to review any terms of use or licenses provided by both Kaggle and Playbill to ensure that the data is being used legally and in compliance with their rules. Since this data set was not being used for a publication, we do not have to cite any source other than the data set itself and the website it was scraped from. 

### If you are referencing sources, be sure to include citations/references as needed.
Kaggle: "Broadway Shows Data," accessed February 2025, available at: https://www.kaggle.com/datasets/praveensh/broadway-shows-data
Playbill.com: Data scraped from Playbill.com.
