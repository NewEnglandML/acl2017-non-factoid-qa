# End-to-End Non-Factoid Question Answering with an Interactive Visualization of Neural Attention Weights

This project contains multiple components that, together, build an end-to-end question answering system. 
A special emphasis lies on the visualization and interactive comparison of neural attention weights. 

Please use the following citation:

```
@InProceedings{rueckle:2017:ACL,
  title = {End-to-End Non-Factoid Question Answering with an Interactive Visualization of Neural Attention Weights},
  author = {R{\"u}ckl{\'e}, Andreas and Gurevych, Iryna},
  publisher = {Association for Computational Linguistics},
  booktitle = {Proceedings of the 55th Annual Meeting of the Association for Computational Linguistics (ACL 2017)},
  pages = {(to appear)},
  month = aug,
  year = {2017},
  location = {Vancouver, Canada}
}
```

> **Abstract:** Advanced attention mechanisms are an important part of successful neural network approaches for non-factoid answer selection because they allow the models to focus on few important segments within rather long answer texts. Analyzing attention mechanisms is thus crucial for understanding strengths and weaknesses of particular models. We present an extensible, highly modular service architecture that enables the transformation of neural network models for non-factoid answer selection into fully featured end-to-end question answering systems. The primary objective  of our system is to enable researchers a way to interactively explore and compare attention-based neural networks for answer selection. Our interactive user interface helps researchers to better understand the capabilities of the different approaches and can aid qualitative analyses.


Contact person: Andreas Rücklé

https://www.ukp.tu-darmstadt.de/

https://www.tu-darmstadt.de/


Don't hesitate to send us an e-mail or report an issue, if something is broken (and it shouldn't be) or if you have further questions.

> This repository contains experimental software and is published for the sole purpose of giving additional background details on the respective publication. 


## Project structure

This repository contains the three sub-projects as described in the related paper:

  - __Candidate-Retrieval:__ Indexes all answers of a data source and allows to find answers with lexical overlap to a question
  - __Candidate-Ranking:__ Contains a framework to train neural network models for answer-selection. Contains a webservice that allows to re-rank answers in regard to their relevance to a given question. 
  - __QA-Frontend:__ The webfrontend that allows the user to ask questions and retrieve answers. All results will contain neural attention weights which researchers can view, inspect, and compare.

Each individual project has its own installation instructions in separate readme files. It is also possible to install each service on a separate machine, because the services communicate over HTTP. 

To setup the project, it makes sense to first install and run the Candidate-Retrieval application, afterwards setup and train a simple neural network with the Candidate-Ranking, and finally install the QA-Frontend to pull everything together.
  