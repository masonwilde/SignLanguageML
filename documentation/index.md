# Sign Language ML Research (A Beginner's Guide)

Disclaimer: A lot of this will center around American Sign Language as sign language across the world is as diverse if not more so than spoken language.

## Resources

### Existing Attempts

* [Signapse](https://www.signapse.ai/)
* [Slait](https://slait.ai/)
* [Signer](https://signer.ai/)
* [Shuwa](https://blog.google/outreach-initiatives/accessibility/ml-making-sign-language-more-accessible/)

### Research

* [1][Modelling and Recognition of the Linguistic Components in American Sign Language](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2757299/)
* 

## Main Questions

* What is the best ML model to train?
  * Likely a Neural Net...
   
* What kind of data needs to be collected to train on?
  * Components of Sign Language
    * Primary Components [[1]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2757299/)
      * Hand Shape
      * Hand Motion
      * Place of Articulation
      * Palm Orientation
    * Other Components
      * Facial Expression
      * Body Language

* How diverse should initial data be?
  * Ideally, a full model would be trained across many dialects, and signer backgrounds.
    * Likely, one would want to train a separate model for each language.
    * Possible to train a base model for [fine-tuning](https://stats.stackexchange.com/questions/331369/what-is-meant-by-fine-tuning-of-neural-network) or other [transfer learning](https://en.wikipedia.org/wiki/Transfer_learning#:~:text=Transfer%20learning%20(TL)%20is%20a,when%20trying%20to%20recognize%20trucks.)
* For a proof-of-concept, restricting an initial model to training data from a single, easily-available, language/dialect would likely be best.
  * Personally, I would start with one person signing ASL, and try to train a basic model, recognizing that it would only model that individual's signing style. This would only require contracting one person for X hours of signing whatever format I required.
    * Next, I would expand to more people within ASL to ideally capture different dialects and signer backgrounds. Specifically including native-ASL signers and people who learned it as a non-native language.
    * Once that was proven, I would expand to further edge-cases (signers who know multiple sign languages)
    * Once the training model was shown to be effective as a general ASL model, I would expand to other languages.
