# About the workshop #

Relational data represents the vast majority of data present in the enterprise world. Yet none of the ML computations happens inside a relational database where data reside. Instead a lot of time is wasted in denormalizing the data and moving them outside of the databases in order to train models. Relational learning, which takes advantage of relational data structure, has been a 20 year old research area, but it hasn’t been connected with relational database systems, despite the fact that relational databases are the natural space for storing relational data.  Recent advances in database research have shown that it is possible to take advantage of the relational structure in data in order to accelerate ML algorithms. Research in relational algebra originating from the database community has shown that it is possible to further accelerate linear algebra operations. Probabilistic Programming has also been proposed as a framework for AI that fits can be realized in relational databases. Data programming, a mechanism for weak/self supervision is slowly migrating to the natural space of storing data, the database. At last as models in deep learning grow several systems are being developed for model management inside relational databases. This workshop aspires to start a conversation on the following topics:

- What is the impact of relations/relational structure in machine learning?
- Why has relational learning not been more successful? Why we don’t have yet the equivalent of tensorflow/pytorch in relational learning?
- Why is there no deep network structure for structured relational data? Are we just not there yet, or is there something intrinsic in random forest/boosted trees that work better for relational data?
- Can relational databases take advantage of the relational nature of graph neural network
- The algorithms and db communities have completely different approaches to relational learning, what is the connection?
- How does data programming connect to relational learning and can it be accelerated with the algorithmic primitives of relational databases?
- The attention network has been interpreted and used as a mechanism for discovering and expressing relations. It has also been considered as a storage mechanism of knowledge in Large Language Models (Transformers). Are transformers equivalent to databases?

## Invited talks ##

- **Speaker:** [Dan Olteanu](https://www.ifi.uzh.ch/en/dast/people/Olteanu.html) (University of Zurich)

    **Title:** Machine Learning through Database Glasses

    *Abstract:* As we witness the data science revolution, each research community legitimately reflects on its relevance and place in this new landscape. The database research community has at least three reasons to feel empowered by this revolution. This has to do with the pervasiveness of relational data in data science, the widespread need for efficient data processing, and the new processing challenges posed by data science workloads beyond the classical database workloads. The first two aforementioned reasons are widely acknowledged as core to the community’s raison d’être. The third reason explains the longevity of relational database management systems success: Whenever a new promising data-centric technology surfaces, research is under way to show that it can be captured naturally by variations or extensions of the existing relational techniques.

    In this talk, I will make the case for a first-principles approach to machine learning over relational databases that guided our recent work and can dramatically improve the runtime performance of machine learning.
    This approach exploits the algebraic and combinatorial structure of relational data processing. It also relies on compilation for hybrid database and learning workloads and on computation sharing across aggregates in learning-specific batches.

    This work is the outcome of extensive collaboration of the author with colleagues from RelationalAI (https://www.relational.ai), in particular Mahmoud Abo Khamis, Molham Aref, Hung Ngo, and XuanLong Nguyen, and from the FDB research project (https://fdbresearch.github.io/), in particular Ahmet Kara, Milos Nikolic, Maximilian Schleich, Amir Shaikhha, and Haozhe Zhang.

- **Speaker:** [Paroma Varma](https://www.paroma.xyz) (Snorkel AI)

    **Title:** Programming Training Data with Snorkel

    *Abstract:* One of the key bottlenecks in building machine learning systems is creating and managing the massive training datasets that today’s models learn from. In this talk, we will describe our work at [Snorkel AI](snorkel.ai) on labeling training data efficiently using our system, Snorkel, which allows users to programmatically label training data. Snorkel has been deployed by major technology companies like Google, Facebook and Intel, academic labs, and government agencies. Rather than hand-labeling training data, users write labeling functions which label data using heuristic strategies such as pattern matching, distant supervision, and other models. These labeling functions can have noisy, conflicting, and correlated outputs, which Snorkel models and combines into clean training labels. This allows training sets to be built in hours or days, rather than months or years.

* **Speaker:** [Arun Kumar](https://cseweb.ucsd.edu/~arunkk/) (UC San Diego)

    **Title:** The New DBfication of ML/AI

    *Abstract:* The recent boom in ML/AI applications has brought into sharp focus the pressing need for tackling the concerns of scalability, usability, and manageability across the entire lifecycle of ML/AI applications. The ML/AI world has long studied the concerns of accuracy, automation, etc. from theoretical and algorithmic vantage points. But to truly democratize ML/AI, the vantage point of building and deploying practical systems is equally critical.

    In this talk, I will make the case that it is high time to bridge the gap between the ML/AI world and a world that exemplifies successful democratization of data technology: databases. I will show how new bridges rooted in the principles, techniques, and tools of the database world are helping tackle the above pressing concerns and in turn, posing new research questions to the world of ML/AI. As case studies of such bridges, I will describe two lines of work from my group: query optimization for ML systems and benchmarking data preparation in AutoML platforms. I will conclude with my thoughts on community mechanisms to foster more such bridges between research worlds and between research and practice.

* **Speaker:** [Olga Papaemmanouil](https://www.brandeis.edu/facultyguide/person.html?emplid=7f4b0188301218e80167e3786d65cff18e144e5d) (Brandeis University)

    **Title:** Towards AI-Native Databases


* **Speaker:** [David Chiang](https://www3.nd.edu/~dchiang/) (University of Notre Dame)

    **Title:** Two Ways of Thinking about Weighted Relations

    *Abstract:* I will talk about two ways of describing weighted or probabilistic relations:

    First, mathematical notation for tensors with named axes, which removes the burden of keeping track of the order of axes and the purpose of each. It also makes it easy to extend operations on low-order tensors to higher order ones (e.g., to extend an operation on images to minibatches of images, or extend the attention mechanism to multiple attention heads). Our notation builds on ideas from many previous papers and software libraries, and we hope their adoption may result in clearer papers and less bug-prone implementations.

    Second, hyperedge replacement graph grammars for factor graphs, or factor graph grammars (FGGs) for short, generate sets of factor graphs and can describe a more general class of models than plate notation, dynamic graphical models, case-factor diagrams, and sum-product networks can. Moreover, inference can be done on FGGs without enumerating all the generated factor graphs. For finite variable domains (but possibly infinite sets of graphs), a generalization of variable elimination to FGGs allows exact and tractable inference in many situations.

* **Speaker:** [Eriq Augustine](https://www.linkedin.com/in/eriq-augustine-77153921/) (UC Santa Cruz)

    **Title:** Collective Grounding: Relational Learning Meets Relational Theory

    *Abstract:* Relational learning takes advantage of relational structure in its inputs, e.g., graphs, and its output, e.g., constraints. Building upon that, statistical relational learning (SRL) defines structure using first-order predicate logic and models probabilistic dependencies between outputs. The use of predicate logic provides a natural groundwork for SRL to take advantage of the relational theory used in modern databases. Despite this common basis, SRL frameworks still have many unexplored opportunities to use the methods developed by the database community.

    Grounding, the process of enumerating all valid instantiations of structured tuples in the model, is one of the most computationally expensive components in SRL systems. In this talk, I explore the use of several concepts from database research to accelerate grounding. To improve grounding, we borrow from three well known problems in the database community: query rewriting, query containment, and multi-query optimization. Although not exact matches, each of these problems appear in SRL grounding in a form analogous to its database counterpart. By recognizing the connection to well-researched database techniques, we are able to address these problems in a way that takes advantage of the structure provided by SRL and the existing research provided by the database community. We show by implementing these techniques within an existing SRL system, we can achieve up to a 60% speedup in grounding.

## Accepted papers ##

*  __DRL-Clusters: Buffer Management with Clustering based Deep Reinforcement Learning.__
    Kai Li, Qi Zhang, Lei Yu, Hong Min.

* __Numerical Reasoning over Legal Contracts via Relational Database.__ Jiani Huang, Ziyang Li, Ilias Fountalis, Mayur Naik.

* __RASL: Relational Algebra in Scikit-Learn Pipelines.__ Kiran Kate, Chirag Sahni, Martin Hirzel, Avraham Shinnar, Thanh Lam Hoang.

* __DP-KB: Data Programming with Knowledge Bases Improves Transformer Fine Tuning for Answer Sentence Selection.__ Nicolaas Paul Jedema, Thuy Vu, Thuy Vu, Manish Gupta, Alessandro Moschitti.

* __Compressing (Multidimensional) Learned Bloom Filters.__ Angjela Davitkova, Damjan Gjurovski, Sebastian Michel.

## Program ##

| Time (ET)  | Program |
|:-------|:--------|
| 8:50 - 9:00 | Welcome and introduction |
| 9:00 - 9:45 |  Talk: Dan Olteanu |
| 9:45 - 10:30 |  Talk: Paroma Varma |
| 10:30 - 11:00|  Break |
| 11:00 - 11:45|   Talk: Arun Kumar |
| 11:45 - 12:00|   Talk: Eriq Augustine |
| 12:00 - 12.15|  Talk: David Chiang |
| 12:15 - 13:30| Lunch Break |
| 13:30 - 14:30| Presentation of contributed papers |
| 14:30 - 15:00|   Talk: Molham Aref |
| 15:00 - 15:15|  Break |
| 15:15 - 15:45|   Talk: Olga Papaemmanouil |
| 15:45 - 17:00|  Panel |
| 17:00 |  Closing Remarks |

## Call for papers ##
**Areas of particular interest for the workshop include (but are not limited to):**
- Data Management in Machine Learning Applications
- Definition, Execution and Optimization of Complex Machine Learning Pipelines
- Systems for Managing the Lifecycle of Machine Learning Models
- Systems for Efficient Hyperparameter Search and Feature Selection
- Machine Learning Services in the Cloud
- Modeling, Storage and Provenance of Machine Learning Artifacts
- Integration of Machine Learning and Dataflow Systems
- Integration of Machine Learning and ETL Processing
- Definition and Execution of Complex Ensemble Predictors
- Sourcing, Labeling, Integrating, and Cleaning Data for Machine Learning
- Data Validation and Model Debugging Techniques
- Privacy-preserving Machine Learning
- Benchmarking of Machine Learning Applications
- Responsible Data Management
- Transparency and Accountability of Machine-Assisted Decision Making
- Impact of Data Quality and Data Preprocessing on the Fairness of ML Predictions

**Submission:**
Submissions can be short papers (4 pages) or long papers (up to 8 pages, plus unlimited references). Authors are requested to prepare submissions following the NeurIPS proceedings format. DBAI is a single-blind workshop, authors must include their names and affiliations on the manuscript cover page.
Submission Website: To be announce upon acceptance of the workshop
Inclusion and Diversity in Writing: http://2021.sigmod.org/calls_papers_inclusion_and_diversity.shtml

**Conflicts:**
Workshops are not a venue for work that has been previously published in other conferences on machine learning or related fields. Work that is presented at the main NeurIPS conference will not be accepted in the workshop, including as part of an invited talk..

**Important Dates**

Paper submission deadline: ~~Sep 17, 2021, 11:59 PM (AoE, UTC-12)~~ **Extended Deadline: Sep 24, 2021, 11:59 PM (AoE, UTC-12)**

Acceptance notification: Oct 22, 2021 EOD

Mandatory SlidesLive upload for speaker videos: Nov 08, 2021

Workshop day: Dec 13, 2021

**Submission Site**

Submission link: [https://openreview.net/group?id=NeurIPS.cc/2021/Workshop/DBAI](https://openreview.net/group?id=NeurIPS.cc/2021/Workshop/DBAI)

All questions about submissions should be emailed to [this address](mailto:dubai2021-organizers@googlegroups.com).


### Organizers ###
- [Nikolaos Vasiloglou](https://www.linkedin.com/in/vasiloglou) (RelationalAI)
- [Maximilian Schleich](https://mjschleich.github.io/) 	(University of Washington)
- [Nantia Makrynioti](http://nantiamakrynioti.com/)	(Centrum Wiskunde & Informatica)
- [Parisa Kordjamshidi](https://www.cse.msu.edu/~kordjams/)  (Michigan State University)
- [Kirk Pruhs](https://people.cs.pitt.edu/~kirk/)	(University of Pitsburg)
- [Zenna Tavares](http://www.zenna.org/) (MIT)

## Links to similar workshops ##

- [KR2ML](https://kr2ml.github.io)
- [DEEM@SIGMOD](http://deem-workshop.org)
- [AIDB@VLDB](https://sites.google.com/view/aidb2020)

## Sponsors ##
- [RelationalAI](https://www.relational.ai/)
![image tooltip here](/assets/relationalai_logo.png)

- [Snorkel](https://snorkel.ai)
![image tooltip here](/assets/Snorkel_Logo.png)
