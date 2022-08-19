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
    - how to write ecnomic models by hal varian (interesting for ideation): [paper](https://people.ischool.berkeley.edu/~hal/Papers/how.pdf)

**How to get data**
- for B2B prjs, start by doing NRE (non-recurring engineering or consulting) work to build highly customized solutions and obtain enough data "to learn the lessons or train the models needed to build a repeatable business". Once you have built something, it is easier to find customers and scale up from there by getting more data. -- Andrew Ng
- beware data drift, concept drift, changing requirements in product specification, and esp. data cascades in AI systems so early on, set up data planning, monitoring, and maintenance code

**How to write applications for ML positions**
- [Popular DeepMind story](https://gordicaleksa.medium.com/how-i-got-a-job-at-deepmind-as-a-research-engineer-without-a-machine-learning-degree-1a45f2a781de)

**Error analysis: debugging ML models**
- (bias vs. variance problem?) Compare the error vs. the training set size to determine if you have a bias or variance problem (bias if train and test set error are similar and higher than desired level of performance and if no matter how much more data you add, your error won't come down; variance if test error is coming down as you add more training data but training error is lower than test set error). 
    - to fix high variance, use a smaller number of features, get more training examples
    - to fix high bias, try a larger set of features 
- (optimization algorithm vs. optimization objective?) between two algorithms, if J(alg1) > loss(alg2) and eval(alg1) > eval(alg2), then problem for alg2 is with optimization algorithm and could (a) run more iterations or try Newton's method; if eval(alg1) > eval(alg2) and J(alg1) <= J(alg2), then problem for alg2 is with objective function and could try using a different regularization
- (error analysis & reasoning) 
    - apply binary search to try to find where code base is failing, focus debugging efforts there (or beam search). If alg does well in simulation but not in real life, problem is with simulator; if J(human) < J(alg), then alg is problem b/c it fails to minize cost function, J; if J(human) >= J(alg), problem is in the cost fx because it doesn't correspond to good performance. 
    - (modularization). First, identify components or modules of ML algorithm. Ask, how much error is attributable to each of the components of the system? To answer, plug in ground-truth per component and see how acc changes (e.g., table of component vs. accuracy where for each component, you have perfect ground truth, e.g., manual background removal vs. algorithmic... if boost in eye segmentation with perfect vs. algorithmic is greatest, then focus on eye segmentation algo and do it cumulatively, e.g. remove background --> face detection + bg removal --> eye segmentation + face detection + bg removal, so that you can compare the marginal eval gain and not get too similar of results when doing one-by-one). 
    - (ablation studies) remove components one at a time (opposite of adding to system to see how it improves). Can do cumulatively and one-at-a-time to see where the biggest gap is and identify which features/component accounts for most of the improvement. If there is no systematic order, then try in one that makes sense

REF: Andrew Ng lecture for STanford CS229 ([YouTube video](https://www.youtube.com/watch?v=ORrStCArmP4&list=WL&index=5&t=2125s))


**How to read papers**
- [3 pass approach from Keshav](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf)
    1. read intro/conclusions to get the gist of the paper and understand whether category, context, contributions, conclusions, clarity
    2. understand results carefully
    3. virtually re-implement paper
- [why reading papers makes you a better data scientist](https://eugeneyan.com/writing/why-read-papers/)
- [mindset](https://www.eecs.harvard.edu/~michaelm/postscripts/ReadPaper.pdf)

**Ideation**
1. talk to researchers in other fields
2. code simple baselines to better understand problems
3. extend the experiments systematically from a paper you like
4. Hal Varian's tips to read non-academic literature for inspiration
5.  

Some ideas from Tom Silver (see blog post [here](https://web.mit.edu/tslvr/www/lessons_two_years.html))


# notation & style

## coding
- [PEP 8](https://www.python.org/dev/peps/pep-0008/)
- pytorch data pipeline; a few [cheat-sheets:](https://stanford.edu/~shervine/teaching/)
    - create unique identifiers, store these in the trainer class as a dictionary, e.g., `partition['train']` and a labels AND metadata dictionary where the keys are these unique identifiers; this way, you just need to pass the train IDs to the built-in data loader (mapping dataset). Can even save data as a tensor `.pt` file and load it. 

# References
1. [summary](https://www.quora.com/How-can-I-publish-papers-in-NIPS-ICML-AAAI-IJCAI-I-dont-know-how-to-get-the-novel-ideas) of Andrew Ng's lecture
2. Guidelines for writing a good NIPS paper, published in 2015 (see [here](https://nips.cc/Conferences/2015/PaperInformation/EvaluationCriteria))
3. Richard Hamming's bro-y recommendations (see "You and Your Research, [here](https://www.cs.virginia.edu/~robins/YouAndYourResearch.html))
4. Hannah Arendt
