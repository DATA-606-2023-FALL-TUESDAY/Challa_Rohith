## 1. Title and Author

**Project Title:** Coursera Course Recommendation System

**Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang**

**Author Name:** Rohith Challa

**GitHub Profile:** ![GitHub](https://github.com/rohithrc6)

**LinkedIn Profile:** ![LinkedIn](https://www.linkedin.com/in/rohith-challa-82868a193)

**PowerPoint Presentation:** [Link to PowerPoint presentation file]

**YouTube Video:** [Link to YouTube video]

## 2. Background

### What is it about?
As part of this project we will be using a course recommendation system to recommend courses to learners based on course rating, skills, course name, course description, etc. We can use content-based similarity filtering or collaborative filtering or a hybrid approach that uses both to make recommendations.

### Why does it matter?
The project addresses a specific problem or question relevant to a particular to online education domain. By providing solutions or insights into this problem, it has the potential to make a decent impact on that domain. This problem-solving aspect is at the core of data science's practical applications.

### What are your research questions?
- How can we create a course recommendation system that takes into account each user's unique learning preferences and history?
- What methods can be used to personalize course recommendations based on a user's academic or career goals?
- How can we address the "cold-start" problem, where the system needs to recommend courses to new users with limited interaction history?
- What strategies can be employed to make relevant recommendations to new users or users with sparse activity?

## 3. Data

### Data Size
8.72 MB

### Data Shape
3522 rows x 7 columns

### Each Row Represents
A course on Coursera

### Columns Details:

| Column             | Non-Null Count | Dtype  |
|--------------------|----------------|-------|
| Course Name        | 3522 non-null  | object|
| University         | 3522 non-null  | object|
| Difficulty Level   | 3522 non-null  | object|
| Course Rating      | 3522 non-null  | object|
| Course URL         | 3522 non-null  | object|
| Course Description | 3522 non-null  | object|
| Skills             | 3522 non-null  | object|
 
### Target/Label Variable
User_Rating

### Features/Predictors
To be extracted from the existing columns (Course Name, Course Description, Course Rating, Skills)
