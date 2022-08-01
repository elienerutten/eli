**Physical Activity data of the 10k cohort: a large‐scale prospective longitudinal study in Israel
Project performed at the Weizmann Institute of Science in the lab of Eran Segal.**

In the 10k project physical activity data is collected in three different ways: 1) tracking application on mobile phone  2) Activity logging by a proprietary smartphone application 3) extensive questionnaires. For data source 1) and 2) the codes that clean the data and extract features can be found in this directory. 

The following Table gives an overview of the defined physical activity features which can be extracted from the third party tracking application physical activity data.  

**Tracking application:**

A distinction is made between the two different types of tracking applications, AppleHealthkit and Googlefitness. AppleHealthkit data is limited to daily steps, whereas GoogleFitness data has a higher resolution and contains next to stepcount also estimated spend calories, distance and activities data. 

_apple_google_daily_steps_ gives the features: amount of days of data, daily steps and some other time-related features for all participants. 
_google_activity_data_ gives all features specified in the Table for participants using GoogleFit.

**Activity logging:**

_google_activity_data_ gives activity type and timing, corresponding MET values, high and moderate activity minutes and Heart points for the activity logging data of all participants. 


| **Feature**                                      | **Tag**                 | **Details**                       |
|--------------------------------------------------|-------------------------|------------------------------------|
| Amount of days of data*                          | datetime_count          |                                    |
| **Steps data**                                   |                         |                                    |
| Steps per day mean*                              | steps_day_mean          |                                    |
| Steps per day std                                | steps_day_std           |                                    |
| Mean pace (steps/min)                            | step_min_mean           | Steps per minute                   |
| Std pace (steps/min)                             | step_min_std            |                                    |
| **Activities**                                   |                         |                                    |
| Average amount of activities per day             | activities_count        |                                    |
| Average amount of activities per day std         | activity_name_count_std |                                    |
| **Metabolism**                                   |                         |                                    |
| BMR (Basal metabolic rate)                       | bmr_eq                  | Derived from Mifflin-St Jeor       |
| Calories per day mean (kcal)                     | calories_std            | Kcal burned, calculated using BMR  |
| Calories per day std (kcal)                      | calories_sum_std        |                                    |
| **Metabolic Equivalent of Task   (MET) values ** |                         |                                    |
| MET mean per day                                 | MET_mean                | MET = calories / (time*weight)     |
| MET max per day                                  | MET_max_mean            |                                    |
| MET min per day                                  | MET_min_mean            |                                    |
| MET std per day                                  | MET_std                 |                                    |
| **Heart Points (HP)**                            |                         |                                    |
| HP-MET mean per day                              | HP_MET_sum_mean         | 1 HP: 3-6 MET, 2 HPs: >6 MET       |
| HP-MET std per day                               | HP_MET_sum_std          |                                    |
| HP-step mean per day                             | HP_step_sum_mean        | 1 HP: 100-130 spm, 2 HPs: >130 spm |
| HP-step std per day                              | HP_step_sum_std         |                                    |
| HP-tot (MET + step) mean per day                 | HP_sum_mean             | HP-MET + HP-step                   |
| HP-tot (MET + step) std per day                  | HP_sum_std              |                                    |
| **Activity score**                               |                         |                                    |
| Activity score per day mean                      | activity_score_mean     | Total calories per day / BMR       |
| Activity score per day std                       | activity_score_std      |                                    |
| **Active minutes**                               |                         |                                    |
| Average time moderate activity per day   (min)   | min_med_sum_mean        | 3-6 MET or 100-130 steps per min   |
| Std time moderate activity per day (min)         | min_med_sum_std         |                                    |
| Average time high activity per day (min)         | min_high_sum_mean       | >6 MET or >130 steps per minute    |
| Std time high activity per day (min)             | min_high_sum_std        |                                    |
| Move minutes per day mean (min)                  | move_min_mean           | >= 30 steps within 1 minute        |
| Move minutes per day std (min)                   | move_min_std            |                                    |

*Overview of the defined features for the physical activity data obtained via a tracking application. _*Feature available also for AppleHealtkit_
