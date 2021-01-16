# Keword Extraction _using (Keyword from Collective Weights)
KCW Model
- Text Preprocessing
- Textual graph representation
- Node weight assignment 
- Keyword Extraction using 'NE Rank'

Reference paper: Monali Bordoloi1 · Saroj Kr. Biswas1(2018)(Keyword extraction from blogs using collective weight, Springer)
https://www.researchgate.net/publication/327616483_Keyword_extraction_from_micro-blogs_using_collective_weight

Model Details
 - Text Preprocessing
   - Tokenization with removal of unwanted characters
   - Lower Casing
   - Stopword removal
   - Lemmatization
   - Removal of words with frequency below AOF(average occurance frequency)
   - Vectorization
 - Textual Graph representation
   - Nodes : Each token has been treated as a node.
   - Edges : Proximity b/w nodes (Edge weights have been determined on the basis of co-occurance frequency)
 - Node Weight asssignment : Parameters Considered-
   - Position of a word
   - Term frequency
   - Selective Centrality
   - Distance from central node
 - Keyword Extraction : NERank

Dataset Used: https://www.kaggle.com/benhamner/nips-papers?select=papers.csv

Model Test: Model has been tested on a set of 10 research papers from the above dataset.

Detailed Project Report: https://github.com/its7ARC/kewordExtraction/edit/main/projectReport.pdf
