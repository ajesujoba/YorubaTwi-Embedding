## Massive vs. Curated Word Embeddings for Low-Resourced Languages. The Case of Yorùbá and Twi

In the paper, we compared pre-trained word embeddings(Fasttext and BERT) and embeddings obtained from curated for Yorùbá and Twi. For this purpose, we gather and select corpora and study the most appropriate techniques for the languages. We also create test sets for the evaluation of the word embeddings within a word similarity task (wordsim353) and the contextual embeddings within a NER task. The Corpora and the embeddings are available in <a href="https://drive.google.com/drive/folders/1jkwLBkxJhnfVvf1yd7PyZw0nY8aNYaNN?usp=sharing">here</a>. 


For the comparison, we define 3 datasets according to the quality and quantity of textual data used for training: 
1. Curated Small Dataset (clean), C1, about 1.6 million tokens for Yorùbá and over 735k tokens for Twi. The clean text for <a href="https://drive.google.com/drive/folders/1cQ5lap1sn-SYbr9LdNo6Xqr--O0l60IQ">Twi</a> is the Bible and for <a href="https://drive.google.com/drive/folders/1fFuP5CBWbMAHn3SP_8kc3eVgf9cozWKW">Yorùbá</a> all texts marked under the C1 column in the figure below. 
2. In Curated Small Dataset (clean + noisy), C2, we add noise to the clean corpus (Wikipedia articles for Twi, and BBC Yorùbá news articles for Yorùbá). This increases the number of training tokens for <a href="https://drive.google.com/drive/folders/1cQ5lap1sn-SYbr9LdNo6Xqr--O0l60IQ">Twi</a> to 742k tokens and <a href="https://drive.google.com/drive/folders/1fFuP5CBWbMAHn3SP_8kc3eVgf9cozWKW">Yorùbá</a> to about 2 million tokens. 
 <!--- 3. Curated Large Dataset, C3 consists of all available texts we are able to crawl and source out for, either clean or noisy (<a href="https://drive.google.com/drive/folders/1cQ5lap1sn-SYbr9LdNo6Xqr--O0l60IQ">Twi</a>, <a href="https://drive.google.com/drive/folders/1fFuP5CBWbMAHn3SP_8kc3eVgf9cozWKW">Yorùbá</a>). --->

The evaluation datasets are the following:
1) Translated WordSim-353 for <a href="https://github.com/ajesujoba/YorubaTwi-Embedding/blob/master/Twi/wordsim_tw.csv">Twi</a>
2) Translated WordSim-353 for <a href="https://github.com/ajesujoba/YorubaTwi-Embedding/blob/master/Yoruba/wordSim353_yo.csv">Yorùbá</a>
3) Yoruba named entity recognition (NER) dataset on Github <a href="https://github.com/ajesujoba/YorubaTwi-Embedding/tree/master/Yoruba/Yor%C3%B9b%C3%A1-NER"> Yorùbá NER </a> dataset

Data set from the Niger Volta-Language Technology Institute can be gotten<a href="https://github.com/Niger-Volta-LTI/yoruba-text"> here  </a>

For reproducing the NER results using our fine-tuned BERT models, please use a modified <a href="https://github.com/dadelani/BERT-NER"> BERT-NER  </a> code. First, copy all the BERT embeddings in the <a href="https://drive.google.com/drive/folders/1VKLegJ3-t9Ro7ZHgsceaLoxAbrZ_3jkW?usp=sharing"> Google drive </a> and Google's <a href="https://github.com/google-research/bert"> uncased-multilingual-bert-base model </a> into the <a href="https://github.com/dadelani/BERT-NER/tree/master/bert_models"> bert_models </a> directory of the github. Then, you can run the following bash scripts in the BERT-NER:
1) sh <a href="https://github.com/dadelani/BERT-NER/blob/master/run_ner_yorubaPM.sh"> run_ner_yorubaPM.sh </a> for the baseline model i.e uncased Multilingual-bert
2) sh <a href="https://github.com/dadelani/BERT-NER/blob/master/run_ner_yorubaFMB.sh"> run_ner_yorubaFMB.sh </a> for the fine-tuned uncased Multilingual-bert on Yorùbá corpus with the default multilingual vocab.txt
3) sh <a href="https://github.com/dadelani/BERT-NER/blob/master/run_ner_yorubaFM.sh"> run_ner_yorubaFM.sh </a> for the fine-tuned uncased Multilingual-bert on Yorùbá corpus but with mostly Yorùbá vocabulary (i.e in vocab.txt) . We found out that using Yorùbá vocabulary for fine-tuning gave a better performance than using the multilingual vocab.txt


If you use any of the resources in this page, please cite the paper:

Jesujoba  O  Alabi,  Kwabena  Amponsah-Kaakyire,  David  I  Adelani,  and  Cristina  Espa ̃na-Bonet. <a href="https://arxiv.org/abs/1912.02481"> Massive vs. curated word embeddings for low-resourced languages. the case of Yor\ub\’a and Twi </a>. In LREC, 2020
