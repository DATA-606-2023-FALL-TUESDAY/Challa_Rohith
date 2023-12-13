## 1. Title and Author

**Project Title:** Coursera Course Recommendation System

**Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang**

**Author Name:** Rohith Challa

**GitHub Profile:** [GitHub](https://github.com/rohithrc6)

**LinkedIn Profile:** [LinkedIn](https://www.linkedin.com/in/rohith-challa-82868a193)

**PowerPoint Presentation:** [PowerPoint](https://github.com/DATA-606-2023-FALL-TUESDAY/Challa_Rohith/blob/main/docs/Project%20Presentation.pptx)

**YouTube Video:** [Link to YouTube video]

## 2. Background

### What is it about?
As part of this project we will be using a course recommendation system to recommend courses to learners based on course rating, skills, course name, course description, etc. We can use content-based similarity filtering or collaborative filtering or a hybrid approach that uses both to make recommendations.

### Why does it matter?
The project addresses a specific problem or question relevant to a particular to online education domain. By providing solutions or insights into this problem, it has the potential to make a decent impact on that domain. This problem-solving aspect is at the core of data science's practical applications.

### Some of the Research questions that will be addressed
- How can we create a course recommendation system that takes into account each user's unique learning preferences and history?

- What methods can be used to personalize course recommendations based on a user's academic or career goals?
- How can we address the "cold-start" problem, where the system needs to recommend courses to new users with limited interaction history?
- What strategies can be employed to make relevant recommendations to new users or users with sparse activity?

## 3. Data

### Data Source

https://www.kaggle.com/datasets/khusheekapoor/coursera-courses-dataset-2021

### Data Size
8.72 MB

### Data Shape
Before Data Cleaning - 3522 rows x 7 columns

After Data Cleaning - 3392 rows x 8 columns

### Each Row Represents
A course on Coursera

### Columns Details:

Before Data Cleaning:

| Column             | Non-Null Count | Dtype  |
|--------------------|----------------|-------|
| Course Name        | 3522 non-null  | object|
| University         | 3522 non-null  | object|
| Difficulty Level   | 3522 non-null  | object|
| Course Rating      | 3522 non-null  | object|
| Course URL         | 3522 non-null  | object|
| Course Description | 3522 non-null  | object|
| Skills             | 3522 non-null  | object|

After Data Cleaning:

| Column             | Non-Null Count | Dtype  |
|--------------------|----------------|-------|
| Index              | 3392 non-null  | int64|
| Course Name        | 3392 non-null  | object|
| University         | 3392 non-null  | object|
| Difficulty Level   | 3392 non-null  | object|
| Course Rating      | 3392 non-null  | float64|
| Course URL         | 3392 non-null  | object|
| Course Description | 3392 non-null  | object|
| Skills             | 3392 non-null  | object|
 
### Target/Label Variable
There is no target variable as this is a recommendation system.

### Features/Predictors
Features used for recommendation - Course Name, Course Description, Difficulty Level, Skills

## 4. EDA

### Data Cleansing and Preparation

In this recommendation system to perform data preprocessing and feature extraction we import the necessary libraries and then perform vectorization and stemming processes. We perform these two tasks on the column 'Tokens', which is a combination of columns 'Course Name', 'Course Description', 'Skills', and 'Difficulty Level'. So to make the data ready for these tasks we remove all the special characters (like,(,),-, etc.) in between words from the four columns mentioned in the previous statement and then make sure that they are only separated by single spaces. Then we concat the four columns into a new column called 'Tokens'. With this, the data is ready for vectorization and stemming processes. We perform these two tasks on a new data frame called 'CourseData'.

### Visualizations and Interpretations

- Universities CertNexus, SV Academy, and Karlsruhe Institute for Technology have the highest course ratings.
- Universities Universidad Nacional Autnoma de Mxico, Carnegie Mellon University, and Yandex have the lowest course ratings.
- Courses from almost all difficulty levels have an average course rating of 4.5
- Number of courses by difficulty level

| Difficulty Level| Count| 
|-----------------|------|
| Beginner        | 1425 | 
| Advanced        | 969  |
| Intermediate    | 823  |
| Conversant      | 175  |

![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Challa_Rohith/assets/97656473/c66da3fb-8e23-440a-a3d9-414c65033f36)

Most of the courses are beginner-level level and the rest of them mostly being advanced and intermediate.

Due to the nature of the dataset, there is relatively less scope for visualizations and interpretations.

## 5. Model

- Model - Item-based collaborative filtering
- Training - Computed cosine-similarity matrix to obtain the correlation coefficients of all the courses with each other.
- Python packages - pandas, numpy, pickle, matplotlib, nltk, scikit-learn
- Development environment - Google CoLab

## 6. Application of the Model
Below is a screenshot from the web application that was developed using Streamlit. For a given course of interest, it recommends courses along with their course ratings and difficulty levels.![image](https://github.com/DATA-606-2023-FALL-TUESDAY/Challa_Rohith/blob/main/docs/WebApp_SS.png)

## 7. Conclusion

### Summary
The presented work involves the development of a Coursera Course Recommendation System. It includes data cleaning, analysis, and visualization to derive insights into universities, course ratings, and difficulty levels. The pre-processing step involves tokenization, stemming, and vectorization of course data, enabling the computation of cosine similarity for course recommendations. paraphrase.
### Potential Application
The Coursera Course Recommendation System serves as a valuable tool for learners, providing personalized course suggestions based on user input. This can significantly enhance the user experience on the platform, making course discovery more tailored and efficient.
### Limitations
While the system offers personalized recommendations, it relies on user interaction data, which may introduce biases. Additionally, the system's effectiveness could be influenced by the availability and quality of data. Acknowledging these limitations is crucial for managing user expectations.
### Lessons Learned
The data cleaning and pre-processing steps are critical for building a robust recommendation system. Handling Inaccurate values, and data types, and removing non-alphabetic characters are key aspects of preparing the data. Stemming and vectorization contribute to the effectiveness of the recommendation algorithm.
### Future Research Direction
Future research can explore advanced recommendation techniques, considering additional features such as course content or user demographics. Addressing biases and improving the handling of new courses could enhance the system's accuracy. Exploring emerging technologies or methodologies in recommendation systems is also a potential avenue for future research.

## 8. References

- https://www.kaggle.com/code/sagarbapodara/coursera-course-recommendation-system-webapp
