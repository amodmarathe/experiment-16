## Experiment 16: Amod Marathe
## Aim:
To study and implement basic Natural Language Processing (NLP) techniques.

## Theory:
# Introduction to NLP:
Natural Language Processing (NLP) is a branch of Artificial Intelligence (AI) that enables computers to understand,
interpret, and manipulate human language. It is widely used in applications like chatbots, text classification, sentiment analysis, and machine translation.
The experiment uses the NLTK library, which provides tools and datasets for processing human language data.

* 1. Tokenization:
Tokenization is the process of breaking text into smaller units such as words or sentences.
Functions Used:
nltk.download('punkt')
Downloads the tokenizer model required for splitting text into words and sentences.
word_tokenize(text)
Splits a sentence into individual words (tokens).
Example:
"Natural Language Processing" → ['Natural', 'Language', 'Processing']

* 2. Sentence Tokenization:
Splits a paragraph into individual sentences.
Functions Used:
sent_tokenize(text)
Breaks text into sentences based on punctuation rules.
Example:
"Python is easy. It is powerful." → ['Python is easy.', 'It is powerful.']

* 3. Stop Word Removal:
Stop words are commonly used words (like is, the, and, in) that do not add significant meaning to the text.
Functions Used:
stopwords.words('english')
Returns a list of English stop words.
set()
Converts the list into a set for faster lookup.
List Comprehension:
[w for w in words if w.lower() not in stop_words]
Filters out stop words from tokenized text.

* 4. Stemming:
Stemming reduces words to their base/root form (may not always be meaningful words).
Functions Used:
PorterStemmer()
Creates a stemmer object using the Porter stemming algorithm.
stemmer.stem(word)
Converts a word to its root form.
Example:
playing → play, studies → studi

* 5. Part of Speech (POS) Tagging:
POS tagging assigns grammatical roles (noun, verb, adjective, etc.) to each word.
Functions Used:
nltk.download('averaged_perceptron_tagger')
Downloads the POS tagging model.
pos_tag(words)
Returns a list of tuples with word and its POS tag.
Example:
('Python', 'NNP') → Proper noun

* 6. Word Frequency Count
Used to count how often each word appears in the text.
Functions Used:
FreqDist(words)
Creates a frequency distribution object.
fd.most_common()
Returns words sorted by frequency in descending order.

* 7. Lemmatization
Lemmatization converts words into their dictionary (base) form, considering meaning and context.
Functions Used:
WordNetLemmatizer()
Initializes the lemmatizer.
lemmatizer.lemmatize(word)
Converts words to meaningful base forms.
Example:
running → running (default noun)
better → good (with proper POS)
* Additional Downloads
nltk.download('stopwords') → Stop word dataset
nltk.download('wordnet') → Required for lemmatization
nltk.download('punkt_tab') → Additional tokenizer support

## Conclusion:
This experiment demonstrates the fundamental preprocessing techniques used in Natural Language Processing.
Tokenization helps break text into manageable units, stop word removal eliminates unnecessary words, stemming and
lemmatization reduce words to their base forms, POS tagging identifies grammatical roles, and frequency distribution helps analyze word imp
