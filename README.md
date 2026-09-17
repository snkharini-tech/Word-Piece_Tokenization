# WordPiece Tokenization 

## Overview

This project implements the WordPiece Tokenization algorithm from scratch using Python and Jupyter Notebook.

WordPiece is a subword tokenization algorithm used by BERT-family models. It splits words into smaller subword tokens and uses `##` to represent tokens that occur inside a word.

## Objectives

- Understand WordPiece tokenization
- Calculate token frequencies
- Calculate pair frequencies
- Calculate WordPiece scores
- Select the highest-scoring pair
- Merge token pairs
- Tokenize new words
- Convert tokens into token IDs
- Handle unknown words using `[UNK]`

## Technologies Used

- Python
- Jupyter Notebook
- Collections Counter

## Corpus

The training data is stored in `corpus.txt`.

The corpus contains:

cat cat cat  
cats cats  
cater  
dog dog

## WordPiece Score

The WordPiece score is calculated using:

**Score = Pair Frequency / (Token 1 Frequency × Token 2 Frequency)**

The pair with the highest score is selected and merged into a new token.

## Working Process

Training Corpus  
↓  
Initial Character Splitting  
↓  
Token Frequencies  
↓  
Pair Frequencies  
↓  
WordPiece Score  
↓  
Best Pair Selection  
↓  
Pair Merging  
↓  
Tokenization  
↓  
Token IDs

## Example

Input:

`cats`

Output:

`Tokens: ['cat', '##s']`

`Token IDs: [11, 5]`

## Unknown Token

If a word cannot be completely represented using the available vocabulary, the tokenizer returns:

`[UNK]`

## Project Structure

WordPiece-Tokenization/  
├── WordPiece_Tokenization.ipynb  
├── corpus.txt  
└── README.md

## How to Run

1. Open the project folder in Jupyter Notebook.
2. Keep `corpus.txt` in the same folder as the notebook.
3. Open `WordPiece_Tokenization.ipynb`.
4. Run all cells from top to bottom.

## Features

- Character-level initial splitting
- Token frequency calculation
- Pair frequency calculation
- WordPiece score calculation
- Highest-score pair selection
- Token pair merging
- Subword tokenization
- Token-to-ID conversion
- `[UNK]` token handling

## Conclusion

This project demonstrates the basic implementation of WordPiece Tokenization from scratch using Python. It covers frequency calculation, score calculation, pair merging, subword tokenization, and token-to-ID conversion.
