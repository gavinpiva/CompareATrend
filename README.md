# CompareATrend
National Football League Quarterback analysis tool.

This repository contains three Python scripts that analyze a dataset of quarterback performance in the NFL.

# NFL Season Data Collection.ipynb
This code uses the nfl_data_py package to import NFL play-by-play data for the 2022 regular season, along with rosters and team descriptions. The data is filtered to only include passing plays, regular season games, and non-two point attempts.

The code then merges player names and team colors into the play-by-play data. It creates a new "location" column based on the home/away team, and groups the data by player, week, result, and location. The group is aggregated by summing the number of passing touchdowns, passing yards, sacks, and interceptions.

A function get_win_loss() is defined to determine if a player's team won, lost, or tied the game. The result and location columns are used to calculate the win-loss status for each player in each game. The resulting data is then printed to the console.

Note: The last line of code that is commented out, agg.to_csv("QB_data_results_2022", index= False), could be used to save the aggregated data to a CSV file named "QB_data_results_2022" in the same directory as the code file. Each of these files are assembled in csv_combine.ipynb.

# QB_data_results_all_years.csv
This CSV file contains the dataset used by the scripts. It includes information about each quarterback's performance in every game they played from 2016-2023. The following columns are included:

year: The date of the game

player_name: The name of the quarterback

location: weather the game was home or away

passing_yards: The number of passing yards the quarterback threw for

pass_touchdown: The number of touchdown passes the quarterback threw

interception: The number of interceptions the quarterback threw

sack: The number of times the quarterback was sacked

win_loss: Whether the quarterback's team won, lost, or tied the game

# csv_combine.ipynb
This Jupyter Notebook contains all of the information and code for assembling each of the files that are created in NFL Season Data Collection

# new_models.py
This script uses logistic and linear regression to analyze the dataset and determine the top quarterbacks by win percentage. It creates two graphs:

A horizontal bar graph of the top 15 quarterbacks by win percentage
A pie chart of the top 15 quarterbacks by win percentage, categorized by win percentage
To run this script, you must have the following Python libraries installed:

pandas
numpy
matplotlib
sklearn


Usage
To use either of these scripts, simply run the file in a Python environment that has the required libraries installed. The output graphs will be displayed automatically.

Note: The CSV file must be in the same directory as the Python script for it to be read properly.

Author:
 Gavin Piva

Each of the plots that are created from the code files listed:

![qb histograms](https://user-images.githubusercontent.com/65461919/234699536-f17db1a7-9915-4ddf-a188-18b6ea8b044f.png)
![qb_horizontal_bar_chart](https://user-images.githubusercontent.com/65461919/234699565-26a671be-4724-432f-ba52-bebd7bb9b008.png)
![qb_pie_chart](https://user-images.githubusercontent.com/65461919/234699592-7df56385-d1da-4290-80b8-f9fb0281f4dd.png)
