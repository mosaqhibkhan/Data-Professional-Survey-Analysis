# Project Documentation — Data Professional Survey Analysis

## Contents

- [1. Project Overview](#1-project-overview)
- [2. Problem Statement](#2-problem-statement)
- [3. Objectives](#3-objectives)
- [4. Tools and Technologies](#4-tools-and-technologies)
- [5. Dataset Overview](#5-dataset-overview)
- [6. Data Preparation and Wrangling](#6-data-preparation-and-wrangling)
- [7. Dashboard Design and Visual Analysis](#7-dashboard-design-and-visual-analysis)
- [8. Findings from the Source Workbook](#8-findings-from-the-source-workbook)
- [9. Interpretation and Limitations](#9-interpretation-and-limitations)
- [10. How to Open the Report](#10-how-to-open-the-report)
- [11. Skills Demonstrated](#11-skills-demonstrated)
- [12. Conclusion](#12-conclusion)

---

## 1. Project Overview

**Data Professional Survey Analysis** is a data-visualization project built using Microsoft Power BI. It explores survey responses from people working in, or interested in, the data profession.

The report brings together information about respondents' locations, current job roles, salary-related satisfaction, work-life balance, programming-language preferences, and perceived difficulty of entering the data industry.

The source dataset was provided in Microsoft Excel format. Before creating visualizations, the data was imported into Power BI and **wrangled using Power Query**. The prepared data was then used to develop the dashboard.

## 2. Problem Statement

Survey datasets can contain many columns and different types of responses. Reading the raw data alone does not make it easy to identify patterns across job roles, countries, programming-language preferences, or satisfaction ratings.

This project addresses that problem by preparing the survey data and presenting selected information in a consolidated dashboard. The report is intended to make the survey easier to explore and its main patterns easier to communicate.

## 3. Objectives

The project aims to:

1. Explore the geographical distribution of survey respondents.
2. Understand the distribution of respondents across current job roles.
3. Present the salary-related metric by current role.
4. Summarize the age profile of respondents.
5. Examine salary and work-life balance satisfaction.
6. Explore respondents' perceptions of the difficulty of entering the data field.
7. Compare programming-language preferences across current roles.
8. Communicate the results through a Power BI dashboard.

## 4. Tools and Technologies

| Technology | Role in the Project |
|---|---|
| Microsoft Excel | Original survey data source |
| Microsoft Power BI Desktop | Data model, report canvas and dashboard visualizations |
| Power Query | Data inspection, wrangling and transformation before visualization |

DAX measures or calculated columns should be added to this list only where they were actually used in the `.pbix` report.

## 5. Dataset Overview

The supplied workbook is named `Power BI - Final Project.xlsx` and contains one worksheet, `Data Professional Survey`.

The workbook has **630 data rows** and 28 columns. The fields cover several themes:

| Theme | Example Information in the Source |
|---|---|
| Response Metadata | Unique ID, date taken, time taken, browser, operating system and time spent |
| Location | City and country fields |
| Professional Background | Current role, career switch into data, industry and yearly salary range |
| Preferences | Favourite programming language and most important factor when looking for a new job |
| Satisfaction | Salary, work-life balance, coworkers, management, upward mobility and learning |
| Career Entry | Perceived difficulty of breaking into data |
| Respondent Profile | Age, education and other demographic survey fields |

The workbook also contains Email and Unique ID fields. These should not be included in a public dataset in identifiable form. Publish an anonymized copy or omit those fields before making the dataset available in a public repository.

## 6. Data Preparation and Wrangling

### 6.1 Importing the Source Data

The survey workbook was imported from Microsoft Excel into Power BI.

### 6.2 Power Query Data Wrangling

Before building the visualizations, the imported data was opened and wrangled in **Power Query Editor**. This preparation stage was used to work with the source data before it was loaded for report development.

The documented high-level sequence is:

1. Connect Power BI to the Excel workbook.
2. Inspect the imported survey data in Power Query.
3. Carry out the required data-wrangling and preparation operations.
4. Apply the query changes and load the prepared data into the Power BI model.
5. Use the prepared data to create the dashboard.

### 6.3 Record the Exact Transformations

The available project information confirms that Power Query was used for data wrangling, but it does not specify every individual transformation.

To keep this documentation accurate, list only the operations that appear in the actual Power Query **Applied Steps** pane.

For example, if they were performed, the steps could be documented under headings such as:

- Changed data types.
- Removed unnecessary columns.
- Handled blank or null values.
- Removed duplicate records.
- Renamed columns.
- Replaced or standardized inconsistent category values.
- Split or merged columns.

Do not claim any of these specific operations unless they were part of the actual query.

### 6.4 Loading the Prepared Data

After the Power Query preparation, the transformed data was loaded into Power BI for the report and visualizations.

## 7. Dashboard Design and Visual Analysis

The report is titled **Data Survey Breakdown**. It combines several visual types to show different aspects of the survey.

### 7.1 Country Wise Tree Map

**Purpose:** Show the distribution of survey respondents across countries.

The treemap uses country categories and relative block sizes to make the geographical distribution easier to compare.

**Reading the Visual:** Larger blocks represent countries with more responses in the report's current filter context.

### 7.2 Average Salary by Current Role

**Purpose:** Compare the salary-related metric across professional roles.

The visual displays categories including:

- Data Scientist
- Data Architect
- Data Engineer
- Other
- Data Analyst
- Database Developer
- Student/Looking/None

**Interpretation Caution:** The source workbook records yearly salary in ranges rather than exact numeric salary values. Before describing the plotted values as average salaries, verify the measure and any conversion from salary bands in the Power BI file. If the visual represents respondent counts or another statistic, update its title to match the actual measure.

### 7.3 Average Age

**Purpose:** Display the average age of respondents represented in the report.

The supplied screenshot shows **29.78**.

### 7.4 Count of Survey Takers

**Purpose:** Show the number of survey takers represented in the report.

The supplied screenshot shows **578**.

This is a report-level value and differs from the 630 data rows in the supplied Excel workbook. The reason should be checked against the report's filters, query steps and measure definition.

### 7.5 Average of Happy With Salary

**Purpose:** Summarize respondents' satisfaction with salary.

The supplied screenshot shows an average rating of **4.26 out of 10**.

### 7.6 Average Happy With Work/Life Balance

**Purpose:** Summarize respondents' satisfaction with work-life balance.

The supplied screenshot shows an average rating of **5.75 out of 10**.

### 7.7 Percentage of Difficulty To Break Into Data

**Purpose:** Show how respondents describe the difficulty of entering the data industry.

The visual groups responses into five categories:

- Neither easy nor difficult
- Difficult
- Easy
- Very Difficult
- Very Easy

The doughnut chart communicates the share of responses in each category.

### 7.8 Favorite Programming Language

**Purpose:** Compare favourite programming-language responses across current professional roles.

The stacked column chart displays language categories such as:

- Python
- R
- Other
- C/C++
- JavaScript
- Java

The stacks distinguish the professional roles represented in each category.

## 8. Findings from the Source Workbook

The following figures are calculated from the **630 data rows in the supplied Excel workbook**. They are workbook-level counts and are not necessarily identical to the report values shown in the screenshot.

### 8.1 Current Role

The most frequent current-role responses include:

| Current Role | Responses |
|---|---:|
| Data Analyst | 381 |
| Student/Looking/None | 90 |
| Data Engineer | 38 |
| Data Scientist | 25 |

Data Analyst is the largest role category in the supplied workbook.

### 8.2 Favourite Programming Language

| Response | Responses |
|---|---:|
| Python | 420 |
| R | 101 |
| Other:SQL | 29 |
| Other:Sql | 11 |

Python is the most frequently selected named programming-language response.

SQL appears in multiple free-text variants, so those categories would need to be standardized before reporting a combined SQL total.

### 8.3 Difficulty Entering the Data Industry

| Response | Responses | Share of 630 |
|---|---:|---:|
| Neither easy nor difficult | 269 | 42.7% |
| Difficult | 156 | 24.8% |
| Easy | 134 | 21.3% |
| Very Difficult | 44 | 7.0% |
| Very Easy | 27 | 4.3% |

Combining the responses:

- Difficult or Very Difficult: **200 responses (31.7%)**.
- Easy or Very Easy: **161 responses (25.6%)**.
- Neither easy nor difficult: **269 responses (42.7%)**.

The neutral category is the largest group. More respondents selected one of the two difficult categories than one of the two easy categories.

### 8.4 Country Distribution

| Country | Responses |
|---|---:|
| United States | 261 |
| India | 73 |
| United Kingdom | 40 |
| Canada | 32 |

The United States has the largest number of responses in the workbook, followed by India, the United Kingdom and Canada.

### 8.5 Satisfaction Ratings

The supplied dashboard screenshot displays:

| Satisfaction Measure | Dashboard Value |
|---|---:|
| Salary | 4.26 / 10 |
| Work-life Balance | 5.75 / 10 |

The displayed work-life-balance score is higher than the displayed salary-satisfaction score.

## 9. Interpretation and Limitations

- **Different Totals:** The Excel workbook contains 630 data rows, while the screenshot displays 578 survey takers. Check report filters, Power Query steps and the survey-taker measure to establish why.
- **Salary Bands:** Salary is supplied as ranges. An average salary requires a documented conversion method; a chart title should accurately describe the calculation.
- **Free-text Categories:** Answers such as SQL/Sql/sql can be split across separate values. Standardization is needed before combining them.
- **Survey Scope:** These findings describe the supplied survey responses. They should not be generalized to every data professional or treated as a representative global estimate.
- **Privacy:** The original workbook includes Email and Unique ID fields. Do not publish respondent-identifying information.
- **Filter Context:** KPI values shown in a Power BI report can change depending on filters, slicers and the measure definition.

## 10. How to Open the Report

1. Download or clone the repository.
2. Open Microsoft Power BI Desktop.
3. Open `Dashboard/Power BI Project.pbix`.
4. If the source workbook path is unavailable, update the data source path to `Dataset/Power BI - Final Project.xlsx`.
5. Refresh the data if necessary.
6. Explore the dashboard visuals.

## 11. Skills Demonstrated

- Importing data from Excel.
- Data wrangling and preparation using Power Query.
- Working with survey data and categorical responses.
- Developing reports in Microsoft Power BI.
- Creating KPI cards and multiple visualization types.
- Comparing groups and interpreting survey results.
- Presenting findings through data visualization.

## 12. Conclusion

The Data Professional Survey Analysis project demonstrates a complete introductory analytics workflow: importing a survey workbook, wrangling the data in Power Query, preparing it for analysis, and presenting selected results in a Power BI dashboard.

The report provides a consolidated view of respondents' roles, locations, programming-language preferences, career-entry experiences and satisfaction ratings.

It also highlights the importance of data preparation, consistent categories, accurate measure definitions and careful interpretation when turning survey data into insights.

---

**Project:** Data Professional Survey Analysis

**Author:** Mohammed Saqhibuddin Khan

**Tools:** Microsoft Power BI, Power Query and Microsoft Excel