# Experiment 1: EDA in IPL Dataset

## Aim:

To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

## Algorithm / Procedure:

### 1. Import Libraries

Import pandas for data handling.

Import matplotlib and seaborn for visualization.
  
### 2.Load Dataset

  Use pd.read_csv() to load the IPL matches dataset.
  
  Check dataset shape using .shape.
  
  View first 5 rows using .head().
  
### 3.Matches per Season (Univariate Analysis)

  Group data by season and count matches.
  
  Plot a bar chart to visualize growth/decline in matches.
  
### 4.Top Winning Teams (Univariate Analysis)

  Use value_counts() on the winner column.
  
  Plot top 5 winning teams in a bar chart.
  
### 5.Toss Decisions (Univariate Analysis)

  Count toss decision preferences (bat vs field).
  
  Plot results using a bar chart.

### 6.Top Venues (Univariate Analysis)

  Count matches per venue.
  
  Display top 5 venues with a horizontal bar chart.
  
### 7.Draw Insights

  Observe patterns in toss decisions.
  
  Identify teams with consistent winning trends.
  
  
  ## Program
  
```py
# Step 1: Import necessary libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```
```py
# Step 2: Load the dataset
matches = pd.read_csv("matches.csv")

# Step 3: Basic info about dataset
print("Dataset Shape:", matches.shape)    
print(matches.head())                     
```
```py
# Step 4: Number of matches per season
season_counts = matches['season'].value_counts().sort_index()
print("Name: Shriram S")
print("Reg no: 212222240098")
print("\nMatches per season:\n", season_counts)

# Plot matches per season
plt.figure(figsize=(8,4))
sns.barplot(x=season_counts.index, y=season_counts.values, palette="viridis")
plt.title("Number of Matches per Season")
plt.xlabel("Season")
plt.ylabel("Matches")
plt.show()
```
```py
# Step 5: Most successful teams
team_wins = matches['winner'].value_counts()
print("Name: Shriram S")
print("Reg no: 212222240098")
print("\nTop Winning Teams:\n", team_wins.head(5))

plt.figure(figsize=(8,4))
sns.barplot(x=team_wins.head(5).index, y=team_wins.head(5).values, palette="magma")
plt.title("Top 5 Winning Teams")
plt.xlabel("Team")
plt.ylabel("Wins")
plt.show()
```
```py
# Step 6: Toss decisions (bat vs field)
toss_decision = matches['toss_decision'].value_counts()
print("Name: Shriram S")
print("Reg no: 212222240098")
print("\nToss Decisions:\n", toss_decision)

plt.figure(figsize=(6,4))
sns.barplot(x=toss_decision.index, y=toss_decision.values, palette="Set2")
plt.title("Toss Decisions (Bat or Field)")
plt.show()
```
```py
# Step 7: Venues hosting most matches
venue_counts = matches['venue'].value_counts().head(5)
print("Name: Shriram S")
print("Reg no: 212222240098")

print("\nTop Venues:\n", venue_counts)

plt.figure(figsize=(8,4))
sns.barplot(y=venue_counts.index, x=venue_counts.values, palette="coolwarm")
plt.title("Top 5 Venues by Matches Hosted")
plt.xlabel("Matches Hosted")
plt.ylabel("Venue")
plt.show()
```

  ## Output

### 1. Top 5 Winning Teams
<img width="388" height="218" alt="image" src="https://github.com/user-attachments/assets/b5b2aa58-04b9-44e8-8f91-057f265f12da" />
<img width="695" height="393" alt="image" src="https://github.com/user-attachments/assets/2ecf56be-56d4-4781-bc56-4cd15bf828da" />

### 2. Toss decision preferences (bat vs field).
<img width="282" height="149" alt="image" src="https://github.com/user-attachments/assets/e5684d3a-b07b-496d-977c-add12f1ddf9d" />
<img width="521" height="393" alt="image" src="https://github.com/user-attachments/assets/5c34ced3-d02d-4d71-b7fc-267917633096" />

### 3. Matches per venue
<img width="482" height="240" alt="image" src="https://github.com/user-attachments/assets/8cc8351c-ad78-48a1-ba98-5c568685ef32" />
<img width="964" height="393" alt="image" src="https://github.com/user-attachments/assets/c7041364-a00a-4fdd-89ab-7f140ce48069" />

### 4. 

 ## Result
  This experiment is executed successfully



Highlight the stadiums hosting maximum matches.
