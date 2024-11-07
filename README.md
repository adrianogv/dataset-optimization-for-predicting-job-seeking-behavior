# Dataset Optimization for Predicting Job-Seeking Behavior

This project focuses on optimizing a large dataset to improve model efficiency and storage requirements for a data science training provider, *Training Data Ltd.*. The goal is to clean and transform the dataset, enabling a more efficient structure for future predictive modeling. The dataset contains anonymized student information that will be used to predict if students are actively seeking new job opportunities, which the company will leverage to connect students with prospective recruiters.

## Project Overview

Large datasets can hinder model performance, particularly when it comes to speed and memory requirements. This project aims to reduce dataset size through data type optimization, while maintaining data integrity and improving processing speed. The resulting dataset will allow predictive models to run on a more reasonable timescale without sacrificing valuable information.

## Dataset

The dataset, `customer_train.csv`, provides anonymized data about students, including:

- `student_id`: Unique identifier for each student
- `city`: Encoded city of residence
- `city_development_index`: Development index of the city
- `gender`: Student’s gender
- `relevant_experience`: Indicator if the student has work experience relevant to their training
- `enrolled_university`: University enrollment status
- `education_level`: Education level of the student
- `major_discipline`: Major discipline in studies
- `experience`: Total work experience (in years)
- `company_size`: Size of the current employer
- `company_type`: Type of the employer company
- `last_new_job`: Years between current and previous jobs
- `training_hours`: Hours of training completed
- `job_change`: Indicator if the student is looking for a new job (1) or not (0)

## Key Steps

1. **Data Type Optimization**: Converted columns with only two unique values to Boolean types, reduced integer and float columns to lower precision, and transformed ordered categories to save memory.

2. **Filtering High-Value Candidates**: Filtered the dataset to include students with **10+ years of experience** working in companies with **at least 1,000 employees**, focusing on high-value profiles for recruiter outreach.

3. **Reduced Memory Usage**: Through data type transformations, reduced memory usage significantly, making the dataset more manageable and efficient for modeling.



## Future Work

Further analysis could include:

- Implementing additional filtering criteria based on job change likelihood.
- Evaluating model performance with the optimized dataset for predictive tasks.
- Exploring parallel processing techniques to further improve processing time.
