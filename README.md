# Data Visualization with Python Matplotlib

<img src="Images/laboratory.jpg" width="100%" align="center"/>

## Description

This repository is designed to analyze laboratory test results from a study aimed at developing treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. In this study, 249 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens.

Sample metadata and study results are stored in two CSV files (Mouse_metadata.csv, Study_results.csv) which are read into the study_analysis.ipynb notebook and merged using an outer join. Duplicate mouse IDs are dropped before calculating summary statistics for each drug regimen.

Data is then visualized using Pandas and Matplotlib to create the following:

- A **bar plot** using both Pandas's DataFrame.plot() and Matplotlib's pyplot that shows the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

- A **pie plot** using both Pandas's DataFrame.plot() and Matplotlib's pyplot that shows the distribution of female or male mice in the study.

The final tumor volume of each mouse across four of the most promising treatment regimens (Capomulin, Ramicane, Infubinol, and Ceftamin) is calculated using Pandas GroupBy and loc functions, and quartiles and IQR are used to quantitatively determine if there are any potential outliers across all four treatment regimens. After removing any outliers, a **box plot** of the final tumor volume of each mouse across four regimens of interest is created using Matplotlib.

Lastly, a **scatter plot** of tumor volume versus mouse weight for the Capomulin treatment regimen is created, and data for mouse #185 (treated with Capomulin) is used to generate a **line plot** of tumor volume vs. time. The correlation coefficient and linear regression model are determined for the scatterplot of mouse weight and average tumor volume for the Capomulin treatment using scipy.stats. Finally, the **linear regression model** is plotted on top of the previous scatter plot.