# Biomedical NLP Corpus Collection

Corpus (datasets) collection about biology and medical NLP, both Chinese and English.

- [信息抽取](# 信息抽取)
  - 命名实体识别
  - 术语标准化
  - 关系抽取
  - 事件抽取
  - 共指消解
- 分子分析
  - 文本分类
  - 双句相似度分析
- 文档检索
- 问答系统
- 知识图谱
- 预训练语言模型
- 其他

***

## 信息抽取

### 命名实体识别

- ###### 2004
  - [BioCreative I Task 1A: Gene Mention Identification](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-i/first-task-gm/)
    - focused on the identification of `gene` or `protein` names in running text.
- ###### 2006
  - [BioCreative II Task 1A: Gene Mention Tagging](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-ii/task-1a-gene-mention-tagging/)
    - named entity extraction of `gene` and `gene product` mentions in text.
- ###### 2012
  - [BioCreative IV Track 2-CHEMDNER Task: Chemical compound and drug name recognition task](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-iv/chemdner/)
    - detect mentions of `chemical compounds` and `drugs`.
  - [BioCreative IV Track 4-GO Task](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-iv/track-4-GO/)
    - SubTask A: Retrieving `GO` evidence sentences for relevant genes.
    - SubTask B: Predicting `GO terms` for relevant genes.
- ###### 2015
  - [BioCreative V Track 2-CHEMDNER-patents](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-v/track-2-chemdner/)
    - automatic extraction of chemical and biological data from medicinal chemistry patents.
    - The CHEMDNER-patents corpora will consist of a **training, development and test set, each comprising a total of 7000 manually annotated records**.
    - CEMP (`chemical` entity mention in patents, main task)
    - CPD (`chemical passage` detection, text classification task)
    - GPRO (`gene` and `protein` related object task)
- ###### 2017
  - [CCKS 2017 Task 2: 电子病历命名实体识别](https://www.biendata.xyz/competition/CCKS2017_2/)
     > **[Data](https://github.com/yhzbit/CNMER/tree/master/data)**
    
    - 实体包括：`身体部位`、`症状和体征`、`疾病和诊断`、`检查和检验`以及`治疗`。
- ###### 2018
  - [CHIP 2018 评测一：中文电子病历中临床医疗实体及属性抽取](http://icrc.hitsz.edu.cn/chip2018/Task.html)
    - 从医学影像学检查结果文本描述中提取“肿瘤相关疾病“的常用字段，包括`肿瘤原发位置`，`原发肿瘤大小`，`转移部位`。
    - 训练数据：600份影像学检查报告，肺癌，乳腺癌相关。
    - 测试数据：200份。
  - [CCKS 2018 面向中文电子病历的命名实体识别](https://www.biendata.xyz/competition/CCKS2018_1/)
    > **[Data](https://github.com/MenglinLu/Chinese-clinical-NER/tree/master/data)**
    - 对于给定的一组电子病历纯文本文档，任务的目标是识别并抽取出与医学临床相关的实体提及。
    - 实体包括：`解剖部位`，`症状描述`，`独立症状`，`药物`，`手术`。
- ###### 2019
  - [BioNLP-OST 2019 CRAFT-CA task: Concept Annotation Task](https://sites.google.com/view/craft-shared-task-2019/craft-ca) 
    
    - `Chemical Entities of Biological Interest (CHEBI)`, `Cell Ontology (CL)`, `Gene Ontology Biological Process (GO_BP)`, `Gene Ontology Cellular Component (GO_CC)`, `Gene Ontology Molecular Function (GO_MF)`, `Molecular Process Ontology (MOP)`, `NCBI Taxonomy (NCBITaxon)`, `Protein Ontology (PR)`, `Sequence Ontology (SO)`, `Uberon (UBERON)`.
  - [BioNLP-OST 2019 PharmaCoNER task](https://temu.bsc.es/pharmaconer/)
    
    - Entity types: `Normalizables`, `No_Normalizables`, `Proteinas`, `Unclear`
  - [BioNLP-OST 2019 AGAC task](https://sites.google.com/view/bionlp-ost19-agac-track)
    - Task 1 is a traditional NER for 12 labels, which cultivate molecular phenomena related to gene mutation. `Variation (Var)`, `Molecular Physiological Activity (MPA)`, `Interaction`, `Pathway`, `Cell Physiological Activity (CPA)`, `Regulation (Reg)`, `Positive Regulation (PosReg)`, `Negative Regulation (NegReg)`;  `Disease`, `Gene`, `Protein`, `Enzyme`.
    - Task 2 is a relation extraction task, which capture the thematic roles between entities. `ThemeOf`, `CauseOf`.
    - Task 3 is a prediction task for the novel link discovery, which extract triple information among gene, function change, and disease out of the corpus texts. `Gene;Function change;disease`.
  - [BioNLP-OST 2019 Bacteria-Biotope Task](https://sites.google.com/view/bb-2019/task-description)
    - the BB task is an information extraction task involving entity recognition, entity normalization, and relation extraction.
    - 4 entity types: `Microorganism`, `Habitat`, `Geographical`, `Phenotype`.
    - 2 relation types: `Lives_in`, `Exhibits`.
  - [CCKS 2019 面向中文电子病历的命名实体识别](http://www.ccks2019.cn/?page_id=62/)
    > [**Data**](http://openkg.cn/dataset/yidu-s4k)
    - 子任务1：医疗命名实体识别。实体包括`疾病和诊断`，`检查`，`检验`，`手术`，`药物`，`解剖部位`。
    - 子任务2：医疗实体及属性抽取（跨院迁移）
### 术语标准化
- ###### 2004
  - [BioCreative I Task 1B: Gene Normalizations](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-i/task-1b-gene-normalizations/)
    - focused on creating normalized **gene** lists.
- ###### 2006
  - [BioCreative II Task 1B: Human Gene Normalizations](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-ii/task-1b-human-gene-normalizati/)
    - Systems will be required to return the **EntrezGene (formerly Locus Link) identifiers** corresponding to the human **genes** and direct **gene products** appearing in a given MEDLINE abstract.
- ###### 2009
  - [BioCreative III: GN: Gene Normalization](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-iii/gn/)
    - link **gene** or **gene products** mentioned in the literature to **standard database identifiers**. However, in this challenge, there are two significant characteristics that make it unique: *1. Instead of using abstracts, full-length articles are provided. 2. Instead of being species-specific, no species information is provided.*
- ###### 2017
  - [BioCreative VI Track 1: Interactive Bio-ID Assignment (IAT-ID)](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-vi/track-1/)
    - Bioentity normalization task

        | Bioentity type         | Identifier type       |
        | ---------------------- | --------------------- |
        | gene/gene products     | Entrez/UniProtKB      |
        | small chemical         | ChEBI (primary)       |
        | subcellular structures | GO CC                 |
        | Cell lines             | Cellosaurus (primary) |
        | Cell types             | Cell Ontology         |
        | Tissues and organs     | Uberon                |
        | Organism               | NCBI Taxon            |

- ###### 2019
  - [CHIP 2019 评测一：临床术语标准化任务](http://www.cips-chip.org.cn:8088/evaluation)
    - 主要目标是针对中文电子病历中挖掘出的真实`手术实体`进行语义标准化。给定一手术原词，要求给出其对应的手术标准词。所有手术原词均来自于真实医疗数据，并以《ICD9-2017协和临床版》 手术词表为标准进行了标注。
    - 训练集数据量：**4000**条。
    - 验证集数据量：**1000**条。
    - 测试集数据量：**2000**条。
### 关系抽取
- ###### 2006
  - [BioCreative II Task 2: Protein-Protein Interactions](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-ii/task-2-protein-protein-interac/)
    - focuses on the prediction of **protein interactions** from full text articles.
- ###### 2010
  - [BioCreative III: PPI: Protein-Protein Interactions](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-iii/ppi/)
    - The aim of this task is to promote the development of automated systems that are able to extract biologically relevant information directly from the literature, in this case related to **protein-protein interaction (PPI)** annotation information.
- ###### 2011
  - [BioNLP Shared Task 2011: Entity Relations Supporting Task (REL)](http://2011.bionlp-st.org/home/entity-relations)
    - The task concerns the detection of relations stated to hold between a gene or gene product and a related entity such as a protein domain or protein complex.
    - Entities:  human-annotated **gene** and **gene product** entities, annotated as "Protein"
    - Relation Type: **Subunit-Complex, Protein-Component**
- ###### 2013
  - [BioNLP-ST-2013: Gene Regulation Network (GRN)](http://2013.bionlp-st.org/tasks/gene-regulation-network)
    -  corpus including entities, events and relations, including genic interactions.
- ###### 2017
  - [BioCreative VI Track 5: Text mining chemical-protein interactions](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-vi/track-5/)
    - automatically detect in running text (PubMed abstracts) relations between **chemical compounds/drug** and **genes/proteins**.
### 事件抽取
- ###### 2004
  - [BioCreative I Task 2: Functional Annotations](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-i/task-2-functional-annotations/)
    - automatic extraction and assignment of **Gene Ontology (GO)** annotations of human proteins, using full text articles.
- ###### 2011
  - [BioNLP Shared Task 2011: GENIA Event Extraction (GENIA)](http://2011.bionlp-st.org/home/genia-event-extraction-genia)
    - The GENIA task aims at extracting events occurring upon genes or gene products, which are typed as "Protein" without differentiating genes from gene products. Other types of physical entities, e.g. cells, cell components, are not differentiated from each other, and their type is given as "Entity"
  - [BioNLP Shared Task 2011: Epigenetics and Post-translational Modifications Task (EPI)](http://2011.bionlp-st.org/home/epigenetics-and-post-translational-modifications)
    - This task focuses on events relating to epigenetic change, including DNA methylation and histone modification, as well as other common post-translational protein modifications.
    - Event type: `Hydroxylation(羟基化)`, `Phosphorylation(磷酸化)`, `Ubiquitination(泛素化)`, `DNA methylation(DNA甲基化)`, `Glycosylation(糖基化)`, `Acetylation(乙酰化)`, `Methylation(甲基化)`, `Catalysis(催化)`.
  - [BioNLP Shared Task 2011: Infectious Diseases Task (ID)](http://2011.bionlp-st.org/home/infectious-diseases)
    - This tasks focuses on the biomolecular mechanisms of infectious diseases.
    - Five entities: `Genes and gene products`, `Two-component systems`, `Chemicals`, `Organisms`, `Regulons/Operons`.
    - Nine events:  `Gene expression`, `Transcription`, `Protein catabolism`, `Phosphorylation`, `Localization`, `Binding`, `Regulation`, `Positive regulation`, `Negative regulation`, `Process`.
  - [BioNLP Shared Task 2011: Bacteria Biotopes (BB)](http://2011.bionlp-st.org/home/bacteria-biotopes)
    - The task consists in extracting bacteria localization events, in other words, mentions of given species and the place where it lives.
    - Entities: `Host`, `HostPart`, `Geographical`, `Environment`, `Food`, `Medical`, `Soil`, `Water`.
    - Events: `Localization`, `PartOf`.
  - [BioNLP Shared Task 2011: Bacteria Gene Interactions (BI)](http://2011.bionlp-st.org/home/bacteria-gene-interactions)
    - This task consists in a full extraction of genetic processes mentioned in scientific texts concerning the bacterium *Bacillus subtilis*.
    - Entities: `GeneProduct`, `Protein`, `PolymeraseComplex`, `Gene`, `ProteinFamily`, `GeneFamily`, `GeneComplex`, `Regulon`, `Site`, `Promoter`, `Action`, `Transcription`, `Expression`.
    - Events: `RegulonDependence`, `BindTo`, `TranscriptionFrom`, `RegulonMember`, `SiteOf`, `TranscriptionBy`, `PromoterOf`, `PromoterDependence`, `ActionTarget`, `Interaction`.
  - [BioNLP Shared Task 2011: Bacteria Gene Renaming (RENAME)](http://2011.bionlp-st.org/home/bacteria-gene-renaming-rename)
    - The task consists in extracting gene renaming acts and gene synonymy reminders in scientific texts about bacteria.
    - Entities: All `gene` and `protein` names have been annotated as text-bound entities of type *Gene*.
    - Events: The only type of event is *Renaming* where both arguments are of type *Gene*.
- ###### 2013
  - [BioNLP-ST 2013: Cancer Genetics (CG) Task](http://2013.bionlp-st.org/tasks/cancer-genetics)
    - The CG task aims to advance the automatic extraction of information from statements on the biological processes relating to the development and progression of cancer.
  - [BioNLP-ST-2013: Pathway Curation (PC) task](http://2013.bionlp-st.org/tasks/pathway-curation)
    - The PC task aims to evaluate the applicability of event extraction systems to support the curation, evaluation and maintenance of biomolecular pathway models and to encourage the further development of methods for these tasks.
  - [BioNLP-ST-2013: Bacteria Biotopes (BB)](http://2013.bionlp-st.org/tasks/bacteria-biotopes)
    - Entity recognition of bacteria taxa and bacteria habitats.
    - Bacteria habitat categorization through the OntoBiotope-Habitat ontology.
    - Extraction of localization relations between bacteria and habitats.
- ###### 2016
  - [BioNLP-ST 2016: Bacteria Biotope-Event extraction of microorganisms and habitats with ontologies and their linking](http://2016.bionlp-st.org/tasks/bb2)
    - Entities: `Bacteria`, `Habitat`, `Geographical`.
    - Events: `Lives_In`.
  - [BioNLP-ST 2016: Event extraction of genetic and molecular mechanisms involved in plant seed development (SeeDev)](http://2016.bionlp-st.org/tasks/seedev)
    - **16** different types of entities.
    - **5** sets of event types that may be combined in complex events.
- ###### 2019
  - [BioNLP-OST 2019 Seedev Task](https://sites.google.com/view/seedev2019/task-description)
    - the SeeDev representation scheme defines **16 entity types**.
    - task1: Binary relation extraction task.
    - task2: Full event extraction task, these entities participates in **21 types of events** that can be grouped into five categories. 
### 共指消解
- ###### 2011
  - [BioNLP Shared Task 2011: Protein/Gene Coreference Task (COREF)](http://2011.bionlp-st.org/home/protein-gene-coreference-task)
    - The COREF task addresses the problem of finding anaphoric references to proteins or genes.
- ###### 2019
  - [BioNLP-OST 2019 CRAFT-CR task: Coreference Resolution Task](https://sites.google.com/view/craft-shared-task-2019/craft-cr)
## 句子分析
### 文本分类
- ###### 2019
  - [CHIP 2019 评测三：临床试验筛选标准短文本分类](http://www.cips-chip.org.cn:8088/evaluation)
    - 临床试验是指通过人体志愿者也称为受试者进行的科学研究，筛选标准是临床试验负责人拟定的鉴定受试者是否满足某项临床试验的主要指标，分为入组标准和排出标准，一般为无规则的自由文本语句。
    - 此评测任务的主要目标是针对临床试验筛选标准进行分类，所有预料均来自于真实临床试验，并经过了初步处理和人工标注。给定事先定义好的44种筛选标准类别和一系列中文临床试验筛选标准的描述句子，参赛者需返回每一条筛选标准的具体类别。
    - 训练集：22962；验证集：7682；测试集：7697。
### 双句相似度分析
- ###### 2018
  - [CHIP 2018 评测二：平安医疗科技智能患者健康咨询问句匹配大赛](http://icrc.hitsz.edu.cn/chip2018/Task.html)
    - 主要目标是针对中文的真实患者健康咨询语料，进行问句意图匹配。给定两个语句，要求判定两者意图是否相同或者相近。所有语料来自互联网上患者真实的问题，并经过了筛选和人工的意图匹配标注。
    - 训练集：**20000**条左右标注好的数据，经过脱敏处理。
    - 测试集：**10000**条左右，不含标注。
- ###### 2019
  - [CHIP 2019 评测二：平安医疗科技疾病问答迁移学习比赛](http://www.cips-chip.org.cn:8088/evaluation)
    - 本次评测任务的主要目标是针对中文的疾病问答数据，进行病种间的迁移学习。具体而言，给定来自5个不同病种的问句对，要求判定两个句子语义是否相同或者相近。所有语料来自互联网上患者真实的问题，并经过了筛选和人工的意图匹配标注。
    - 病种包括：`diabetes`，`hypertension`，`hepatitis`，`aids`，`breast cancer`。
    - 训练集，数据量分别为：10000，2500，2500，2500，2500
    - 验证集，数据量分别为：2000，2000，2000，2000，2000
    - 测试集，数据量为50000
## 文档检索
- ###### 2010
  - [BioCreative III: IAT: Interactive Demostration Task for Gene Indexing and Retrieval](https://biocreative.bioinformatics.udel.edu/tasks/biocreative-iii/iat/)
    - focus on **indexing** (identifying which genes are being studied in an article and linking these genes to standard database identifiers) and **gene-oriented document retrieval** (identifying full-text papers relevant to a selected gene).
- ###### 2019
  - [BioNLP-OST 2019 RDoc Task](https://sites.google.com/view/rdoc-task/task)
    - task1 (RDoC-IR) is on retrieving PubMed Abstracts related to RDoC constructs. **250** abstracts for train and **200** abstracts for test.
    - task 2 (RDoC-SE) is on extracting the most relevant sentences for an RDoC construct from a relevant abstract. **250** abstracts for train and **50** abstracts for test.
## 问答系统
- ###### 2019
  - [CCIR 2019 评测： 基于电子病历的数据查询类问答](http://ir.fzu.edu.cn/ccir2019/test.html)
    - 给定医疗知识图谱、医疗事件图谱和一系列自然语言问题，参赛者返回问题结果。
    - [病人事件图谱数据集](http://openkg.cn/dataset/peg)
    - 训练数据：**1800**条自然语言问句，SPARQL查询语句，以及答案。
    - 验证数据：**600**条自然语言问句，SPARQL查询语句，以及答案。
    - 测试数据：**600**条自然语言问句。
  - [PubMedQA: A Dataset for Biomedical Research Question Answering](https://pubmedqa.github.io/)
    
    >  **[paper](https://arxiv.org/abs/1909.06146)**        **[github](https://github.com/pubmedqa/pubmedqa)**        [**website**](https://pubmedqa.github.io/)
## 知识图谱
- ###### 2020
  - [CCKS 2020 新冠知识图谱构建与问答](http://sigkg.cn/ccks2020/?page_id=69)
    - 四个子任务：1）新冠百科知识图谱类型推断， 2）新冠概念图谱的上下位关系预测，3）新冠科研抗病毒药物图谱的链接预测，4）新冠百科知识图谱问答评测。
## 预训练语言模型
- ###### SciBERT: A Pretrained Language Model for Scientific Text
  > **[paper](https://arxiv.org/abs/1903.10676)**        [**github**](https://github.com/allenai/scibert)

- ###### BioBERT: a pre-trained biomedical language representation model for biomedical text mining
  > **[paper](https://academic.oup.com/bioinformatics/article/36/4/1234/5566506)**        **[github](https://github.com/dmis-lab/biobert)**

- ###### BERTCNER: Chinese clinical named entity recognition (CNER) using pre-trained BERT model
  > **[paper](https://doi.org/10.1016/j.jbi.2020.103422)**        **[github](https://github.com/lxy444/bertcner)**
## 其他




