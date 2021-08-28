## Tips

**How to do ML research**
- read recent papers in research area to get an understanding of the current problems and how to communicate it with the intended audience (authors of those papers)
- reproduce results of those papers and then implement their method for data you're interested in
- do the data science dirty work to make sure there is no stone unturned for end-to-end understanding of research solutions
- doing the above 3 things ensures that we'll make opinions about the problem, "which can result in a workable idea"
- ambitions for any research product is to produce ML papers that could in theory be highly judged by a NIPS-like mindset... from their guidelines: ML papers will be judged on at least five criteria: (1) novelty of algorithm, e.g., a new and elegant derivation for an algorithm or a new approach to an existing problem; (2) novelty of the application or problem, e.g., one that introduces a novel ML problem like ICA and structured prediction and that proposes an algorithm for it; (3) difficulty of the application, e.g., an application of ML to a difficult, important, and "real" application that takes into account the full complexity of getting a non-trivial system to work; (4) quality of results; (5) insight conveyed, e.g., whether paper conveys insight into the nature of an algo, the nature of a practical application or problem, or that conveys general lessons and theoretical or mathematical tools that will be used by others in future work
- From a [reddit post](https://www.reddit.com/r/MachineLearning/comments/p88v9w/d_we_are_facebook_ai_researchs_nethack_learning/) by Edward Grefenstette
    ```
    - Don’t try to read and understand everything. There’s too much stuff coming out even on individual topics. Be curious, but don’t try to be a completionist.
    - Become good at implementing models, training and evaluation loops, with good logging practices and a clear way of varying hyper-parameters. Don’t over-engineer your codebases (research code is often best thrown away after a few weeks/months). In learning to do this, through practice, you will reduce the effect of the unseen force that often blocks us from immediately going from a cool idea we’ve just had to implementing and experimenting with it.
    - Most papers make honest mistakes. Most methods make simplifying assumptions. Most approaches don’t necessarily apply as generally as the authors claim. Find out where things break, then find out why they break, then improve things. You can build a good research career over just doing this over and over.
    ```

**How to get data**
- for B2B prjs, start by doing NRE (non-recurring engineering or consulting) work to build highly customized solutions and obtain enough data "to learn the lessons or train the models needed to build a repeatable business". Once you have built something, it is easier to find customers and scale up from there by getting more data. -- Andrew Ng
- beware data drift, concept drift, changing requirements in product specification, and esp. data cascades in AI systems so early on, set up data planning, monitoring, and maintenance code

# References
1. [summary](https://www.quora.com/How-can-I-publish-papers-in-NIPS-ICML-AAAI-IJCAI-I-dont-know-how-to-get-the-novel-ideas) of Andrew Ng's lecture
2. Guidelines for writing a good NIPS paper, published in 2015 (see [here](https://nips.cc/Conferences/2015/PaperInformation/EvaluationCriteria))
3. Richard Hamming's bro-y recommendations (see "You and Your Research, [here](https://www.cs.virginia.edu/~robins/YouAndYourResearch.html))
4. Hannah Arendt
