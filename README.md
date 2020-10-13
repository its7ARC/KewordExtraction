# kewordExtraction
KWC Model in use (Preprocessing -> Textual graph representation -> Node weight assignment -> Keyword Extraction)

//Reference: Monali Bordoloi1 · Saroj Kr. Biswas1(2018)(Keyword extraction from blogs using collective weight, Springer)

//KWC model
 -> Preprocessing: Stopword Removal + regExpTokenizer + removal of words with frequency less than AOF(average occurance frequency)
 -> Textual Graph representation : Nodes(words) , edges(dist b/w words) : edgeWt = freq(i,j)/(freq(i) + freq(j) - freq(i,j)) ... freq(i,j) => co-occurance frequency
 -> Node Wt asssignment : first/last Word + term frequency + selective Centrality + dist from central node 
 -> Keyword Extraction : NERank{ R = (1-d)*W(Vi) + d*W(Vi)*sigma((w(ij) * R(j))/sigma(w(jk))) }
