# Text Classification Using Various Embedding Techniques

## Description
This project explores the application of different text data preparation methods—Raw Counts, TF-IDF, LSA (Latent Semantic Analysis), and Word2Vec—for document classification using Logistic Regression. The goal is to differentiate between "Sense and Sensibility" by Jane Austen and "Alice's Adventures in Wonderland" by Lewis Carroll.

## Performance Analysis
The performance of each method was evaluated based on training and testing accuracy:
1. **Raw Counts:**
   - Training accuracy: 98.87%
   - Testing accuracy: 96.87%

2. **TF-IDF:**
   - Training accuracy: 99.93%
   - Testing accuracy: 97.16%

3. **LSA:**
   - Training accuracy: 96.77%
   - Testing accuracy: 95.07%

4. **Word2Vec:**
   - Training accuracy: 93.70%
   - Testing accuracy: 91.34%

## Comparison and Insights
- **Raw Counts vs. TF-IDF:** TF-IDF slightly outperforms Raw Counts. While Raw Counts consider term frequency, TF-IDF also accounts for term uniqueness, aiding in better distinguishing the two authors.
- **Raw Counts and TF-IDF vs. LSA:** LSA underperforms compared to the first two methods, likely due to its dimensionality reduction, which may lead to significant information loss.
- **Word2Vec's Performance:** Word2Vec shows the lowest performance, possibly due to its focus on semantic similarities, which may not capture the specific stylistic features crucial for authorship attribution.

## Conclusion
TF-IDF emerges as the most effective method, with the highest training and testing accuracy, indicating its efficiency in capturing distinguishing features between authors. The training accuracy is consistently higher than the testing accuracy for all methods, hinting at potential overfitting, especially with TF-IDF.

## Technologies Used
- Python
- Gensim
- NLTK
- NumPy
- Scikit-learn

## Implementation Details
The project implements the following steps:
1. **Data Preparation:** Tokenizing and vectorizing sentences from "Sense and Sensibility" and "Alice's Adventures in Wonderland."
2. **Method Implementations:**
   - Generating data with raw token counts.
   - Applying TF-IDF scaling.
   - Implementing LSA for dimensionality reduction.
   - Utilizing a pre-trained Word2Vec model.
3. **Model Training and Evaluation:** Logistic Regression is used to train and evaluate models based on different text representation techniques.
4. **Comparison of Methods:** An analysis of the performance of each method in classifying the documents correctly.

## Usage
To replicate the experiment and view the performance comparison, run the `run_experiment` function in the provided script.
