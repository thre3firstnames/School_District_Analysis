# Test Score Audit using Pandas and Jupyter Notebook
## Overview
Assist Maria with analyzing standardized test data from a number of schools within a certain district. Since one school is under scrutiny for tampering with scores from a particular grade level, it was my task to null that grade’s test scores from the overall calculations and recalculate the statistics without those students’ grades.

## Results
### District Summary
After making edits to the Thomas High School (THS) data, I observed the following:
##### *Original Analysis*
![original_DistrictDF.png](/Resources/original_DistrictDF.png)
##### *Edited Analysis*
![edited_DistrictDF.png](/Resources/edited_DistrictDF.png)
- With the exception of the **Average Reading Score**, all other averages and percentages showed a decrease in the updated summary statistics. 

### Effects of changing the THS Data within the School Summary
#### *Original Analysis*
![original_SchoolDF.png](/Resources/original_SchoolDF.png)
##### *Edited Analysis*
![edited_SchoolDF.png](/Resources/edited_SchoolDF.png)
- Most of THS’s averages and percentages also decreased with the alteration of the 9th grader’s scores with the exception of **Average Reading Score**, which increased by .05% after the change. 
- Broadly, the editing of the scores affected only minor changes on the averages and percentages for THS. Had the scores in the school summary been rounded to the nearest whole number, there would have been no marked change in our results. 
- Interestingly, the change did not affect THS’s ranking in the top 5 schools *(illustrated in the below comparison*).
#### *Original Analysis*
![original_Top5DF.png](/Resources/original_Top5DF.png)
##### *Edited Analysis*
![edited_Top5DF.png](/Resources/edited_Top5DF.png)

### Replacement of 9th Grade Test Scores 
- The editing of the 9th-grade test data affected the math & reading scores by grade by giving a null value for the 9th graders at THS. Their scores were not used in the overall statistic calculations.
- Scores by school spending
#### *Original Analysis* 
![original_ScoresbySpending.png](/Resources/original_ScoresbySpending.png)
#### *Edited Analysis*
![edited_ScoresbySpending.png](/Resources/edited_ScoresbySpending.png)
- Scores by school size
#### *Original Analysis* 
![original_ScoresbySize.png](/Resources/original_ScoresbySize.png)
#### *Edited Analysis*
![edited_ScoresbySize.png](/Resources/edited_ScoresbySize.png)
- Scores by school type
#### *Original Analysis* 
![original_ScoresbyType.png](/Resources/original_ScoresbyType.png)
#### *Edited Analysis*
![edited_ScoresbyType.png](/Resources/edited_ScoresbyType.png)
  - Sub bullet




## Summary
Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs
The total student count for the district remains unchanged by the exclusion of the 9th-grade student grades. I *did* skip over them on the “Per School” level calculations relating to averages and percentages ( and removed the count of those omitted students from those calculations), but doing away with the data points themselves would have heavily skewed the “Per Student Budget” that should remain unchanged by this audit. 
Since THS is a charter school with a relatively low student population, they still rank 
- 3
- 4

