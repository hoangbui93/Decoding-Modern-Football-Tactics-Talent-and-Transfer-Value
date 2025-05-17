# DECODING MODERN FOOTBALL - TACTICS, TALENT AND TRANSFER VALUE

# Introdution
Football is known as “the beautiful game” because of its enduring appeal throughout history. Today, as technology permeates modern football, data analytics has become an integral part of the sport, offering invaluable support to players, coaches, and decision-makers. By leveraging data, tactics can be optimized, player performance assessed more objectively, and strategic or transfer decisions made with greater precision. Against this backdrop, this project harnesses longitudinal data from EA SPORTS FIFA (now EA SPORTS FC) to analyze the evolution of tactical trends, uncover the attributes that define an outstanding player and evaluate the accuracy of virtual market valuations. The findings aim to provide actionable insights for squad building and strategic development in contemporary football.

# 🎯 Purpose
- To analyze the evolution of modern football using EA SPORTS FIFA in-game data and data from Transfermarkt, by exploring tactical trends, player development, and market valuation logic.
- Analyzing tactical changes in modern football based on FIFA dataset from version 15 to 23 (2015 - 2023), through changes in player stats according to role, position and technical requirements.

# Outcome
A comprehensive analysis that uncovers modern tactical shifts, reveals factors behind great footballers, and highlights discrepancies between perceived and real-world player values. This can offer valuable insights for heah coach, managers and football analysts.

# Project Structure
- Part 1 - Tactical Shift Over Time
- Part 2 – The Making of a Great Player
- Part 3 - Market Pulse: Underrated vs Overrated


# 🧩 Research questions
- Which position has evolved the most in modern football?
- What attributes of positions have changed significantly over the years?
- Is there a shift in the tactics and playing style of football teams over time?
- What main attributes make a great player?
- What core attributes make a great player?
- What factors greatly affect a player's value?
- Is a player overrated or underrated?

# 🔎 Expectation insights
✅ Modern defenders need more versatile.

✅ Midfielders are becoming more all-round.

✅ Goalkeepers are probably the most changed position as they have to play with their feet more.
✅ Stats such as volleys, long shots, crossing have decreased, while vision, passing, reactions have increased sharply.
✅ Playing style has changed from simple - direct to controlled - well-coordinated.
✅ Excellent players often stand out in stats such as ball control, reactions, composure.
✅ Player value is strongly influenced by overall, age, reputation, skill moves and technical stats.
✅ Players who are mispriced can be detected by comparing predicted value with actual value.

# Tools and Technologies
## Tools
- Python (pandas, numpy, matplotlib, seaborn, scikit-learn...).
- Google Colab: using Python to load, process, clean, analyze data and build Machine Learning models and analyze features importance.
- Google Slices: create slices for presentation.

## Technologies
- Linear Regression
- Logistic Regression
- Random Forrest Regression

# 📁 Files
- `🎓_Graduation_Project.ipynb`: Complete Google Colab notebook with code, analysis, and visualizations
- `🎓_graduation_project.py`: Python version of the project (extracted from notebook)
- `charts/`: Folder for project visualizations (for embedding in README)
- `README.md`: 

# Data Sources
- Public dataset from Kaggle (FIFA 23 complete player dataset: [https://www.kaggle.com/datasets/stefanoleone992/fifa-23-complete-player-dataset?select=male_players+%28legacy%29.csv](https://www.kaggle.com/datasets/stefanoleone992/fifa-23-complete-player-dataset?select=male_players+%28legacy%29.csv))
- Public dataset from Kaggle (Football Data from Transfermarkt: [https://www.kaggle.com/datasets/davidcariboo/player-scores/data?select=players.csv](https://www.kaggle.com/datasets/davidcariboo/player-scores/data?select=players.csv))
- Public dataset from Kaggle (Countries by Continent: [https://www.kaggle.com/datasets/hserdaraltan/countries-by-continent?select=Countries+by+continents.csv](https://www.kaggle.com/datasets/hserdaraltan/countries-by-continent?select=Countries+by+continents.csv))

# 📊 Data Overview
|index|player\_id|player\_url|fifa\_version|fifa\_update|fifa\_update\_date|short\_name|long\_name|player\_positions|overall|potential|value\_eur|wage\_eur|age|dob|height\_cm|weight\_kg|league\_id|league\_name|league\_level|club\_team\_id|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|158023|/player/158023/lionel-messi/150002|15|2|2014-09-18|L\. Messi|Lionel Andrés Messi Cuccittini|CF|93|95|100500000\.0|550000\.0|27|1987-06-24|169|67|53\.0|La Liga|1\.0|241\.0|
|1|20801|/player/20801/c-ronaldo-dos-santos-aveiro/150002|15|2|2014-09-18|Cristiano Ronaldo|Cristiano Ronaldo dos Santos Aveiro|LW, LM|92|92|79000000\.0|375000\.0|29|1985-02-05|185|80|53\.0|La Liga|1\.0|243\.0|
|2|9014|/player/9014/arjen-robben/150002|15|2|2014-09-18|A\. Robben|Arjen Robben|RM, LM, RW|90|90|54500000\.0|275000\.0|30|1984-01-23|180|80|19\.0|Bundesliga|1\.0|21\.0|
|3|41236|/player/41236/zlatan-ibrahimovic/150002|15|2|2014-09-18|Z\. Ibrahimović|Zlatan Ibrahimović|ST|90|90|52500000\.0|275000\.0|32|1981-10-03|195|95|16\.0|Ligue 1|1\.0|73\.0|
|4|167495|/player/167495/manuel-neuer/150002|15|2|2014-09-18|M\. Neuer|Manuel Peter Neuer|GK|90|90|63500000\.0|300000\.0|28|1986-03-27|193|92|19\.0|Bundesliga|1\.0|21\.0|

## Description
- This dataset contains detailed information on 161,583 male players in FIFA 23, in the "Career Mode" game. The data includes personal information, skill attributes, financial valuation, playing position and many other characteristics related to in-game performance.
- Because the player attributes and stats in the dataset are based on detailed statistics from EA SPORTS based on real-life performance and take into account a wide range of real-life factors to determine player stats, this dataset is suitable for analytical purposes such as:
  - Player valuation
  - Classification by position, nationality, or skill
  - Tracking tactical trends
  - Detecting potential or underrated players

## 🧱 Data Structure
- Number of rows: 161,583 players
- Number of columns: 110 features

| **Group**              | **Description** |
|------------------------|-----------------|
| **Basic Information**  | `player_id`, `short_name`, `long_name`, `dob`, `age`, `height_cm`, `weight_kg`, `international_reputation` |
| **Club Information**   | `club_name`, `league_name`, `club_position`, `club_jersey_number`, `club_contract_valid_until_year` |
| **National Team Info** | `nationality_name`, `nation_position`, `nation_team_id` |
| **Footedness & Skills**| `preferred_foot`, `weak_foot`, `skill_moves`|
| **Financial Values**   | `value_eur`, `wage_eur`, `release_clause_eur` |
| **General Attributes** | `overall`, `potential`, `pace`, `shooting`, `passing`, `dribbling`, `defending`, `physic` |
| **Detailed Attributes**| Includes 35+ skill-related columns such as `attacking_finishing`, `movement_sprint_speed`, `power_shot_power`, `mentality_vision`, `defending_sliding_tackle`, `goalkeeping_reflexes`, etc. |

# Data Restrictions

# Data Cleaning

## FIFA 23 complete player dataset
- Remove unnessary columns
- Check data consistency
- Convert data type
- Rename columns like Transfermarkt dataset to set join key
- Drop duplicates

## Football Data from Transfermarkt
- Convert data type
- Check 'position' columns consistency
- Rename columns like FIFA dataset to set join key
- Drop N/A values in 'position' columns (~0.6%)
- Drop duplicates

***

- In the project we need to analyze by position, but in FIFA data this column is not suitable for the current analysis needs, so we will process it to merge with data from Transfermarkt, the steps are as follows:
  - Normalize the 'name' column in both datasets
  - Create a standardized join key (include name, date_of_birth and nationality_name).
  - Drop duplicates join key and merge both datasets
  - Mapping Transfermarkt position into 4 main groups
- Because in football the sets of stats for the 4 main position groups are different (for example, a goalkeeper cannot have a high shooting stat like a striker or a striker cannot defend as well as a defender), so we will fill N/A numeric columns by median in each position group (GK, DF, MF, FW).
- Drop N/A values and reset index
- Here is main dataset after cleaning:
```
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 68830 entries, 0 to 68829
Data columns (total 67 columns):
 #   Column                       Non-Null Count  Dtype         
---  ------                       --------------  -----         
 0   player_id                    68830 non-null  int64         
 1   fifa_version                 68830 non-null  category      
 2   short_name                   68830 non-null  object        
 3   long_name                    68830 non-null  object        
 4   player_positions             68830 non-null  object        
 5   overall                      68830 non-null  int64         
 6   potential                    68830 non-null  int64         
 7   value_eur                    68830 non-null  float64       
 8   wage_eur                     68830 non-null  float64       
 9   age                          68830 non-null  int64         
 10  date_of_birth                68830 non-null  datetime64[ns]
 11  height_cm                    68830 non-null  int64         
 12  weight_kg                    68830 non-null  int64         
 13  club_name                    68830 non-null  object        
 14  nationality_name             68830 non-null  object        
 15  preferred_foot               68830 non-null  category      
 16  weak_foot                    68830 non-null  int64         
 17  skill_moves                  68830 non-null  int64         
 18  international_reputation     68830 non-null  int64         
 19  work_rate                    68830 non-null  category      
 20  body_type                    68830 non-null  category      
 21  player_tags                  7179 non-null   object        
 22  player_traits                37459 non-null  object        
 23  pace                         68830 non-null  float64       
 24  shooting                     68830 non-null  float64       
 25  passing                      68830 non-null  float64       
 26  dribbling                    68830 non-null  float64       
 27  defending                    68830 non-null  float64       
 28  physic                       68830 non-null  float64       
 29  attacking_crossing           68830 non-null  float64       
 30  attacking_finishing          68830 non-null  float64       
 31  attacking_heading_accuracy   68830 non-null  float64       
 32  attacking_short_passing      68830 non-null  float64       
 33  attacking_volleys            68830 non-null  float64       
 34  skill_dribbling              68830 non-null  float64       
 35  skill_curve                  68830 non-null  float64       
 36  skill_fk_accuracy            68830 non-null  float64       
 37  skill_long_passing           68830 non-null  float64       
 38  skill_ball_control           68830 non-null  float64       
 39  movement_acceleration        68830 non-null  float64       
 40  movement_sprint_speed        68830 non-null  float64       
 41  movement_agility             68830 non-null  float64       
 42  movement_reactions           68830 non-null  float64       
 43  movement_balance             68830 non-null  float64       
 44  power_shot_power             68830 non-null  float64       
 45  power_jumping                68830 non-null  float64       
 46  power_stamina                68830 non-null  float64       
 47  power_strength               68830 non-null  float64       
 48  power_long_shots             68830 non-null  float64       
 49  mentality_aggression         68830 non-null  float64       
 50  mentality_interceptions      68830 non-null  float64       
 51  mentality_positioning        68830 non-null  float64       
 52  mentality_vision             68830 non-null  float64       
 53  mentality_penalties          68830 non-null  float64       
 54  mentality_composure          68830 non-null  float64       
 55  defending_marking_awareness  68830 non-null  float64       
 56  defending_standing_tackle    68830 non-null  float64       
 57  defending_sliding_tackle     68830 non-null  float64       
 58  goalkeeping_diving           68830 non-null  float64       
 59  goalkeeping_handling         68830 non-null  float64       
 60  goalkeeping_kicking          68830 non-null  float64       
 61  goalkeeping_positioning      68830 non-null  float64       
 62  goalkeeping_reflexes         68830 non-null  float64       
 63  name                         68830 non-null  object        
 64  join_key                     68830 non-null  object        
 65  position                     68830 non-null  string        
 66  position_group               68830 non-null  object        
dtypes: category(4), datetime64 , float64(42), int64(9), object(10), string(1)
memory usage: 33.3+ MB
```

# EXPLORATORY DATA ANALYSIS
## Dataset overview

|index|player\_id|fifa\_version|short\_name|long\_name|player\_positions|overall|potential|value\_eur|wage\_eur|age|date\_of\_birth|height\_cm|weight\_kg|club\_name|nationality\_name|preferred\_foot|weak\_foot|skill\_moves|international\_reputation|work\_rate|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|count|68830\.0|68830\.0|68830|68830|68830|68830\.0|68830\.0|68830\.0|68830\.0|68830\.0|68830|68830\.0|68830\.0|68830|68830|68830|68830\.0|68830\.0|68830\.0|68830|
|unique|NaN|9\.0|16845|17443|1324|NaN|NaN|NaN|NaN|NaN|NaN|NaN|NaN|1313|145|2|NaN|NaN|NaN|9|
|top|NaN|23\.0|Paulinho|Danny Ward|CB|NaN|NaN|NaN|NaN|NaN|NaN|NaN|NaN|nan|England|Right|NaN|NaN|NaN|Medium/Medium|
|freq|NaN|8017\.0|41|18|8773|NaN|NaN|NaN|NaN|NaN|NaN|NaN|NaN|571|6040|51690|NaN|NaN|NaN|35840|
|mean|208749\.0405927648|NaN|NaN|NaN|NaN|68\.54832195263693|73\.48827546128142|3798948\.612523609|17088\.55949440651|25\.182202527967455|1992-12-19 07:13:57\.995060480|182\.22573005956704|75\.98220252796746|NaN|NaN|NaN|2\.997297689960773|2\.4279383989539447|1\.206131047508354|NaN|
|min|2\.0|NaN|NaN|NaN|NaN|44\.0|49\.0|1000\.0|500\.0|16\.0|1970-01-17 00:00:00|158\.0|53\.0|NaN|NaN|NaN|1\.0|1\.0|1\.0|NaN|
|25%|192587\.0|NaN|NaN|NaN|NaN|64\.0|69\.0|575000\.0|3000\.0|22\.0|1989-06-07 00:00:00|178\.0|71\.0|NaN|NaN|NaN|3\.0|2\.0|1\.0|NaN|
|50%|212483\.0|NaN|NaN|NaN|NaN|68\.0|73\.0|1200000\.0|7000\.0|25\.0|1993-03-23 00:00:00|183\.0|76\.0|NaN|NaN|NaN|3\.0|2\.0|1\.0|NaN|
|75%|232671\.0|NaN|NaN|NaN|NaN|73\.0|77\.0|3300000\.0|20000\.0|28\.0|1996-10-03 00:00:00|187\.0|80\.0|NaN|NaN|NaN|3\.0|3\.0|1\.0|NaN|
|max|271815\.0|NaN|NaN|NaN|NaN|94\.0|95\.0|194000000\.0|575000\.0|44\.0|2005-09-23 00:00:00|208\.0|110\.0|NaN|NaN|NaN|5\.0|5\.0|5\.0|NaN|
|std|36651\.54724099746|NaN|NaN|NaN|NaN|6\.767823670221086|5\.88045296938514|8191432\.130305095|29255\.562871151258|4\.559804532531502|NaN|6\.68024431192149|7\.024546057214901|NaN|NaN|NaN|0\.681227083361879|0\.8032217527773016|0\.5195255186810177|NaN|

## Distribution by FIFA Version (Year)
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/NumofPlayersbyFFVersion.png)

The bar chart shows that the number of players with complete attribute data (i.e., no major missing values) is quite consistent across FIFA versions from 2015 to 2023, ranging from approximately **6,800 to over 8,000 players per year**. This indicates that the filtered dataset is **balanced and reliable**, with no specific year being over- or under-represented. Such consistency allows for trustworthy time-series analyses.

## Distribution by position groups
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/PlayerDistributionbyPositionGroup.png)

The bar chart shows the distribution of players by position group:
- **Defenders (DF)** are the most numerous, with over **22,000 players**, indicating a wide variety of defensive roles represented in the data.
- **Midfielders (MF)** and **Forwards (FW)** have a fairly balanced count (around **18,000–20,000**), offering enough representation for detailed role-based analysis.
- **Goalkeepers (GK)** have the smallest count (around **7,000**), which is expected given that teams typically have fewer goalkeepers.
➡️ Overall, the player distribution is **balanced and sufficient**, allowing for meaningful position-based comparisons in subsequent analyses. In addition, if we look more closely, in a relative way we can see that based on the number of players in each position, the most popular formation used is 4-3-3 (4 defenders - 3 midfielders - 3 forwards), quite interesting, right?

## Distribution of main attributes
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/DistributionbyMainAttrs.png)

**Insights:**
- **Pace:** slight right-skewed distribution, with most players having pace between **60–80**, peaking around **75–80**. Very fast players (90+) are rare.
- **Shooting:** highly right-skewed, most players have average shooting in the **30–70** range. Exceptional shooters (80+) are relatively few.
- **Passing:** almost normal distribution centered around **55–65**, indicating a balanced spread. Top-tier passers (above 80) are rare.
- **Dribbling:** concentrated around **60–70** with slight variation on both ends, reflecting consistent dribbling ability across player groups.
- **Defending:** bimodal shape, one peak at **30–40** (attackers, midfielders) and another at **60–70** (defensive roles), reflecting a clear divide between attack and defense.
- **Physic:** widely distributed with most values in the **60–80** range, peaking at **75–80**, showing physicality is a generally well-represented attribute.

## Correlation matrix of Main Attributes
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/CorrMatrxofMainAttrs.png)

**Insights:**
**🔍 Strong Correlations:**
- **Passing – Dribbling:** 0.82 → Players who are good passers often excel at dribbling. This makes sense for playmakers (CAM, CM).
- **Shooting – Dribbling:** 0.72 → Players who shoot well also tend to dribble well — commonly seen in technical forwards (ST, CF, wingers like Messi, Neymar, Mbappé).
- **Shooting – Passing:** 0.64 → Players with good shooting ability often have decent passing skills — typical for all-rounded attacking midfielders.

**📉 Strong Negative Correlations:**
- **Shooting – Defending:** -0.50 → Attacking players (good shooters) usually aren't strong defenders — clearly reflecting the difference between strikers and defenders.
- **Dribbling – Defending:** -0.24 → Players good at dribbling tend to be weaker at defending — common for offensive roles.

**📌 Other Notable Relationships:**
- **Pace – Dribbling:** 0.51 → Fast players often dribble well — usually wide players and wingers.
- **Defending – Physic:** 0.58 → Defenders and defensive midfielders usually possess strong physical attributes (CB, CDM).
- **Pace – Defending:** -0.24 → Good defenders aren't necessarily fast (with exceptions like modern fullbacks: Walker, Hakimi, etc).

**🧠 Insight Summary:** Players can generally be grouped into two major clusters:
- **Technical – Attacking Group:** Dribbling, Passing, Shooting, Pace (strong positive correlation within).
- **Physical – Defensive Group:** Defending, Physic (positive correlation within, negatively correlated with technical attributes).

This correlation heatmap is useful for clustering player roles or building classification models based on player positions.

## Mean of main attributes by year and position groups
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/MeanofMainAttrsbyYear%26Pos.png)

**Insights:**
- **Pace:** The average speed of forwards (FW) and defenders (DF) remains relatively stable over the years, while midfielders (MF) have seen a slight decline.
- **Shooting:** Forwards consistently have the highest shooting statistics with a slight upward trend, midfielders also have a slight upward trend while defenders are almost unchanged
- **Passing:** Midfielders (MF) lead the way in passing and show a steady increase over time. Other positional groups also show slight improvements.
- **Dribbling:** Dribbling remains high and stable for both forwards and midfielders. However, defenders show noticeable improvement over time, reflecting the increasing importance of ball control.
- **Defending:** Defenders maintain high and consistent defensive stats. Midfielders show a gradual increase, showing more all-round responsibility. Forwards also improve slightly despite their low values.
- **Physic:** Midfielders show slight improvement, while defenders and forwards remain largely unchanged.

# Boxplot of main attributes by year to check outliers
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/BoxplotMainAttrsbyyear.png)

**Insights:**
- **Stable distribution:** The Pace, Shooting, Passing, Dribbling, Defending and Physic indicators all have a fairly stable distribution across FIFA versions. The Median and IQR do not change significantly, indicating that the player rating structure is maintained consistently.
- **Outliers:** There are many outliers, mainly players with very low ratings. This reflects the diversity of player quality in the game.
- **Differences between indicators:** Pace, Dribbling and Physic tend to be higher than Passing, Shooting and Defending, which are often concentrated at the average/low level.

> The EDA results show that the data has a clear structure, is stable over time and has a clear stratification between indicators. We don't need to remove outliers because these are all important data points that support the subsequent analysis well.

# Part 1 - Tactical Shift Over Time
## Which position has evolved the most in modern football?
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/MainAttrsbyPosOvertime.png)

Analyzing the evolution of average player attributes by position across FIFA editions provides an interesting lens for observing how tactical trends in contemporary football can be modeled and emphasized in-game. The charts show:
- **Core roles remain but with adjustments:** While the core positions remain specialised (Defensive/Physical Defenders, Passing/Dribbling Midfielders, Speed/Shooting Forwards), the change in average attributes shows an adaptation to modern tactics.
- **Increased Defensive Ability of Midfielders:** The most notable is the significant increase in the average Defensive attribute of the Midfielder (MF) group across editions. This clearly reflects the tactical trends in contemporary football, where midfielders are increasingly asked to participate in defensive work, from pressing high, covering the defence to recovering the ball in the midfield. Tactical systems such as Gegenpressing or formations with a mobile, versatile central midfielder are becoming increasingly popular.
- **The enduring importance of pace:** The pace attribute is quite stable in defenders and forwards. This emphasizes that, despite the increasing complexity of tactics, pace remains an extremely important factor in modern football, necessary for quick transitions, individual breakthroughs, or pressing and covering. However, in midfielders, there is a slight decrease, indicating the role of keeping the rhythm, controlling or regulating the tempo of the match.
- **A slight trend towards more well-rounded players:** The slight increase in some non-positional attributes (e.g. Passing/Dribbling in DF, Shooting/Physic in MF) may imply that modern football requires players in all positions to have a more diverse skill base to contribute to multiple aspects of the game, in line with tactics that emphasize versatility and positional interchangeability.
- **Traditional Strengths Remain Priorities:** Despite a slight ‘versatility’, the core attributes that characterize each position remain the ones with the highest and most consistent average scores. This suggests that regardless of tactical changes, having players who excel in the core skills appropriate to their position of expertise remains the key to success.

> **In summary, data from FIFA suggests that the most notable tactical change reflected is the increased role and defensive demands on midfielders, alongside the continued importance of pace and the (slight) demand for greater versatility from players in all positions.**

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/GkAttrsOvertime.png)

- Footwork stats such as short passing, long passing have increased slightly over the years, especially vision has increased significantly, reflecting the need for goalkeepers to participate more in situations of developing the ball from the back line, and can play the role of a sweeper goalkeeper.
- Traditional stats such as diving, reflexes, positioning... remain stable over the years.
> **Modern goalkeepers must be good at both technical skills and coordination, becoming the "first initiator of attack".**

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/DFAttrsOvertime.png)

**Modern defenders are significantly improving their ability to play with their feet:**
- Stats such as short passing, ball control, dribbling, long passing, vision have all increased steadily over the years.
- On the contrary, skills such as long shots and finishing have increased slowly, remained the same or decreased slightly, showing that the goal-scoring role of defenders has not changed much.
> **The trend of ball-playing defenders is becoming more and more obvious, they not only defend but also participate in build-up play, distributing the ball from the back line.**

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/MFAttrsOvertime.png)

**Midfielders continue to be at the heart of tactics with consistent and consistent improvements in both:**
- Tactical thinking: positioning, vision
- Ball control & passing skills: short passing, long passing, dribbling, ball control
- Defensive ability: standing tackle, sliding tackle, marking awareness – increased sharply, especially in the period 2019–2023.
> **Shows the emergence of complete midfielders – both offensive and defensive, and controlling the tempo of the match.**

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/FWAttrsOvertime.png)
**Forwards in this period also had changes in their playing style:**
- Slight increase in short passing and vision skills, showing the role of supporting attack coordination and connecting with the lines is increasingly clear.
- Defensive indicators increased steadily and continuously from 2016 - 2023 (standing tackle, sliding tackle), especially marking awareness increased sharply from 2018 - 2019, reflecting the trend of strikers having to actively participate in high pressing/defending from a distance.
> **Forwards in modern football are no longer "poachers" who just wait for the ball but are also the first link in the defensive system.**
> 
**Conclusion**
> **In modern football, all positions have undergone significant evolution to adapt to increasingly complex tactical requirements and a higher pace of play. However, in terms of the ability to change and expand roles beyond traditional definitions, it can be said that the Goalkeeper (GK) and Defender (especially the full-back) are the two positions with the most obvious and revolutionary "evolution".**

## **What attributes of positions have changed significantly over the years?**
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/MeanYearlyChangeinMainAttrs.png)

- Dribbling and Defending are the two most changed attributes
 - Defender (DF): Dribbling has increased the most, followed by Passing
➤ Defenders today need individual technique and the ability to deploy the ball from the back, not just pure defense.
 - Midfielder (MF): Defending has increased very strongly, surpassing Shooting and Dribbling
➤ Reflecting the trend of comprehensive midfielders: both organizing the play and participating in pressing, intercepting, and supporting defenders.
 - Forward (FW): Increasing steadily in many attributes, but Passing and Defending are notable
➤ Modern strikers not only know how to score goals but also participate in supporting pressing, building play, they are the first line of defense when the home team does not have the ball.

- Pace (speed) decreased significantly in midfielders, increased at least in the other 2 groups
➤ Shows that speed is no longer the decisive factor — instead, tactical thinking, coordination and movement without the ball are.

**📌 Conclusion**
- The most significant changes over the years are Dribbling (especially in defenders), Defending (clearly in midfielders), and Passing (in defenders and forwards).
- The general trend is that modern players need to be more versatile, supporting the overall play instead of just doing well in individual roles.
- Speed ​​(Pace) is no longer a priority as before.

## **Is there a shift in the tactics and playing style of football teams over time?**

> ***Here we do not analyze the tactics of a specific team because the tactics of each team or a specific group of teams are different and there are many teams, we only rely on the changes in the core attributes of the players to see the overall picture of the typical playing styles of the teams.***

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/Top10Acs%26DescinCoreAttrsOvertime.png)

From this chart we can see that there has been a clear shift in the tactical meta of football during this period:
- **Volleys** have dropped the most, showing that **live shots that score goals are no longer popular** and that there are no players with good volleying ability during this period.
- **Long shots** have dropped the second most, showing that teams are **no longer relying on long-range shots** to score goals, but are shifting to **more methodical and calculated combinations.**
- **Crossing and heading accuracy are both in the top 10 of the biggest declines**, showing that teams are **no longer favoring the Anglo-Saxon style of overlapping, cross-heading or corner kicks** to score goals, which often relies heavily on **high-ball situations**.
- The indicators such as **vision, long passing, short passing, reactions and marking awareness** are all in the top 10 with the strongest increase, which reflects the **synchronous pressing and escaping pressing style from many lines that requires the ability to control, pass the ball, catch people and react quickly**, a hallmark of in modern football.
- The **goalkeeper's index** sets have also increased significantly over the years, showing that **goalkeepers must be more and more comprehensive and excellent** because in modern football, a save is no different from a goal, especially in big matches.

**Conclusion**
> **Football has always been in constant motion and change throughout its history, with increasingly high and complex tactical requirements, players also need to change to adapt, they are no longer constrained in traditional roles but are increasingly flexible and versatile.**

# **Part 2 – The Making of a Great Player**
> ***This study focuses on in-game attributes only, not real-life performance metrics.***
## **What main attributes make a great player?**
> ***Analysis is based on player attributes in EA FIFA game data, which reflect a gamified interpretation of real-life performance.***

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/MainAttrsbyPos(5%25vsOthrs).png)

- **Goalkeepers (GK):** Top 5% excel in **Diving, Handling, Positioning, Reflexes, Reactions.**
> A top goalkeeper cannot lack any GK skills – from reflexes, positioning to ball handling. **Reactions** play a key role in dealing with dangerous situations.
- **Defenders (DF):** Top 5% have superior **Defending**, along with significantly higher **Passing, Dribbling, Shooting.**
> Modern defenders must not only defend well but also **handle the ball, pass the ball and support the attack.** Pace does not need to be too high if they can read the situation well.
- **Midfielders (MF):** The biggest difference lies in **Passing, Dribbling**, followed by Shooting.
> A great midfielder is someone who **holds the ball well, passes creatively and has the ability to finish the situation.** They dictate play and create chances for their teammates and themselves.
- **Forwards (FW):**
> Top 10% excel in **Shooting, Dribbling, Passing** – the ultimate attacking skill set.
> Legendary forwards are those who **can decide the game with their individual skill** and scoring ability.

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/GkAttrsDistribution(5%25vsOthrs).png)

- In the **goalkeeper (GK)** group, the players in the **top 5%** have a **well-rounded and consistent skill set.** They are not just excellent in a few stats, but are **equally good in all the mandatory aspects** of the GK position – from **reflexes, positioning, kicking** to **reactions.**
- The Top 5% group has a shorter box, meaning low variability and few outliers, for example goalkeeping_reflexes and movement_reactions of the Top 5% group are both concentrated around 80–88. This implies that **Legend GKs are consistent**, maintaining a **high level of performance regardless of temporary fluctuations** in form.
- Notably, **reactions** and **reflexes** are the attributes that show the biggest gap between the Legend group and the rest – this is related to the ability to **make spectacular saves**, which is **what makes a great goalkeeper.**

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/MainAttrsbyPos(5%25vsOthrs).png)

- **Overall:**
 - Across all metrics and roles, the **Top 5% are clearly superior** to the rest.
 - Not only do they have higher median values, but the **Top 5% are also more consistent** (shorter boxes, fewer outliers), showing that they are well-rounded and consistent players.
- **Defenders (DF):**
 - **Defending** is the most prominent strength, with the Top 5% having a median >80 compared to the rest of the group around ~65.
 - **Dribbling, Passing and Physic** also stand out, showing that today's top defenders are not only defensive but also participate in building play and competing strongly.
 - There is also a difference in **Pace** - speed is the factor that distinguishes normal defenders from top defenders.
>✅ *A Great Defender is not only good at defending but also has good speed, stamina and ball handling technique.*
- **Midfielders (MF):**
 - **Passing and Dribbling** are the two most distinguishing factors – Top 5% have excellent passing and dribbling abilities (~80 and above).
 - **Shooting, Defending and Physic** are also slightly better, showing that they are not only playmakers but can also defend or score directly when needed.
 - The difference in **pace** is less, a good midfielder does not need to be too fast.
> ✅ *A Great Midfielder is a versatile player, capable of controlling the game with technique and physicality, while contributing to both attack and defense.*
- **Forwards (FW):**
 - **Shooting** is the most distinguishing factor – Top 5% have median >80, while the other group ~65.
 - **Dribbling and Passing** are also clearly superior, showing that ball handling and passing skills are core factors.
 - **Pace and Physic** are also better – a great forward is not only a goal scorer but also has good physicality and speed.
> ✅ *A Great Forward is a player with excellent scoring ability, good dribbling and coordination, and has the speed to break through to create breakthroughs.*

**Conclusion**
> *In every position, the Top 5% players not only excel in a specific stat, but also have a **comprehensive and consistent performance**. The biggest difference between them and the rest lies in the core skills of each position – for example: Reflexes & Reactions for Goalkeepers, Passing & Dribbling for Midfielders or Shooting & Dribbing for Forwards. It is this **consistent excellence** that is the foundation for creating a great player in football.*

## **What core attributes make a great player?**
> ***Based on FIFA player attributes, what are the core features that distinguish top 5% players from the rest?***
> 
- To analyze this we will use a logistic regression model to distinguish the great players (top 5%) from the rest.
- After determining the core attributes, we will train the model and evaluate it based on the classification report and the ROC Curve graph.

![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/ClassRp.jpg)
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/ROCCurve-LR.png)

Based on classification report and ROC Curve:
- Overall performance is very good: **Accuracy 97%**, **ROC AUC 0.99** → the model distinguishes very well between top 5% players and the rest.
- The model achieves: **Precision = 0.82** and **Recall = 0.71** for class 1 (top 5% excellent players), meaning the model correctly detects many "great" players, **limiting false positives relatively well.**
- Note the imbalance of the data set: Class 1 only accounts for **about 6%** of the data set, this explains why Recall class 1 = 0.71, lower than class 0. However, **high precision** for class 1 is a positive point.

> ✅ Logistic Regression Model Easy to understand, simple, shows very good efficiency in classifying "great players". Used to **determine the core attributes that make a great player** (via coefficients).

- Next, we will analyze features importance via model and see which 15 features have the most impact.
![Alt text](https://github.com/hoangbui93/Decoding-Modern-Football-Tactics-Talent-and-Transfer-Value/blob/main/pics/LRCoffs-Top15Attrs.png)

"What core attributes make a great player?"
The most important attributes (by coefficient):
- **Reactions (↑)** - Highest coefficient:
 - **The ability to react to second-ball situations in the match** is the most important factor that helps distinguish the top 5% players.
 - "Great" players often react quickly to situations, making the difference in important moments.
- **Positioning (↓)** - Highest negative coefficient. Although it seems paradoxical, the negative coefficient here **does not mean that this index is bad**, but it can be due to:
 - This index is often high in forwards, not common in midfielders or defenders
 - Or because this variable is negatively correlated with being in the top 5% because the model differentiates by position.
- **Ball control (↑)** and **short passing (↑)**
→ Technical ball handling, control and short passing skills are important for top players.
- **Reflexes (↑)** and other GK stats → Suggests that the top 5% also **include excellent goalkeepers**, who are considered half of the team.
- **Sprint speed (↑)** and **heading accuracy (↑)** → Sprint speed and heading ability – typical skills of high-class forwards.

> 📌 The best players usually possess:
- **Quick reactions**
- **Good ball control and short passing**
- **High speed**
- **Role-specific skills – such as reflexes (GK), short passing (MF) or heading accuracy (FW)**

**Conclusion**
> ***Apart from the goalkeeper position, which is a very special position in football, we can see that the most core attributes of a great player are all in the stats that serve the ability to attack and find goals. This means that a midfielder or forward who plays well will always have an advantage over a defender in the race for individual titles, which is absolutely true in modern football.***

# **Part 3 - Market Pulse: Underrated vs Overrated**



























# 🔗 Colab Notebook
👉 [Open in Google Colab](https://colab.research.google.com/drive/1w2ujPKMu_N34T_5yPHjzB6c2SmDKoO1i?usp=sharing)

# ✨ Author
Hoang Bui - Data Analyst
