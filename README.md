# Divvy Bike Share Data Analysis Project

## Project Objective

The project aims to perform an insightful analysis of Divvy Bike Share data to uncover patterns and provide strategic optimization recommendations. The objective is to systematically collect, clean, and transform the data, then analyze and visualize it to identify key trends and actionable insights that can improve the operational efficiency and user satisfaction of the Divvy Bike Share system.

## Data Collection and Cleaning

### Data Collection
For the Divvy Bike Share Data project, I collected data from a public AWS repository, which included 24 CSV files with a total of 11 million records and 13 columns each.

### Data Cleaning
Using the pandas library in Python, I performed the following steps:
1. **Combining Data:** Read all CSV files and combined them into a single dataset for ease of processing.
2. **Handling Missing Values:** Removed records with null entries.
3. **Standardizing Text Data:** Converted start and end station names to lowercase and trimmed any leading or trailing white spaces.
4. **Date-Time Conversion:** Converted start and end date-time columns into pandas datetime format.
5. **Ride Duration Calculation:** Computed the total ride duration by subtracting the start time from the end time and converting the result into minutes.
6. **Feature Creation:** Extracted components such as month, day, year, hour, day of the week, and quarter from the start date-time for temporal analysis. Created a 'route' column by concatenating the start and end station names. Introduced a 'season' column categorizing data into Fall, Winter, Summer, and Spring based on the month.
7. **Error Filtering:** Filtered out records where the ride duration was less than zero.

After these steps, the cleaned dataset was written back to a CSV file, ensuring it was ready for further analysis.

## Data Analysis and Visualization

### Data Analysis
In the analysis phase, I read the cleaned CSV file using pandas and conducted both univariate and multivariate analyses using the matplotlib library.

1. **Univariate Analysis:** Understanding the distribution of individual variables, such as the frequency of rides per season or the average duration of rides.
2. **Multivariate Analysis:** Exploring relationships between multiple variables, such as ride durations across different times of the day and days of the week, and how these patterns differed between bike types and user demographics.

### Visualization
By visualizing the data, key patterns and trends were identified to inform strategic optimization. For example:
- **Heat Maps:** Revealed peak usage times.
- **Scatter Plots:** Illustrated the relationship between ride duration and distance.

These insights helped identify the busiest stations during different seasons and peak hours, forming the basis for recommendations on improving operational efficiency and user satisfaction.

## Tableau Visualization

Using Tableau, I created a comprehensive geographical visualization of the bike routes:
- Constructed a map depicting start and end stations of bike trips, connected by lines representing the routes.
- Created precise points for each station and dynamically drew lines to visualize the paths using calculated fields.

This map allowed users to select a start station and view the various routes originating from that station, broken down by bike type and season. The spatial analysis was crucial for identifying high-demand areas and optimizing resource allocation.

## Visualizations

1. **Number of Rides by Membership Type:** Throughout the 12 months according to year.
2. **Number of Rides by Bike and Membership Types:** In 2021 and 2022.
3. **Number of Rides in Each Quarter:** In 2021 & 2022.
4. **Geographical Ride Map:** Shows routes based on selected station name, bike type, and seasons, with membership type represented by color.
5. **Interactive Visualization (D3.js):** Number of rides in end & start station name based on ride type and membership type.
6. **Interactive Visualization (D3.js):** Top 10 routes by number of rides based on seasons and membership type.

## Conclusion

This project provided a deep dive into the Divvy Bike Share data, resulting in actionable insights to optimize operational efficiency and enhance user satisfaction. By combining robust data cleaning techniques, comprehensive analysis, and intuitive visualizations, the project demonstrated the power of data-driven decision-making in the context of a bike share system.
