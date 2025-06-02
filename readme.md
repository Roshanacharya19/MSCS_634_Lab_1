# Personality Traits Data Analysis Lab - READM

# Purpose of Laboratory Work

This experiment demonstrates end-to-end data science processes for the personality psychology data of 2,900 individual assessments. Its primary purpose was to examine how the personality types (Extrovert and Introvert) relate to other attributes in their behaviors based on the complete data science pipeline: data collection, visualization, preprocessing, and statistical inference.

The research attempted to
- Identify distinctive behavioral patterns in extroverts and introverts
- Incorporate data preprocessing techniques to handle real-world dirty data
- Create thoughtful visualizations to reveal emotional truths
- Perform statistical analysis to assess personality-behavior correlations

## Key Insights from Visualizations and Metrics

### Major Breakthroughs:

**1. Clear Behavioral Segregation**
Scatter plot revealed two distinct clusters: extroverts (low alone time, high social events) and introverts (high alone time, low social events)
Negative correlation of -0.85 for alone time and social events attendance

**2. Stage Fear as A Predictor**
- Bar graph indicated that 70%+ of individuals suffering from stage fright are introverts
Stage fright seemed one of the most reliable indicators of personality

**3. Friend Circle Size Differences**
- Histogram revealed that extroverts possess 8-15 friends whereas introverts possess 0-8
Box plot revealed that extroverts were more variable in their social behaviors

**4. Surprising Social Media Similarity**
Line graph revealed that the posting frequency on social media by personalities surprisingly resembles one another
- it contradicts assumptions regarding on-line and off-line social behavior

**5. Validación Est
- Time spent alone was confirmed through correlation and was the best predictor of personality (r = 0.82)
Central tendency measurements indicated stark median discrepancies: extroverts attend ~7 events per month and introverts ~2 events per month.

### **Confirmed Psychology Theories:**
Extroverts tend to be more social and possess bigger social networks
- Introverts like to be alone and are more socially anxious (stage fear)
- Personality types have characteristic patterns across many behavioral dimensions

Challenges Facing and Decisions Made

**Challenge 1: Missing Data Handling**
**Problem:** Dataset contained ~2% missing values in multiple columns
**Decision:** Utilized personality-based imputation in place of overall mean/median
**Rationale:** Replacing missing values by personality type (i.e., using extrovert medians to replace missing values for extroverts) preserves behavioral patterns and enhances accuracy

**Challenge 2: Sklearn Dependency Issues**


**Issue:** Original code relied on sklearn that introduced import errors
**Decision:** Utilized manual scaling and encoding procedures
**Rationale:** Educational value in understanding the mathematical formula used for Min-Max scaling (x-min)/(max-min) and hand label encoding

**Test Case 3: Mix-Up of Overview Color**
**Problem:** The original scatter plot showed both types of personalities as blue dots
**Decision:** Included data cleaning and diagnostic checks prior to plotting
**Rationale:** Ensured missing values were handled properly and seaborn was able to map colors to the proper personality types

**Challenge No. 4: Treatment of Out
**Problem:** Friend count in the circle had extreme outliers (15+ friends)
**Decision:** Identified outliers by the IQR rule but included them in the analysis
**Explanation:** In personality testing, extreme scores can be instances of true behavioral tendencies as contrasted to measurement error

### **Challenge 5: Scaling Feature Selection**
**Problem:** Identifying variables to be scaled and discretized **Decision:** Based on Time_spent_Alone and Friends_circle_size as examples for illustration

**Rationale:** They were on disparate scales and were best suited for the analysis of personality

**Challenge 6: Creating Useful Categories**

**Problem: Discretizing Continuous Variables into Interpretable Categories**

**Decision:** Created "Low/Moderate/High" groups according to quartiles of data distribution

**Rationale:** Psychologically meaningful categories corresponding to standard practice in assessment of personality

## Technical Decisions Made **Data Preprocessing Strategy**: Used conservative outlier detection (IQR method) to keep valid extreme personalities **Visualization Strategy:** Preferred individual plots over subplots based on legibility and educational reasons **Statistical Analysis**: A focus on descriptive statistics and correlation over complex modeling **Documentation:** Gave extensive markdown explanation to make the findings understandable to non-technical audiences 
## Lessons Learnt 
1. **Knowledge specific to domains is essential**: Domain knowledge helped facilitate effective preprocessing decisions 
2. **Data Quality Matters**: Small issues such as missing values can severely impact subsequent visualizations 
3. **Manual Implementation Value**: Manual implementation was more enlightening than using black-box libraries 
4. **Pattern Recognition:** Empirical behavioral data demonstrates unmistakable patterns validating psychology theories 
5. **Individual Differences**: Even within personality types, there is considerable individual variation 

This lab successfully demonstrated how data science principles can be applied in psychology to reveal interesting patterns in human behavior and personality.
