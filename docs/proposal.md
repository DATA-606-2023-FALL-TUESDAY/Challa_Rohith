## 1. Title and Author

**Project Title:** Coursera Course Recommendation System

**Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang**

**Author Name:** Rohith Challa

**GitHub Profile:** ![GitHub](https://github.com/rohithrc6)

**LinkedIn Profile:** ![LinkedIn](https://www.linkedin.com/in/rohith-challa-82868a193/)

**PowerPoint Presentation:** [Link to PowerPoint presentation file]

**YouTube Video:** [Link to YouTube video]

## 2. Background

### What is it about?
As part of this project we will be using a course recommendation system to recommend courses to learners based on course rating, skills, course name, course description, etc. We can use content-based similarity filtering or collaborative filtering or a hybrid approach that uses both to make recommendations.

### Why does it matter?
[Explain why your project is important or relevant.]

### What are your research questions?
[List your research questions here, if applicable.]






##3. Dataset Description
Data Size: 8.72 MB
Data Shape: 3522 rows x 7 columns
Each Row Represents: A course on Coursera

Columns and their data types:

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3522 entries, 0 to 3521
Data columns (total 7 columns):
 #   Column              Non-Null Count  Dtype 
---  ------              --------------  ----- 
 0   Course Name         3522 non-null   object
 1   University          3522 non-null   object
 2   Difficulty Level    3522 non-null   object
 3   Course Rating       3522 non-null   object
 4   Course URL          3522 non-null   object
 5   Course Description  3522 non-null   object
 6   Skills              3522 non-null   object
dtypes: object(7)
memory usage: 192.7+ KB
None

Target/Label Variable: User_Rating
Feature/Predictor Columns : To be extracted from the existing columns (Course Name, Course Description, Course Rating)
