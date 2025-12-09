# Task 2 – Chatbot for FAQs (AI / NLP)

## Steps Implemented

1. **Collect FAQs**
   - FAQs stored in `faqs.json` as an array of `{question, answer}`.

2. **Preprocess Text**
   - Uses **NLTK** for tokenization.
   - Steps:
     - Lowercasing.
     - Removing punctuation.
     - Tokenizing and joining back to clean text.

3. **Vectorization + Similarity**
   - Uses **TfidfVectorizer** from `scikit-learn`.
   - Computes **cosine similarity** between user query and FAQ questions.
   - Selects the best matching FAQ based on similarity score.
   - If score < threshold (default 0.2), returns a fallback message.

4. **Chat UI**
   - Built with **Streamlit**.
   - Maintains simple chat history.
   - Displays best matching answer as chatbot response.
   - Shows all FAQs inside an expandable panel.

## How to Run

```bash
cd task2_faq_chatbot
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # macOS / Linux

pip install -r requirements.txt
streamlit run app.py
