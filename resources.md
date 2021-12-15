# fields

## single_cell
* Updated [list](https://github.com/mdozmorov/scRNA-seq_notes#differential-expression) of tools for scRNA-seq analysis

# textbooks

1. Dive into DL https://d2l.ai/index.html
2. Deep learning. Goodfellow et al. 2016
3. Statistical learning. Tibshirani et al. 2014
4. Deep learning with PyTorch, [pdf here](https://pytorch.org/assets/deep-learning/Deep-Learning-with-PyTorch.pdf)
5. Introduction to Algorithms, MIT Press
6. concepts in software engineering: Design patterns : elements of reusable object-oriented software and Code Complete (Developer Best Practices) and Docker for Data Scientists
7. Cracking the coding interview by Gayle Laakmann, https://github.com/ml874/Cracking-the-Data-Science-Interview
8. Mathematics of deep learning, https://github.com/mml-book/mml-book.github.io
9. Python ML (online) https://github.com/rasbt/python-machine-learning-book-2nd-edition
10. Graph representation learning book, https://www.cs.mcgill.ca/~wlh/grl_book/
11. ML and interpretability (book), https://christophm.github.io/interpretable-ml-book/simple.html 
12. Deep learning for coders with fastai & Pytorch
13. Deep learning in production (pre-book), https://github.com/The-AI-Summer/Deep-Learning-In-Production
14. Flask for Web Development, O'Reilly
15. Draft on learning theory: https://francisbach.com/i-am-writing-a-book/
16. Cormen et al. Introduction to Algorithms, MIT Press, 2009
17. for time series basics: "Forecasting: Principles and Practice", https://otexts.com/fpp3/
18. Natural Language Processing w/Python: http://www.nltk.org/book_1ed/
19. Practical Time Series Analysis by Aileen Nielsen [yale library link](https://learning.oreilly.com/library/view/practical-time-series/9781492041641/?sso_link=yes&sso_link_from=yale-university); [stanford lib link](https://searchworks.stanford.edu/view/12744528)
20. Geometric Deep Learning book by Bronstein, Taco Cohen, and Petar: https://arxiv.org/abs/2104.13478
21. Graph Algorithms, by Needham & Hodler (stanford library, https://searchworks.stanford.edu/view/13317193)

# courrses
- Yann Lecun's DL course @NYU: https://cds.nyu.edu/deep-learning/


# topics

## reproducibility
- ML reproducibility checklist, v2.0: https://www.cs.mcgill.ca/~jpineau/ReproducibilityChecklist.pdf

# code

## time-series
- https://github.com/okrasolar/pytorch-timeseries
- InceptionTime implementation: https://github.com/TheMrGhostman/InceptionTime-Pytorch
- 

# data

## ML
- https://paperswithcode.com/datasets
- https://datasetsearch.research.google.com/


## bio
- see Table 2 for single-cell data that can be used for drug discovery and "perturbation modeling", https://doi.org/10.1016/j.cels.2021.05.016
- open data collection organized by *Scientific Data*: https://www.nature.com/collections/ebaiehhfhg
- TorchDrug (DL drug discovery environment): https://torchdrug.ai/?fbclid=IwAR19V66qAdaI3FOBlVfXy6oFPH4va4hVdwy1U5vbFB9S7ShfXb9W2LhwAd8
- protein localization and interaction partners (by mass-spec pull down of mNG) in HEK cells: https://opencell.czbiohub.org/

# activism

- organizing, pol.is (https://pol.is/home) and decidim (https://decidim.org/)
- https://github.com/philsturgeon/awesome-earth


# settings
- **figures** constructed in python: 
```
plt.rc('font', size = 9)
plt.rc('font', family='sans serif')
plt.rcParams['pdf.fonttype']=42
plt.rcParams['ps.fonttype']=42
plt.rcParams['legend.frameon']=False
plt.rcParams['axes.grid']=False
plt.rcParams['legend.markerscale']=0.5
plt.rcParams['savefig.dpi']=600
sns.set_style("ticks")
```
