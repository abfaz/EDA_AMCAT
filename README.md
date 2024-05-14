# EDA Project AMCAT Data Analysis


## Objective
The dataset, sourced from Aspiring Mind Employment Outcome 2015 (AMEO), focuses on engineering students and encompasses essential employment outcomes such as salary, job titles, and locations. With around 40 variables and 4000 data points, it includes a mix of continuous and categorical features, providing insights into cognitive, technical, and personality skills. 

The objective of the project is to conduct exploratory data analysis (EDA) on the Aspiring Minds Employment Outcome 2015 (AMEO) dataset to:

• Gain insights into the employment outcomes of engineering graduates. 

• Understand the factors influencing salary expectations and specialization preferences among graduates. 

• Provide recommendations for optimizing recruitment strategies and improving graduate outcomes based on datadriven insights. 


## Dataset
The dataset consist of following columns (features):

```
• ID - A unique ID to identify a candidate
• Salary - Annual CTC oﬀered to the candidate (in INR)
• DOJ - Date of joining the company
• DOL - Date of leaving the company
• Designation - Designation oﬀered in the job
• JobCity - Location of the job (city)
• Gender - Candidate’s gender
• DOB - Date of birth of candidate
• 10percentage - Overall marks obtained in grade 10 examination
• 10board - The school board whose curriculum the candidate followed in grade 10
• 12graduation - Year of graduation - senior year high school
• 12percentage - Overall marks obtained in grade 12 examinations
• 12board - The school board whose curriculum the candidate followed in grade 12
• CollegeID - Unique ID identifying the college which the candidate attended
• CollegeTier - Tier of college
• Degree - Degree obtained/pursued by the candidate
• Specialization - Specialization pursued by the candidate
• CollegeGPA - Aggregate GPA at graduation
• CollegeCityID - A unique ID to identify the city in which the college is located in
• CollegeCityTier - The tier of the city in which the college is located
• CollegeState - Name of States
• GraduationYear - Year of graduation (Bachelor’s degree)
• English - Scores in AMCAT English section
• Logical - Scores in AMCAT Logical section
• Quant - Scores in AMCAT Quantitative section
• Domain - Scores in AMCAT’s domain module
• ComputerProgramming - Score in AMCAT’s Computer programming section
• ElectronicsAndSemicon - Score in AMCAT’s Electronics & Semiconductor Engineering section
• ComputerScience - Score in AMCAT’s Computer Science section
• MechanicalEngg - Score in AMCAT’s Mechanical Engineering section
• ElectricalEngg - Score in AMCAT’s Electrical Engineering section
• TelecomEngg - Score in AMCAT’s Telecommunication Engineering section
• CivilEngg - Score in AMCAT’s Civil Engineering section
• conscientiousness - Scores in one of the sections of AMCAT’s personality test
• agreeableness - Scores in one of the sections of AMCAT’s personality test
• extraversion - Scores in one of the sections of AMCAT’s personality test
• neuroticism - Scores in one of the sections of AMCAT’s personality test
• openess_to_experience - Scores in one of the sections of AMCAT’s personality test
```


## Data Cleaning and Feature Engineering

• The dataset consists of 3998 rows and 39 columns, with no missing values. Initially, missing data was indicated by -1, but we replaced these instances with NaN for thorough data analysis.

• Additionally, we converted the 'DOJ' (Date of Joining) and 'DOB' (Date of Birth) columns to datetime format for consistency and ease of manipulation.

• In the 'DOL' (Date of Leaving) column, we utilized a lambda function to categorize entries as 'Leave' or 'Present' based on the presence of a '/' character, facilitating further analysis and interpretation.


## Univariate Analysis Results

• Salary has a wide range of values, with the minimum salary being $35,000 and the maximum being $4,000,000. The mean salary is approximately $307,700, with a median of $300,000, indicating a positively skewed distribution.

• Academic performance metrics reveal distinctive patterns. In the 10th-grade, percentages span from 43.0 to 97.76, with an average of 77.93 and a median of 79.15. The mode at 78.0 signifies the most common percentage.

• For 12th-grade percentages, the range is 40.0 to 98.7, showcasing a balanced distribution with a mean of 74.47, median of 74.4, and mode at 70.0. The 12percentage column aligns closely with a normal distribution, as affirmed by the Q-Q plot.

• College GPAs range from 6.45 (with potential outliers less than 40 that can be considered for removal) to 99.93, exhibiting negatively skewed distributions

• There is a notable gender imbalance within the dataset, with a substantial majority of 3041 males compared to 957 females confirmed by a bar plot. This disparity may introduce bias in gender-specific analyses. 

• 53 % of employees left the company while 47 % are still in their present roles. This distribution provides insights into the employment status of the dataset, with a slightly higher representation of individuals who have left their jobs.

• The majority of individuals in the dataset hold technical roles, with 'Software Engineer,' 'Software Developer,' and 'System Engineer' being the most prevalent designations. Additionally, managerial positions such as 'Assistant Manager' are also notable among the top 15 designations.

• Bangalore, Noida, and Hyderabad are the most preferred cities for employment among the top 15 cities. This suggests a concentration of job opportunities in these urban centers.

• Looking at educational backgrounds, a significant majority of candidates hold a B.Tech/B.E. degree, suggesting a predominant technical education. MCA, M.Tech./M.E., and M.Sc. (Tech.) represent a smaller proportion of the degrees among the candidates.

• Most candidates in the dataset hail from Uttar Pradesh, Karnataka, and Tamil Nadu, and they predominantly attended Tier 2 colleges. Uttar Pradesh, in particular, has a significantly higher representation compared to other states, while several states have lower representation overall.

• Majority of candidates passed out 12th in year 2009 and completed graduation in 2013 suggested that it took about 4 years to graduate after 12th standard.


## Biivariate Analysis Results

• The scatter plots between '10percentage', '12percentage', 'collegeGPA', and 'Salary' suggest a probable linear relationship, supported by the rejection of the null hypothesis in the Pearson correlation tests. This indicates that higher academic performance is associated with higher salary levels in the dataset.

• The box plot between Salary and college tier shows a significant disparity in Salary between Tiers, where Tier 1 exhibits higher salaries than Tier 2 supported by two sample t test(stat=5.080, p_val=0.000). In contrast, Salary variations based on Gender and College City Tier are not statistically significant.

• The salary analysis indicates that there is a slight difference among the degree categories, with B.Tech/B.E., M.Sc. (Tech.), and M.Tech./M.E. showing comparable salary levels. However, MCA stands out with a significantly lower salary compared to the other degrees, suggesting a potential impact of the degree type on salary variations. This observation is further supported by a one-way ANOVA test, revealing a p-value of 0.047, which signifies a significant difference between the salary groups associated with different degrees.

• The Salary distribution across different job cities highlights a significant difference, with Mumbai exhibiting the highest mean salary and Bangalore, Gurgaon, Pune and Hyderabad following suit. The one-way ANOVA test (p_val=0.000) supports this observation, rejecting the null hypothesis and confirming a substantial disparity in Salary based on Job City.

• The box plot for the top 10 Designations highlights noteworthy variations in Salary, with "Senior Software Engineer" exhibiting a significantly higher mean Salary compared to other roles.

• 






















