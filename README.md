# Multitask Learning for Emotionally Analyzing Sexual Abuse Disclosures


<br>
<p align="center">
  <img src="https://github.com/midas-research/bhaav/blob/master/MIDAS-logo.jpg" alt="MIDAS lab at IIIT-Delhi"  width="60%"/>
  <br>
</p>
<br>


This repository contains code for the paper ```Multitask Learning for Emotionally Analyzing Sexual Abuse Disclosures``` accepted at the proceddings of NAACL-HLT 2021 as a long paper. In a first of its kind work we jointly model the tasks related to identifying linguistic behaviours of #MeToo movement along with emotional attributes of the text. In this work we also propose a flexible cross-stiched paramter sharing architecture which takes advantage of both hard parameter sharing and soft paramater sharing for task specific settings. This allows both the models to have their own set of parameters while also encouraging knowledge transfer via the shared encoder weights. 

<br>
<p align="center">
  <img src="https://github.com/midas-research/metoo-mtl-naacl/blob/master/main_diag.png" alt="Flexible Cross Stiched Parameter Sharing Architecture"  width="60%"/>
  <br>
</p>
<br>

Please follow these links for more information,
- Paper: https://aclanthology.org/2021.naacl-main.387.pdf
- Blog: https://medium.com/geekculture/multitask-learning-approach-for-identifying-online-sexual-abuse-disclosure-narratives-32b80413b6f6



## Datasets 
In our work, we use two datasets which have been mined from the same source -- Twitter:
1. **MeTooMA**, consisting of tweets pertaining to the MeToo movement on social media platforms. Thw tweets have been various linguistic behaviours such as (directed-hate, generalized-hate, sarcasm, justification, refuation, support, oppose, relevance). The dataset details, collection methadology, pre-processing information, and instructions to access are present [here](https://github.com/midas-research/MeTooMA).
2. **SemEval 2018**, consists of tweets representing mental state of the authors in the form of emotions distributed into 11 distinct labels. The details of this dataset are present [here](https://competitions.codalab.org/competitions/17751).

## Text Embeddings
We use [BERTweet](https://github.com/VinAIResearch/BERTweet) embeddings in our work and provide the same for both the datasets in the ```Embeddings``` folder. The key component in transformer based models is the token level self attention that enables them to generate dynamic contextualized embeddings as opposed to the static embeddings of GloVe. Please follow the paper link for more details. 

## Experiments, Results and Discussions
The code and their explanation for all the experiments are present in the Jupyter Notebook. We document interesting findings, resuts, discussions and qualitative analysis in the manuscript.

<br>
<p align="center">
  <img src="https://github.com/midas-research/metoo-mtl-naacl/blob/master/result1.png" alt="Flexible Cross Stiched Parameter Sharing Architecture"  width="60%"/>
  <br>
</p>
<br>


<br>
<p align="center">
  <img src="https://github.com/midas-research/metoo-mtl-naacl/blob/master/result2.png" alt="Flexible Cross Stiched Parameter Sharing Architecture"  width="60%"/>
  <br>
</p>
<br>

## Terms of Use

1. This work can be used freely for research purposes.
2. The paper listed below provide details of this work. If you use the expirements, then please cite the paper.
3. If interested in commercial use of the corpus, send email to midas@iiitd.ac.in.
4. If you use the corpus in a product or application, then please credit the authors and [Multimodal Digital Media Analysis Lab - Indraprastha Institute of Information Technology, New Delhi](http://midas.iiitd.edu.in) appropriately. Also, if you send us an email, we will be thrilled to know about how you have used the corpus.
5. Multimodal Digital Media Analysis Lab - Indraprastha Institute of Information Technology, New Delhi, India disclaims any responsibility for the use of the corpus and does not provide technical support. However, the contact listed above will be happy to respond to queries and clarifications.
6. Rather than redistributing the corpus, please direct interested parties to this [page](https://github.com/midas-research/MeTooMA)
7. To provide feedback or report any issues in the code, please drop an email [here](mailto:jaintaru@ieee.org)

Please feel free to send us an email:
- with feedback regarding the corpus.
- with information on how you have used the corpus.
- if interested in having us analyze your social media data.
- if interested in a collaborative research project.

Copyright (C) 2019 Multimodal Digital Media Analysis Lab - Indraprastha Institute of Information Technology, New Delhi (MIDAS, IIIT-Delhi)


## References

Please cite this paper if you feel the relevant resources in this repository are useful.

```
@inproceedings{sawhney-etal-2021-multitask,
    title = "Multitask Learning for Emotionally Analyzing Sexual Abuse Disclosures",
    author = "Sawhney, Ramit  and
      Mathur, Puneet  and
      Jain, Taru  and
      Gautam, Akash Kumar  and
      Shah, Rajiv Ratn",
    booktitle = "Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies",
    month = jun,
    year = "2021",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2021.naacl-main.387",
    pages = "4881--4892",
    abstract = "The {\#}MeToo movement on social media platforms initiated discussions over several facets of sexual harassment in our society. Prior work by the NLP community for automated identification of the narratives related to sexual abuse disclosures barely explored this social phenomenon as an independent task. However, emotional attributes associated with textual conversations related to the {\#}MeToo social movement are complexly intertwined with such narratives. We formulate the task of identifying narratives related to the sexual abuse disclosures in online posts as a joint modeling task that leverages their emotional attributes through multitask learning. Our results demonstrate that positive knowledge transfer via context-specific shared representations of a flexible cross-stitched parameter sharing model helps establish the inherent benefit of jointly modeling tasks related to sexual abuse disclosures with emotion classification from the text in homogeneous and heterogeneous settings. We show how for more domain-specific tasks related to sexual abuse disclosures such as sarcasm identification and dialogue act (refutation, justification, allegation) classification, homogeneous multitask learning is helpful, whereas for more general tasks such as stance and hate speech detection, heterogeneous multitask learning with emotion classification works better.",
}
```





