
2026-06-19 11:56:36 | INFO | P06 | === RUN START ===
2026-06-19 11:56:36 | INFO | P06 | project=P06
2026-06-19 11:56:36 | INFO | P06 | repo_dir=datafun-06-applied
2026-06-19 11:56:36 | INFO | P06 | python=3.14.5
2026-06-19 11:56:36 | INFO | P06 | os=Windows 11
2026-06-19 11:56:36 | INFO | P06 | shell=powershell
2026-06-19 11:56:36 | INFO | P06 | cwd=.
2026-06-19 11:56:36 | INFO | P06 | github_actions=False
2026-06-19 11:56:36 | INFO | P06 | === RUN START ===
2026-06-19 11:56:36 | INFO | P06 | project=EDA
2026-06-19 11:56:36 | INFO | P06 | repo_dir=datafun-06-applied
2026-06-19 11:56:36 | INFO | P06 | python=3.14.5
2026-06-19 11:56:36 | INFO | P06 | os=Windows 11
2026-06-19 11:56:36 | INFO | P06 | shell=powershell
2026-06-19 11:56:36 | INFO | P06 | cwd=.
2026-06-19 11:56:36 | INFO | P06 | github_actions=False
2026-06-19 11:56:36 | INFO | P06 | ========================
2026-06-19 11:56:36 | INFO | P06 | START main()
2026-06-19 11:56:36 | INFO | P06 | ========================
2026-06-19 11:56:36 | INFO | P06 | --- Section 2: Load dataset: netflix_titles ---
2026-06-19 11:56:36 | INFO | P06 | Loading dataset: netflix_titles
2026-06-19 11:56:36 | INFO | P06 | Loaded: 8807 rows, 14 columns
2026-06-19 11:56:36 | INFO | P06 | --- Section 3: Inspect shape and basic structure ---
2026-06-19 11:56:36 | INFO | P06 | Previewing first few rows of the dataset
2026-06-19 11:56:36 | DEBUG | P06 | 
  show_id     type                  title         director                                               cast  \
0      s1    Movie   Dick Johnson Is Dead  Kirsten Johnson                                                NaN   
1      s2  TV Show          Blood & Water              NaN  Ama Qamata, Khosi Ngema, Gail Mabalane, Thaban...   
2      s3  TV Show              Ganglands  Julien Leclercq  Sami Bouajila, Tracy Gotoas, Samuel Jouy, Nabi...   
3      s4  TV Show  Jailbirds New Orleans              NaN                                                NaN   
4      s5  TV Show           Kota Factory              NaN  Mayur More, Jitendra Kumar, Ranjan Raj, Alam K...   

         country date_added  release_year rating   duration                                          listed_in  \
0  United States 2021-09-25          2020  PG-13     90 min                                      Documentaries   
1   South Africa 2021-09-24          2021  TV-MA  2 Seasons    International TV Shows, TV Dramas, TV Mysteries   
2            NaN 2021-09-24          2021  TV-MA   1 Season  Crime TV Shows, International TV Shows, TV Act...   
3            NaN 2021-09-24          2021  TV-MA   1 Season                             Docuseries, Reality TV   
4          India 2021-09-24          2021  TV-MA  2 Seasons  International TV Shows, Romantic TV Shows, TV ...   

                                         description  duration_minutes  year_added  
0  As her father nears the end of his life, filmm...              90.0      2021.0  
1  After crossing paths at a party, a Cape Town t...               2.0      2021.0  
2  To protect his family from a powerful drug lor...               1.0      2021.0  
3  Feuds, flirtations and toilet talk go down amo...               1.0      2021.0  
4  In a city of coaching centers known to train I...               2.0      2021.0  
2026-06-19 11:56:36 | INFO | P06 | Column names
2026-06-19 11:56:36 | DEBUG | P06 | ['show_id', 'type', 'title', 'director', 'cast', 'country', 'date_added', 'release_year', 'rating', 'duration', 'listed_in', 'description', 'duration_minutes', 'year_added']
2026-06-19 11:56:36 | INFO | P06 | DataFrame info (types and non-null counts)
<class 'pandas.DataFrame'>
RangeIndex: 8807 entries, 0 to 8806
Data columns (total 14 columns):
 #   Column            Non-Null Count  Dtype         
---  ------            --------------  -----         
 0   show_id           8807 non-null   str           
 1   type              8807 non-null   str           
 2   title             8807 non-null   str           
 3   director          6173 non-null   str           
 4   cast              7982 non-null   str           
 5   country           7976 non-null   str           
 6   date_added        8709 non-null   datetime64[us]
 7   release_year      8807 non-null   int64         
 8   rating            8803 non-null   str           
 9   duration          8804 non-null   str           
 10  listed_in         8807 non-null   str           
 11  description       8807 non-null   str           
 12  duration_minutes  8804 non-null   float64       
 13  year_added        8709 non-null   float64       
dtypes: datetime64[us](1), float64(2), int64(1), str(10)
memory usage: 963.4 KB
2026-06-19 11:56:36 | INFO | P06 | Dataset shape: 8807 rows, 14 columns
2026-06-19 11:56:36 | INFO | P06 | --- Section 4: Create Data Dictionary and Check Data Quality ---
2026-06-19 11:56:36 | INFO | P06 | Building starter data dictionary
2026-06-19 11:56:36 | DEBUG | P06 | 
              column           dtype  missing_count  missing_pct
0            show_id             str              0         0.00
1               type             str              0         0.00
2              title             str              0         0.00
3           director             str           2634        29.91
4               cast             str            825         9.37
5            country             str            831         9.44
6         date_added  datetime64[us]             98         1.11
7       release_year           int64              0         0.00
8             rating             str              4         0.05
9           duration             str              3         0.03
10         listed_in             str              0         0.00
11       description             str              0         0.00
12  duration_minutes         float64              3         0.03
13        year_added         float64             98         1.11
2026-06-19 11:56:36 | INFO | P06 | Missing values per column:
2026-06-19 11:56:36 | INFO | P06 | 
show_id                0
type                   0
title                  0
director            2634
cast                 825
country              831
date_added            98
release_year           0
rating                 4
duration               3
listed_in              0
description            0
duration_minutes       3
year_added            98
dtype: int64
2026-06-19 11:56:36 | INFO | P06 | Checking missing values per column
2026-06-19 11:56:36 | DEBUG | P06 | 
director            2634
country              831
cast                 825
date_added            98
year_added            98
rating                 4
duration_minutes       3
duration               3
show_id                0
type                   0
title                  0
release_year           0
description            0
listed_in              0
dtype: int64
2026-06-19 11:56:36 | INFO | P06 | Duplicate rows detected: 0
2026-06-19 11:56:36 | INFO | P06 | Call describe() for numeric columns
2026-06-19 11:56:36 | DEBUG | P06 | 
       release_year  duration_minutes   year_added
count   8807.000000       8804.000000  8709.000000
mean    2014.180198         69.846888  2018.887932
std        8.819312         50.814828     1.567961
min     1925.000000          1.000000  2008.000000
25%     2013.000000          2.000000  2018.000000
50%     2017.000000         88.000000  2019.000000
75%     2019.000000        106.000000  2020.000000
max     2021.000000        312.000000  2021.000000

2026-06-19 11:56:36 | INFO | P06 | --- Section 5: Create a cleaned view for EDA ---
2026-06-19 11:56:36 | INFO | P06 | Creating cleaned view for EDA (dropping rows with key missing values)
2026-06-19 11:56:36 | DEBUG | P06 | Columns required to be non-missing: ['release_year', 'duration_minutes', 'year_added', 'type']
2026-06-19 11:56:36 | INFO | P06 | Original rows: 8807
2026-06-19 11:56:36 | INFO | P06 | Clean rows:    8706
2026-06-19 11:56:36 | INFO | P06 | Rows dropped:  101
2026-06-19 11:56:36 | INFO | P06 | --- Section 6: Descriptive statistics for numeric columns ---
2026-06-19 11:56:36 | INFO | P06 | --------------- Manual statistics ---------------
2026-06-19 11:56:36 | DEBUG | P06 | duration_minutes Statistics (using numpy):
2026-06-19 11:56:36 | DEBUG | P06 |   Mean: 70.59
2026-06-19 11:56:36 | DEBUG | P06 |   Std Dev: 50.61
2026-06-19 11:56:36 | DEBUG | P06 |   Min: 1.00
2026-06-19 11:56:36 | DEBUG | P06 |   Max: 312.00
2026-06-19 11:56:36 | DEBUG | P06 |   Range: 311.00
2026-06-19 11:56:36 | INFO | P06 | --------------- Using pandas describe() method ---------------
2026-06-19 11:56:36 | INFO | P06 | Computing overall descriptive statistics
2026-06-19 11:56:36 | DEBUG | P06 | 
                   count         mean        std     min     25%     50%     75%     max
release_year      8706.0  2014.197105   8.827570  1925.0  2013.0  2017.0  2019.0  2021.0
duration_minutes  8706.0    70.590627  50.610750     1.0     3.0    89.0   106.0   312.0
year_added        8706.0  2018.888812   1.567489  2008.0  2018.0  2019.0  2020.0  2021.0
2026-06-19 11:56:36 | INFO | P06 | --------------- Using pandas groupby() and agg() ---------------
2026-06-19 11:56:36 | INFO | P06 | Computing descriptive statistics by group
2026-06-19 11:56:36 | DEBUG | P06 | 
        release_year                                   duration_minutes                                   year_added  \
               count         mean      std   min   max            count       mean        std  min    max      count   
type                                                                                                                   
Movie           6128  2013.121084  9.68030  1942  2021             6128  99.577187  28.290593  3.0  312.0       6128   
TV Show         2578  2016.754849  5.57988  1925  2021             2578   1.688518   1.485263  1.0   17.0       2578   

                                                
                mean       std     min     max  
type                                            
Movie    2018.850522  1.561276  2008.0  2021.0  
TV Show  2018.979829  1.578738  2008.0  2021.0  
2026-06-19 11:56:36 | INFO | P06 | 
Stacked view - easier to read in logs:
2026-06-19 11:56:36 | DEBUG | P06 | 
                          count         mean        std     min     max
type                                                                   
Movie   release_year       6128  2013.121084   9.680300  1942.0  2021.0
        duration_minutes   6128    99.577187  28.290593     3.0   312.0
        year_added         6128  2018.850522   1.561276  2008.0  2021.0
TV Show release_year       2578  2016.754849   5.579880  1925.0  2021.0
        duration_minutes   2578     1.688518   1.485263     1.0    17.0
        year_added         2578  2018.979829   1.578738  2008.0  2021.0
2026-06-19 11:56:36 | INFO | P06 | --- Section 7: Correlation matrix for numeric columns ---
2026-06-19 11:56:36 | INFO | P06 | Computing correlation matrix for numeric columns
2026-06-19 11:56:36 | INFO | P06 | 
Correlation matrix:
2026-06-19 11:56:36 | DEBUG | P06 | 
                  release_year  duration_minutes  year_added
release_year           1.00000         -0.255090    0.110490
duration_minutes      -0.25509          1.000000    0.016436
year_added             0.11049          0.016436    1.000000
2026-06-19 11:56:36 | INFO | P06 | ---------Visualize Correlation Matrix as a Heatmap---------------
2026-06-19 11:56:37 | INFO | P06 | 
CUSTOM: Update these notes and use Markdown cells to narrate and tell the story as you explore. For example:

Interpretation:

 - Values close to 1 (dark red) = strong positive correlation (both increase together)
 - Values close to -1 (dark blue) = strong negative correlation (one increases, other decreases)
 - Values close to 0 (white) = little or no linear relationship
 - The diagonal is always 1 (each variable correlates perfectly with itself)

From this heatmap, we can see how release year,
duration, and year added are related.

2026-06-19 11:56:37 | INFO | P06 | --- Section 8: Charts ---
2026-06-19 11:56:37 | INFO | P06 | ---- Creating Scatter Plot to see Relationships ------
2026-06-19 11:56:37 | INFO | P06 | ----   Use clean dataframe ---------------------------
2026-06-19 11:56:37 | INFO | P06 | ----   Set x to Release Year -----------------------
2026-06-19 11:56:37 | INFO | P06 | ----   Set y to Duration (Minutes) --------------------------
2026-06-19 11:56:37 | INFO | P06 | ----   Set the hue (color mapping) to the group column --
2026-06-19 11:56:37 | INFO | P06 | ------ Creating Box Plot to see Distribution: ---------
2026-06-19 11:56:37 | INFO | P06 | ------   Use clean dataframe --------------------------
2026-06-19 11:56:37 | INFO | P06 | ------   Set x to the group column --------------------
2026-06-19 11:56:37 | INFO | P06 | ------   Set y to Duration (Minutes) ----------------------
2026-06-19 11:56:37 | INFO | P06 | --- Section 9: Summary and next steps ---
2026-06-19 11:56:37 | INFO | P06 | ========================
2026-06-19 11:56:37 | INFO | P06 | SUMMARY
2026-06-19 11:56:37 | INFO | P06 | ========================
2026-06-19 11:56:37 | INFO | P06 | Dataset: netflix_titles
2026-06-19 11:56:37 | INFO | P06 | Original rows: 8807
2026-06-19 11:56:37 | INFO | P06 | Clean rows:    8706
2026-06-19 11:56:37 | INFO | P06 | Groups found in type: ['Movie', 'TV Show']
2026-06-19 11:56:37 | INFO | P06 | ======================
2026-06-19 11:56:37 | INFO | P06 | Review the results. 
2026-06-19 11:56:37 | INFO | P06 | Determine the strongest correlations. 
2026-06-19 11:56:37 | INFO | P06 | ======================
2026-06-19 11:56:37 | INFO | P06 | Look for interesting patterns in the charts. 
2026-06-19 11:56:37 | INFO | P06 | Repeat the process, exploring additional angles.
2026-06-19 11:56:37 | INFO | P06 | After finding interesting insights, conclude your analysis.
2026-06-19 11:56:37 | INFO | P06 | ======================
2026-06-19 11:56:37 | INFO | P06 | Include instructions and specifics in your README.md file.
2026-06-19 11:56:37 | INFO | P06 | Write up your narrative on your docs/index.md file.
2026-06-19 11:56:37 | INFO | P06 | Include your next step suggestions for further analysis or modeling.
2026-06-19 11:56:37 | INFO | P06 | ======================
2026-06-19 11:56:37 | INFO | P06 | ----- in a script, call plt.show() once at the end to display all charts -----
2026-06-19 11:56:37 | INFO | P06 | ----- in a script, close the chart windows (with the close button) to continue  -----
2026-06-19 11:56:43 | INFO | P06 | EDA workflow complete
2026-06-19 11:56:43 | INFO | P06 | IMPORTANT: This script creates chart windows.
2026-06-19 11:56:43 | INFO | P06 | Close any chart windows and terminate this process with CTRL+c as needed.
2026-06-19 11:56:43 | INFO | P06 | ========================
2026-06-19 11:56:43 | INFO | P06 | Executed successfully!
2026-06-19 11:56:43 | INFO | P06 | ========================
