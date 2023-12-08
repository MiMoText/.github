## Project context
The project Mining and Modeling Text (MiMoText, 2019-2023) at Trier University (Germany) aims to establish an information network fed from various sources.In creating Linked Open Data and feeding the data into the wikibase instance of the project – the [MiMoTextBase](https://data.mimotext.uni-trier.de/wiki/Main_Page) – makes them freely available and connectable to other knowledge graphs.
Focusing on the history of the French novel from 1751-1800 the project integrates information extracted from three different sources in the knowledge graph. These sources are 
- metadata from **reference works**, in this case the Bibliographie du genre romanesque français created by Martin, Mylne and Frautschi 1977. 
- textual features from **primary sources** that is french novels created 1751-1800
- statements from **scholarly publications**.

In creating Linked Open Data from statements mined from the different sources, we were able to build a wikibase instance, the MiMoTextBase, fed with various information about the French enlightenment novel.
For further information on the project, see:

- project homepage: https://mimotext.uni-trier.de/english/ 
- MiMoTextBase: https://data.mimotext.uni-trier.de
- SPARQL endpoint interface: https://query.mimotext.uni-trier.de/
- SPARQL Tutorial using the MiMoTextBase (and Wikidata): https://mimotext.github.io/MiMoTextBase_Tutorial/ 

Schöch, Christof, Maria Hinzmann, Röttgermann Julia, Anne Klee, and Katharina Dietz. “Smart Modelling for Literary History.” IJHAC: International Journal of Humanities and Arts Computing [Special Issue on Linked Open Data] 16, no. 1 (2022): 78–93. https://doi.org/10.3366/ijhac.2022.0278.
Hinzmann et al. “Patterns in modeling and querying a knowledge graph for literary history” (in print).

zotero
https://www.zotero.org/groups/2342956/mimotext/library

In the following all repositories used within the project MiMoText are listed divided in the sections either from the three pillars of the project or infrastructure and dissemination: 

**Reference work**: repositories concerning the reference works 

**Primary sources**: repositories concerning primary sources such as novels as well as scripts dealing with those

**Scholarly publications**: repositories concerning scholarly publication such as scripts dealing with statement extraction from scholarly publications

**MiMoTextBase**: repositories concerning the wikibase instance of the project, called MiMoTextBase

**Presentations**: repositories that contains slides to different presentation, for more information please have a look here: https://mimotext.uni-trier.de/aktivitaten/ 

**Further repositories**: repositories that were created during the project containing different experiments or preparation work for follow-up projects

### Reference work (BGRF):
One of the pillars of the project is the *Bibliographie du genre romanesque français 1751-1800*, written by Angus Martin, Vivienne G. Mylne and Richard Frautschi 1977. As we are mining the statements within it for populating the knowledge graph of the project, there are various steps and scripts concerning this task. The following repositories contribute to this:
- [BGRF](https://github.com/MiMoText/BGRF): Collection of the scripts and all data concerning the BGRF such as mapping tables and statements on themes, tone, intention and page counts.
- [BibliographicErrorFinder](https://github.com/MiMoText/BibliographicErrorFinder): Python Script for identifying errors in xml version of the BGRF
- [BibliographicErrorSearch](https://github.com/MiMoText/BibliographicErrorSearch): Script to find errors in raw bibliographic data

### Primary sources:
The main repository for our primary sources is “[roman18](https://github.com/MiMoText/roman18)”, a Collection of Eighteenth-Century French novels (1751-1800). All files are stored in XML-TEI, a normalized and modernized version of the texts as well as a non-normalized and non-modernized version in txt-format. All the metadata concerning these files are stored within the XML-TEI-folder. Scripts that deal with the texts, such as metadata extraction, conversion of txt-files to simple XML-TEI format and the modernization step can be found here.

Connected in the building the corpus are following repositories:
- [convert_novels](https://github.com/MiMoText/convert_novels): contains python scripts that were used in converting digitally available sources such as texts from [wikisource](https://fr.wikisource.org), hub18CFrench, [rousseauonline](https://www.rousseauonline.ch/) to XML-TEI files.
- [balance_novels](https://github.com/MiMoText/balance_novels): contains a jupyter notebook for visualizing statistical information of both the corpus (roman18) and the bibliographic metadata using the sparql-endpoint. It is used to balance out the corpus in comparison to the whole literary production in French 1751-1800. Balancing criteria were year of first publication, gender of the authors, narrative form of the novels.

Using the modernized, normalized txt-files further analysis were performed that you can find in the following repositories:
- [topicmodeling](https://github.com/MiMoText/topicmodeling): contains scripts for topic modeling on the roman18-corpus as well as the outputs and interpretations such as labeling of the topics and generating statements for feeding into the MiMotextBase. 
- [text_match_novels](https://github.com/MiMoText/text_match_novels): contains a script to match snippets from one text to other texts to identify text-reuses.
- [sentiment_novels](https://github.com/MiMoText/sentiment_novels): contains scripts for a sentiment analysis of the roman18-corpus
- [Stylometric_Analysis](https://github.com/MiMoText/Stylometric_Analysis):  an exploration of authorship attribution within the roman18 corpus, taking two novels as examples (L'Étourdi, L'enfant du bordel).
- [mmt_2020-11-19_11-38](https://github.com/MiMoText/mmt_2020-11-19_11-38): This repository contains the results, scripts and input files for a topic modeling performed on the roman18 corpus (with a size of 92 texts) in November 2020.
- [mmt_2023-10-12_16-46](https://github.com/MiMoText/mmt_2023-10-12_16-46): This repository contains the results, scripts and input files for a topic modeling performed on the roman18 corpus (with a size of 200 texts) in October 2023.
- [NER_novels](https://github.com/MiMoText/NER_novels): documents the named entity recognition performed on the roman18 corpus with the help of SpaCy.

Additional corpora were created within the project for subsequent research work
- [roman17](https://github.com/MiMoText/roman17): corpus of french texts of the 17th century
- [Romankorpus_dt](https://github.com/MiMoText/Romankorpus_dt): corpus of german texts 1750 to 1820

### Scholarly publications:
Unlike the novels from the primary literature, the publications of the secondary literature are not in the public domain. Therefore, there are only repos on GitHub that deal with the extraction and analysis of the secondary texts.

Repositories that are connected to the INCEpTION workflow:
- [inception_tone_intention](https://github.com/MiMoText/inception_tone_intention): contains scripts for extracting statements about tone and intention from scholarly literature texts annotated in INCEpTION 
- [inception_themes](https://github.com/MiMoText/inception_themes): contains scripts for extracting thematic statements from scholarly works annotated in INCEpTION

Repositories that are dealing with different analysis of the corpus:
- [lit_cooccurence](https://github.com/MiMoText/lit_cooccurence): analysis of the relationship between literary works mentioned in scholarly publications based on the co-occurrences.
- [lit2vec](https://github.com/MiMoText/lit2vec): analysis of the relationship between literary works mentioned in scholarly publications based on word2vec method to measure context similarity
- [NER_Pubs](https://github.com/MiMoText/NER_Pubs): Named Entity Recognition for Scholarly publications
- [KeywordExtractor](https://github.com/MiMoText/KeywordExtractor): script for extracting keywords from RDF data
- [TaggingFixer](https://github.com/MiMoText/TaggingFixer): script for fixing issues in tagged data

### MiMoTextBase:
One goal of the project is the creation of a knowledge base on French novels of the second half of the 18th century, which is called MiMoTextBase. The following repositories are all connected in building and describing the MiMoTextBase such as the documentation of the ontology models, the Wikibase-Bot for importing data or the tutorial for querying the knowledge graph via SPARQL.
- [ontology](https://github.com/MiMoText/ontology): The repository ontology contains the modeling of the domain of the French Enlightenment Novel.
- [Wikibase-Bot](https://github.com/MiMoText/Wikibase-Bot): contains a bot and the data for importing data into the MiMoTextBase
- [MiMoTextBase_Tutorial](https://github.com/MiMoText/MiMoTextBase_Tutorial): contains all files for building a GitHub-pages page. Used for creating a SPARQL tutorial using data on the MiMoTextBase
- [vocabularies](https://github.com/MiMoText/vocabularies): contains controlled vocabularies on themes, locations, narrative forms, tone and intention within the context of Eighteenth-Century French Novels.

### Presentations / Slides:
Here you can find various slides to different presentations held during the project, for different activities and presentations, please have a look here: https://mimotext.uni-trier.de/aktivitaten/ 
- [lod-lithist](https://github.com/MiMoText/lod-lithist): Slides to presentations about Linked Open Data and Literary History within the context of the project ‘Mining and Modeling Text’
- [modeling](https://github.com/MiMoText/modeling): slides about the project
- [slides](https://github.com/MiMoText/slides): Slides with general information about the project
- [fid-romanistik2020](https://github.com/MiMoText/fid-romanistik2020): “Erheben, Sammeln und Vernetzen von Metadaten: Praxisbeispiel MiMoText”
- [literary-history](https://github.com/MiMoText/literary-history): “How Could Digital Literary Historiography Work?”
- [zurich2020](https://github.com/MiMoText/zurich2020): “Mining and Modeling Text: Informationsextraktion und Linked Open Data für die Literaturgeschichtsschreibung”
- [oam](https://github.com/MiMoText/oam): “Offene Publiaktionsformate”

### Further repositories:
Repositories that were created during the project either for experimenting different workflows, testing various softwares or which serve to prepare follow-up projects or project applications.
- [Wikidata](https://github.com/MiMoText/Wikidata): java scripts that searches for labels and ID on wikidata for specific vocabularies
- [sparql-queries](https://github.com/MiMoText/sparql-queries): SPARQL Queries with java on the data created by Andreas Lüschow (https://zenodo.org/records/3401429)
- [DescriptionDetector](https://github.com/MiMoText/DescriptionDetector): Script for identification of passages in novels containing descriptions 
