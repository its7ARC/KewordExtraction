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
   - Edges : Proximity b/w nodes. (Edge weight = freq(i,j)/(freq(i) + freq(j) - freq(i,j)) ... freq(i,j) => co-occurance frequency of 'i', 'j', freq(i) => frequency of word 'i')
 - Node Weight asssignment : Parameters Considered
   - First/last Word
   - Term frequency
   - Selective Centrality
   - Dist from central node
 - Keyword Extraction : NERank

Dataset Used: https://www.kaggle.com/benhamner/nips-papers?select=papers.csv

