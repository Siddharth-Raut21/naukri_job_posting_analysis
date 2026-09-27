# Naukri Job Market Analysis: Data Analyst & Data Scientist Roles in India

**Data Scientist and Hybrid roles carry a median disclosed salary roughly 2x that of Analyst and Other Data Role postings despite largely overlapping skill requirements.** 

``` text
This project analyzes 62,468 deduplicated Naukri.com job postings to understand how India's Data & AI job market varies by role type, compensation, skills, and geography.
```

## Dashboard Preview:

The project is presented through 3 analytical tiers.

### Tier 1 - Executive Overview:
A high-level view of job-market demand, role composition, top skills, compensation, and geographic concentration.

![Tier 1 - Executive Dasboard](Screenshots/Tier%201%20Executive%20View.png)

**Answers:**
1. How large is the market represented in the dataset?
2. Which role categories dominate?
3. Which skill appears most frequently?
4. Which city has the highest posting volume?
5. What compensation track appears at the top of the disclosed-salary data?


### Tier 2 - Diagnostic Deep-Dive:
A deeper analysis of disclosed compensation, skill demand, and skill co-occurrence.


![Tier 2 - Diagnostic Dashboard](Screenshots/Tier%202%20Diagnostic%20View.png)

**Answers:**
1. How does the highest disclosed package differ by role?
2. Which skills have the largest posting counts?
3. Which skills frequently occur together?
4. What patterns emerge beneath the headline KPIs?

### Tier 3 — Self-Serve Explorer
An interactive job-posting explorer allowing users to filter postings by role, city, and experience level and drill into relevant opportunities.

![Tier 3 - Self-Serve Explore](Screenshots/Tier3%20Self%20serve.png)

**Answers:**
1. Filter by Role
2. Filter by City
3. Filter by Experience
4. Browse matching job postings
5. Drill from skill-level analysis into relevant postings


#

## Business Questions:
This project was built to answer six specific questions, though before any cleaning began.

```text
1. How is the Data Analyst / Data Scientist job market in India actually composed by role type?

2. Does compensation differ meaningfully between Analyst, Scientist, Hybrid, and other data-adjacent roles?

3. Which skills are genuinely in demand, and which ones differentiate one role type from another?

4. Which skills tend to be requested together on the same posting?

5. Where is hiring geographically concentrated?

6. What can a job seeker realistically self-serve, filtering by their own target role, city, and experience level, to find relevant postings?
```
# 

## Dataset Source:
- Dataset Platform: Kaggle
- Dataset: [Naukri.com Job Postings Dataset](https://www.kaggle.com/datasets/iqbal303/job-postings-dataset-from-naukri-com?resource=download)
- Input files: 3 independently scraped CSV files
- Final analyzed postings: 62,468 after schema alignment, cleaning, and deduplication

## Data Caveat/Caution:
This dataset is a fixed scrape snapshot, not a live job feed. Therefore:
- Findings describe the dataset's collection window.
- They do not represent today's complete Indian job market.

#

## Methodology:
This project follows a lightweight CRISP-DM-style analytics lifecycle: 

| # | Visualization                 | Analytical Purpose                    |
| - | ----------------------------- | ------------------------------------- |
| 1 | Business Understanding       | Think, define, and decide the  6 analytical questions before cleaning the data.                |
| 2 | Data Understanding     | Understand & elaborate on all three raw files, row counts, schema mismatches, duplicate rates, and missingness.    |
| 3 | Data Preparation | Schema-aligned and unioned the three files; deduplicated; standardized text and locations; parsed salary and experience from free text; classified roles into buckets; extracted skills against a maintained reference vocabulary |
| 4 | Exploratory Analysis          | Examined role composition, disclosed compensation, skill demand, skill co-occurrence, and geographic concentration.               |
| 5 | Validation   | Full write-up in Exploratory Data Analysis/EDA for Naukri Job Posting Analysis. Documented the skill-extraction logic.    |
| 6 | Presentation  | 3-Tier Tableau dashboard covering Executive/Diagnostic/Self-Serve analysis.  |

#

## Key Findings:
**1. Compensation tracks role type:**

Distinct-counted (frequently posted) compensation differs substantially by role bucket.

| # | Role Bucket | Counted Distinct Compensation (18-22.5 LPA) |
| - | ----------- | --------------------------------------------|
| 1 | Scientist   | 346 |
| 2 | Hybrid | 252 |
| 3 | Other | 107 |
| 4 | Analyst | 4 |

```text
- This comparison applies only to postings where compensation was disclosed.
```
You can refer 1st, 2nd, and 3rd most frequently posted packages by role bucket in [EDA Report.](Exploratory_Data_Analysis/EDA_for_Naukri_Job_Posting_Analysis.pdf)

#

**2. Salary Evidence is Limited:**

- Only **6,704 of 62,468** postings (on average, only **11.54%** of postings) disclosed the salary for all 4 roles.

#

**3. Skill differentiation varies by role:**

- Across all postings **R** specified in **56,787** posting and **Python** in **6,899** postings.
- **Business Analysis** appears only in the Analyst top 5 skills but not in other role buckets.
- Many other commonly expected skills, particularly **SQL** and **data analysis** skills appear across a range of diverse roles.

#

**4. Other Data Roles Form the Largest Role Bucket**

The Role distribution is approximately:

| # | Role Bucket | Share of Postings|
| - | ------------| -----------------|
| 1 | Other Data Roles | **38.6%** |
| 2 | Analysts | **32.6%** |
| 3 | Scientist | **18.4%** |
| 4 | Hybrid | **10.5%** |

The **“Other Data Roles”** category contains neither “Analyst” nor “Scientist”. It contains roles like Data Governance Manager, Data Modeler, and similar. It is the largest group at 38.6% in 62,468 postings.

#

**5. Hiring is geographically concentrated:**

- **Bangalore** dominates hiring, accounting for more postings than the next several cities combined. 

Full methodology, charts, and caveats behind each finding are in 
[EDA Report.](Exploratory_Data_Analysis/EDA_for_Naukri_Job_Posting_Analysis.pdf)

#

## Tools & Technologies:

### Data Preparation
1. Python
2. pandas
3. NumPy
4. Regular Expressions (re)
5. VS Code

#

### Analysis & Reporting
1. Python
2. matplotlib
3. ReportLab
4. Tableau Desktop

#

### Outputs
1. Cleaned CSV datasets
2. Exploratory Data Analysis notebook
3. EDA report
4. Three-tier Tableau workbook
5. Dashboard screenshots



















