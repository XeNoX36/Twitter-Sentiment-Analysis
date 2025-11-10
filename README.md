# Project Report  

**1. Data Preparation**  
**- Data Cleaning**  
Converted text columns to string type for consistency.  
Handled missing values using dropna() and validation checks (isnull().sum()).  
Removed unwanted characters, links, special symbols, and numerals using regular expressions (re).  

Normalized text by:  
Lowercasing all words.  
Removing stopwords (e.g., “the”, “and”, “is”).  
Applying stemming using PorterStemmer to reduce words to their root form (e.g., “running” → “run”).  

**- Tokenization and Feature Extraction**  
Implemented TF-IDF Vectorization using TfidfVectorizer to convert tweet text into numerical form suitable for machine learning.  
The feature matrix represents the importance of each word relative to others across all tweets.  

**- Data Splitting**  
Data was split into training (80%) and testing (20%) subsets using train_test_split().  
Ensured stratified sampling to maintain balanced sentiment distribution.  

**2. Modeling and Machine Learning**  
Model Used: Logistic Regression (LogisticRegression from scikit-learn)  
Training Phase:  
The model was trained on the TF-IDF-transformed tweet texts.  
Target variable (target) was encoded as binary (positive/negative).    

Testing Phase:  
Predictions were generated for unseen test data.  
Model performance was assessed using accuracy score.  

Evaluation Metric:  
Accuracy Score: Calculated using accuracy_score(y_test, y_pred)  
Accuracy: 75%  

**3. Results & Insights**  
The model effectively distinguished between positive and negative sentiments.  
TF-IDF representation successfully captured contextual word importance, improving classification performance.  
Most influential positive words likely include terms like “good”, “love”, “great”, while negative ones include “bad”, “hate”, “worst”.  
