# 📌 **Spam SMS Detection Model**
This project is a **Spam SMS Detection System** that classifies text messages as either **Spam** or **Not Spam** using **Machine Learning (ML)** techniques. It includes:
- **Data Preprocessing with Dynamic Column Mapping**
- **Text Vectorization with TF-IDF**
- **Model Training and Evaluation**
- **User Interaction for Predictions**
- **Model Persistence (Saving and Loading)**

---

## 🚀 **Features**
- Dynamically handles different CSV structures with flexible column mapping.  
- Uses **TF-IDF vectorization** for text feature extraction.  
- Trains with both **Multinomial Naive Bayes** and **Random Forest**, selecting the better-performing model.  
- Provides an **interactive interface** for user SMS input classification.  
- Supports **model saving and loading** for future predictions.  

---

## 📊 **Dataset**
- The model uses a **CSV file** containing labeled SMS messages.
- Columns:  
    - `label`: Indicates whether the message is **spam** or **ham**.  
    - `message`: The actual SMS content.  
- Example:  
```
label,message  
ham,Hello, how are you?  
spam,Win a free vacation now! Click here!  
```

---

## 🔥 **Technologies Used**
- Python  
- Pandas  
- Scikit-Learn  
- Joblib  

---

## ⚙️ **Setup Instructions**

### 1️⃣ **Clone the Repository**
```bash
git clone <repository_link>
cd spam_sms_detection
```

### 2️⃣ **Install Dependencies**
Make sure you have the required libraries installed.  
You can install them using:
```bash
pip install pandas scikit-learn joblib
```

### 3️⃣ **Add Dataset**
- Place your **CSV file** in the project folder.  
- Ensure it contains the `label` and `message` columns (or `v1` and `v2` which will be automatically renamed by the script).

### 4️⃣ **Run the Script**
```bash
python spam_detection.py
```

---

## ✅ **Usage**

### **Training the Model**
The script:
1. **Loads the Dataset:**  
   - Automatically handles different column names by renaming them to `label` and `message` if necessary.  
2. **Splits the Data:**  
   - Splits the dataset into **training (80%)** and **testing (20%)** sets.  
3. **Vectorizes the Text:**  
   - Uses **TF-IDF vectorization** to convert SMS messages into numerical format.  
4. **Trains and Evaluates Models:**  
   - Trains both **Multinomial Naive Bayes** and **Random Forest** classifiers.  
   - Selects the better-performing model.  
5. **Saves the Model and Vectorizer:**  
   - The best model and vectorizer are saved using `joblib` for future use.  

---

### **User Interaction**
After training, you can:
- **Enter SMS messages** for classification.  
- Type `exit` to stop the program.  

### **Example Execution**
```
Enter an SMS to classify (or type 'exit' to quit): You have won a free iPhone! Claim now.
Prediction: Spam

Enter an SMS to classify (or type 'exit' to quit): Are you coming to the meeting tomorrow?
Prediction: Not Spam

Enter an SMS to classify (or type 'exit' to quit): exit  
Exiting... 🚀
```

---

## 📁 **File Structure**
```
📂 spam_sms_detection  
 ├── spam_detection.py        # Main Python script  
 ├── spam.csv                 # SMS dataset  
 ├── spam_model.pkl           # Saved model  
 ├── vectorizer.pkl           # Saved vectorizer  
 ├── README.md                # Project documentation  
```

---

## 📈 **Evaluation Metrics**
- **Accuracy:** Measures overall correctness.  
- **Confusion Matrix:** Shows TP, TN, FP, and FN.  
- **Classification Report:** Includes precision, recall, and F1-score.  

---

## 🛠️ **Model Improvement Suggestions**
- Use **hyperparameter tuning** for better performance.  
- Add **deep learning models** (LSTM, BERT) for more accurate predictions.  
- Implement **real-time message filtering** in a web app or mobile app.  
- Add **data augmentation** techniques to enhance the dataset.  

---

## 🚀 **Contributors**
- Aman Pawade

---

## 📚 **References**
- [Scikit-Learn Documentation](https://scikit-learn.org/)  
- [Pandas Documentation](https://pandas.pydata.org/)  
- [TF-IDF Vectorization](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)  

---


