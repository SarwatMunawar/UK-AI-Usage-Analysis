# UK AI Usage Impact Analysis

## Project Overview

This project analyses the impact of Artificial Intelligence (AI) adoption and usage on organisations and employees across the UK.

The analysis focuses on how AI affects:

* Employee productivity
* Task completion
* Task processing time
* Error rates
* Quality of work
* Manager performance ratings
* Employee confidence and satisfaction
* AI training and adoption
* AI governance and operational risk
* AI-related costs and estimated financial value

The project uses **Python, Pandas, Excel and Power BI** to clean, analyse and visualise the data and provide evidence-based business recommendations.

---

## Business Objective

The main objective of this project is to understand whether AI adoption is generating measurable improvements in workplace productivity while identifying the operational, governance and employee-related risks associated with AI usage.

### Key Business Questions

1. How widely is AI being adopted across UK organisations?
2. What percentage of employees are actively using AI?
3. Which AI tools are most commonly used?
4. How frequently are employees using AI?
5. Has AI increased the number of tasks completed?
6. Has AI reduced the average time required to complete tasks?
7. Has AI improved work quality?
8. Has AI reduced error rates?
9. What is the relationship between AI training and AI usage?
10. What are the major AI governance and operational risks?
11. What are the estimated financial benefits of AI?
12. What actions should organisations take to maximise AI benefits while controlling risk?

---

# Dataset

The dataset contains multiple interconnected tables representing organisations, employees, AI usage, productivity, training and employee sentiment.

## Dataset Structure

| Table           | Records | Purpose                                         |
| --------------- | ------: | ----------------------------------------------- |
| Organisations   |      30 | Organisation-level information                  |
| Employees       |     720 | Employee demographics, roles and AI adoption    |
| AI_Usage        |   4,162 | AI tools, usage frequency, costs and time saved |
| Productivity    |   8,640 | Before vs current productivity metrics          |
| AI_Training     |     576 | AI training, assessment and confidence          |
| Employee_Survey |     720 | Employee attitudes, concerns and satisfaction   |
| Calendar        |     365 | Date and reporting calendar                     |

---

# Data Model

```text
                    ┌──────────────────┐
                    │  Organisations   │
                    └────────┬─────────┘
                             │
                       Organisation_ID
                             │
                    ┌────────▼─────────┐
                    │    Employees     │
                    └────────┬─────────┘
                             │
                         Employee_ID
                             │
          ┌──────────────────┼──────────────────┐
          │                  │                  │
          ▼                  ▼                  ▼
   ┌─────────────┐   ┌──────────────┐   ┌───────────────┐
   │  AI_Usage   │   │ Productivity │   │ AI_Training   │
   └─────────────┘   └──────────────┘   └───────────────┘
          │                  │
          │                  │
          ▼                  ▼
   ┌────────────────────────────────┐
   │       Employee_Survey          │
   └────────────────────────────────┘

                 Calendar
                    │
                    ▼
       Reporting / Date Analysis
```

---

# Data Cleaning & Preparation

The dataset was reviewed and prepared before analysis.

### Data Quality Checks

* Checked all datasets for duplicate records.
* Reviewed missing values.
* Checked data types.
* Standardised categorical fields.
* Converted date columns to appropriate date formats.
* Validated numerical fields.
* Reviewed AI usage and productivity metrics.
* Preserved genuine missing values rather than incorrectly converting them to zero.

### Missing Values

| Table           | Column                      | Missing Values |
| --------------- | --------------------------- | -------------: |
| AI_Training     | Assessment_Score            |             44 |
| Employee_Survey | Training_Satisfaction_Score |            272 |

These missing values were retained because they may represent records where the relevant assessment or satisfaction score was not applicable or not provided.

---

# Key Findings

## AI Adoption

The dataset contains **720 employees**, of which:

* **523 employees are AI users**
* **197 employees are non-users**
* AI user rate = **72.6%**

This indicates that AI has already achieved substantial penetration across the organisations represented in the dataset.

### AI Training

* 448 employees have completed AI training.
* 272 employees have not completed AI training.
* Training completion rate = **62.2%**

This creates a potential gap between AI adoption and employee preparedness.

---

# AI Usage Analysis

## Most Used AI Tools

| AI Tool                           | Usage Records |
| --------------------------------- | ------------: |
| Microsoft 365 Copilot             |         1,671 |
| ChatGPT Enterprise                |         1,016 |
| Google Gemini                     |           500 |
| Claude for Work                   |           427 |
| Microsoft Teams Intelligent Recap |           188 |
| Power Automate AI Builder         |           188 |
| GitHub Copilot                    |           172 |

Microsoft 365 Copilot is the most frequently used AI tool in the dataset, followed by ChatGPT Enterprise.

This suggests that AI adoption is particularly strong in productivity, communication and knowledge-work applications.

---

## AI Usage Frequency

| Usage Frequency      | Records |
| -------------------- | ------: |
| Daily                |   2,214 |
| Several Times a Week |   1,579 |
| Weekly               |     327 |
| Occasional           |      42 |

Approximately **91.1%** of AI usage occurs either daily or several times per week.

This indicates that AI is not merely being experimented with but has become part of regular employee workflows.

---

# AI Governance & Risk

## Tool Approval

| Approval Status | Records |
| --------------- | ------: |
| Approved        |   3,614 |
| Unapproved      |     548 |

Approximately **13.2% of recorded AI usage is unapproved**.

This represents a significant governance risk because employees may be using AI tools outside organisational policies.

---

## Human Review

| Human Review | Records |
| ------------ | ------: |
| Yes          |   3,461 |
| No           |     701 |

Approximately **16.8% of AI outputs are used without recorded human review**.

This creates potential risks related to:

* Accuracy
* Data privacy
* Compliance
* Hallucinations
* Incorrect decision-making
* Reputational damage

---

# AI Productivity Impact

The Productivity table provides a comparison between performance before AI and current performance.

| KPI               | Before AI |  Current | Change |
| ----------------- | --------: | -------: | -----: |
| Tasks Completed   |    101.76 |   106.56 |  +4.7% |
| Average Task Time |  1.73 hrs | 1.67 hrs |  -3.6% |
| Error Rate        |     7.18% |    6.71% |  -6.5% |
| Quality Score     |     76.94 |    79.24 |  +3.0% |
| Manager Rating    |      3.56 |     3.70 |  +3.9% |

### Interpretation

The results indicate a positive relationship between AI adoption and workplace productivity.

Employees are:

* Completing more tasks.
* Spending less time per task.
* Producing higher-quality work.
* Making fewer errors.
* Receiving slightly higher manager ratings.

However, these results should be interpreted as observed before-vs-current differences rather than definitive proof that AI alone caused all improvements.

---

# Time Savings

The AI Usage dataset records:

**38,112.8 hours of total estimated time saved.**

This represents a significant potential productivity benefit.

Time savings can potentially be redirected towards:

* Higher-value analytical work
* Customer service
* Innovation
* Strategic activities
* Employee development
* Process improvement

---

# AI Costs

## AI Subscription Cost

Total recorded AI subscription cost:

**£99,001.67**

## Training Cost

Total AI training cost:

**£176,361.64**

## Training Hours

Total recorded AI training hours:

**3,344 hours**

The organisation should therefore evaluate AI investments based on both productivity gains and implementation costs.

---

# Employee Sentiment

The employee survey provides insight into how employees perceive AI.

| Survey Metric          | Average Score |
| ---------------------- | ------------: |
| Perceived Productivity |     6.72 / 10 |
| AI Confidence          |     6.41 / 10 |
| Job Satisfaction       |     6.66 / 10 |
| Stress Level           |     5.40 / 10 |
| AI Usefulness          |     6.51 / 10 |
| Data Privacy Concern   |     5.55 / 10 |
| Job Security Concern   |     5.26 / 10 |
| Trust in AI Output     |     5.82 / 10 |
| Training Satisfaction  |     7.57 / 10 |

### Employee Sentiment Insight

Employees generally perceive AI as useful and productivity-enhancing, but confidence and trust are not exceptionally high.

Privacy and job-security concerns also indicate that successful AI adoption requires more than technology deployment.

Organisations must also address employee communication, training and change management.

---

# Organisation-Level Findings

## Organisation Size

| Organisation Size | Organisations |
| ----------------- | ------------: |
| Medium            |            13 |
| Large             |            11 |
| Small             |             6 |

Medium-sized organisations represent the largest group in the dataset.

---

## AI Adoption Stage

| Adoption Stage      | Organisations |
| ------------------- | ------------: |
| Partial Adoption    |            15 |
| Pilot               |             9 |
| Enterprise Adoption |             4 |
| Exploring           |             2 |

Most organisations are currently in the **Partial Adoption** stage.

This suggests that many organisations have moved beyond experimentation but have not yet fully integrated AI across the enterprise.

---

# AI Policy Status

| Policy Status | Organisations |
| ------------- | ------------: |
| Draft Policy  |            15 |
| Formal Policy |            13 |
| No Policy     |             2 |

The existence of organisations with no formal AI policy, combined with unapproved AI usage, highlights a need for stronger AI governance.

---

# Key Observations

### 1. AI adoption is already widespread

More than 72% of employees in the dataset are classified as AI users.

### 2. AI usage is becoming embedded in daily workflows

More than 91% of recorded AI usage occurs daily or several times per week.

### 3. Productivity indicators have improved

Task completion increased while task time and error rates decreased.

### 4. Quality has improved

Quality scores increased from approximately 76.9 to 79.2.

### 5. AI training is not keeping pace with adoption

AI usage is high, while training completion is only approximately 62.2%.

### 6. Governance requires improvement

Approximately 13.2% of AI usage is recorded as unapproved.

### 7. Human oversight remains important

Approximately 16.8% of AI outputs have no recorded human review.

### 8. Employees recognise AI's value but still have concerns

Employees report moderate confidence and trust alongside privacy and job-security concerns.

### 9. AI generates substantial time savings

More than 38,000 hours of estimated time savings have been recorded.

### 10. Organisations are still developing AI maturity

Most organisations are classified as being in the Partial Adoption stage.

---

# Business Insights

## Insight 1: AI is delivering measurable operational benefits

The increase in task completion and quality, combined with reductions in task time and errors, suggests that AI can contribute to operational efficiency.

**Business implication:** Organisations should identify workflows where AI can produce the highest productivity gains.

---

## Insight 2: AI adoption is moving faster than AI governance

Daily AI usage is high, but a proportion of activity remains unapproved.

**Business implication:** Organisations need clear AI policies, approved-tool lists and monitoring processes.

---

## Insight 3: Training is a strategic requirement

Only around 62.2% of employees have completed AI training.

**Business implication:** Increasing training coverage could improve employee confidence, responsible usage and adoption quality.

---

## Insight 4: Human oversight remains critical

AI outputs are not always reviewed by humans.

**Business implication:** High-risk activities should require mandatory human validation before AI-generated outputs are used.

---

## Insight 5: Employee trust will influence long-term adoption

Employees recognise AI's usefulness but have concerns about privacy, job security and trust.

**Business implication:** Organisations should combine AI implementation with transparent communication and change-management programmes.

---

# Recommendations

| Priority | Recommendation                       | Evidence                                          | Expected Outcome                                |
| -------- | ------------------------------------ | ------------------------------------------------- | ----------------------------------------------- |
| High     | Increase AI training coverage        | Only 62.2% completed training                     | Higher confidence and responsible AI usage      |
| High     | Introduce approved AI tool catalogue | 13.2% usage is unapproved                         | Reduced governance and compliance risk          |
| High     | Implement human-review rules         | 16.8% lacks recorded review                       | Improved accuracy and reduced AI-related errors |
| High     | Monitor AI ROI                       | £99k subscription cost + £176k training cost      | Better investment decisions                     |
| Medium   | Identify high-impact workflows       | Productivity improvements observed                | Greater productivity gains                      |
| Medium   | Expand AI into repetitive tasks      | 38,112.8 hours saved                              | More capacity for higher-value work             |
| Medium   | Improve AI communication             | Employee concerns around privacy and job security | Higher employee trust                           |
| Medium   | Create AI champions                  | Training and adoption gap                         | Faster knowledge sharing                        |
| Medium   | Monitor AI performance monthly       | Productivity data available                       | Early identification of problems                |

---

# Recommended AI Governance Framework

A practical AI governance framework should include:

### 1. Approved Tools

Maintain an approved list of AI applications.

### 2. Data Protection

Define what organisational and customer information can be entered into AI systems.

### 3. Human Review

Require human validation for high-risk AI outputs.

### 4. Training

Provide mandatory AI literacy and responsible-use training.

### 5. Monitoring

Track:

* AI adoption
* Usage frequency
* Unapproved usage
* Time saved
* Errors
* Quality
* Costs
* Employee sentiment

### 6. Continuous Improvement

Use performance data to identify where AI delivers the highest return.

---

# Dashboard Design

The project is designed around three Power BI dashboards.

## Dashboard 1 — Executive Overview

### Recommended KPIs

* Total Organisations
* Total Employees
* AI Users
* AI Adoption Rate
* AI Usage Records
* Total Time Saved
* AI Subscription Cost
* Training Completion Rate

### Recommended Visuals

* AI adoption by organisation
* AI users vs non-users
* AI adoption stage
* AI usage by tool
* AI usage frequency
* AI policy status
* AI usage by industry
* Regional AI adoption

### Filters

* Industry
* UK Region
* Organisation Size
* Organisation
* AI Adoption Stage
* Working Model

---

# Dashboard 2 — Before vs Current Performance

### Recommended KPIs

* Tasks Before AI
* Tasks Current
* Task Improvement %
* Task Time Before
* Task Time Current
* Time Reduction %
* Error Rate Before
* Error Rate Current
* Quality Before
* Quality Current
* Manager Rating Before
* Manager Rating Current

### Recommended Visuals

* Before vs Current task completion
* Before vs Current task time
* Before vs Current error rate
* Before vs Current quality
* Before vs Current manager rating
* Productivity trend by month
* Productivity by department
* Productivity by job level

### Filters

* Department
* Job Role
* Job Level
* Organisation
* Reporting Month
* Working Model

---

# Dashboard 3 — Operational Efficiency & Risk

### Recommended KPIs

* Total Time Saved
* Estimated Value of Time Saved
* AI Subscription Cost
* Training Cost
* Unapproved Usage %
* No Human Review %
* Training Completion %
* AI Confidence Score
* AI Trust Score

### Recommended Visuals

* Time saved by AI tool
* Time saved by use case
* AI cost by organisation
* Approved vs unapproved usage
* Human review vs no review
* AI training completion
* AI confidence
* Privacy concerns
* Job-security concerns
* Risk matrix

### Filters

* Organisation
* Industry
* AI Tool
* AI Tool Category
* Use Case
* Department
* Risk Category
* Date

---

# Suggested Calculated Measures

The following measures can be implemented in Power BI using DAX.

## AI Adoption Rate

```DAX
AI Adoption Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Employees),
        Employees[AI_User_Status] = "AI User"
    ),
    COUNTROWS(Employees)
)
```

## Training Completion Rate

```DAX
Training Completion Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Employees),
        Employees[AI_Training_Completed] = "Yes"
    ),
    COUNTROWS(Employees)
)
```

## Total Time Saved

```DAX
Total Time Saved =
SUM(AI_Usage[Time_Saved_Hours])
```

## Total AI Cost

```DAX
Total AI Cost =
SUM(AI_Usage[Subscription_Cost_GBP])
```

## Task Improvement %

```DAX
Task Improvement % =
DIVIDE(
    AVERAGE(Productivity[Tasks_Completed_Current_Month]) -
    AVERAGE(Productivity[Tasks_Completed_Before_AI]),
    AVERAGE(Productivity[Tasks_Completed_Before_AI])
)
```

## Task Time Reduction %

```DAX
Task Time Reduction % =
DIVIDE(
    AVERAGE(Productivity[Average_Task_Time_Before_Hours]) -
    AVERAGE(Productivity[Average_Task_Time_Current_Hours]),
    AVERAGE(Productivity[Average_Task_Time_Before_Hours])
)
```

## Error Rate Reduction %

```DAX
Error Rate Reduction % =
DIVIDE(
    AVERAGE(Productivity[Error_Rate_Before_Percent]) -
    AVERAGE(Productivity[Error_Rate_Current_Percent]),
    AVERAGE(Productivity[Error_Rate_Before_Percent])
)
```

## Quality Improvement

```DAX
Quality Improvement =
AVERAGE(Productivity[Quality_Score_Current]) -
AVERAGE(Productivity[Quality_Score_Before])
```

## Estimated Value of Time Saved

```DAX
Estimated Value of Time Saved =
SUMX(
    AI_Usage,
    AI_Usage[Time_Saved_Hours] *
    RELATED(Employees[Annual_Salary_GBP]) / 1950
)
```

---

# Technology Stack

### Data Analysis

* Python
* Pandas
* NumPy
* Jupyter Notebook

### Data Visualisation

* Matplotlib
* Seaborn
* Power BI

### Data Storage

* Microsoft Excel

### Documentation

* Markdown
* GitHub

---

# Project Workflow

```text
Raw Dataset
     ↓
Data Quality Assessment
     ↓
Data Cleaning
     ↓
Data Transformation
     ↓
Exploratory Data Analysis
     ↓
KPI Development
     ↓
Business Analysis
     ↓
Power BI Dashboard
     ↓
Business Insights
     ↓
Recommendations
```

---

# Key Business Takeaway

The analysis indicates that AI adoption is associated with meaningful improvements in workplace productivity.

Employees are completing approximately **4.7% more tasks**, average task time has decreased by approximately **3.6%**, error rates have fallen by approximately **6.5%**, and quality scores have increased by approximately **3.0%**.

However, the analysis also identifies important challenges.

AI usage is progressing faster than formal training and governance. Approximately **13.2% of AI usage is unapproved**, while approximately **16.8% of AI outputs have no recorded human review**.

Therefore, the next stage of AI adoption should not focus only on increasing usage. Organisations should focus on **responsible scaling** through better training, governance, human oversight, monitoring and ROI measurement.

---

# Limitations

The analysis has several limitations:

* The dataset represents a defined sample of UK organisations and employees.
* Before-vs-current comparisons do not prove that AI alone caused the observed improvements.
* Estimated time savings may not directly translate into financial savings.
* Employee survey responses may contain subjective bias.
* Missing survey and training values may affect certain averages.
* Further causal analysis would be required to establish the precise impact of AI.

---

# Future Analysis

Future versions of the project could include:

* ROI by organisation
* ROI by AI tool
* AI adoption vs productivity correlation
* Training vs productivity analysis
* AI usage by department
* AI impact by job level
* Employee sentiment vs AI adoption
* Risk scoring model
* AI maturity score
* Cost-benefit analysis
* Predictive modelling
* Regression analysis
* Employee-level productivity segmentation
* AI adoption forecasting

---

# Project Outcomes

This project demonstrates practical skills in:

* Data cleaning
* Data validation
* Exploratory Data Analysis
* Pandas
* Business intelligence
* KPI development
* Data visualisation
* Power BI dashboard design
* DAX
* Business storytelling
* Risk analysis
* Financial analysis
* Evidence-based recommendations

---

# Conclusion

AI is becoming an important component of modern workplace operations.

The dataset shows positive improvements across productivity, task completion, quality and error rates following AI adoption. At the same time, organisations face challenges around training, governance, employee trust, privacy and human oversight.

The strongest strategy is therefore not simply to increase AI usage, but to create a structured AI operating model that combines:

**AI Adoption + Employee Training + Governance + Human Oversight + Performance Measurement**

Organisations that successfully combine these areas will be better positioned to achieve sustainable productivity improvements while managing operational and employee-related risks.

---

## Author

**Sarwat Ali**

Data Analyst | Python | Pandas | SQL | Power BI | Excel

---

## Project Files

```text
UK-AI-Usage-Impact-Analysis/
│
├── README.md
├── UK_AI_Usage_Impact_Analysis_Dataset.xlsx
│
├── notebooks/
│   └── AI_Usage_Impact_Analysis.ipynb
│
├── dashboard/
│   └── AI_Usage_Impact_Dashboard.pbix
│
└── reports/
    └── Final_Analysis_Report.pdf
```

---

## Keywords

`Data Analysis` `Python` `Pandas` `Power BI` `DAX` `Excel` `Artificial Intelligence` `AI Analytics` `Business Intelligence` `Productivity Analysis` `Workforce Analytics` `Operational Efficiency` `Risk Analysis` `UK Business Analytics`
