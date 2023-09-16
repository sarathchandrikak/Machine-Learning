# NLP Advanced Lexical Analysis Techniques

Stemming and Lemmatization are a part of canonicalisation. Simply put, canonicalisation means to reduce a word to its base form. Stemming and lemmatization were just specific instances of it. Stemming tries to reduce a word to its root form. Lemmatization tries to reduce a word to its lemma. The root and the lemma are nothing but the base forms of the inflected words.

### Phonetic Hashing 

Phonetic hashing buckets all the similar phonemes (words with similar sound or pronunciation) into a single bucket and gives all these variations a single hash code. Hence, the word ‘Dilli’ and ‘Delhi’ will have the same code. Phonetic hashing is done using the Soundex algorithm. American Soundex is the most popular Soundex algorithm. It buckets British and American spellings of a word to a common code. It doesn't matter which language the input word comes from - as long as the words sound similar, they will get the same hash code.


### Edit Distance 

Edit Distance is one of the method to correct All the misspelt words to the correct spelling. An edit distance is a distance between two strings which is a non-negative integer number. An edit distance is the number of edits that are needed to convert a source string to a target string.

* Insertion of a letter in the source string. To convert ‘color’ to ‘colour’, insert the letter ‘u’ in the source string.
* Deletion of a letter from the source string. To convert ‘Matt’ to ‘Mat’, delete one of the ‘t’s from the source string.
* Substitution of a letter in the source string. To convert ‘Iran’ to ‘Iraq’, substitute ‘n’ with ‘q’

 
 
