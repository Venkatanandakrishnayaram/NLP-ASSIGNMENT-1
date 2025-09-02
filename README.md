

## Student Information
- **Name**: [venkata nanda krishna yaram]  
- **Student ID**: [700765514]  
- **Course**: Natural Language Processing  


## Project Overview
This repository contains solutions to four core NLP tasks. Each task focuses on a different aspect of text processing, from basic tokenization to computing edit distances between words. The solutions include both code and written explanations.

By working through these tasks, we get exposure to:
- Fundamental preprocessing steps (tokenization, stemming, lemmatization).  
- Higher-level linguistic processing (NER).  
- Subword-level models (Byte Pair Encoding).  
- String alignment and edit distance computation for real applications.  

## Tasks

### 1. Tokenization
- **Objective**: Break a paragraph into tokens.  
- **Steps**:  
  - Naïve tokenization using whitespace.  
  - Manual correction by removing punctuation and handling contractions.  
  - Comparison with **spaCy’s tokenizer**.  
- **Key Point**: Tokenization directly affects downstream tasks like POS tagging and NER.  
- **MWEs Identified**: Phrases like “New York City” or idiomatic expressions should not be split because they carry single semantic meanings.  

---

### 2. Named Entity Recognition (NER)
- **Tool Used**: `spaCy (en_core_web_sm)` model.  
- **Entities Detected**: People, places, organizations, dates, and money values.  
- **Extended Example**: By adding a date (“in 2023”) or monetary amount (“$5 million”), new entity types were recognized.  
- **Reflection**: While NER is powerful, context matters. The same word can have different roles (e.g., “Apple” as fruit vs. company).  

---

### 3. Stemming & Lemmatization
- **Libraries**: `nltk.PorterStemmer` and `WordNetLemmatizer`.  
- **Examples**:  
  - `running → run (lemma)` vs `run (stem)`  
  - `flies → fly (lemma)` vs `fli (stem)`  
  - `better → good (lemma)` (irregular case handled well by lemmatizer)  
- **Analysis**:  
  - **Stemming** is rule-based and fast but can produce incorrect forms.  
  - **Lemmatization** requires a dictionary but provides linguistically correct forms.  

---

### 4. Edit Distance (Sunday → Saturday)
- **Models Considered**:  
  - **Model A (Sub=1, Ins=1, Del=1)** → Distance = 3  
  - **Model B (Sub=2, Ins=1, Del=1)** → Distance = 4  
- **DP Table (first rows/columns)**: Computed up to `D(3,4) = 3`.  
- **Operations**: Insertions and deletions were more cost-effective than substitutions.  
- **Reflections**:  
  - Spell-checkers prefer **Model A** since substitutions are cheap.  
  - DNA/protein alignment prefers **Model B**, where insertions/deletions dominate.
    Reflections

### Preprocessing: 
Small differences in tokenization can lead to large differences in analysis.

NER: Works well for common names and dates but may miss domain-specific terms.

Subword Models (BPE): Greatly reduce the out-of-vocabulary problem by breaking rare words into smaller units.

Edit Distance: Highlights how alignment cost choices can shift application suitability.

Overall: The assignment bridges theory (manual edits, DP table) with practice (libraries and automation).

### Conclusion:

This assignment provided hands-on experience with essential NLP techniques. From splitting raw text into tokens, recognizing entities, reducing words to their base forms, to aligning strings with edit distance — these tasks show how foundational techniques power advanced systems like search engines, machine translation, and spell checkers.By implementing both manual steps and automated tools, the project reinforced the importance of understanding both low-level linguistic details and high-level algorithmic trade-offs.
