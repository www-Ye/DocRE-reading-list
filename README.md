
This is a paper reading list on Document level Relation Extraction.

Our list is still incomplete and the categorization might be inappropriate. We will keep adding papers and improving the list. Any suggestions are welcomed!

### Datasets

* DocRED, CDR, GDA

## Doc RE Papers

### 2021

1. EMNLP 2021. [Learning Logic Rules for Document-level Relation Extraction](https://aclanthology.org/2021.emnlp-main.95/). Dongyu Ru, Changzhi Sun, Jiangtao Feng, Lin Qiu, Hao Zhou, Weinan Zhang, Yong Yu, Lei Li.

1. EMNLP 2021. [Modular Self-Supervision for Document-Level Relation Extraction](https://arxiv.org/pdf/2109.05362). Sheng Zhang, Cliff Wong, Naoto Usuyama, Sarthak Jain, Tristan Naumann, Hoifung Poon.
  <br> 👉 Method: Decompose document-level relation extraction into relation detection and argument resolution.

1. ACL 2021. [Three Sentences Are All You Need — Local Path Enhanced Document Relation Extraction](https://arxiv.org/abs/2106.01793), [code](https://github.com/AndrewZhe/Three-Sentences-Are-All-You-Need). Quzhe Huang, Shengqi Zhu, Yansong Feng, Yuan Ye, Yuxuan Lai and Dongyan Zhao.
  <br> 👉 Method: Using huristic rules to select at most 3 sentences for an entity pair

1. ACL 2021 Findings. [SIRE: Separate Intra- and Inter-sentential Reasoning for Document-level Relation Extraction](https://arxiv.org/abs/2106.01709), [code](https://github.com/DreamInvoker/SIRE). Shuang Zeng, Yuting Wu, Baobao Chang.
  <br> 👉 Method: Seperate intra and inter relations: for intra, using sentence for mention pair representation, then aggregate all the mention pairs to entity pair representation; for inter, using the graph in GAIN. Furthermore, a novel logical reasoning method is used.

1. ACL 2021 Findings. [Discriminative Reasoning for Document-level Relation Extraction](https://arxiv.org/abs/2106.01562), [code](https://github.com/xwjim/DRN). Wang Xu, Kehai Chen, Tiejun Zhao.
  <br> 👉 Method: Represent 3 types of paths for each relation pair, the paths including: intra-sentence reasoning path, logical reasoning path, and coreference reasoning path.

1. ACL 2021 Findings. [MRN: A Locally and Globally Mention-Based Reasoning Network for Document-Level Relation Extraction](https://aclanthology.org/2021.findings-acl.117.pdf). Jingye Li, Kang Xu, Fei Li, Hao Fei, Yafeng Ren and Donghong Ji.

1. EACL 2021. [An End-to-end Model for Entity-level Relation Extraction using Multi-instance Learning](https://arxiv.org/abs/2102.05980). Markus Eberts, Adrian Ulges.
  <br> 👉 Method: a model for JOINT mention detection and doc RE: finetune BERT for 4 tasks: entity mention localization, coreference resolution, entity classification and relation classification

1. IJCAI 2021. [Document-level Relation Extraction as Semantic Segmentation](https://arxiv.org/abs/2106.03618), [code](https://github.com/zjunlp/DocuNet).
  <br> 👉 Method: Capturing the corelation between relations by U-net, which is to enlarge the reciptove field

1. AAAI 2021. [Document-Level Relation Extraction with Reconstruction](https://arxiv.org/abs/2012.11384). Wang Xu, Kehai Chen, Tiejun Zhao.
  <br> 👉 Method: build a graph like EoG, use LSTM to calculate the probability of "inference meta path", then maximize the probability of relationed entity pairs using BCE

1. AAAI 2021. [Document-Level Relation Extraction with Adaptive Thresholding and Localized Context Pooling](https://arxiv.org/abs/2010.11304). Wenxuan Zhou, Kevin Huang, Tengyu Ma, Jing Huang.
  <br> 👉 Method: improve BERT with marker, log-sum-exp pooling, group bilinear + adaptive threshold class + directly use transformer's attn matrix to aggregation words into doc representation

1. AAAI 2021. [Entity Structure Within and Throughout: Modeling Mention Dependencies for Document-Level Relation Extraction](https://arxiv.org/abs/2102.10249). Benfeng Xu, Quan Wang, Yajuan Lyu, Yong Zhu, Zhendong Mao.
  <br> 👉 Method: add a structured attentive bias when calculating attention scores, to enable BERT attend more to coreference tokens

1. AAAI 2021. [Multi-view Inference for Relation Extraction with Uncertain Knowledge](https://www.researchgate.net/publication/347879225_Multi-view_Inference_for_Relation_Extraction_with_Uncertain_Knowledge). Bo Li, Wei Ye, Canming Huang, Shikun Zhang.
  <br> 👉 Method: use KG concept knowledges: 3 attention aggregation(e2c, c2e, m2e) to get contextual and global entity pair representation, another attention aggregation to get sentence representation, concat for final classification

1. PAKDD 2021. [Densely Connected Graph Attention Network Based on Iterative Path Reasoning for Document-Level Relation Extraction](https://link.springer.com/content/pdf/10.1007%2F978-3-030-75765-6_22.pdf). Hongya Zhang, Zhen Huang, Zhenzhen Li, Dongsheng Li, and Feng Liu.
  <br> 👉 Method: DCGAT for structural representation + inference same as EoG

1. PAKDD 2021. [SaGCN: Structure-Aware Graph Convolution Network for Document-Level Relation Extraction](https://link.springer.com/content/pdf/10.1007%2F978-3-030-75768-7_30.pdf). Shuangji Yang, Taolin Zhang, Danning Su, Nan Hu, Wei Nong, and Xiaofeng He.
  <br> 👉 Method: a graph with explicit structure (depandency tree) and implicit structure (from hardkuma distribution) for structural representation, and a graph for inference

1. ECML-PKDD 2021 [NA-Aware Machine Reading Comprehension for Document-Level Relation Extraction](https://2021.ecmlpkdd.org/wp-content/uploads/2021/07/sub_591.pdf). Zhenyu Zhang, Bowen Yu, Xiaobo Shu, and Tingwen Liu.
  <br> 👉 Method: using MRC-style encoder, aggragate mentions using directional attention flow, and add nota into labels

1. ICASSP 2021. [Multi-Granularity Heterogeneous Graph for Document-Level Relation Extraction](https://ieeexplore.ieee.org/abstract/document/9414755).
  <br> 👉 Method: RGCN for graph reasoning, and entity-ware attn for final relation representation

1. IEEE. [Multi-Scale Feature and Metric Learning for Relation Extraction](https://arxiv.org/abs/2107.13425). Mi Zhang, Tieyun Qian.

1. Knowledge-Based Systems. [Document-level relation extraction using evidence reasoning on RST-GRAPH](https://www.sciencedirect.com/science/article/pii/S0950705121005360). Hailin Wang, Ke Qin, Guoming Lu, Jin Yin, Rufai Yusuf Zakari, Jim Wilson Owusu.

1. Information Sciences. [Document-level relation extraction with entity-selection attention](https://www.sciencedirect.com/science/article/abs/pii/S0020025521003285). Changsen Yuan, Heyan Huang, Chong Feng, Ge Shi, and Xiaochi Wei.
  <br> 👉 Method: Select the essential sentence-level features and document-level features from the document by inter-sentenceattention and combine them with the document gating.

1. Pattern Recognition Letters. [Document-level Relation Extraction via Graph Transformer Networks and Temporal Convolutional Networks](https://www.sciencedirect.com/science/article/pii/S016786552100218X). Yong Shi, Yang Xiao, Pei Quan, MingLong Lei, and Lingfeng Niu.
  <br> 👉 Method: Temporal convolutional networks as encoder, build graph with huristic rules, and graph transformer networks for path gengration

1. arXiv 2021. [SAIS: Supervising and Augmenting Intermediate Steps for Document-Level Relation Extraction](https://arxiv.org/pdf/2109.12093.pdf). Yuxin Xiao, Zecheng Zhang, Yuning Mao, Carl Yang, Jiawei Han.

1. arXiv 2021. [Eider: Evidence-enhanced Document-level Relation Extraction](https://arxiv.org/abs/2106.08657). Yiqing Xie, Jiaming Shen, Sha Li, Yuning Mao, Jiawei Han.
  <br> 👉 Method: Predict evidence sentences to construct pseudo document, and use a blend layer to combine the predictions of origin/pseudo document.

1. arXiv 2021. [BERT-GT: Cross-sentence n-ary relation extraction with BERT and Graph Transformer](https://arxiv.org/abs/2101.04158). Po-Ting Lai, Zhiyong Lu.
  <br> 👉 Method: densely connect Graph Transformer(neighbor attention) & Transformer to improve BERT

1. arXiv 2021. [MrGCN: Mirror Graph Convolution Network for Relation Extraction with Long-Term Dependencies](http://arxiv.org/abs/2101.00124). Xiao Guo, I-Hung Hsu, Wael AbdAlmageed, Premkumar Natarajan, Nanyun Peng.
  <br> 👉 Method: pooling-unpooling after GCN layers to enlarge receptive field (like u-net)

1. arXiv 2021. [Mention-centered Graph Neural Network for Document-level Relation Extraction](http://arxiv.org/abs/2103.08200v1). Jiaxin Pan, Min Peng, Yiyan Zhang.
  <br> 👉 Method: introduce mention-mention edge weight when building a graph


### 2020

1. ACL 2020. [Reasoning with Latent Structure Refinement for Document-Level Relation Extraction](https://arxiv.org/abs/2005.06312). Guoshun Nan, Zhijiang Guo, Ivan Sekulić, Wei Lu.
  <br> 👉 Method: Latent Structure + DCGCN

1. EMNLP 2020. [Double Graph Based Reasoning for Document-level Relation Extraction](https://arxiv.org/abs/2009.13752). Shuang Zeng, Runxin Xu, Baobao Chang, Lei Li.
  <br> 👉 Method: Mention graph(mention + doc node) + entity graph (2-hot at most)

1. EMNLP 2020. [Global-to-Local Neural Networks for Document-Level Relation Extraction](https://www.aclweb.org/anthology/2020.emnlp-main.303). Difeng Wang, Wei Hu, Ermei Cao, Weijian Sun.
  <br> 👉 Method: EoG + R-GCN + entity-pair attention

1. EMNLP 2020. [Denoising Relation Extraction from Document-level Distant Supervision](https://arxiv.org/abs/2011.03888). Chaojun Xiao, Yuan Yao, Ruobing Xie, Xu Han, Zhiyuan Liu, Maosong Sun, Fen Lin, Leyu Lin.
  <br> 👉 Method: using DS data to pre-train model for DocRE with 3 tasks: Mention-Entity Matching, Relation Detection, Relational Fact Alignment

1. COLING 2020. [Graph Enhanced Dual Attention Network for Document-Level Relation Extraction](https://www.aclweb.org/anthology/2020.coling-main.136/). Bo Li, Wei Ye, Zhonghao Sheng, Rui Xie, Xiangyu Xi, Shikun Zhang.
  <br> 👉 Method: bi-directional attn between sentence & relation instance + attn duality + support evidence guide

1. COLING 2020. [Global Context-enhanced Graph Convolutional Networks for Document-level Relation Extraction](https://www.aclweb.org/anthology/2020.coling-main.461/). Huiwei Zhou, Yibin Xu, Zhe Liu, Weihong Yao, Chengkun Lang, Haibin Jiang.
  <br> 👉 Method: entity graph with attn gate & attn adj matrix for entity representation + entity graph with multi-head attn as adj matrix for reasoning + dense-node&edge-GCN

1. COLING 2020. [Document-level Relation Extraction with Dual-tier Heterogeneous Graph](https://www.aclweb.org/anthology/2020.coling-main.143/). Zhenyu Zhang, Bowen Yu, Xiaobo Shu, Tingwen Liu, Hengzhu Tang, Yubin Wang and Li Guo.
  <br> 👉 Method: strcuct modeling graph + relation reasoning graph + weighted RGCN

1. PAKDD 2020. [HIN: Hierarchical Inference Network for Document-Level Relation Extraction](https://arxiv.org/abs/2003.12754). Hengzhu Tang, Yanan Cao, Zhenyu Zhang, Jiangxia Cao, Fang Fang, Shi Wang, Pengfei Yin.
  <br> 👉 Method: Hierarchical (entity & document level) inference representation (using LSTMs, attention and all kinds of "concat") for an entity pair's representation

1. ICKG 2020. [Improving Document-level Relation Extraction via Contextualizing Mention Representations andWeighting Mention Pairs](https://ieeexplore.ieee.org/document/9194547), [code](https://github.com/nefujiangping/EncAttAgg). Ping Jiang, Xian-Ling Mao, Binbin Bian and Heyan Huang.

1. arXiv 2020. [Coarse-to-Fine Entity Representations for Document-level Relation Extraction](https://arxiv.org/abs/2012.02507). Damai Dai, Jing Ren, Shuang Zeng, Baobao Chang, Zhifang Sui.
  <br> 👉 Method: a word graph for coarse representation, Bi-GRU for path encoding, and an attention aggregator

1. arXiv 2020. [Entity and Evidence Guided Relation Extraction for DocRED](https://arxiv.org/abs/2008.12283). Kevin Huang, Guangtao Wang, Tengyu Ma, Jing Huang.
  <br> 👉 Method: convert a doc into N {head entity; doc} samples for BERT, bilinear for RE, and double bilinear for evidence prediction as an auxiliary task

1. IEEE Access 2020. [A Novel Document-Level Relation Extraction Method Based on BERT and Entity Information](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=9098945). Xiaoyu Han and Lei Wang.
  <br> 👉 Method: using marker to wrap mention as {[entity type] mention [entity X]}, then using BERT + bilinear

### 2019

1. ACL 2019. [Inter-sentence Relation Extraction with Document-level Graph Convolutional Neural Network](https://www.aclweb.org/anthology/P19-1423/). Sunil Kumar Sahu, Fenia Christopoulou, Makoto Miwa, and Sophia Ananiadou.
  <br> 👉 Method: GCN + bi-affine classification

1. ACL 2019. [Attention Guided Graph Convolutional Networks for Relation Extraction](https://www.aclweb.org/anthology/P19-1024.pdf). Zhijiang Guo, Yan Zhang, Wei Lu.
  <br> 👉 Method: multi-head attention to get multi graph with different adj matrix + dense GCN

1. EMNLP 2019. [Connecting the Dots: Document-level Neural Relation Extraction with Edge-oriented Graphs](https://arxiv.org/abs/1909.00228). Fenia Christopoulou, Makoto Miwa, Sophia Ananiadou.
  <br> 👉 Method: Edge-oriented graph + Iterative Inference Mechanism

1. NAACL 2019. [Document-Level N-ary Relation Extraction with Multiscale Representation Learning](https://arxiv.org/abs/1904.02347). Robin Jia, Cliff Wong, Hoifung Poon.
  <br> 👉 Method: multioscale representation of mention and entity: lstm for paragraph-level mention representation, log-sum-exp pooling for entity representation

1. arXiv 2019. [Fine-tune Bert for DocRED with Two-step Process](https://arxiv.org/abs/1909.11898). Hong Wang, Christfried Focke, Rob Sylvester, Nilesh Mishra, William Wang.
  <br> 👉 Method: BERT + bilinear, 2 step training: binary classification for relation detection, then multi classification for relation type

### 2018

1. EMNLP 2018. [N-ary Relation Extraction using Graph-State LSTM](https://www.aclweb.org/anthology/D18-1246). Linfeng Song, Yue Zhang, Zhiguo Wang, and Daniel Gildea.

1. NAACL 2018. [Simultaneously Self-Attending to All Mentions for Full-Abstract Biological Relation Extraction](https://www.aclweb.org/anthology/N18-1080/). Patrick Verga, Emma Strubell, and Andrew McCallum.
  <br> 👉 Method: Transformers + CNN as encoder, head MLP and tail MLP for position-specific representations, bilinear + log-sum-exp for entity pair representation

### 2017

1. TACL 2017. [Cross-Sentence N-ary Relation Extraction with Graph LSTMs](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/05/tacl17.pdf). Nanyun Peng, Hoifung Poon, Chris Quirk, Kristina Toutanova, and Wen-tau Yih.

## Related Papers

The task of those papers are somewhat relevant to Doc RE (i.e. cross-sentence RE, GCN for RE, reasoning for MRC, etc.), of much value as well

### 2021


1. ACL 2021. [Injecting Knowledge Base Information into End-to-End Joint Entity and Relation Extraction and Coreference Resolution](https://ugentt2k.github.io/papers/2021/verlinden2021.pdf).
  <br> 👉 task: joint information extraction (used DocRED dataset)
  <br> 👉 Method: inject KB-text and KB-graph information into the model, using span representation to do NER, coreference, and RE

1. EACL 2021. [Two Training Strategies for Improving Relation Extraction over Universal Graph](https://arxiv.org/abs/2102.06540). Qin Dai, Naoya Inoue, Ryo Takahashi and Kentaro Inui.
  <br> 👉 Task: DSRE
  <br> 👉 Method: merge text into KG, and improve the "select path" stage with path type (textual, hybrid, KG paths) adaptive pretraining & complexity ranking guided attention

### 2019

1. ACL 2019. [Multi-hop reading comprehension across multiple documents by reasoning over heterogeneous graphs](https://www.aclweb.org/anthology/P19-1260.pdf). Ming Tu, Guangtao Wang, Jing Huang, Yun Tang, Xiaodong He, and Bowen Zhou.

1. ACL 2019. [Graph Neural Networks with Generated Parameters for Relation Extraction](https://www.aclweb.org/anthology/P19-1128.pdf). Hao Zhu, Yankai Lin, Zhiyuan Liu, Jie Fu, Tat-seng Chua, and Maosong Sun.

1. EMNLP 2019. [KagNet: Knowledge-Aware Graph Networks for Commonsense Reasoning](https://www.aclweb.org/anthology/D19-1282.pdf). Bill Yuchen Lin, Xinyue Chen, Jamin Chen, and Xiang Ren.

1. NAACL 2019. [Question Answering by Reasoning Across Documents with Graph Convolutional Networks](https://arxiv.org/abs/1808.09920). Nicola De Cao, Wilker Aziz, Ivan Titov.

1. NAACL 2019. [BAG: Bi-directional Attention Entity Graph Convolutional Network for Multi-hop Reasoning Question Answering](https://arxiv.org/abs/1904.04969). Yu Cao, Meng Fang, and Dacheng Tao.

1. NAACL 2019. [Long-tail relation extraction via knowledge graph embeddings and graph convolution networks](https://www.aclweb.org/anthology/N19-1306.pdf). Ningyu Zhang, Shumin Deng, Zhanlin Sun, Guanying Wang, Xi Chen, Wei Zhang, and Huajun Chen.
  <br> 👉 Task: RE
  <br> 👉 Method: Using KG knowledges to improve the performance of long-tail instances in RE. Using KG embeddings and GCN to learn relational knowledge, then attention aggregation to get final relation representation

1. AAAI 2019. [Neural Relation Extraction within and across Sentence Boundaries](https://arxiv.org/abs/1810.05102). Pankaj Gupta, Subburam Rajaram, Bernt Andrassy, Hinrich Schutze, Thomas Runkler.
  <br> 👉 Task: cross sentence RE
  <br> 👉 Method: Using RNN to model the dependancy subtree

### 2018

1. EMNLP 2018. [Graph Convolution over Pruned Dependency Trees Improves Relation Extraction](https://www.aclweb.org/anthology/D18-1244/). Yuhao Zhang, Peng Qi, and Christopher D Manning.

1. Journal of Biomedical Informatics 2018. [An effective neural model extracting document level chemical-induced disease relations from biomedical literature](https://pubmed.ncbi.nlm.nih.gov/29746916/). Wei Zheng, Hongfei Lin, Zhiheng Li, Xiaoxia Liu, Zhengguang Li, Bo Xu, Yijia Zhang, Zhihao Yang, and Jian Wang.

1. NeurIPS 2018. [Recurrent Relational Networks](https://arxiv.org/abs/1711.08028). Rasmus Palm, Ulrich Paquet, Ole Winther.

1. ACL 2018. [A Walk-based Model on Entity Graphs for Relation Extraction](https://www.aclweb.org/anthology/P18-2014/). Fenia Christopoulou, Makoto Miwa, Sophia Ananiadou.

### 2017

1. ACL 2017. [Distant Supervision for Relation Extraction beyond the Sentence Boundary](https://www.aclweb.org/anthology/E17-1110). Chris Quirk and Hoifung Poon. 

1. EMNLP 2017. [Incorporating relation paths in neural relation extraction](https://www.aclweb.org/anthology/D17-1186). Wenyuan Zeng, Yankai Lin, Zhiyuan Liu, and Maosong Sun.
