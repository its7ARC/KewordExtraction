# kewordExtraction _using (Keyword from Collective Weights)
KCW Model in use (Preprocessing -> Textual graph representation -> Node weight assignment -> Keyword Extraction)

//Reference paper: Monali Bordoloi1 · Saroj Kr. Biswas1(2018)(Keyword extraction from blogs using collective weight, Springer)
https://www.researchgate.net/publication/327616483_Keyword_extraction_from_micro-blogs_using_collective_weight

//KCW model

 -> Preprocessing: Stopword Removal + regExpTokenizer + removal of words with frequency less than AOF(average occurance frequency)
 
 -> Textual Graph representation : Nodes(words) , edges(dist b/w words) ; edgeWt = freq(i,j)/(freq(i) + freq(j) - freq(i,j)) ... freq(i,j) => co-occurance frequency of 'i', 'j', freq(i) => frequency of word 'i'

 -> Node Wt asssignment : on the basis (first/last Word + term frequency + selective Centrality + dist from central node) 
 
 -> Keyword Extraction : NERank{ R = (1-d)*W(Vi) + d*W(Vi)*sigma((w(ij) * R(j))/sigma(w(jk))) }

//Dataset : https://www.kaggle.com/benhamner/nips-papers?select=papers.csv

//Detailed project report : https://github.com/its7ARC/kewordExtraction/blob/main/projectReport.pdf
