# 🚶 Personal Activity Monitoring Analysis

## 📖 Overview
This project analyzes data collected from a personal activity monitoring device over a two-month period (October–November 2012).  
The data captures the number of steps taken in 5-minute intervals throughout each day.  

The goal is to explore daily activity patterns, handle missing data, and visualize differences in activity between weekdays and weekends.

---

## 📊 Dataset

**Source:** [Activity Monitoring Dataset](https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2Factivity.zip) (~52 KB)  

**Variables:**

- **steps** – Number of steps taken in a 5-minute interval (missing values are coded as `NA`)  
- **date** – Date of measurement (YYYY-MM-DD)  
- **interval** – 5-minute interval identifier  

**Observations:** 17,568 rows  

---

## 🛠️ Data Loading and Preprocessing

- Load the data using `read.csv()`.  
- Convert `date` to a `Date` object.  
- Handle missing values as needed (e.g., imputation using interval means or medians).  
- Prepare the dataset for daily aggregation and visualization.

---

## 📈 Analysis Tasks

### 1. Mean Total Number of Steps Per Day
- Compute total steps per day (ignoring missing values).  
- Plot a histogram of daily total steps.  
- Calculate and report the **mean** and **median** total steps per day.

### 2. Average Daily Activity Pattern
- Compute the average number of steps for each 5-minute interval across all days.  
- Create a time series plot of interval vs. average steps.  
- Identify the interval with the maximum average number of steps.

### 3. Imputing Missing Values
- Count total missing values in the dataset.  
- Fill in missing values using a chosen strategy (e.g., mean for that interval).  
- Recompute daily totals, plot a histogram, and compare the mean/median with the original dataset.  
- Assess the impact of imputation on the daily activity summary.

### 4. Differences Between Weekdays and Weekends
- Create a new factor variable indicating "weekday" or "weekend".  
- Compute average steps for each interval separately for weekdays and weekends.  
- Create a panel plot comparing activity patterns across weekdays and weekends.

---

## 📂 Repository Structure

- `activity_analysis.Rmd` – R Markdown document with all analysis code and outputs  
- `activity_analysis.html` – HTML version of the report generated via **knitr**  
- `activity_analysis.md` – Markdown version of the report  
- `figure/` – Folder containing generated plots

---

## 🚀 How to Run

1. Download and unzip the dataset.  
2. Place the `activity_analysis.Rmd` file in your working directory.  
3. Open R and ensure the required packages are installed: `dplyr`, `ggplot2`, `lubridate`.  
4. Knit the R Markdown file to generate HTML and Markdown reports.  

```r
library(knitr)
knit("activity_analysis.Rmd")
