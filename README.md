from pathlib import Path

# Content of the README file
readme_content = """# NLP Assignment

## Student Information
- **Name**: [venkata nanda krishna yaram]  
- **Student ID**: [700765514]  
- **Course**: Natural Language Processing  


## Project Overview
This repository contains solutions to four core NLP tasks. Each task focuses on a different aspect of text processing, from basic tokenization to computing edit distances between words. The solutions include both code and written explanations.

## Tasks

### 1. Tokenization
- **Approach**: Performed naïve space-based tokenization on a short paragraph.  
- **Manual Correction**: Adjusted tokens by removing punctuation and handling suffixes/clitics.  
- **Comparison with Tool**: Used spaCy tokenizer for automatic tokenization. Differences arose in how punctuation and multiword expressions were handled.  
- **Multiword Expressions (MWEs)**: Identified idioms, place names, and fixed phrases (e.g., "New York City"). These should be treated as single tokens for semantic correctness.  

---

### 2. Named Entity Recognition (NER)
- **Method**: Applied spaCy’s `en_core_web_sm` model.  
- **Entities Extracted**: Detected entities such as persons, locations, dates, organizations, and monetary values.  
- **Observation**: Adding explicit dates or money values improved the diversity of detected entities.  



### 3. Stemming & Lemmatization
- **Library**: Used NLTK stemmer and WordNet lemmatizer.  
- **Examples**:  
  - `running → run (stem) / run (lemma)`  
  - `flies → fli (stem) / fly (lemma)`  
  - `better → better (stem) / good (lemma)`  
- **Reflection**: Lemmatization provides linguistically accurate base forms, whereas stemming often produces truncated tokens.  


### 4. Edit Distance (Sunday → Saturday)
- **Models Considered**:  
  - **Model A (Sub=1, Ins=1, Del=1)** → Distance = 3  
  - **Model B (Sub=2, Ins=1, Del=1)** → Distance = 4  
- **Operations Used**: Insertions and deletions were more efficient than substitutions.  
- **DP Table (first rows/columns)**: Computed up to `D(3,4) = 3`.  
- **Reflection**:  
  - Distances differ across models since substitution cost changes.  
  - Model A is better suited for applications like spell checking.  
  - Model B is more realistic for DNA/protein alignment tasks.  

