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



This repo contains the select, processed clinical and translational data that was 
used in the above publication.


## DATA DICTIONARY
### clinical-data
#### Subject-Level Data: AMADEUS_primarycohort_subject.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* crossover.to.ipi.nivo = "Y" indicates the subject was enrolled to the CD8 HIGH group and subsequently crossed over and received nivolumab + ipilimumab
* crossover.day = Study Day of First Nivolumab + Ipilimumab Dose
* age	= Age
* sex	= Sex
* race = Race
* ethnicity	= Ethnicity
* tumor.type = Type of Cancer
* tumor.type.abbr = Abbreviation of tumor.type
* prior.lines.of.therapy = prior lines of cancer therapy
* ecog.screening = Eastern Cooperative Oncology Group (ECOG) Performance Status at Screening
* stage.at.diagnosis	= Stage of disease when initially diagnosed 
* stage.at.enrollment	= Stage of disease at study enrollment
* treatment.duration.months = Time in months from first dose of study drug to last dose
* cd8.percent.baseline = Tumoral CD8 Percentage by IHC at Baseline / Screening
* cd8.percent.max.ontrt = Tumoral CD8 Percentage by IHC On-Treatment. If multiple on-treatment CD8 results were obtained, the maximum is reported.
* best.overall.response	= Best Overall Response by RECIST
* pfs.months = Progression free survival (months)
* pfs.event.flag = "0" represents a censored value, "1" represents a PFS event was observed
* os.months	= Overall Survival (months)
* os.event.flag	= "0" represents a censored value, "1" represents an OS event (death) was observed
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### Adverse Events: AMADEUS_primarycohort_ae.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* ae.coded.preferred.term = AE Preferred Term, coded using dictionary MedDRA v25.0
* ae.coded.soc = AE System Organ Class, coded using dictionary MedDRA v25.0
* study.day.start = Study Day of AE Start
* study.day.end = Study Day of AE End. "NA" represents an event that was ongoing at time of study discontinuation.
* ae.severity = AE Severity Grade
* ae.serious = "Yes" represents the AE was a Serious Adverse Event (SAE)
* immune.related.ae = "Yes" represents the AE met criteria for an immune related AE (irAE)
* ae.relationship.to.nivolumab = Investigator-assessed Relationship to nivolumab
* ae.relationship.to.ipilimumab = Investigator-assessed Relationship to ipilimumab
* ae.outcome = AE Outcome
* coding.dictionary = Dictionary that AE Terms were Coded to (MedDRA v25.0)
  

#### Biopsy Data: AMADEUS_primarycohort_biopsy.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* study.day.biopsy = Study Day of Tumor Biopsy
* biopsy.location = Anatomical Location of Biopsy
* biopsy.target.lesion = "Yes" represents that the biopsy was taken from a target lesion
* cd8.percentage = Tumoral CD8 Percentage by IHC
  

#### Clinical Labs: AMADEUS_primarycohort_labs.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* visit = Visit Name when Lab Test was Performed
* study.day	= Study Day of Lab Test
* lab.category = Lab Test Type (Chemistry, Hematology, Thyroid Function Testing)
* lab.test = Lab Test Name
* lab.value = Value of Lab Test
* lab.unit = Units of Lab Test
* lower.limit.normal	= Lower Limit of Normal Range
* upper.limit.normal	= Upper Limit of Normal Range


#### Prior Therapies: AMADEUS_primarycohort_priortherapy.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* therapy.type = Type of Prior Therapy (Systemic Treatment, Surgery, Radiation)
* therapy.line = Line of Therapy
* therapy.setting = Therapy Setting
* study.day.start = Study Day Prior Therapy Started
* study.day.end = Study Day Prior Therapy Ended
* therapy.verbatim.name = Verbatim (site-reported) Name of Therapy
* therapy.coded.preferred.name = Therapy Preferred Name, coded using dictionary WHODrug
* therapy.coded.trade.name = Therapy Trade Name, coded using dictionary WHODrug
* coding.dictionary = Dictionary that Prior Therapies were Coded to (WHODrug-Global-B3 September 2021)
* therapy.best.response = Best Response to the Therapy


### translational-data
#### ctDNA: AMADEUS_primarycohort_ctDNA.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* timepoint.id = Timepoint of Blood Collection
* ctDNA.tumor.molecules.per.mL.plasma = ctDNA Value, measured as Tumor Molecules per mL of Plasma
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### CyTOF: AMADEUS_primarycohort_cytof_percent-of-parent.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* timepoint.id = Timepoint of Blood Collection
* cell.population.name = Cell Population
* percent.of.parent = Abundance Value, measured as the Percentage of the Parent Population
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### Whole Exome Sequencing - MSI and Tumor Mutational Burden: AMADEUS_primarycohort_msi_tmb.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* msi = MSI Classification
* tmb = Tumor Mutational Burden, measured as Number of Mutations per Megabase
* tmb.categories = TMB High/Low Classification
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### Olink Serum Proteomics: AMADEUS_primarycohort_olink.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* timepoint.id = Timepoint of Blood Collection
* protein.name = Name of Protein
* npx = Protein Expression, measured as NPX Units
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### TCR Sequencing: AMADEUS_primarycohort_tcr.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* sample.id = Biopsy Tissue Unique Sample ID
* timepoint.id = Timepoint of Biopsy Collection
* tra.trb = TCR Alpha (TRA) or TCR Beta (TRB) Sequence
* tcr.id = TCR Sequence
* count = Count
* frequency = Frequency
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### Vectra mIF Imaging: AMADEUS_primarycohort_Vectra.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* panel.id = Vectra Panel 
* timepoint.id = Timepoint of Biopsy Collection
* cell.population.name = Cell Population
* percent.of.parent = Abundance Value, measured as the Percentage of the Parent Population
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


#### X50 Flow Cytometry: AMADEUS_primarycohort_x50_percent-of-parent.csv
* subject.id = Deidentified Subject ID
* manuscript.id = Deidentified Subject ID reported in the manuscript
* arm = Treatment Group (CD8 LOW or CD8 HIGH)
* treatment = Treatment Regimen
* tumor.type = Type of Cancer
* timepoint.id = Timepoint of Blood Collection
* cell.population.name = Cell Population
* percent.of.parent = Abundance Value, measured as the Percentage of the Parent Population
* best.overall.response	= Best Overall Response by RECIST
* responder.flag.crpc = "Y" represents a best overall response of Complete or Partial Response
* disease.control.flag = "Y" represents a best overall response of Complete or Partial Response or Stable Disease >= 6 months
* cd8.converter.flag = "Y" represents a CD8 LOW subject with a baseline CD8 <15% and on-treatment CD8 >= 15%. "N" represents an on-treatment CD8 < 15% and "NA" represents subjects in the CD8 HIGH arm (>=15% at baseline) or those without an on-treatment biopsy.


