# Extending NLP project dictionary through lexicon parcing 
This small project is designed to extract named entities from webpages with a "term — definition" structure. It is required to cover a wider range of illicit terms as a first approximation of potentially illicit messages. The code integrates these terms into an existing database while preventing duplicates.

## Overview
This project processes a plain text file (Narcoterms.txt) containing slang terms for drugs, extracts and cleans the data, saves it to a temporary CSV, then merges it into a master dictionary CSV file (illegal_terms_dictionary_edit.csv).

## Features
* Parsing text entries: Extracts terms and definitions from lines.
* Normalization: Removes stress marks (diacritics) and cleans up punctuation/whitespace.
* CSV export: Saves parsed entries into a structured CSV file.
* Safe merging: Adds only new, non‑duplicate terms to the target dictionary.

## Usage
Place your input text file as Narcoterms.txt in the same directory.

Ensure illegal_terms_dictionary_edit.csv exists (can be empty or pre‑populated).

Run the script:

```bash
python main.py
```

Check output:

New terms will be added to illegal_terms_dictionary_edit.csv.
A summary of added entries is printed to the console.

## Configuration
You can modify these variables at the bottom of the script:

```python
INPUT_TXT  = 'Narcoterms.txt'
SOURCE_CSV = 'narcoterms.csv'
TARGET_CSV = 'illegal_terms_dictionary_edit.csv'
