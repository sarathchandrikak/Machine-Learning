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
5. Four types of quantifiers - \
   
       The ‘?’ operator - If the pattern can have 0/any times.
       Eg: Regex that match both car & cars - 'cars?' 
       'cars?' => In the sentences/text 'S' can be absent or present.
   
       The ‘*’ operator 
       The ‘+’ operator 
       The ‘{m, n}’ operator
