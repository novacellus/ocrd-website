---
layout: page
lang: en
lang-ref: module-projects
---

# Module Projects

In the first project phase, a functional model for the OCR-D workflow was
developed. Full text recognition is seen as a complex process that includes
several upstream and downstream steps in addition to the actual text
recognition. First, a digital image is preprocessed for text recognition by
cropping, deskewing, dewarping, despeckling and binarizing it into a black and
white image. This is followed by layout recognition, which identifies the text
areas of a page down to line level. The recognition of the lines or the
baseline is particularly important for the subsequent text recognition, which
is based on neural networks in all modern approaches. The individual structures
or elements of the fully text-recognized document are then classified according
to their typographic function before the OCR result is improved in the
post-correction, if necessary. Finally the end result is transferred to
repositories for long-term archiving.

From the project proposals for the DFG's module project call in March 2017,
eight projects were approved:

* [Scalable methods of text and structure recognition for the full text digitisation of historical prints: Image Optimisation](# Image Optimisation)
* [Scalable methods of text and structure recognition for full text digitization of historical prints: layout recognition](# Layout Recognition)
* [Further development of a semi-automatic open source tool for layout analysis and region extraction and classification (LAREX) of early printing](# Larex)
* [NN/FST – Unsupervised OCR-Postcorrection based on Neural Networks and Finite-state Transducers](# NN-FST)
* [Optimized use of OCR processes – Tesseract as a component in the OCR-D workflow](# Tesseract)
* [Automatic correction of historical OCR captured prints with integrated optional interactive correction](# PoCoTo)
* [Development of a model repository and an automatic font recognition for OCR-D](# Font Recognition)
* [OLA-HD - An OCR-D Long-Term Archive for Historical Books](# OLA-HD)

<a id=" Image Optimisation" name=" Image Optimisation">**Scalable methods of text and structure recognition for full text digitization of historical prints: Image Optimisation**</a>  
_German Research Center for Artificial Intelligence (DFKI)_

Project participants: Andreas Dengel, Martin Jenckel, Khurram Hashmi
Git hub: [https://github.com/mjenckel/OCR-D-LAYoutERkennung/tree/master](https://github.com/mjenckel/OCR-D-LAYoutERkennung/tree/master)

The "Image Optimisation" forms the basis, which enables a high-quality OCR afterwards. The project develops tools for the pre-processing steps binarization, deskewing, dewarping, despeckling and cropping, whereby the DFKI can partly build on its own development OCRopus. This software is now further adapted to the requirements and special features of early modern books. Despeckling is seen as a side effect of binarization and cropping. Dewarping is based on a more recent approach of a pix2pix image translation network with a Generative Adversarial Network (GAN), with which lines of high-resolution images can be straightened without other pre-processing or segmentation steps. 

<a id=" Layout Recognition" name=" Layout Recognition">**Scalable text and structure recognition methods for the full text digitization of historical prints: Layout Recognition**</a>  
_DFKI_

Project participants: Andreas Dengel, Martin Jenckel, Khurram Hashmi
Git hub: [https://github.com/mjenckel/OCR-D-LAYoutERkennung/tree/master](https://github.com/mjenckel/OCR-D-LAYoutERkennung/tree/master)

Module 2 "Layout Recognition" is the most important processing step apart from the OCR itself. Correct layout recognition can not only improve the results in the subsequent OCR, but also makes a significant contribution to our knowledge about the digitized document by providing information on the layout and context of the individual text elements. Tools are developed for page segmentation, text line recognition, segment classification and document analysis, which are optimized for early modern prints. 

<a id=" Larex" name=" Larex">**Further development of a semi-automated open source tool for layout analysis and region extraction and classification (LAREX) of early printing**</a> 

_Julius-Maximilians-University of Würzburg  
Institute of Computer Science: Chair of Artificial Intelligence and Applied Computer Science_

Project participants: Frank Puppe, Alexander Gehrke
Git-Hub: [https://github.com/ocr-d-modul-2-segmentierung](https://github.com/ocr-d-modul-2-segmentierung)

The second project in the field of layout analysis further develops the semi-automatic and easy-to-use open source segmentation tool LAREX and integrates it into the OCR-D framework. The previously developed tool LAREX (Layout Analysis and Region EXtraction) enables both rough segmentation by separating text and non-text and fine segmentation by recognizing and semantically classifying different text blocks. LAREX is based on an efficient implementation of the Connected Component approach. It has already been used in the digitization of various early prints and has always been able to significantly reduce the time required for high-quality page segmentation. The main objective of the further development of LAREX is to increase the degree of automation by means of a pixel classifier, the result of which is corrected using traditional segmentation methods. This requires a more robust segmentation and a further development of the control and constraint system. On the one hand, users should be able to adapt and evaluate the basic settings to the particularities of individual books using a declarative rule language and, on the other hand, learning algorithms. Furthermore, the comfortable user interface of LAREX for the correction of individual segmentation errors is further developed, which is also necessary for the creation of a ground truth for learning algorithms or for evaluation. The overall goal is to find an optimal combination of manual and automatic methods. 

<a id=" NN-FST" name=" NN-FST">**NN/FST – Unsupervised OCR-Postcorrection based on Neural Networks and Finite-state Transducers**</a>  
_University of Leipzig  
Institut für Informatik: Department of Automatic Language Processing_


Project participants: Gerhard Heyer, Robert Sachunsky
Git hub: [https://github.com/ASVLeipzig/cor-asv-fst](https://github.com/ASVLeipzig/cor-asv-fst)

In the NN/FST project, operational software solutions for module 3 Text Optimisation for the OCR-D functional model are to be developed. The focus of the developments is on post-correction, which should be automated as far as possible. The main technologies used are neural networks (NN) together with finite transducers (FST) for decoding recognized text lines in a noisy channel model, which are then reweighted. In total, pre-trained standard models for historical texts of different kinds will be developed and the creation of new language- or domain-specific models on the basis of own reference corpora will be made possible. 

<a id=" Tesseract" name=" Tesseract">**Optimized use of OCR processes – Tesseract as a component in the OCR-D workflow**</a>  
_University of Mannheim  
University Library Mannheim_

Project participants: Stefan Weil, Noah Metzger
Git hub: [http://github.com/tesseract-ocr/tesseract/](http://github.com/tesseract-ocr/tesseract/ "http://github.com/tesseract-ocr/tesseract/")

Tesseract is a free software for text recognition and has been developed continuously for over 30 years. In the Open Source Software group, Tesseract is one of the programs with the best recognition rates. Since the end of 2016, Tesseract also supports text recognition using artificial neural networks (LSTM) and is therefore technologically up-to-date. The project extends Tesseract by interfaces for the integration into an OCR workflow according to the OCR-D module description (command line, API, REST-based web service). In addition, stability, performance and practical applicability are further improved. 

<a id=" PoCoTo" name=" PoCoTo">**Automatic post-correction of historical OCR captured prints with integrated optional interactive correction**</a>  
_Ludwig-Maximilians-University of Munich  
Centre for Information and Language Processing (CIS)_

Project participants: Klaus Schulz, Floran Fink, Tobias Englmeier
Git hub: [https://github.com/cisocrgroup/ocrd-postcorrection](https://github.com/cisocrgroup/ocrd-postcorrection), [https://github.com/cisocrgroup/cis-ocrd-py](https://github.com/cisocrgroup/cis-ocrd-py)

Another project for post-correction is based on its proprietary development "PoCoTo" for the interactive post-correction of OCR-captured historical prints. For the planned mass full text digitization, this software is to be developed into a correction tool that is as automated as possible. The main problem with automatic correction is to avoid replacing OCR tokens, which are not entered in the correction dictionary but are correct, by supposed corrections. The objective of the project is to develop a powerful system for fully automatic correction based on PoCoTo, which avoids such "bad corrections" as far as possible. To this end, the existing technology will be substantially extended by the possibility of using lexicons and several OCR results to determine the correct text. In addition, the fully automatic correction will also be usable as a preliminary stage of an optional semi-automatic or interactive post-correction. Procedures for semi-automatic or interactive post-correction, which make use of the data and insights gained during the automatic correction phase, will be integrated directly into the system.  

<a id=" Font Recognition" name=" Font Recognition">**Development of a model repository and an automatic font recognition for OCR-D**</a> 
_University Leipzig  
Institute of Computer Science: Chair of Digital Humanities_  
_Friedrich Alexander University Erlangen-Nuremberg  
Department of Computer Science: Chair of Computer Science 5: Pattern Recognition_  
_Johannes Gutenberg University Mainz  
Gutenberg Institute for World Literature and Writing-Oriented Media: Department of Book Science_

Project participants: Gregory Crane, Nikolaus Weichselbaumer, Saskia Limbach, Andreas Meier, Vincent Christlein, Mathias Seuret, Rui Dong
Git hub: [https://github.com/Doreenruirui/OCRD](https://github.com/Doreenruirui/OCRD "https://github.com/Doreenruirui/OCRD") , [https://github.com/seuretm/ocrd_typegroups_classifier](https://github.com/seuretm/ocrd_typegroups_classifier)

The recognition models required for OCR are usually trained either on the basis of modern corpora which do not reproduce the specifics of historical prints. Or unfiltered historical corpora are used, whose wide range of fonts, character sets, etc., makes a tailored training impossible. This also hinders the achievement of high recognition rates which are already possible for digital images of modern books. Compiling font specific corpora manually is not realistic, as this requires special knowledge of the history of printing and such an approach scales poorly. Due to the repetitive task, this is also very error-prone. The project aims to enable the historical humanities to use OCR with a manageable amount of effort for specific fonts, i.e. to carry out OCR that fits a font perfectly. A deep residual network is used to calculate local form features of the font from the image files with automatically recognized type mirrors, which are then combined to form a global descriptor. To this end, the project pursues three subgoals: The development of an online training infrastructure that makes it possible to train specific models for these font groups online with manageable effort and simultaneously for different OCR software. The development of a tool for the automatic recognition of fonts in digital images of historical prints. The provision of a model repository in which font-specific OCR models are made available to the community.

<a id=" OLA-HD" name=" OLA-HD">**OLA-HD – An OCR-D long-term archive for historical books**</a>  
_Georg-August-University of Göttingen  
State and University Library of Lower Saxony_  
_Society for Scientific Data Processing mbH Göttingen_

Project participants: Mustafa Dogan, Kristine Schima-Voigt, Philip Wieder, Triet Doan, Jörg-Holger Panzer
Git hub: [https://github.com/subugoe/OLA-HD-IMPL](https://github.com/subugoe/OLA-HD-IMPL)

For the further usage of the printed works listed in the VD, a sustainable archiving and identification of the digital copies, the bibliographic metadata as well as the indexed full texts and their versions is required. For this purpose a standardised concept must be developed. In addition, the availability and citability of the OCR texts is an important prerequisite for verifying scientific results. This means that the existing archiving of an object with its structure and metadata as well as digital images must be supplemented by its OCR texts. The intellectual indexing, corrections, improvements in the OCR procedure or the use of different OCR techniques result in different versions of the same source material, which represent a new challenge for persistent identification and long-term archiving. This problem includes aspects related to research data management and also requires the examination of methods and strategies for handling research data. The above mentioned requirements will be conceptually prepared, integrated into an extended context and implemented as a technical solution in order to meet the requirements of data holders and users. Based on this initial situation, this project defines the necessary steps to realize a solution for long-term archiving and a persistent identification of OCR texts.  
