# Test Score Audit using Pandas and Jupyter Notebook
## Overview
Assist Maria with analyzing standardized test data from several schools within a particular district. Since one school is under scrutiny for tampering with scores from a particular grade level, it was my task to null that grade’s test scores from the overall calculations and recalculate the statistics without those students’ grades.

## Results
### District Summary
After making edits to the Thomas High School (THS) data, I observed the following:
###### *Original Analysis*
![original_DistrictDF.png](/Resources/original_DistrictDF.png)
######  *Edited Analysis*
![edited_DistrictDF.png](/Resources/edited_DistrictDF.png)
- Except for the **Average Reading Score**, all other averages and percentages showed a decrease in the updated summary statistics. 

### Effects of changing the THS Data within the School Summary
######  *Original Analysis*
![original_SchoolDF.png](/Resources/original_SchoolDF.png)
######  *Edited Analysis*
![edited_SchoolDF.png](/Resources/edited_SchoolDF.png)
- Most of THS’s averages and percentages also decreased with the alteration of the 9th grader’s scores except **Average Reading Score**, which increased by .05% after the change. 
- Broadly, the editing of the scores affected only minor changes on the averages and percentages for THS. Had the scores in the school summary been rounded to the nearest whole number, there would have been no marked change in our results. 
- Interestingly, the change did not affect THS’s ranking in the top 5 schools *(illustrated in the below comparison*).
######  *Original Analysis*
![original_Top5DF3.png](/Resources/original_Top5DF3.png)
######  *Edited Analysis*
![edited_Top5DF3.png](/Resources/edited_Top5DF3.png)

### Replacement of 9th Grade Test Scores 
- The editing of the 9th-grade test data affected the math & reading scores by grade by giving a null value for the 9th graders at THS. Their scores were not considered in the overall statistical calculations.
- The **$630-644** category (where THS falls) remains unaffected by the nulling of the 9th graders’ scores. Since these numbers are rounded, and the changes only show themselves in the second decimal place and beyond, no differences were observed.
######  *Original Analysis* 
![original_ScoresbySpending.png](/Resources/original_ScoresbySpending.png)
######  *Edited Analysis*
![edited_ScoresbySpending.png](/Resources/edited_ScoresbySpending.png)
- In the **Medium** category which includes THS, again, any changes to the scores are not significant enough to show in our outputs. 
######  *Original Analysis* 
![original_ScoresbySize.png](/Resources/original_ScoresbySize.png)
######  *Edited Analysis*
![edited_ScoresbySize.png](/Resources/edited_ScoresbySize.png)
- Finally, there is no noticeable change in the **Charter** school category following the change in the 9th grade test scores. 
######  *Original Analysis* 
![original_ScoresbyType.png](/Resources/original_ScoresbyType.png)
######  *Edited Analysis*
![edited_ScoresbyType.png](/Resources/edited_ScoresbyType.png)

## Summary
The total student count for the district remains unchanged by the exclusion of the 9th-grade student grades. I *did* skip over them on the “Per School” level calculations relating to averages and percentages ( and removed the count of those omitted students from those calculations), but doing away with the data points themselves would have heavily skewed the *Per Student Budget* that should remain unchanged for the audit.

Given the small sample size of students whose scores were removed, the somewhat dramatic shift in the district-wide statistics suggests that the school district was likely correct in assuming the grades had been altered. That being the case, it might be wise to repeat this process and remove all of the THS scores (and their student count [1635 –4.17% of total students]) to eliminate any further questions in regards to the school’s submitted scores. 

All charter schools in this analysis rank higher than the district schools. Since THS is among them despite their omission, it might be worth taking a closer look at each charter school to ensure their adherence to academic standards set out in their charter agreements with state and local government.

On the whole, omitting the scores of only 461 students (1.17% of total) caused minor shifts in the overall district data, and had almost no effect on those district-wide summary statistics that inform school performance (Size, Spending, and School Type).
