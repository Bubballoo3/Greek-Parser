# Greek-Parser
Agentic AI Greek Parser

This agentic system uses LangGraph to connect a chatGPT model to a set of tools that give it precise knowledge about Ancient Greek syntax and forms. 
This allows us to produce accurate parsing and translation of words without hallucination. 

## Resources
Some external files that are accessed via tools by the model. 
If you are running in Google Colab, you will have to upload the entire "resources" folder to the colab session in order for it to work

- Liddel and Scott's *Greek-English Lexicon* (source: [Perseids Project/lsj-js](https://github.com/perseids-project/lsj-js.git))
- Herbert Weir Smyth's *A Greek Grammar for Colleges* (source: [Alpheios Project/grammar-smyth](https://github.com/alpheios-project/grammar-smyth.git))

##  Testing

- The testing consists of three levels of words. 
- At each level, we give 12 words of varying parts of speech.
- At the easy and medium level, examples are drawn from Aelian's *Epistulae Rusticae*. Hard examples are drawn from multiple sources to test Attic, Homeric, and Ionian dialects.
- The model is scored on each word out of 5, losing points for each part of the parsing they get wrong.
An additional point is lost if the formatting is not right, such as forgetting to include a dictionary entry (if they know there is one). 
- All inputs lack accents and breathings.

### Easy Words - 95% accurate (57/60 points)
Easy words consist of common nouns and present tense verbs, differing at most two letters from dictionary form

| **Word** | **Response** | **Score** | **Explanation**|
| -------- | ------------ | --------- | ---------------|
| λεγω   | **Word**: λεγω<br>**Root**: λέγω<br>**Form**: 1st person singular present active indicative<br>**Meaning**: "I say" or "I speak"                                                                    | 5/5   |
| μανια  | **Word**: μανια<br>**Root**: μανία<br>**Form**: Noun, feminine, nominative singular<br>**Meaning**: "madness," "enthusiasm," or "inspired frenzy"                                                    | 5/5   |
| αυτη   | **Word**: αυτη<br>**Root**: αὕτη<br>**Form**: Demonstrative pronoun, feminine singular nominative<br>**Meaning**: "this" (feminine)                                                                  | 5/5   |
| καλα |  **Word**: καλα <br> **Root**: καλός <br> **Form**: Nominative plural neuter <br> **Meaning**: "good things" or "beautiful things" | 5/5 |
| φρουρος |  **Word**: φρουρος <br> **Root**: φρουρός <br> **Form**: Noun, masculine singular nominative <br> **Meaning**: "watcher, guard" | 5/5|
| ασμενως | **Word**: ασμενως <br> **Root**: ἄσμενος <br> **Form**: Adverb <br> **Meaning**: "gladly" or "readily" | 5/5 |
| εικοτως | **Word**: εικοτως <br> **Root**: ἔοικα <br> **Form**: Adverb <br> **Meaning**: "suitably," "fairly," or "reasonably" | 5/5 | 
| γλυκειας | **Word**: γλυκειας <br> **Root**: γλυκύς <br> **Form**: Likely genitive singular feminine of "γλυκεία" (feminine form of "sweet"). <br> **Meaning**: "of the sweet one" or "of sweetness." | 4/5| Answer as given was correct, but the qualifiers and lack of certainty cost it a point| 
| μακροις | **Word**: μακροις <br> **Root**: μακρός <br> **Form**: Dative plural <br> **Meaning**: "to the long (things)" or "to the far (places)" depending on context. | 4/5 | Did not specify gender, which in this case should have been "masculine/neuter" |
| εχει | **Word**: εχει <br> **Root**: ἔχω <br> **Form**: 3rd person singular present indicative active <br> **Meaning**: "he/she/it has" or "he/she/it holds" | 5/5|
| θαυμαζουσιν | **Word**: θαυμαζουσιν <br> **Root**: θαυμάζω <br> **Form**: Present indicative active, third person plural <br> **Meaning**: "they wonder" or "they marvel" | 5/5 |
|χρηματιζεσθαι | **Word**: χρηματιζεσθαι <br> **Root**: χρηματίζω <br> **Form**: Infinitive, middle-passive <br> **Meaning**: "to negotiate" or "to deal with financial matters," specifically in a context where one is engaging in business for personal profit. | 4/5 | Did not specify tense, in this case "present" |



### Medium Words
Medium words are less frequent, expand to all tenses and moods, and generally require more logical steps.

| **Word** | **Response** | **Score** | **Explanation**|
| -------- | ------------ | --------- | ---------------|
| σιμβλους | 
| σμηνη | **Word**: σμηνη <br> **Root**: σμήν <br> **Form**: Nominative singular feminine <br> **Meaning**: "hive" or "swarm" | 2/5| This form is the irregular plural of the neuter σμῆνος. The model was unable to arrive at this root form, and introduced σμήν, an unrelated word, without looking up the definition. 
