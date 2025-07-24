# 🎓 Academic Performance Analysis
Data analytics is increasingly valuable in education, helping institutions identify at-risk students, personalize learning, and improve academic outcomes. The data-driven approach can support educators make informed decisions to better tailor teaching strategies and allocate resources.

This project explores the relationship between students' demographics, academic performance, and engagement attributes to understand how these factors influence overall academic success.


## 1 Dataset Content
The dataset is sourced from Kaggle and can be downloaded from the link below.

https://www.kaggle.com/datasets/aljarah/xAPI-Edu-Data/data


## 2 Business Requirements
There are 4 areas we aim to cover in this project:

1. **Hypotheses Testing**: Validate assumptions about factors affecting Pass/Fail status.  The assumptions are set out in the next section
2. **Prediction Model**: Build a model to predict whether a student will Pass or Fail
3. **Key drivers identification**: Identify which attributes influence predictions the most
4. **Executive Dashboard**: Build an interactive dashboard to provide insight into Pass/Fail distribution by key attributes


## 3 Hypothesis
1. Students who raised their hands more often were more likely to pass
2. Students who visited more resources were more likely to pass
3. Students with a parent (or guardian) involved were more likely to pass
4. Female students had a higher pass rate than male students


## 4 File structure
The project files are managed in GitHub and the arrangement is as follows:

| Folder | File | Key content | Business requirement |
|----------|----------|----------|----------|
| dashboard | academic_performance_dashboard.pbix* |Executive dashboard in PowerBI| 4 |
| data/inputs/raw |xAPI-Edu-Data.csv |csv file downloaded from Kaggle| 1|
| data/inputs/cleaned |edu_data_cleaned.csv |csv file saved after data cleaning| 1|
| jupyter_notebooks |1_data_etl.ipynb |Analysis Step 1 - data extract, transform and load| 1|
| jupyter_notebooks |2_exploratory_analysis.ipynb |Analysis Step 2 - exploratory data analysis| 1|
| jupyter_notebooks |3_hypothesis_testing.ipynb |Analysis Step 3 - hypothesis testing| 1|
| jupyter_notebooks |4_prediction_model.ipynb|Analysis Step 4 - prediction model and key drivers identification| 2 and 3|
| pictures |relationships_between_parent_variables.jpg|screenshot of the Plotly graph used in Analysis Step 2| 1|
| y_profiling_report |profile_report.html**|Ydata profiling report used in Analysis Step 2| 1|

*Due to limitations with the version of PowerBI being used, a link cannot be provided.  The file can be downloaded from the "dashboard" folder.

**The Ydata profiling report can also be viewed directly in https://8osco.github.io/

Version control is mostly managed via GitHub, using regular commits and pushes to track changes.  The only exceptions are PowerBI files, where version control is managed on PowerBI workspace.  Only the final version is copied to GitHub.


## 5 Project Plan
The project plan was initiated following the establishment of the 4 business requirements. The first 3 requirements are addressed primarily through the use of Jupyter Notebooks. The corresponding implementation is reflected in the file structure outlined above, with each analysis step detailed as follows:

**Analysis Step 1** – Data extraction and familiarisation with the dataset. Python functions were used to identify missing values, duplicates and outliers. A list of data quality issues and change requirements was prepared and investigated further. Data cleaning tasks were prioritised, leading to the delivery of the first version of the cleaned dataset.

**Analysis Step 2** – Further feature analysis was conducted using the YData Profiling tool. Visualisations were employed to explore relationships between features, supporting initial views on feature selection.

**Analysis Step 3** – The four hypotheses were explored using data visualisations and evaluated with statistical measures (e.g., mean, variance), followed by validation using appropriate statistical tests.

**Analysis Step 4** – A prediction model was developed and evaluated to assess performance. Key features influencing academic outcomes were identified to inform the metrics and visual elements of the executive dashboard.

Project planning, monitoring and evaluation process was supported by Github project board, which can be found in https://github.com/users/8osco/projects/8/views/1.  User stories were created to guide the sequencing and formation of individual analysis steps.


## 6 Analysis techniques used
The analysis approach was guided by an exploratory mindset, experimenting with the data and making observations to steer further investigation. Visualisations were created to uncover patterns and relationships, informing the next steps in the analysis. Given the relatively large number of variables, efforts were made to examine feature relationships and consider potential dimensionality reduction options. This process not only can help minimise the risk of model overfitting, it also supported data validation and prompted data quality issues, e.g. a potential typo in a student’s grade, that might have otherwise gone unnoticed. 

To support the analysis, a range of tools and techniques were explored, including the YData Profiling tool, various Python libraries, and statistical methods.


## 7 Ethical considerations
The data has been anonymised at the source and does not present any immediate concerns regarding data privacy.

Analysis shows that the pass rate appears higher for students in certain countries.  However, this finding should be communicated with appropriate caveats, given the relatively small size of the dataset. Without further evidence, the results do not raise immediate concerns about bias or fairness.

It is also noted that the dataset includes records from multiple jurisdictions. As such, any use or further processing of the data should take into account relevant local data handling and privacy regulations.


## 8 Dashboard Design
An interactive dashboard was developed to provide clear and accessible insights into the pass/fail distribution across key student attributes. Designed with simplicity in mind, the dashboard caters to both technical and non-technical audiences by consolidating all key metrics into a single, easy-to-navigate interface.

The main metrics displayed are the pass rate and the number of students, with the ability to explore how these vary by:

- Nationality
- Gender
- Education stage
- Parental survey response status

User interaction is enabled through selectable buttons and interactive map elements. The dashboard also includes additional breakdowns by absence category and subject.

The attributes presented were selected based on insights from the coefficient ranking exercise, which revealed several notable patterns:

- Students from Saudi Arabia have a comparatively higher pass rate

- Students in the low absence group perform better

- Middle school students tend to have higher pass rates than those in other education stages

- Female students outperform male students in terms of pass rate

- Students whose parents responded to the survey show higher success rates

The dashboard also allows for cross-feature comparisons, enabling users to explore how combinations of these attributes impact academic outcomes.


## 9 Unfixed Bugs
There are a few features in the PowerBI dashboard that I was hoping to fix but am still searching for solutions:

1) locking down the map so that user won't inadvertently drag away and cannot find the country buttons;
2) putting school buttons in the following order - high, middle, lower;
3) disallowing buttons being switched off all at the same time for each button slicer


## 10 Development Roadmap
The work on ordering categorical values took more time than anticipated, and the ordering information was lost due to the use of csv files to break the process into stages for clearer presentation. This exercise offered valuable insight into how categorical handling works under the hood and also highlighted limitations in some of the functions, e.g. df.info() does not show ordered categorical as a data type.

Looking ahead, I would like to explore different approaches to enhance prediction models . This includes experimenting with unsupervised learning techniques to uncover potential hidden clusters that could improve predictive performance.


## 11 Main Data Analysis Libraries
- NumPy and Pandas for data interrogation and manipulation
- Seaborn and Plotly, supported by Matplotlib, for the visualisations
- Ydata profiling for exploratory data analysis
- Pingouin for statistical testing
- Scikit-learn for machine learning model building, evaluation and pipeline management
- Feature-engine for feature encoding and transformation


## 12 Credits 
Research papers associated with the dataset:

- Amrieh, E. A., Hamtini, T., & Aljarah, I. (2016). Mining Educational Data to Predict Student’s academic Performance using Ensemble Methods. International Journal of Database Theory and Application, 9(8), 119-136.

- Amrieh, E. A., Hamtini, T., & Aljarah, I. (2015, November). Preprocessing and analyzing educational data set using X-API for improving student's performance. In Applied Electrical Engineering and Computing Technologies (AEECT), 2015 IEEE Jordan Conference on (pp. 1-5). IEEE.

ChatGPT and GitHub Copilot for ideation such as hypotheses filtering, learning and checking understanding of data analytical concepts and techniques, code creation and clarification.

Code Institute course materials, SME, data coach, PDBA sessions.

## 13 Acknowledgements
A special thanks to the tutors at Code Institute, the support received and discussions have been invaluable.

