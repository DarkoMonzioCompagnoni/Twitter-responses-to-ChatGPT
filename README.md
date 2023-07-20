# Women's World cup 

In occasion of the Women World Cup 2023, I analyzed a dataset containing information about women's soccer teams in the World Cup, with the year of the tournament, some characteristics of the team, and various statistics about the team's performance. 

This analysis should provide a good starting point for further in-depth analysis and hypothesis testing. For example, you could look into the effects of different strategies on team performance, or how the age or size of a team influences its results.


### Columns

- **id**: A unique identifier for each row
- **squad**: The name of the country that the team represents
- **year**: The year of the World Cup
- **players**: The number of players in the squad
- **age**: The average age of the players in the team
- **possession**: The average possession percentage of the team during the matches
- **matches_played**: The number of matches played by the team in the tournament
- **starts**: The number of matches in which the team started
- **min_playing_time**: The total minutes of playing time by the team in the tournament
- **minutes_played_90s**: The total playing time of the team in units of 90 minutes (equivalent to one match)
- **goals**: The total number of goals scored by the team in the tournament
- **assists**: The total number of assists by the team in the tournament
- **non_penalty_goals**: The total number of goals scored by the team excluding penalty kicks
- **penalty_kicks_made**: The total number of successful penalty kicks by the team
- **penalty_kicks_attempted**: The total number of penalty kicks attempted by the team
- **yellow_cards**: The total number of yellow cards received by the team
- **red_cards**: The total number of red cards received by the team
- **goals_per_90**: The average number of goals scored by the team per 90 minutes of play
- **assists_per_90**: The average number of assists by the team per 90 minutes of play
- **goals_plus_assists_per_90**: The average number of goals plus assists by the team per 90 minutes of play
- **goals_minus_penalty_kicks_per_90**: The average number of goals scored by the team per 90 minutes of play, excluding penalty kicks
- **goals_plus_assists_minus_penalty_kicks_per_90**: The average number of goals plus assists by the team per 90 minutes of play, excluding penalty kicks

### Data Cleaning

There are missing values in the possession, yellow_cards, and red_cards columns. This could mean that these data points were not recorded or not applicable for some teams.

### Exploratory Analysis 
- The average number of players in the squad is around 17, with the smallest squad having 13 players and the largest having 23.
- The average age of players across all teams and years is approximately 25 years, with a minimum of 18.2 and a maximum of 29.7.
- The average ball possession across all teams where this data is available is approximately 49.25%, with a range from 30% to 63%.
- Teams played an average of around 4 matches in the tournament, with a minimum of 3 and a maximum of 7.
- The average number of goals scored by teams is around 6.6, with a range from 0 to 25.
- The average number of assists is approximately 3.5, with a range from 0 to 14.
- The average number of yellow cards received by teams where this data is available is about 2.5, with a range from 0 to 8.
- The average number of red cards received by teams where this data is available is quite low (around 0.08), indicating that red cards are rare.

Now let's visualize some of these variables. Specifically, we'll look at the distribution of age, possession, goals, and assists. We'll also create a scatter plot to see if there's a relationship between possession and goals.

This analysis provides insights into the offensive (goals, assists) and disciplinary (yellow and red cards) performances of the teams. While the USA dominated in terms of scoring and assists, they were not among the teams with the most disciplinary actions, which suggests effective and fair play.

Let's continue the analysis by examining the correlation between different variables in the dataset. Correlation can help identify relationships between different performance metrics.

![](https://github.com/DarkoMonzioCompagnoni/media/blob/main/Screenshot%202023-07-20%20at%2012.49.29.png)

This heatmap visualizes the correlation between different variables in the dataset:

- Lighter cells indicate positive correlation; darker cells indicate negative correlation.
- Correlation coefficients closer to +1 or -1 indicate a stronger linear relationship between the two variables.

From the heatmap, we can observe some strong correlations:

- matches_played, starts, min_playing_time, and minutes_played_90s are highly correlated with each other. This makes sense as they all are different measures of how long a team has played in the tournament.
- goals, assists, non_penalty_goals, and various per-90-minutes metrics are also highly correlated with each other, reflecting a team's offensive performance.
- penalty_kicks_made and penalty_kicks_attempted are highly correlated, as we would expect.

However, correlation does not imply causation. While two variables might be correlated, it doesn't necessarily mean that one causes the other to change. It could be that both variables are influenced by other factors, or the observed correlation could be coincidental.

