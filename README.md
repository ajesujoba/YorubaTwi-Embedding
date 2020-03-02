## Massive vs. Curated Word Embeddings for Low-Resourced Languages. The Case of Yorùbá and Twi

In the paper, we compared pre-trained word embeddings(Fasttext and BERT) and embeddings obtained from curated for Yorùbá and Twi. For this purpose, we gather and select corpora and study the most appropriate techniques for the languages. We also create test sets for the evaluation of the word embeddings within a word similarity task (wordsim353) and the contextual embeddings within a NER task. The Corpora and the embeddings are available in <a href="https://drive.google.com/drive/folders/1jkwLBkxJhnfVvf1yd7PyZw0nY8aNYaNN?usp=sharing">here</a>. 


For the comparison, we define 3 datasets according to the quality and quantity of textual data used for training: 
1. Curated Small Dataset (clean), C1, about 1.6 million tokens for Yorùbá and over 735k tokens for Twi. The clean text for <a href="https://drive.google.com/drive/folders/1cQ5lap1sn-SYbr9LdNo6Xqr--O0l60IQ">Twi</a> is the Bible and for <a href="https://drive.google.com/drive/folders/1fFuP5CBWbMAHn3SP_8kc3eVgf9cozWKW">Yorùbá</a> all texts marked under the C1 column in the figure below. 
2. In Curated Small Dataset (clean + noisy), C2, we add noise to the clean corpus (Wikipedia articles for Twi, and BBC Yorùbá news articles for Yorùbá). This increases the number of training tokens for <a href="https://drive.google.com/drive/folders/1cQ5lap1sn-SYbr9LdNo6Xqr--O0l60IQ">Twi</a> to 742k tokens and <a href="https://drive.google.com/drive/folders/1fFuP5CBWbMAHn3SP_8kc3eVgf9cozWKW">Yorùbá</a> to about 2 million tokens. 
3. Curated Large Dataset, C3 consists of all available texts we are able to crawl and source out for, either clean or noisy (<a href="https://drive.google.com/drive/folders/1cQ5lap1sn-SYbr9LdNo6Xqr--O0l60IQ">Twi</a>, <a href="https://drive.google.com/drive/folders/1fFuP5CBWbMAHn3SP_8kc3eVgf9cozWKW">Yorùbá</a>).

The evaluation datasets are the following:
1) Translated WordSim-353 for <a href="https://github.com/ajesujoba/YorubaTwi-Embedding/blob/master/Twi/wordsim_tw.csv">Twi</a>
2) Translated WordSim-353 for <a href="https://github.com/ajesujoba/YorubaTwi-Embedding/blob/master/Yoruba/wordSim353_yo.csv">Yorùbá</a>
3) <a href="https://github.com/ajesujoba/YorubaTwi-Embedding/tree/master/Yoruba/Yor%C3%B9b%C3%A1-NER"> Yorùbá NER </a> dataset

Data set from the Niger Volta-Language Technology Institute can be gotten<a href="https://github.com/Niger-Volta-LTI/yoruba-text"> here  </a>

If you use any of the resources in this page, please cite the paper:

Jesujoba  O  Alabi,  Kwabena  Amponsah-Kaakyire,  David  I  Adelani,  and  Cristina  Espa ̃na-Bonet. <a href="https://arxiv.org/abs/1912.02481"> Massive vs. curated word embeddings for low-resourced languages. the case of Yor\ub\’a and Twi </a>. In LREC, 2020
