# Greek-Parser
Agentic AI Greek Parser

This agentic system uses LangGraph to connect a chatGPt model to a set of tools that give it precise knowledge about Ancient Greek syntax and forms. 
This allows us to produce accurate parsing and translation of words without hallucination. 

## Resources
Some external files that are accessed via tools by the model. 
If you are running in Google Colab, you will have to upload the entire "resources" folder to the colab session in order for it to work

- Liddel and Scott's *Greek-English Lexicon* (source: [Perseids Project/lsj-js](https://github.com/perseids-project/lsj-js.git))
- Herbert Weir Smyth's *A Greek Grammar for Colleges* (source: [Alpheios Project/grammar-smyth](https://github.com/alpheios-project/grammar-smyth.git))

##  Testing

The testing consists of three levels of words. 
For each level, we give 20 words of varying parts of speech.

The model is scored on each word out of 5, losing points for each part of the parsing they get wrong.
An additional point is lost if the formatting is not right, such as forgetting to include a dictionary entry (if they know there is one). All inputs lack accents and breathings.

### Easy Words
Easy words consist of common nouns and present tense verbs, differing at most two letters from dictionary form
- **λεγω**

- **μανια**

- **αυτη**
 
- **σκελος**

- **καλα**

- **φρουρος**


| **Word** | **Response** | **Score** |
| -------- | ------------ | --------- |
| λεγω   | **Word**: λεγω<br>**Root**: λέγω<br>**Form**: 1st person singular present active indicative<br>**Meaning**: "I say" or "I speak"                                                                    | 5/5   |
| μανια  | **Word**: μανια<br>**Root**: μανία<br>**Form**: Noun, feminine, nominative singular<br>**Meaning**: "madness," "enthusiasm," or "inspired frenzy"                                                    | 5/5   |
| αυτη   | **Word**: αυτη<br>**Root**: αὕτη<br>**Form**: Demonstrative pronoun, feminine singular nominative<br>**Meaning**: "this" (feminine)                                                                  | 5/5   |

