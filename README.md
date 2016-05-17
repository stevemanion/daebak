# Daebak!

This project provides tools for conducting graph-based [Word Sense Disambiguation](https://en.wikipedia.org/wiki/Word-sense_disambiguation "Wikipedia Page for Word Sense Disambiguation") and [Entity Linking](https://en.wikipedia.org/wiki/Entity_linking "Wikipedia Page for Entity Linking"). It uses [BabelNet](http://babelnet.org/) which is a fusion of [WordNet](https://wordnet.princeton.edu/ "WordNet Home Page") and [Wikipedia](https://en.wikipedia.org/wiki/Main_Page "Wikipedia English Home Page"), among other lexical knowledge bases.


Also provided in this project is the code necessary to reproduce results from the project's publications, this primarily includes:

1. Highly competitive submissions to SemEval disambiguation tasks in [SemEval 2013](http://wwwusers.di.uniroma1.it/~navigli/pubs/Semeval_2013_Navigli_etal.pdf "SemEval-2013 Task 12: Multilingual Word Sense Disambiguation") as team **_DAEBAK!_** and [SemEval 2015](http://www.aclweb.org/anthology/S15-2049 "SemEval-2015 Task 13: Multilingual All-Words Sense Disambiguation and Entity Linking") as team **_SUDOKU_**.
2. Experiments completed that demonstrate treating WSD and EL as an _iterative_ and _interactive_ Sudoku-like problem  as beneficial over _conventional_ disambiguation (_see_ [Manion & Sainudiin 2014](http://stevemanion.com/pdfs/Manion&Sainudiin2014(StarSEM).pdf "An Iterative “Sudoku Style” Approach to Subgraph-based Word Sense Disambiguation")).

## Project  Publications

* Manion, S. L. (2015).  [SUDOKU: Treating Word Sense Disambiguation & Entity Linking as a Deterministic Problem – via an Unsupervised & Iterative Approach](http://stevemanion.com/pdfs/Manion2015(SemEval-Task13).pdf "SUDOKU: Treating Word Sense Disambiguation & Entity Linking as a Deterministic Problem – via an Unsupervised & Iterative Approach"). In Proceedings of the 9th International Workshop on Semantic Evaluation (SemEval-2015) (pp. 365–369). Denver, Colorado.

* Manion, S. L. (2014).  [Unsupervised Knowledge-based Word Sense Disambiguation: Exploration & Evaluation of Semantic Subgraphs](http://stevemanion.com/pdfs/SteveLawrenceManion2014(PhD-Thesis).pdf "Unsupervised Knowledge-based Word Sense Disambiguation: Exploration & Evaluation of Semantic Subgraphs") PhD Thesis, University of Canterbury.

* Manion, S. L., & Sainudiin, R. (2014).  [An Iterative “Sudoku Style” Approach to Subgraph-based Word Sense Disambiguation](http://stevemanion.com/pdfs/Manion&Sainudiin2014(StarSEM).pdf "An Iterative “Sudoku Style” Approach to Subgraph-based Word Sense Disambiguation"). In Proceedings of the 3rd Joint Conference on Lexical and Computational Semantics (*SEM’14) (pp. 40–50). Dublin, Ireland.

* Manion, S. L., & Sainudiin, R. (2013).  [DAEBAK!: Peripheral Diversity for Multilingual Word Sense Disambiguation](http://stevemanion.com/pdfs/Manion&Sainudiin2013(SemEval-Task12).pdf "DAEBAK!: Peripheral Diversity for Multilingual Word Sense Disambiguation"). In Proceedings of the 7th International Workshop on Semantic Evaluation (SemEval-2013), in conjunction with the Second Joint Conference on Lexical and Computational Semantics (*SEM’13) (pp. 250–254). Atlanta, Georgia.


## Getting Started

### Project Build ###
First install Java 1.7.x and Maven 3.x or later versions. Clone this project, navigate to its location via the command line, then run the following Maven command:

```
mvn package
```

This should acquire all the project dependencies from the project's ```../pom.xml``` file.

### Local BabelNet Jars ###
Since the ```babelnet-api``` and ```jlt``` jars are not managed on Maven, they are included locally for this project with ```babelnet-api-2.5.1.jar``` as the default version. If you wish to use an alternative version of BabelNet simply point to another jar in the ```../pom.xml``` file of this project, by modifying the following line:

```
<systemPath>${basedir}/src/main/resources/localjar/babelnet-api-2.5.1.jar</systemPath>
```

The versions ```1.1.1```, ```2.5.1```, and ```3.0``` of BabelNet can be found in ```../resources/localjar/```. For additional versions of the BabelNet API you will need to acquire the jar and point to its location via the ```../pom.xml``` file.


### Property Files ###
All the default property files of the BabelNet project are included under ```../resources/```, with the addition of the property file ```../resources/daebak.properties``` that defines input parameters specific to this project.


