# Historical Climate Change Data Project

**All repository code and future direction of research is the property of Environment Analytics and currently cannot be publicly distributed due to research group policies, intellectual property concerns, and ethical considerations** (Publications pending with Logan McLaurin as primary author)

**Author**: Logan McLaurin

This repository highlights research presented at the 2023 and 2022 NCSU Summer Symposiums and the 2022 Kenan Institute for Engineering, Technology & Science (KIETS) Climate Symposium.
Research was completed for Environment Analytics, conducted in collaboration with the Department of Marine, Earth, and Atmospheric Sciences and the Center for Geospatial Analytics at North Carolina State University.

**Skills**: Advanced Python Programming, Statistical Data Analysis, Science Communication, Data Cleaning, Pragmatic Thinking, Project Management and Ownership, Skill Development

## Overview
Traditional climate analyses often rely on daily averages or extreme values, which fail to capture the granular impacts of temperature fluctuations over time. People, plants, and animals experience weather hour-by-hour, and understanding these patterns is critical for pragmatic climate change decision-making for mitigation and local adaptation measures. This research focuses on uncovering regional trends in climate change using historical hourly weather station data to create meaningful metrics for non-scientists.

Despite not having the authorization to distribute the coding repository related to this work (yet), the discussion of project motivations, data processing methods, statistical methods, and preliminary results can be shared amongst the three poster presentations attached to the repository. 

Personally, this project also illustrates directly the growth and development I have had as an analyst over the course of my time at Environment Analytics working on this project.

## Methods
The analysis uses hourly weather station data (1970s - 2021) from the Integrated Surface Database (ISD), maintained by NOAA’s National Centers for Environmental Information. Variables include air temperature, wind speed, pressure, precipitation amount, sky cover, etc. The primary focus of this project has been the anlysis of hourly air temperature data and other derived metrics to function as proxies for heat stress. 

Data from 361 active stations across North America and southern Canada were analyzed for trends using:
* Derived Metrics: Including heating and cooling degree hours, hours below freezing, and hours above 30°C or 78°F wet bulb temperature thresholds.
* Linear Regression: To quantify changes in hours above/below specific temperature thresholds (based on literature)
* Hypothesis Testing: To assess the significance of observed trends. The latest hypothesis testing for slope significance is using a permutation test (nonparametric) at the 95% confidence interval (stationary block bootstrapping was another method used in the posters)
* Residual standard deviation: proxy for observational variability amongst the stations

## Featured Dataset
The posters showcase Raleigh-Durham International Airport (KRDU) results as an example. KRDU trends illustrate reductions in winter energy demands and increases in summer heat stress hours over the study period.

## Why it Matters
This project provides actionable insights into regional climate changes using an innovative approach that prioritizes lived experiences of temperature changes. This research bridges the gap between scientific analysis and practical decision-making by presenting data in terms of hourly impacts.

## Programming Scheme
### Data Processing Scheme
Object-oriented programming approach utilized to perform the following tasks:
* User input station IDs allow for the processing of raw data to save table of hourly weather observations for each station; enhanced by parallel processing techniques
* Station selection features based on latitude, longitude, state, elevation, and the period for when the weather station is active
* Automated filtering to determine station reliability based upon the number of observations, presence of discontinuities, and outlier detection
* Methods to produce station climatological data based on hourly distribution characteristics
* All methods variable agnostic (same methods work for filtering by air temperature, precipitation, wind speed, etc.)

### Analysis Scheme
* Automated processing to diagnose slopes, significance, and plotting
* User defined inputs to control specific metrics, statistical testing used, plotting parameters, etc.
* Standardized Plotting Scheme
