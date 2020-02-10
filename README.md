# bioinformatics_project
Final Project for the Intro to Bioinformatics (CSIE5122) course at National Taiwan University (NTU)

This was my own implementation of the following research paper: 
<a href="https://www.ncbi.nlm.nih.gov/pubmed/30418485" target="_blank"> "Identifying antimicrobial peptides using word embedding with deep recurrent neural networks"</a> by Hamid and Friedberg.

This was part of a group project done in collaboration with Albert Li (李律), a fellow classmate. Together, we trained a neural network to classify whether or not amino acid sequences belonged to bacteriocins.

We compiled our own datasets of amino acid sequences from <a href="https://www.uniprot.org/downloads" target="_blank">Uniprot</a> and <a href="http://bagel4.molgenrug.nl/databases.php" target="_blank">BAGEL</a> databases. Amino acid sequences were split into trigrams, which then were used to train word embeddings using Gensim. The weights from the trained word embeddings were then loaded into a Tensorflow Embedding layer, which was followed by two bidirectional GRU layers, followed by a Dense layer. Due to a smaller dataset size and due to time constraints, we only trained the model with 5-fold crossvalidation instead of 10-fold crossvalidation as was originally performed in the paper. Also note that we used a relatively large batch size to speed up training, for the purpose of presenting our work to the class TAs.
