- [Papers](#papers)
  - [2021](#2021)
  - [2020](#2020)
  - [2019](#2019)
- [TODOS](#todos)
  - [2021](#2021-1)
  - [2019](#2019-1)
  - [2018](#2018)
  - [Earlier](#earlier)

This is a paper reading list on Document level Relation Extraction.

Our list is still incomplete and the categorization might be inappropriate. We will keep adding papers and improving the list. Any suggestions are welcomed!

## Papers

### 2021

* AAAI 2021 [Document-Level Relation Extraction with Reconstruction](https://arxiv.org/abs/2012.11384), Wang Xu, Kehai Chen, Tiejun Zhao
  <br> 👉 Method: build a graph like EoG, use LSTM to calculate the probability of "inference meta path", then maximize the probability of relationed entity pairs using BCE

* AAAI 2021 [Document-Level Relation Extraction with Adaptive Thresholding and Localized Context Pooling](https://arxiv.org/abs/2010.11304), Wenxuan Zhou, Kevin Huang, Tengyu Ma, Jing Huang
  <br> 👉 Method: improve BERT with marker, log-sum-exp pooling, group bilinear + adaptive threshold class + directly use transformer's attn matrix to aggregation words into doc representation

* AAAI 2021 Entity Structure Within and Throughout: Modeling Mention Dependencies for Document- Level Relation Extraction, Benfeng Xu, Quan Wang, Yajuan Lyu, Yong Zhu, Zhendong Mao

* AAAI 2021 [Multi-view Inference for Relation Extraction with Uncertain Knowledge](https://www.researchgate.net/publication/347879225_Multi-view_Inference_for_Relation_Extraction_with_Uncertain_Knowledge), Bo Li, Wei Ye, Canming Huang, Shikun Zhang
  <br> 👉 Method: use KG concept knowledges: 3 attention aggregation(e2c, c2e, m2e) to get contextual and global entity pair representation, another attention aggregation to get sentence representation, concat for final classification

* arXiv 2021 [BERT-GT: Cross-sentence n-ary relation extraction with BERT and Graph Transformer](https://arxiv.org/abs/2101.04158), Po-Ting Lai, Zhiyong Lu
  <br> 👉 Method: densely connect Graph Transformer(neighbor attention) & Transformer to improve BERT

* arXiv 2021 [MrGCN: Mirror Graph Convolution Network for Relation Extraction with Long-Term Dependencies](http://arxiv.org/abs/2101.00124), Xiao Guo, I-Hung Hsu, Wael AbdAlmageed, Premkumar Natarajan, Nanyun Peng
  <br> 👉 Method: pooling-unpooling after GCN layers to enlarge receptive field (like u-net)

### 2020

* ACL 2020 [Reasoning with Latent Structure Refinement for Document-Level Relation Extraction](https://arxiv.org/abs/2005.06312), Guoshun Nan, Zhijiang Guo, Ivan Sekulić, Wei Lu
  <br> 👉 Method: Latent Structure + DCGCN

* EMNLP 2020 [Double Graph Based Reasoning for Document-level Relation Extraction](https://arxiv.org/abs/2009.13752), Shuang Zeng, Runxin Xu, Baobao Chang, Lei Li
  <br> 👉 Method: Mention graph(mention + doc node) + entity graph (2-hot at most)

* EMNLP 2020 [Global-to-Local Neural Networks for Document-Level Relation Extraction](https://www.aclweb.org/anthology/2020.emnlp-main.303), Difeng Wang, Wei Hu, Ermei Cao, Weijian Sun
  <br> 👉 Method: EoG + R-GCN + entity-pair attention

* EMNLP 2020 [Denoising Relation Extraction from Document-level Distant Supervision](https://arxiv.org/abs/2011.03888), Chaojun Xiao, Yuan Yao, Ruobing Xie, Xu Han, Zhiyuan Liu, Maosong Sun, Fen Lin, Leyu Lin
  <br> 👉 Method: using DS data to pre-train model for DocRE with 3 tasks: Mention-Entity Matching, Relation Detection, Relational Fact Alignment

* COLING 2020 [Graph Enhanced Dual Attention Network for Document-Level Relation Extraction](https://www.aclweb.org/anthology/2020.coling-main.136/),Bo Li, Wei Ye, Zhonghao Sheng, Rui Xie, Xiangyu Xi, Shikun Zhang
  <br> 👉 Method: bi-directional attn between sentence & relation instance + attn duality + support evidence guide

* COLING 2020 [Global Context-enhanced Graph Convolutional Networks for Document-level Relation Extraction](https://www.aclweb.org/anthology/2020.coling-main.461/), Huiwei Zhou, Yibin Xu, Zhe Liu, Weihong Yao, Chengkun Lang, Haibin Jiang
  <br> 👉 Method: entity graph with attn gate & attn adj matrix for entity representation + entity graph with multi-head attn as adj matrix for reasoning + dense-node&edge-GCN

* COLING 2020 [Document-level Relation Extraction with Dual-tier Heterogeneous Graph](https://www.aclweb.org/anthology/2020.coling-main.143/), Zhenyu Zhang, Bowen Yu, Xiaobo Shu, Tingwen Liu, Hengzhu Tang, Yubin Wang and Li Guo
  <br> 👉 Method: strcuct modeling graph + relation reasoning graph + weighted RGCN

* PAKDD 2020 [HIN: Hierarchical Inference Network for Document-Level Relation Extraction](https://arxiv.org/abs/2003.12754), Hengzhu Tang, Yanan Cao, Zhenyu Zhang, Jiangxia Cao, Fang Fang, Shi Wang, Pengfei Yin
  <br> 👉 Method: Hierarchical (entity & document level) inference representation (using LSTMs, attention and all kinds of "concat") for an entity pair's representation

* arXiv 2020 [Coarse-to-Fine Entity Representations for Document-level Relation Extraction](https://arxiv.org/abs/2012.02507), Damai Dai, Jing Ren, Shuang Zeng, Baobao Chang, Zhifang Sui
  <br> 👉 Method: a word graph for coarse representation, Bi-GRU for path encoding, and an attention aggregator

* arXiv 2020 [Entity and Evidence Guided Relation Extraction for DocRED](https://arxiv.org/abs/2008.12283), Kevin Huang, Guangtao Wang, Tengyu Ma, Jing Huang

* IEEE Access 2020 [A Novel Document-Level Relation Extraction Method Based on BERT and Entity Information](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9098945), Xiaoyu Han and Lei Wang
  <br> 👉 Method: using marker to wrap mention as {[entity type] mention [entity X]}, then using BERT + bilinear

### 2019

* NAACL 2019 [Document-Level N-ary Relation Extraction with Multiscale Representation Learning](https://arxiv.org/abs/1904.02347), Robin Jia, Cliff Wong, Hoifung Poon
  <br> 👉 Method: multioscale representation of mention and entity: lstm for paragraph-level mention representation, log-sum-exp pooling for entity representation

* EMNLP 2019 [Connecting the Dots: Document-level Neural Relation Extraction with Edge-oriented Graphs](https://arxiv.org/abs/1909.00228), Fenia Christopoulou, Makoto Miwa, Sophia Ananiadou, EMNLP 2019
  <br> 👉 Method: Edge-oriented graph + Iterative Inference Mechanism

* ACL 2019 [Inter-sentence Relation Extraction with Document- level Graph Convolutional Neural Network](https://www.aclweb.org/anthology/P19-1423/), Sunil Kumar Sahu, Fenia Christopoulou, Makoto Miwa, and Sophia Ananiadou
  <br> 👉 Method: GCN + bi-affine classification

* ACL 2019 [Attention Guided Graph Convolutional Networks for Relation Extraction](https://www.aclweb.org/anthology/P19-1024.pdf), Zhijiang Guo, Yan Zhang, Wei Lu
  <br> 👉 Method: muoti-head attention to get multi graph with different adj matrix + dense GCN

* arXiv 2019 [Fine-tune Bert for DocRED with Two-step Process](https://arxiv.org/abs/1909.11898), Hong Wang, Christfried Focke, Rob Sylvester, Nilesh Mishra, William Wang
  <br> 👉 Method: BERT + bilinear, 2 step training: binary classification for relation detection, then multi classification for relation type

## TODOS

Didn't read yet, but the title is somewhat relevant to DocRE.

### 2021

* Two Training Strategies for Improving Relation Extraction over Universal Graph
Qin Dai, Naoya Inoue, Ryo Takahashi and Kentaro Inui, EACL 2021

### 2019

* Robin Jia, Cliff Wong, and Hoifung Poon. 2019. Document-level n-ary relation extraction with mul- tiscale representation learning. In Proceedings of the 2019 Conference of the North American Chap- ter of the Association for Computational Linguistics, pages 3693–3704.
* Gupta, P.; Rajaram, S.; Schu ̈tze, H.; and Runkler, T. A. 2019. Neural Relation Extraction within and across Sen- tence Boundaries. In AAAI 2019, 6513–6520.
* Zhijiang Guo, Yan Zhang, and Wei Lu. Atten- tion guided graph convolutional networks for rela- tion extraction. ACL 2019
* Ningyu Zhang, Shumin Deng, Zhanlin Sun, Guanying Wang, Xi Chen, Wei Zhang, and Huajun Chen. 2019. Long-tail relation extraction via knowledge graph embeddings and graph convolution networks. In NAACL-HLT, pages 3016–3025, Minneapolis, MN, USA. ACL.
* Ming Tu, Guangtao Wang, Jing Huang, Yun Tang, Xi- aodong He, and Bowen Zhou. 2019. Multi-hop read- ing comprehension across multiple documents by reasoning over heterogeneous graphs. In Proc. of ACL.
* Bill Yuchen Lin, Xinyue Chen, Jamin Chen, and Xi- ang Ren. 2019. Kagnet: Knowledge-aware graph networks for commonsense reasoning. In Proc. of EMNLP.
* Nicola De Cao, Wilker Aziz, Ivan Titov. Question Answering by Reasoning Across Documents with Graph Convolutional Networks. NAACL 2019.
* Yu Cao, Meng Fang, and Dacheng Tao. 2019. Bag: Bi-directional attention entity graph convolutional network for multi-hop reasoning question answering. In Proc. of NAACL.
* Hao Zhu, Yankai Lin, Zhiyuan Liu, Jie Fu, Tat-seng Chua, and Maosong Sun. 2019. Graph Neural Networks with Generated Parameters for Relation Extraction. ACL 2019


### 2018

* Linfeng Song, Yue Zhang, Zhiguo Wang, and Daniel Gildea. 2018c. N-ary relation extraction using graph state lstm. In Proc. of EMNLP.
* Patrick Verga, Emma Strubell, and Andrew McCallum. 2018. Simultaneously self-attending to all mentions for full-abstract biological relation extraction. In Proc. of NAACL-HLT.
* Yuhao Zhang, Peng Qi, and Christopher D Manning. 2018. Graph convolution over pruned dependency trees improves relation extraction. In EMNLP, pages 2205–2215, Brussels, Belgium. ACL.
* Wei Zheng, Hongfei Lin, Zhiheng Li, Xiaoxia Liu, Zhengguang Li, Bo Xu, Yijia Zhang, Zhihao Yang, and Jian Wang. 2018. An effective neural model extracting document level chemical-induced disease relations from biomedical literature. Journal of Biomedical Informatics, 83:1–9.
* Rasmus Palm, Ulrich Paquet, Ole Winther. Recurrent Relational Networks. NeurIPS 2018.
* Dat Quoc Nguyen and Karin Verspoor. Convolutional neural networks for chemical-disease relation extraction are improved with character-based word embeddings. BioNLP 2018
* Christopoulou, F.; Miwa, M.; and Ananiadou, S. 2018. A Walk-based Model on Entity Graphs for Relation Extraction. In ACL.


### Earlier

* Nanyun Peng, Hoifung Poon, Chris Quirk, Kristina Toutanova, and Wen-tau Yih. 2017. Cross-sentence n-ary relation extraction with graph LSTMs. Trans- actions of the Association for Computational Lin- guistics, 5:101–115.
* Chris Quirk and Hoifung Poon. 2017. Distant super- vision for relation extraction beyond the sentence boundary. In Proceedings of the 15th Conference of the European Chapter of the Association for Compu- tational Linguistics: Volume 1, Long Papers, pages 1171–1182.
* Wenyuan Zeng, Yankai Lin, Zhiyuan Liu, and Maosong Sun. 2017. Incorporating relation paths in neural relation extraction. In Proceedings of the Conference on Empirical Methods in Natural Lan- guage Processing, pages 1768–1777. Association for Computational Linguistics.
