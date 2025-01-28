# Pymaceuticals

#Background
I have recently joined a Pymaceuticals, Inc. a new pharmaceutical company that specializes in anti-cancer medications. This company recently began screening for squamous cell carcinoma (SCC) for any potential treatments to treat this form of skin cancer. As a senior data analysist my task is to generate all the tables and figures needed for the clinical report to view if Capomulin can be a drug used for SCC treatment compared to other drugs in the study. I've been given the access of the complete data that contains the most recent studies of 249 mice who were identified with SCC tumors over the course of 45 days to measure tumor development. 

#Set-Up & Dependencies
This assignment is broken down into the following tasks:
-Prepare the data
-- The way the data was prepared, I merged the mouse_metadata and study_results into a single DataFrame. By merging the datasets this provided a full display of the unique mice IDs, and data associated by mouse ID. Next step was to remove all duplicates found and to create a new DataFrame were duplicates and data associated with the duplicates was removed.  
---Mouse_metadata.csv: Contains metadata for the mice used in the study. Study_results.csv: Contains the study results, including tumor measurements
-Generate summary statistics.
-- The summary sratistics contains a row for each drug regimen and columns for mean, median, variance, SD and SEM of tumor volume 
-Create bar charts and pie charts.
--Bar chart and Pie chart were created using matplotlib and pandas
---Bar chart contains information such as the total number of rows (Mouse ID & Timpoints) for each drug regimen
---Pie chart shows the distribution of female versus male mice in the study
-Calculate quartiles, find outliers, and create a box plot
-- To do this part a new DataFrame was created. This DataFrame included the last(greatest) time point for each mouse, then it was merged with the cleaned DataFrame. A list was then created to hold treatment names, as well as tumor volume data. As a final step, the new DataFrame was looped through to demostrate each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Resluts were then append to show final tumor volumes for each drug. 
--- A box plot was created to show ther distrubution of the final tumor volume for all the mice in each treatment group.
-Create a line plot and a scatter plot
--Line plot was created to show tumor volume versu time plot for a single mouse treated with Capomulin
--Scatter plot was created to show mouse weight versus average observed tumor volume for the entire treatment of Capomulin
-Calculate correlation and regression.
-- Lastly, correlation, coefficient and linear regression was calculated for mouse weight and average observed tumor volume for the entire treatment regimen of Capomulin

#Final Analysis
After finalizing and clean my data, there were some trends that were noticeable. One trend that I saw during my analysis was that Campmulin and Ramicane had the lowest tumor volume at the end of the experiement. Suggesting that these two drug regimen could be the best potential anti-cancer medication to treat SCC. As well that there is a positive correlation with the weight of mouse to tumor size. As weight increases the tumor volume increases as well. Lastly, comparing all 4 drug regimen, the least affected drugs were Infubinol, and Ceftamin because both yeild a higher tumor volume at the end of the experiment.

