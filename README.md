# amadeus-trial-data


Apostolia M. Tsimberidou, Farah A. Alayli, Kwame Okrah, Alexandra Drakaki, Danny 
N. Khalil, Shivaani Kummar, Saad A. Khan, F. Stephen Hodi, David Y. Oh, Christopher 
R. Cabanski, Shikha Gautam, Stefanie Meier, Meelad Amouzgar, Shannon M. Pfeiffer, 
Robin Kageyama, EnJun Yang, Marko Spasic, Michael T. Tetzlaff, Wai Chin Foo, Travis 
J. Hollmann, Yanyun Li, Matthew Adamow, Phillip Wong, Jonni S. Moore, Sharlene 
Velichko, Richard O. Chen, Dinesh Kumar, Samantha Bucktrout, Ramy Ibrahim, Ute 
Dugan, Lisa Salvador, Vanessa M. Hubbard-Lucey, Jill O’Donnell-Tormey, Sandra 
Santulli-Marotto, Lisa H. Butterfield, Diane M. Da Silva, Justin Fairchild, Theresa 
M. LaVallee, Lacey J. Padrón and Padmanee Sharma. Immunologic Signatures of 
Response and Resistance to Nivolumab with Ipilimumab in Advanced Metastatic Cancer 
from the AMADEUS Trial. Submitted.



This repo contains the select, processed translational data and accompanying 
clinical/metadata that was used in the above publication.

## DATA DICTIONARY
### Clinical
#### PICI0002_Labs_2021-03-24.csv
* Deidentified.ID	= Deidentified Subject ID
* Visit = Cycle Timing of Lab Test
* Study Day	= Equivalent Study Day of Lab test
* Lab Test = Lab Test Name
* Result = Value of Lab Test
* Units	= Units of Lab Test
* Normal Range - Low	= Low limit of normal range
* Normal Range - High	= High limit of normal range
* Result in Standard Units	= Value of Lab Test in Standard Units
* Standard Units	= Standard Units
* Standard Normal Range - Low	= Low limit of normal range with standard units
* Standard Normal Range - High = High limit of normal range with standard units
* Reference Range Indicator	= HIGH/NORMAL/LOW for how lab test fell in range
* Baseline Flag = Y(Yes) if there were abnormal baseline levels

#### PICI0002_ph2_clinical.csv
* Deidentified.ID	= Deidentified Subject ID
* Age	= Age
* Sex	= Sex
* Race	= Race
* Ethnicity	= Ethnicity
* HEIGHT (cm)	= Height in centimeters
* WEIGHT (lb)	= Weight in pounds
* Arm	= Randomized Enrollment Arm
* Arm Description	= Description of Arm
* Actual Arm	= Actual Arm based on treatment received
* Phase = Phase of Study When Patient Enrolled (Phase 1b/Phase 2)
* Participant Dosed	= Yes(Y)/No(N) if patient received any study agent
* Received APX005M		= Yes(Y)/No(N) if patient received sotigalimab
* Received Nivolumab		= Yes(Y)/No(N) if patient received nivolumab
* DLT Evaluable = Dose limiting toxicity evaluable
* Efficacy Population Flag	= Yes(Y)/No(N) Efficacy Population Flag
* Cancer Type = Type of Cancer (Adenocarcinoma)
* Cancer Location = Site of Cancer in Pancrease (Head/Body/Tail)
* Stage at Initial Diagnosis	= Stage of disease when initially diagnosed (de novo vs recurrent)
* Stage at Enrollment	= Stage of disease on enrollment
* Prior Cancer Surgery	= History of cancer surgery prior to study enrollment
* Prior Radiation	= Use of radiation prior to study enrollment
* Prior Chemo = Use of chemotherapy prior to study enrollment
* ECOG at Screening = Eastern Cooperative Oncology Group (ECOG) Performance Status Scale at Screening
* Tobacco History = History of Tobacco Usage e.g Smoking
* Hematocrit (%) at Baseline	= Percentage by volume of red blood cells in blood at baseline
* BOR	= Best Overall Response by RECIST
* OS (days)	= Overall Survival
* OS Event	= Death Event
* PFS (days) = Progression free survival (days)
* PFS Event = Progression Event
* PFS Reason = reason for leaving study

### CyTOF
#### NatureMed_CyTOF_metadata.csv
* Deidentified.ID	= Deidentified Subject ID
* sample.id	= sample identifier
* ms = sample type/assay/%parent(par)/%leukocyte(leuk)
* timepoint.id = timepoint of blood collection
#### NatureMed_CyTOF_select_cell_populations.csv
* sample.id	= sample identifier
* value = fraction of population (parent or leukocyte respectively)
* paper.name = Naming of cell population from publication
#### NatureMed_CyTOF_select_MSI.csv
* sample.id	= sample identifier
* value = relative median signal intensity (arcsinh transformed raw intensity/150, normalized relative to upper (0.9) and lower (0.1) quantiles)
* epitope.id	= UniProt Protein Name
* paper.name = Naming of cell population from publication

### Olink
#### NatureMed_Olink_metadata.csv
* Deidentified.ID	= Deidentified Subject ID
* sample.id	= sample identifier
* ms = sample type/assay
* timepoint.id = timepoint of blood collection
#### NatureMed_Olink_select_proteins.csv
* sample.id	= sample identifier
* value	= log2(NPX) - Normalized Protein Expression from Olink
* paper.name = Name used for protein from publication


### RNAseq
#### NatureMed_GX_ph2_metadata
* Deidentified.ID	= Deidentified Subject ID
* sample.id	= sample identifier
* timepoint.id = timepoint of tumor biopsy
* filename = Name of respective processed data file
* gdc.anatomic.site.name	= GDC Anatomic Site of Biopsy
#### Data files
* Gene Symbol = Gene Symbol
* NCBI Gene ID	= NCBI Gene Symbol
* RNA-Seq Raw Counts	= Raw Counts
* FPKM	= Fragments Per Kilobase of transcript per Million mapped reads
* CPM	= Reads per million mapped reads or Counts per million mapped reads
* TPM	= Transcripts per million
* Percentile Rank = Percentile Rank
* Is Expressed =	Yes/No if gene is expressed
* sample = sample identifier

### Vectra
#### NatureMed_Vectra_metadata.csv
* Deidentified.ID	= Deidentified Subject ID
* sample.id	= sample identifier
* ms	= sample type/assay/%parent(par)/%total(tot)
* timepoint.id = timepoint of tumor biopsy
#### NatureMed_Vectra_select_cell_counts.csv
* sample.id	= sample identifier
* assay.name	= Vectra assay
* value	= median cell count across all regions of interest (ROI)
* timepoint.id = timepoint of tumor biopsy
* gdc.anatomic.site.name	= GDC Anatomic Site of Biopsy
* variable = Naming of cell population from publication
#### NatureMed_Vectra_select_cell_populations.csv
* sample.id	= sample identifier	
* median.value = median fraction of population parent/total across all regions of interest (ROI)
* variable = Naming of cell population from publication


### X50
#### NatureMed_X50_metadata.csv
* Deidentified.ID	= Deidentified Subject ID
* sample.id	= sample identifier
* ms = sample type/assay/%parent(par)/%leukocyte(leuk)
* timepoint.id = timepoint of blood collection
#### NatureMed_X50_select_cell_populations.csv
* sample.id = sample identifier
* value = fraction of population (parent or leukocyte respectively)
* paper.name = Naming of cell population from publication
#### NatureMed_X50_select_MFI.csv
* sample.id	= sample identifier
* value = relative median fluorescence intensity (arcsinh transformed raw intensity/150, normalized relative to upper (0.9) and lower (0.1) quantiles)
* epitope.id	= UniProt Protein Name
* paper.name = Naming of cell population from publication
