# 🎓 Academic Performance Analysis
Data analytics is increasingly valuable in education, helping institutions identify at-risk students, personalize learning, and improve academic outcomes. The data-driven approach can support educators make informed decisions to better tailor teaching strategies and allocate resources.

This project explores the relationship between students' demographics, academic performance, and engagement attributes to understand how these factors influence overall academic success.


## 1 Dataset Content
The dataset is sourced from Kaggle and can be downloaded from the link below.

https://www.kaggle.com/datasets/aljarah/xAPI-Edu-Data/data


## 2 Business Requirements
There are 4 areas we aim to cover in this project:

1. **Hypotheses Testing**: Validate assumptions about factors affecting Pass/Fail status.  The assumptions are set out in the next section.
2. **Prediction Model**: Build a model to predict whether a student will Pass or Fail.
3. **Key drivers identification**: Identify which attributes influence predictions the most.
4. **Executive Dashboard**: Build an interactive dashboard to provide insight into Pass/Fail distribution by key attributes.


## 3 Hypothesis
1. Students who raised their hands more often were more likely to pass.
2. Students who visited more resources were more likely to pass.
3. Students with a parent (or guardian) involved were more likely to pass.
4. Female students had a higher pass rate than male students.


## 4 File structure
The project files are managed in GitHub and the arrangement is as follows:

| Folder | Sub Folder| File | Business requirement | Key content |
|----------|----------|----------|----------|----------|
| dashboard | |academic_performance_dashboard.pbix | 4 |Executive dashboard in PowerBI|
| data |inputs/raw |xAPI-Edu-Data.csv | 1|csv file downloaded from Kaggle|
| data |inputs/cleaned |edu_data_cleaned.csv | 1|csv file saved after data cleaning|
| jupyter_notebooks ||1_data_etl.ipynb | 1|Analysis Step 1 - data extract, transform and load|
| jupyter_notebooks ||2_exploratory_analysis.ipynb | 1|Analysis Step 2 - exploratory data analysis|
| jupyter_notebooks ||3_hypothesis_testing.ipynb | 1|Analysis Step 3 - hypothesis testing|
| jupyter_notebooks ||4_prediction_model.ipynb| 2 and 3|Analysis Step 4 - prediction model and key drivers identification|
| pictures ||relationships_between_parent_variables.jpg| 1|screenshot of the Plotly graph used in Analysis Step 2|
| y_profiling_report ||profile_report.html*| 1|Ydata profiling report used in Analysis Step 2|

*The Ydata profiling report can also be viewed in https://8osco.github.io/

Version control is mostly managed via GitHub, using regular commits and pushes to track changes.  The only exceptions are PowerBI files, where version control is managed on PowerBI workspace.  Only the final version is copied to GitHub.


## 5 Project Plan
* Outline the high-level steps taken for the analysis.
* How was the data managed throughout the collection, processing, analysis and interpretation steps?
* Why did you choose the research methodologies you used?


The project plan was initiated following the establishment of the 4 business requirements. The first 3 requirements are addressed primarily through the use of Jupyter Notebooks. The corresponding implementation is reflected in the file structure outlined above, with each analysis step detailed as follows:

Analysis Step 1 – Data extraction and familiarisation with the dataset. Python functions were used to identify missing values, duplicates and outliers. A list of data quality issues was prepared and investigated further. Data cleaning tasks were prioritised, leading to the delivery of the first version of the cleaned dataset.

Analysis Step 2 – Further feature analysis was conducted using the YData Profiling tool. Visualisations were employed to explore relationships between features, supporting initial views on feature selection.

Analysis Step 3 – The four hypotheses were explored using data visualisations and evaluated with statistical measures (e.g., mean, variance), followed by validation using appropriate statistical tests.

Analysis Step 4 – A prediction model was developed and evaluated to assess performance. Key features influencing academic outcomes were identified to inform the metrics and visual elements of the executive dashboard.

Project planning, monitoring and evaluation process was supported by Github project board, which can be found in https://github.com/users/8osco/projects/8/views/1.  User stories were created to guide the sequencing and formation of individual analysis steps.


## 6 The rationale to map the business requirements to the Data Visualisations
* List your business requirements and a rationale to map them to the Data Visualisations

[placeholder!! - Articulate complex data insights in the dashboard, using visualisations and narratives to enhance user understanding. The README could include a section on how data insights were communicated to technical and non-technical audiences. The dashboard should include visualisations that are easy to understand and provide clear insights into the data. The README should explain how the dashboard was designed to communicate complex data insights to different audiences. The dashboard should include both technical metrics (e.g., statistical outputs, model accuracy) and simplified summaries or visualisations for a general audience.]

[placeholder!! - Employ visualisations and narratives in the dashboard to enhance user understanding. The notebook could include markdown on how visualisations were chosen and designed to communicate data insights. Learners can use visual tools like Matplotlib, Plotly, or Seaborn to visualise data in the notebook and ensure the dashboard includes clear charts and infographics.]

## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
* How did you structure the data analysis techniques. Justify your response.
* Did the data limit you, and did you use an alternative approach to meet these challenges?
* How did you use generative AI tools to help with ideation, design thinking and code optimisation?

[placeholder!! - model performance analysis, feature selection for 2, PCA for 5]

[placeholder!! - Explain the research methodologies used in the project, such as data collection, analysis, and interpretation. This could be done in the notebook through a methodology section or in the dashboard through a research methods section. In the notebook, learners should explain why they chose specific methodologies (e.g., experimental, observational) and data analysis techniques for their project goals.]

[placeholder!! - Learners should provide commentary on why they chose specific methods and explain limitations or alternative approaches. This can be done in a markdown section of the notebook or as a reflective section in the dashboard.]

Explain how data analytics and AI can address specific challenges or opportunities. Learners can outline AI solutions (e.g., Copilot or gen AI ideation) used in the analysis and their impact on solving domain-specific problems.]

--------------------------

exploratory mentality, given there are many variables

think of possible way to reduce number of variables/dimensionality to minimise risk of model overfitting 

re-run code e.g. Mother vs mum

ordering lost due to use of csv to break the process up for better presentation.  Won't lose ordering otherwise.  However, ordering won't carry through to PowerBI charts

Seaborn Charts not displayed - need additional command

exploratory data analysis step provided further checks on data, e.g. flagged potential typo in grade for one student

Try more statistical tests if time permits 

Y-profiling report not displayed on VScode - need additional packages/upgrades

Y-profiling report not displayed on Github - need create html file and create new GitHub page to display on browser

Use of CategoricDtype brings out interesting warning messages.  Reveal Panda's quirks re dtype showing in df.info()

Experiment with the data, make observations, shortlist for further analysis, create charts to visualise, inform further actions

------------------------------

## Ethical considerations
* Were there any data privacy, bias or fairness issues with the data?
* How did you overcome any legal or societal issues?

[placeholder!! - Discuss ethical considerations in the project, such as data privacy, bias, and fairness. This could be done in the notebook through a reflective section or in the dashboard through a data ethics section.]

[placeholder!! - Explain the legal (e.g. GDPR) and social implications of the data handling and findings. This could be done in the dashboard through a data governance section or in the notebook through a reflective section.]


## Dashboard Design
* List all dashboard pages and their content, either blocks of information or widgets, like buttons, checkboxes, images, or any other item that your dashboard library supports.
* Later, during the project development, you may revisit your dashboard plan to update a given feature (for example, at the beginning of the project you were confident you would use a given plot to display an insight but subsequently you used another plot type).
* How were data insights communicated to technical and non-technical audiences?
* Explain how the dashboard was designed to communicate complex data insights to different audiences. 

[placeholder!! - Articulate complex data insights in the dashboard, using visualisations and narratives to enhance user understanding. The README could include a section on how data insights were communicated to technical and non-technical audiences. The dashboard should include visualisations that are easy to understand and provide clear insights into the data. The README should explain how the dashboard was designed to communicate complex data insights to different audiences. The dashboard should include both technical metrics (e.g., statistical outputs, model accuracy) and simplified summaries or visualisations for a general audience.]

[placeholder!! - The notebook should include well-documented sections, while the dashboard should feature clear labels, tooltips, or explanations for each visualisation or insight. The dashboard should include a clear narrative that guides the audience through the data story, explaining key insights and findings.]
The dashboard can reflect a well-thought-out user experience, guiding the audience through the data story.

Determine key attributes to present

Create a dashboard which provides interactive insights into the pass/fail distribution by key attributes

Provide logic of the charts used

Provide narratives and highlight key observations

[Placeholder!! - 

Dashboard items informed by the key features identified from the coefficient ranking exercise

Pass rate and number of students involved were key metrics

Pass rate derived using DAX

ISO code needed for country location (as country names can be ambiguous)

Challenge - couldn't sort the school order, despite following AI suggestions]


[placeholder!! - due to limitations with the version of PowerBI being used, a link cannot be provided, however, a file is available in XXXXX folder labelled YYYYY]


## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
* Did you recognise gaps in your knowledge, and how did you address them?
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.

[Placeholder!! - In your bug section of the README, mention how you adapted the code to overcome challenges. This can include identifying specific moments where you recognised gaps in your knowledge and how you addressed them. If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.]


## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
* What new skills or tools do you plan to learn next based on your project experience? 

 [Placeholder!! - In the notebook, learners should reflect on challenges like dataset size or deployment issues and discuss potential solutions.]
 [In the notebook, learners can discuss challenges they faced during the analysis, such as data limitations, and suggest alternative approaches (e.g., using different techniques or more extensive datasets).]


 [Placeholder!! - reflect on your progress, the challenges you've faced, and the strategies used to overcome these challenges. This shows a continuous learning mindset. Within your README, include a development roadmap that details what new skills or tools you plan to learn next based on your project experience.]


Prediction Model Enhancement.  Explore potential hidden clusters to enhance prediction, e.g. through unsupervised learning


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.

[Placeholder!! - Explain why you chose specific tools (e.g., comparing different Python libraries like Matplotlib vs. Plotly for visualisation). Detail in Jupyter any experiments with new tools or methodologies, showing code snippets and explaining their results. Incorporate new tools/technologies you've researched (such as a new library). The project would show evidence of trial, adaptation, and application in a meaningful way. Focus on challenges encountered and solutions found, explaining how you adapted to using them in the project.]



## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 


[Placeholder!! - Learners could integrate an AI assistant, such as Copilot, into their notebook to suggest or optimise code snippets. They can document examples where AI tools helped in tasks like data cleaning, ideation or design thinking.]

[Placeholder!! - Use AI tools to generate insights from data, such as creating a narrative or summarising key findings. This could be showcased in the dashboard through visualisations or text summaries. The dashboard could have an AI-generated summary of key data insights, visualisations, and explanations that are designed for both technical and non-technical audiences. Use Gen AI agent-based prompts for ideation, design thinking and business requirements.]

Amrieh, E. A., Hamtini, T., & Aljarah, I. (2016). Mining Educational Data to Predict Student’s academic Performance using Ensemble Methods. International Journal of Database Theory and Application, 9(8), 119-136.

Amrieh, E. A., Hamtini, T., & Aljarah, I. (2015, November). Preprocessing and analyzing educational data set using X-API for improving student's performance. In Applied Electrical Engineering and Computing Technologies (AEECT), 2015 IEEE Jordan Conference on (pp. 1-5). IEEE.

Ideation with gen AI
Gen AI to help learn and check understanding of stats concept and code structure



## Acknowledgements
A special thanks to the tutors at Code Institute, the support received and discussions have been invaluable.




[Placeholders!! - check yellow cells in 'capstone checklist']
[Placeholder!! - recheck jpg link]
[Placeholders!! - submission questionnaire]