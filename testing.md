# Greek Parser Testing

The testing consists of three levels of words. 
For each level, we give 20 words of varying parts of speech.

The model is scored on each word out of 5, losing points for each part of the parsing they get wrong.
An additional point is lost if the formatting is not right, such as forgetting to include a dictionary entry (if they know there is one). All inputs lack accents and breathings.

### Easy Words
- **λογω**

- **μανια**

- **αυτη**
 


| **Word** | **Response** | **Score** |
| -------- | ------------ | --------- |
| λογω   | **Word**: λεγω<br>**Root**: λέγω<br>**Form**: 1st person singular present active indicative<br>**Meaning**: "I say" or "I speak"                                                                    | 5/5   |
| μανια  | **Word**: μανια<br>**Root**: μανία<br>**Form**: Noun, feminine, nominative singular<br>**Meaning**: "madness," "enthusiasm," or "inspired frenzy"                                                    | 5/5   |
| αυτη   | **Word**: αυτη<br>**Root**: αὕτη<br>**Form**: Demonstrative pronoun, feminine singular nominative<br>**Meaning**: "this" (feminine)                                                                  | 5/5   |
