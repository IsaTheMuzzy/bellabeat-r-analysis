# Bellabeat R Analysis

This repository contains an R analysis of Bellabeat's daily activity data, focusing on trends in user activity levels, calorie expenditure, and user segmentation.

## Project Overview
- **Goal**: Use R to analyze Bellabeat activity data and uncover insights into user behavior and engagement.
- **Skills Demonstrated**: Data cleaning, visualization, statistical analysis, and R programming.

## Files
- `bellabeat_analysis.Rmd`: The RMarkdown file containing all R code and analysis steps.
- `bellabeat_analysis.pdf`: The knitted PDF report with visualizations and results.

## Analysis Highlights
- **Daily Activity Trends**: Visualization of daily steps and calorie expenditure over time.
- **Activity Level Proportions**: Breakdown of time spent in various activity levels (e.g., sedentary, lightly active).
- **User Segmentation**: Grouping users based on activity levels and examining differences in steps and calorie burn.

## Example Code
- **Data Wrangling**:
  ```r
  daily_summary <- dailyactivity %>%
    summarise(
      avg_steps = mean(TotalSteps, na.rm = TRUE),
      avg_calories = mean(Calories, na.rm = TRUE)
    )

# Visualization
```r
ggplot(dailyactivity, aes(x = ActivityDate, y = TotalSteps)) +
  geom_line() +
  labs(title = "Daily Steps Over Time")
```

## Insights and Findings

This analysis of Bellabeat's daily activity data reveals the following insights:

- **Activity Levels and Calorie Burn**: Higher activity levels correlate with increased calorie expenditure, with users who engage in more intense activities burning more calories overall. This suggests that Bellabeat could encourage users to increase active minutes to meet calorie burn goals.

- **Daily Activity Patterns**: Users tend to have fluctuating activity levels throughout the week, with some days showing significant drops in both steps and calorie burn. These dips may indicate lower motivation or routine changes, and Bellabeat could introduce reminders or challenges to help maintain consistency.

- **Time Allocation in Activity Levels**: Users spend a considerable portion of their time in sedentary or lightly active states, with only a small fraction engaged in very active minutes. Brief, frequent active breaks could be suggested to users to reduce sedentary time and increase activity gradually.

- **User Segmentation**: Segmenting users into Low, Moderate, and High activity groups revealed distinct differences in steps, calories burned, and time spent in various activity levels. High-activity users consistently had greater step counts and calorie expenditure, while low-activity users had lower engagement. These segments could be used to tailor in-app notifications and suggestions, motivating low-activity users to increase their daily steps.

These findings can help Bellabeat develop targeted strategies to enhance user engagement, encourage consistent activity, and support users in reaching their fitness goals.
