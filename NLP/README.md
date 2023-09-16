# Natural Language Processing 

It deals with text data. Different areas where text analytics is predominat in the current era
  
      1. Social Media Analytics
      2. Banking and Loan Processing
      3. Insurance Claim Processing
      4. Customer Relationship Processing
      5. Anti social activities over emails 
      6. E-commerce

  ## Steps undertaken for the raw data (Traditional Practice)

      1. Lexical Processing -> Convert raw text into words
      2. Syntactic Processing -> Extract meaning from the sentence by using syntax, grammar
      3. Semantic Processing -> Look for relations and learn (Deep Learning architectures help in this layer)

  ## Text Encoding
    
 A new standard - the Unicode standard supports all the languages in the world, both modern and the older ones.
Unicode has UTF-8, UTF-16. 

![Encoding](https://github.com/sarathchandrikak/Machine-Learning/blob/main/NLP/encoding.png)

# Regular Expressions 
  
#### Quantifiers

1. Quanitifer is an indicator.
2. Pattern to be executed in the given text / data
3. Use to match anytype of specialized words like time, email, dates
4. Quantifiers allows to mention and have control over how many times you want the character(s) in pattern to occur.
5. Four types of quantifiers
   
   1. The ‘?’ operator  =>  If the pattern can have 0/any times. It supports Optional preceding character. 
   
   2. The ‘*’ operator  =>  If the pattern can be 0 or more times.
       
   3. The ‘+’ operator  =>  If the pattern can be 1 or more times.
       
   4. The ‘{m, n}’ operator  => If the pattern can be fixed number of times.

       - {m, n}: Matches the preceding character ‘m’ times to ‘n’ times.
       - {m, }: Matches the preceding character ‘m’ times to infinite times, i.e. there is no upper limit to the occurrence of the preceding character.
       - {, n}: Matches the preceding character from zero to ‘n’ times, i.e. the upper limit is fixed regarding the occurrence of the preceding character.
       - {n}: Matches if the preceding character occurs exactly ‘n’ number of times.

    '?' is equivalent to zero or once, or {0, 1}
    '*' is equivalent to zero or more times, or {0, }
    '+' is equivalent to one or more times, or {1, }


#### Escape Sequences

The escape sequence, denoted by a backslash ‘\’, is used to escape the special meaning of the special characters. To match a question mark in whole of document '\?' is used. (this is called escaping the character).

#### Regex Flags 

A flag has a special meaning. A regex to ignore the case of the text then pass the 're.I' flag. Similarly, a flag with the syntax re.M enables to search in multiple lines (in case the input text has multiple lines). All these flags can be used in the re.search() function. 

    re.search(pattern, string, flags=re.I | re.M)

#### re.compile() function 

This function stores the regular expression pattern in the cache memory and is said to result in a little faster searches.

    # without re.compile() function
    result = re.search("a+", "abc")

    # using the re.compile() function
    pattern = re.compile("a+")
    result = pattern.search("abc")

#### Anchors, Wildcard, Character Sets

* Anchors  - Used to specify the start (^) and end ($) of the string
* Wildcard - A placeholder and can match any character in the given input string (.)
* Character Set - A character set is similar to a wildcard because it can also be used with or without a quantifier

| S.No. | Text Input | Regular Expression | 
|---|---|---|
| 1 | A pattern that starts with 1 and ends with zero but has arbitrary number of 1s (zero or more) in between |  '^1(1*0*)0$'  | 
| 2 | A binary number that starts with 101 and ends with zero or more number of zeroes | '^101(0*)$' |
| 3 | A pattern that matches numbers that are power of 10 |'^1+0*'|
| 4 | A pattern to match the word ‘hurray’. But with a minimum of two ‘r’s and a maximum of five ‘r’s. | '^hu(r{2,5})ay$' |
| 5 | A regular expression to match a term that has three or more ‘0’s followed by one or more ‘1’s| 0{3,}1+ |
| 6 | A regular expression that matches any string that starts with one or more ‘1’s, followed by three or more ‘0’s, followed by any number of ones (zero or more), followed by ‘0’s (from one to seven), and then ends with either two or three ‘1’s | '^1(1*)(000)0*1*0{1,7}(11|111)$' |


#### Greedy Vs Non-Greedy approach

Greedy approach - When a regular expression is used to match a string, the regex greedily tries to look for the longest pattern possible in the string. 

For example, when you specify the pattern 'ab{2,5}' to match the string 'abbbbb', it will look for the maximum number of occurrences of 'b' (in this case 5).

    Quantifiers for Greedy approach - *, +, ?, {m, n}, {m,}, {, n}, {n}

Non-Greedy approach - Also known as lazy approach. A regex stops looking for the pattern once a particular condition is satisfied. 

For example, when you specify the pattern '30+' to match the string '3000', the non-greedy technique, it will only match ‘30’ because it still satisfies the pattern ‘30+’ but stops as soon as it matches the given pattern.

    Quantifiers for Non-Greedy approach - *?, +?, ??, {m, n}?, {m,}?, {, n}?, {n}?

#### Commonly Used RE Functions 

* re.search() -> Scans through the entire text and finds match at any location
* re.match() -> It tries to look for the begining of the string
* re.findall() -> Find all substrings where the RE matches and returns them as a list
* re.finditer() -> Find all subbstrings where the RE matches and returns them as an iterator
* re.sub() -> Find all substrings where the RE matches and substitute them with the given string


# Basic Lexical Processing

## Tokenization 

A technique that’s used to split the text into smaller elements. These elements can be characters, words, sentences, or even paragraphs depending on the application.

In NLTK, you also have different types of tokenisers present that you can use in different applications. The most popular tokenisers are:

  * Word tokeniser splits text into different words.
  * Sentence tokeniser splits text in different sentence.
  * Tweet tokeniser handles emojis and hashtags that you see in social media texts
  * Regex tokeniser lets you build your own custom tokeniser using regex patterns of your choice.

## Bag of Words Representation

A bag-of-words model is one of the method to represent text in a format that you can feed into machine learning algorithms. It is just the matrix from text data. Each document sits on a separate row and each word of the vocabulary has a its own column. These vocabulary words are also called as features of the text. The values inside any cell can be filled in two ways 

  1. either fill the cell with the frequency of a word (i.e. a cell can have a value of 0 or more) 
  2. fill the cell with either 0, in case the word is not present or 1, in case the word is present (binary format).

## Stemming & Lemmatization 

Stemming is a rule-based technique that just chops off the suffix of a word to get its root form, which is called the 'stem'. Porter stemmer was developed in 1980 and works only on English words. Snowball stemmer is a more versatile stemmer that not only works on English words but also on words of other languages such as French, German, Italian, Finnish, Russian, and many more languages.  

Lemmatization is a more sophisticated/ intelligent technique in the sense that it doesn’t just chop off the suffix of a word. Instead, it takes an input word and searches for its base word by going recursively through all the variations of dictionary words. The base word in this case is called the lemma.

Stemming is much faster than the lemmatizer (which searches the dictionary to look for the lemma of a word). On the other hand, a stemmer typically gives less accurate results than a lemmatizer.

## TF-IDF

TF-IDF stands for term frequency - inverse document frequency. The TF-IDF representation, also called the TF-IDF model, takes into the account the importance of each word. In the bag-of-words model, each word is assumed to be equally important. The formula to calculate TF-IDF weight of a term in a document is:

![image](https://github.com/sarathchandrikak/Machine-Learning/assets/65502906/e83ef97e-cc8a-4d9b-873f-75462ce483d8) 

The log in the above formula is with base 10. Now, the tf-idf score for any term in a document is just the product of these two terms: 

![image](https://github.com/sarathchandrikak/Machine-Learning/assets/65502906/f0629e09-f6bd-4428-bf83-6c1de8897c59) 
