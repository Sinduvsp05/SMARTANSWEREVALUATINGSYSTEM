---

# 🧠 Smart Answer Evaluator

**An AI-powered application to automatically evaluate descriptive student answers by comparing them with model answers using NLP techniques. Built with Streamlit for an easy-to-use web interface.**

---

## 🚀 Features

* 📄 **PDF/Image Upload:** Supports scanned student answers and model answers (PDF, JPG, PNG).
* 🔍 **OCR Extraction:** Uses Tesseract to read text from images or PDFs.
* ✨ **Advanced Text Similarity:** Computes:

  * Cosine Similarity (TF-IDF)
  * Jaccard Similarity
  * Bigram Overlap
  * Synonym Matching via WordNet
* 📝 **Grammar Check:** Counts grammar errors using LanguageTool.
* 🎯 **Final Scoring:** Combines metrics into an overall percentage score.
* ✅ **Simple UI:** Built with Streamlit for interactive use.

---

## 🛠️ How It Works

1️⃣ User uploads:

* Student Answer (PDF/Image)
* Model Answer (PDF/Image)

2️⃣ App extracts text via Tesseract OCR.

3️⃣ Text is **preprocessed** (lowercased, tokenized, stopwords removed, lemmatized).

4️⃣ Multiple **similarity metrics** are calculated:

* **Cosine Similarity:** Measures overall semantic similarity.
* **Jaccard Similarity:** Compares unique word sets.
* **Bigram Similarity:** Matches consecutive word pairs.
* **Synonym Similarity:** Matches words with their synonyms from WordNet.

5️⃣ **Grammar errors** are counted via LanguageTool.

6️⃣ A **final weighted score** is computed:

```
30% Cosine + 20% Jaccard + 20% Bigram + 20% Synonym
```

7️⃣ Results displayed in a friendly Streamlit UI with performance feedback.

---

## 📦 Requirements

* Python 3.8+
* Tesseract OCR installed and path set correctly

  * [Download Tesseract](https://github.com/tesseract-ocr/tesseract)
* Packages (install with pip):

  ```
  streamlit
  pytesseract
  pillow
  numpy
  scikit-learn
  PyMuPDF
  nltk
  language-tool-python
  ```

---

## ⚡ Quick Start

1. **Clone the repo:**

   ```
   git clone https://github.com/yourusername/smartanswerevaluator.git
   cd smartanswerevaluator
   ```

2. **Install dependencies:**

   ```
   pip install -r requirements.txt
   ```

3. **(Optional) Set Tesseract path in app.py:**

   ```
   pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"
   ```

4. **Run the app:**

   ```
   streamlit run app.py
   ```

5. **Open in browser:**
   Usually at `http://localhost:8501`

---

## 📸 Screenshots

> *Add screenshots here if desired!*

---

## 🤖 Built With

* **Streamlit** – Web app framework
* **Tesseract OCR** – Text extraction from images/PDFs
* **NLTK** – Text preprocessing, tokenization, stopwords, WordNet
* **scikit-learn** – TF-IDF and Cosine similarity
* **PyMuPDF** – PDF processing
* **LanguageTool** – Grammar checking

---

## 👩‍💻 Author

* [Sinduvsp05](https://github.com/Sinduvsp05)

---

## 📜 License

This project is licensed under the MIT License – see the LICENSE file for details.

---

If you want, I can also write you:

✅ A shorter **minimal README**
✅ A requirements.txt example
✅ A more formal academic-style description

Just tell me!
