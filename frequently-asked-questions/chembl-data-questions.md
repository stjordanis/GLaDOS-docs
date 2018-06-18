# ChEMBL Data Questions

### How often do you update the data?

The data is updated regularly, with releases approximately every 3-4 months.

### Can you provide of list of all changes and additions you've made since the last release?

We provide a list of all downgraded compounds with each release. However, it would be impossible to note all structural changes and/or changes to compound names etc. If there is something specific that you need to check, please contact us and we will be able to let you know what, if anything, has happened to that compound.

### Are my queries stored and if so, are they routinely deleted?

We do not analyse the nature of any queries or note structures that are processed through the website. However, to implement the link shortening functionality we store the queries and relate them to a hash. This in an example of a shortened url: https://www.ebi.ac.uk/chembl/beta/chembl/beta/g/tiny/GvKCBuljiVr/s1XL8m6Duw==. In our elasticsearch servers, we have a mapping of GvKCBuljiVr/s1XL8m6Duw== to the original query, but nothing else is stored. There is not other data that can identify the user(s) who used that query.

We use https:// wherever possible to maintain the security of the searches. Additionally, the EBI has terms of use and these can be found at: http://www.ebi.ac.uk/Information/termsofuse.html. This will tell you what information is retained by the EBI, if any.


### Why are there so many different types of Standard Units in the database?

The published units are taken directly from the literature and we then attempt to standardise these to report as a standard type. This is an ongoing curation task, which was started with the most common units first.

### What is the 'Confidence Score'?

As part of the manual curation process applied to the data we assign a confidence score to the assay-to-target relationships represented in the database. The confidence score value reflects both the type of target assigned to a particular assay and the confidence that the target assigned is the correct target for that assay. The confidence scores range from 0, for as yet uncurated data entries, to 9, where a single protein target has been assigned a high degree of confidence. Assays assigned a non-molecular target type, for example a cell-line or an organism, receive a confidence score of 1, while assays with assigned protein targets receive a confidence score of at least 4. 

| CONFIDENCE_SCORE | DESCRIPTION |
| --- | --- |
| 0	| 	Default value - Target assignment has yet to be curated |
| 1	|		Target assigned is non-molecular |
| 3	|		Target assigned is molecular non-protein target |
| 4	|		Multiple homologous protein targets may be assigned |
| 5	|		Multiple direct protein targets may be assigned |
| 6	|		Homologous protein complex subunits assigned |
| 7	|	Direct protein complex subunits assigned |
| 8	|	Homologous single protein target assigned |
| 9	|		Direct single protein target assigned |

### Do you show which compounds and/or bioactivity data has been changed or deleted with each release of ChEMBL?

As the data and the compounds are continually being curated, it is not possible to keep a track of these alterations or additions. However, if our users contact us personally, we are always happy to try and give them this type of information on individual data or compounds, wherever possible.


### Is there a list of all the Activity Types in ChEMBL?

No, we do not keep a list of activity types but we are happy to create such a list as and when a user would require it. This can also be found if the ChEMBL data is downloaded from the FTP site and installed into a database.

### What literature coverage is there in ChEMBL?

Data are routinely extracted from seven core journals: 

  - Bioorg Med Chem Lett (https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry-letters)
  - J Med Chem (https://pubs.acs.org/journal/jmcmar)
  - Bioorg Med Chem (https://www.sciencedirect.com/journal/bioorganic-and-medicinal-chemistry)
  - J Nat Prod (https://pubs.acs.org/journal/jnprdf)
  - Eur J Med Chem (https://www.sciencedirect.com/journal/european-journal-of-medicinal-chemistry)
  - ACS Med Chem Lett (https://pubs.acs.org/journal/amclct)
  - MedChemComm (http://www.rsc.org/journals-books-databases/about-journals/medchemcomm/).

However, we also have data from selected articles in more than 200 journals including Antimicrob Agents Chemother, Med Chem Res and Drug Metab Dispos. ChEMBL currently contains data from more than 65,000 journal articles, and we also now include data from selected patents.

### How are the SMILES and InChI created for ChEMBL?

The canonical SMILES are calculated using Accelrys's Pipeline Pilot using an algorithm that belongs to Accelrys but it was derived from Daylight's algorithm (http://www.daylight.com/dayhtml/doc/theory/theory.smiles.html). The standard InChI is calculated using the command line InChI generator and was developed by the InChI Trust (http://www.inchi-trust.org/inchi/) and is executed via the command line. The version of InChI used in ChEMBL is 1.05

### How is the LogP calculated?

The LogP, and other compound properties are calculated according to the following document: [Property_Definitions](https://www.dropbox.com/s/mixm4cn5x7azmg4/property_definitions.docx?dl=0). Please note, we are now using RDKit to calculate many of these properties.

### How can I be informed of updates in ChEMBL?

You can sign up to our ChEMBL Announce mailing list (http://listserver.ebi.ac.uk/mailman/listinfo/chembl-announce), where you will be kept up to date with all new releases and changes to the database.

### Which sub-set of the PubChem Bioassay data has been integrated into ChEMBL?

In PubChem, depositors may assign multiple result types to an assay. However, if an assay is deposited as a 'confirmatory' assay (defined as an assay where a range of SID concentrations have been tested, with a view to determining a measurement of potency), then one of the result types must be marked up as an 'Active Concentration' (AC) result type. Panel assays may contain many 'AC' result types, one per panel member. The AC result type is the calculated potency measurement from the data, and is typically an IC50, EC50, AC50, GI50 or Ki. In addition, the PubChem deposition process requires that each SID in an assay must be assigned a single 'Activity Summary', from a controlled vocabulary which includes 'inactive', 'active' and 'inconclusive'. Only assays containing 'AC' result types have been integrated into ChEMBL, and from these assays, only activity data and SIDs associated with 'AC' result types have been integrated. The 'Activity Summary' field in PubChem associated with each integrated activity is also captured and shown in the 'Activity Comment' field in ChEMBL. Panel assays are divided into separate assays in ChEMBL, one ChEMBL assay for each panel member. A number of additional assays which do not match the above criteria, have also been included in the PubChem integration. These have been chosen individually, on the basis that they have been specifically requested to be included by ChEMBL users. These are: AID1, AID3, AID5, AID7, AID9, AID11, AID13, AID15, AID17, AID19, AID21, AID23, AID25, AID27, AID29, AID31, AID33, AID35, AID37, AID39, AID41, AID43, AID45, AID47, AID49, AID51, AID53, AID55, AID57, AID59, AID61, AID63, AID65, AID67, AID69, AID71, AID73, AID75, AID77, AID79, AID81, AID83, AID85, AID87, AID89, AID91, AID93, AID95, AID97, AID99, AID101, AID103, AID105, AID107, AID109, AID111, AID113, AID115, AID117, AID119, AID121, AID123, AID125, AID127, AID129, AID131, AID133, AID135, AID137, AID139, AID141, AID143, AID145, AID1851 and AID493040. A number of assays have been excluded since they contain data already present in ChEMBL. These assays include all ChEMBL-derived assays, and AID1433 (A data set that has been manually added to ChEMBL). An automatic 'standardization' of SID structures downloaded from PubChem is carried out prior to integration (using in house protocols). Standard inchis are generated from the standardized mol files, and used to normalize with existing ChEMBL structures. SIDs matching exactly on standard inchi to existing ChEMBL structures are assigned to the existing CHEMBLID (and the mol file already associated with the existing ChEMBL structure is used to represent the searchable structure for this CHEMBLID). Where no match to a standard inchi is achieved, the incoming SID is assigned to a new CHEMBLID, and the standardized mol file for the SID is used to represent the searchable structure. A very small number of SIDs (<0.1%) with standardized mol files that fail to produce valid standard inchis, or to load into a oracle symyx cartridge without errors, are each assigned a new CHEMBLID, and associated with a 'null' structure (ie: no mol file is associated with this new CHEMBLID). Mappings to ChEMBL targets for each integrated PubChem assay has been automated for the initial load. However, manual review of these mappings by expert curators may result in ongoing changes. Users who prefer to exclude the integrated PubChem data (or any other integrated external data set) from their ChEMBL web-interface searches can do so by clicking 'Activity Source Filter' next to the main ChEMBL search bar, and deselecting the sources not required in future searches. Note, however, that these deselections persist between browser sessions. Users querying ChEMBL database dumps directly using SQL, and wishing to achieve this same filtering, should inspect the 'source' table, and the foreign keys to this table in the 'assays' and 'compound_records' tables.

### What is the difference between ChEMBLdb, Malaria Data, ChEMBL-NTD and Kinase SARfari?

[ChEMBLdb](https://www.ebi.ac.uk/chembl/beta/) is a database of bioactive drug-like small molecules, it contains 2-D structures, calculated properties (e.g. logP, Molecular Weight, Lipinski Parameters, etc.) and abstracted bioactivities (e.g. binding constants, pharmacology and ADMET data). We attempt to normalise the bioactivities into a uniform set of end-points and units where possible, and also to tag the links between a molecular target and a published assay with a set of varying confidence levels. The data is abstracted and curated from the primary scientific literature, and cover a significant fraction of the SAR and discovery of modern drugs. 

[Malaria Data](https://www.ebi.ac.uk/chembl/malaria/) provides a service to access to hundreds of thousands of data points on malaria-related compounds, assays and targets, thus facilitating research for this neglected tropical disease. Inspired by the successful ChEMBL interface, a user may query the database using keywords, synonyms, chemical structures or protein sequences, review and filter the hits using tables or charts and then download the resulting subset. 

[ChEMBL-NTD](https://www.ebi.ac.uk/chemblntd)[ is a repository for Open Access primary screening and medicinal chemistry data directed at neglected diseases - endemic tropical diseases of the developing regions of the Africa, Asia, and the Americas. The primary purpose of ChEMBL-NTD is to provide a freely accessible and permanent archive and distribution centre for deposited data. ChEMBL-NTD is a subset of the data in the free medicinal chemistry and drug discovery database ChEMBLdb. 

[Kinase SARfari](https://www.ebi.ac.uk/chembl/sarfari/kinasesarfari) is an integrated chemogenomics workbench focused on Kinases. The system incorporates and links Kinase sequence, structure, compounds and screening data. It is both biology and chemistry aware and provides a central resource for Protein Kinase knowledge.

## What data sources are stored in ChEMBLdb?

ChEMBL consists of data from a wide variety of data sources including scientific literature and patents, deposited data sets, PubChem BioAssay and BindingDB databases, toxicology data sets and drug/clinical candidate resources. The current list of sources is:

1.	Scientific Literature 
2.	GSK Malaria Screening 
3.	Novartis Malaria Screening 
4.	St Jude Malaria Screening 
5.	Sanger Institute Genomics of Drug Sensitivity in Cancer 
7.	PubChem BioAssays 
8.	Clinical Candidates 
9.	Orange Book 
11.	Open TG-GATEs 
12.	Manually Added Drugs 
13.	USP Dictionary of USAN and International Drug Names 
14.	Drugs for Neglected Diseases Initiative (DNDi) 
15.	DrugMatrix 
16.	GSK Published Kinase Inhibitor Set 
17.	MMV Malaria Box 
18.	TP-search Transporter Database 
19.	Harvard Malaria Screening 
20.	WHO-TDR Malaria Screening 
21.	Deposited Supplementary Bioactivity Data 
22.	GSK Tuberculosis Screening 
23.	Open Source Malaria Screening 
25.	External Project Compounds 
26.	Gene Expression Atlas Compounds 
27.	AstraZeneca Deposited Data 
28.	FDA Approval Packages 
29.	GSK Kinetoplastid Screening 
30.	K4DD Project 
31.	Curated Drug Metabolism Pathways 
32.	St Jude Leishmania Screening 
33.	Gates Library compound collection 
34.	MMV Pathogen Box 
35.	HeCaToS Compounds 
36.	Withdrawn Drugs 
37.	BindingDB Database 
38.	Patent Bioactivity Data 
39.	Curated Drug Pharmacokinetic Data 
40.	CO-ADD antimicrobial screening data 
41.	WHO Anatomical Therapeutic Chemical Classification 
42.	British National Formulary 
43.	Published Kinase Inhibitor Set 2

### Can you provide some details on how ChEMBL compound properties (e.g. LogP, MW, PSA,..) are calculated?

Yes, please refer to the following document: [Property_Definitions](https://www.dropbox.com/s/mixm4cn5x7azmg4/property_definitions.docx?dl=0). Please note, we are now using RDKit to calculate many of these properties.

### What is pChEMBL?

In addition to the conversion of published activity types/values/units to standard activity types/values/units, we have now added an additional field called pChEMBL to the Activities table. This value allows a number of roughly comparable measures of half-maximal response concentration/potency/affinity to be compared on a negative logarithmic scale. For example, an IC50 measurement of 1nM would have a pChEMBL value of 9. pChEMBL is defined as: -Log(molar IC50, XC50, EC50, AC50, Ki, Kd or Potency).


### What is the Data Validity column?

The Data Validity column has been added to the interface and to the database (as column data_validity_comment) to flag activity values that are outside a range typical for that activity type, or even for potentially missing data. For example, an IC50 of 23000000nM would be flagged as Outside Typical Range. The use of the flag will allow users to decide whether or not to retain those values in their results set after running a search on the interface or using the downloaded database. The flags currently in use in this field are: 

  - Potential missing data
  - Potential author error
  - Manually validated
  - Potential transcription error
  - Outside typical range
  - Non standard unit for type
  - Author confirmed error