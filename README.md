# LoL Worlds 2022 Dashboard
29/3/2023\
An interactive dashboard based on a dataset taken from the League of Legends Worlds 2022 Championship.  
_*slight knowledge on League of Legends may be needed_

**Reason for project:** to practice and sharpen data visualization skills  
**Goal:** to create an interactive dashboard that displays champion pick / ban rate, and winrates in Worlds 2022  
**Dataset source:** https://gol.gg/champion/list/season-S12/split-ALL/tournament-World%20Championship%202022/  

**The interactive dashboard displays the following:**  
- a stacked column chart showing game presence by champion (%)  
- a stacked column chart showing winrate by champion (%)  
- a slicer to select champions  
- multiple cards each showing champion selected, ban rate, pick rate, game presence, games won, games lost, and overall winrate  

**Steps applied to the dataset:**  
1) rename everything in "Champion" column as the dataset's values were doubled
    - exp: Aatrox Aatrox -> Aatrox  

2) removed multiple columns as they are unrelated to Goal (see line 7), such as CS/M, DP/M, GP/M, and etc.  

3) removed champions that had 0% presence (not picked or banned) from the dataset
    - changed data in column "presence" from 0 to null in power query editor
    - excluded values with null from showing  

4) added a new custom column called "games appeared in"
    - numerical form of column "Presence" as it is just a percentage  

5) changed value of "Presence" & "Winrate" from numerical to percentages
    - personally, I think having a percentage instead of a decimal is better for visualization  

**Reasoning for choice of visualization tools:**  
Stacked column charts: values are stacked closer together when compared to a simple bar chart, making comparison easier when no singular values are selected  

Slicer: form of selection / interactive tool to make dashboard more interesting as different data can be seen when different values are picked in the slicer  

Card: clean and neat way of displaying data that can change according to value selected in slicer  

**What can be improved**  
1) (drill down) reasoning for why certain champions had higher winrates despite having low game presence
    - taking out anomalies (champions that are picked / banned <5 times in total), there are certain champions with extremely high winrates
    - factors such as match up, build, team composition, team playstyle, player playstyle are not taken into account
    - off-meta / one-trick picks such as Heimerdinger & Kindred
    - more data that are not provided may be needed to drill down  

2) Better visualization tools / design, factors such as:
    - consider importing
    - colour scheme
    - positioning of visualization tools  


