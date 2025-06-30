# 📝 **NLP Assignment: Processing *Moby Dick* with Python and NLTK**

## 📌 **Objective**

In this assignment, you will apply essential NLP techniques to the text of *Moby Dick* using Python and the NLTK library. Your goal is to process and analyze the text step-by-step, preparing it for deeper linguistic analysis.

---

## 📚 **Tools You Will Use**

* `re` (Python's Regular Expressions)
* `nltk.tokenize.word_tokenize`, `nltk.tokenize.sent_tokenize`
* `nltk.corpus.stopwords`
* `nltk.pos_tag`
* `nltk.stem.WordNetLemmatizer`
* `nltk.RegexpParser`

---

## ⚡ **Setup**

1. Install NLTK if you haven't:

   ```bash
   pip install nltk
   ```

2. In your Python script or notebook, make sure to download NLTK data you’ll need:

   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('stopwords')
   nltk.download('averaged_perceptron_tagger')
   nltk.download('wordnet')
   nltk.download('omw-1.4')
   ```

3. Load the text of *Moby Dick*. You can:

   * Download it from [Project Gutenberg](https://www.gutenberg.org/ebooks/2701)
   * Or use an online source / pre-supplied text file.

---

## 🛠 **Tasks**

### 1️⃣ **Noise Removal**

* Use **regular expressions** to clean the raw text.
* Focus on removing:

  * Numbers
  * Special characters (except periods that mark sentence ends)
  * Extra whitespace
* Think about which `re` functions (e.g., `re.sub`, `re.findall`, `re.search`, `re.match`) will help you identify and replace/remove these patterns.

---

### 2️⃣ **Sentence and Word Tokenization**

* First, split the cleaned text into **sentences** using `nltk.tokenize.sent_tokenize`.
* Then, break each sentence into **words** using `nltk.tokenize.word_tokenize`.

---

### 3️⃣ **Stop Words Removal**

* Load the English stop words from `nltk.corpus.stopwords`.
* Filter out stop words from your tokenized word list.
* Consider whether you want to apply this step to **all words**, or selectively depending on the type of analysis.

---

### 4️⃣ **POS Tagging**

* Apply `nltk.pos_tag` to your list of word tokens.
* This will assign part-of-speech tags (e.g., noun, verb) to each word.
* Keep track of both the word and its tag for the next steps.

---

### 5️⃣ **Lemmatization**

* Initialize a `WordNetLemmatizer`.
* Lemmatize each word using its POS tag (you may need to convert NLTK tags to WordNet-compatible tags).
* This will reduce words to their base or dictionary form (e.g., *running* → *run*).

---

### 6️⃣ **Chunking**

* Write chunking patterns using `nltk.RegexpParser` to identify:

  * **Noun Phrases** (e.g., determiner + adjectives + noun)
  * **Verb Phrases** (optional)
* Apply your chunk parser to your tagged tokens.
* Inspect and print the resulting chunks to see which phrases were found.
