<h1 align='center'> DOCUMENT-CLASSIFICATION-USING-NLP </h1>

## Objective
Perform document classification into four defined categories (World, Sports, Business, Sci/Tech). Compare the classifier accuracy with different models ranging from Naïve Bayes to Convolutional Neural Network (CNN) and RCNN. By making use of different feature engineering techniques and extra Natural Language Processing (NLP) features create an accurate text classifier.

## Document/Text Classification
Document/Text classification is an important task that has use cases in many real-world problems. Assigning topics to documents like news article, books, webpages, social media post has many applications like spam filtering, sentiment analysis, tagging customer queries, fake news detection etc. Natural language's vastly large size, unrestrictive nature, and ambiguity led to two problems when using standard parsing approaches that relied purely on symbolic, hand-crafted rules: unmanageable numerous rules and inability to understand ungrammatical text something which is human comprehensible easily. A problem statement apt for machine learning. NLP is a branch of data science that consists of systematic processes for analyzing, understanding, and deriving information from the text data in a smart and efficient manner. By utilizing NLP and its components, one can organize the massive chunks of text data, perform numerous automated tasks and solve a wide range of problems such as – automatic summarization, machine translation, named entity recognition, relationship extraction, sentiment analysis, speech recognition, and topic segmentation etc.
#

## Dataset
The chosen dataset is the ‘AG News’ dataset consisting of 1,20,000 news articles for training categorized in four categories- World, Sports, Business, Sci/Tech. It also includes 7600 testing samples in csv format.

## Text Pre-processing
It is predominantly comprised of three steps:

- Tokenization – It is about splitting strings of text into smaller pieces, or “tokens”. Paragraphs can be tokenized into sentences and sentences can be tokenized into words.

- Noise Removal – I have further cleaned up the text in this step. I have achieved so by removing punctuations, stop words, extra whitespaces and many other data points which was irrelevant to the NLP tasks. The NLTK library has inbuild functionalities for many such operations. A brief description of few of the steps taken is as:
Removed HTML tags: Since articles scrapped from web are likely to contain HTML tags, therefore have used Python package BeautifulSoup to remove HTML tags.
Remove stop words, accented characters and punctuation: As stop words, punctuations, extra whitespaces and accented characters do not add useful information to our text processing algorithm, therefore have removed them using modules such as Unicode and spaCy.
Treating Numbers: In our application numbers do not provide any significant knowledge and so, we have removed them. Firstly, in order to standardize the text, have converted number words to numeric form and then removed them from the textual data.

- Normalization – In this process, I have standardized the text into uniform sequence. I have converted the text to lowercase and using NLTK libraries performed stemming and lemmatization. Stemming refers to removing the suffixes attached to a word and lemmatization refers to conserving the root word of a word. We have used lemmatization for our textual data because that performed better with the pre-trained word embedding.

## Result
The model that gave me the best performance on the test data is was CNN with an accuracy of 90.87 % with 10 epochs. The model can be used to process any document and predict a class for it.

## Conclusion
While the classical models provided a good accuracy the neural network models improved it further. With more data the deep learning models will outmatch classical models. Using word embedding provided an additional 2-3% improvement in accuracy and faster training time. CNN provided the best performance in neural networks.
