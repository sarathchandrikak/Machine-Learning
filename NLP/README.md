# Natural Languate Processing 

It deals with text data Different areas where text analytics is predominat in the current era
  
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

  ## Regular Expressions: Quantifiers - I

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



| S.No. | Text Input | Regular Expression | 
|---|---|---|
| 1 | A pattern that starts with 1 and ends with zero but has arbitrary number of 1s (zero or more) in between |  '^1(1*0*)0$'  | 
| 2 | A binary number that starts with 101 and ends with zero or more number of zeroes | '^101(0*)$' |
| 3 | A pattern that matches numbers that are power of 10 |'^1+0*'|
| 4 | A pattern to match the word ‘hurray’. But with a minimum of two ‘r’s and a maximum of five ‘r’s. | '^hu(r{2,5})ay$' |
| 5 | A regular expression to match a term that has three or more ‘0’s followed by one or more ‘1’s| 0{3,}1+ |


'?' is equivalent to zero or once, or {0, 1}
'*' is equivalent to zero or more times, or {0, }
'+' is equivalent to one or more times, or {1, }

