# drug-discovery
The working of the 5 parts are described here:
PART 1: data preprocessing
Here we have fetched data form CHEMBL and performed multiple preprocessing activities.
The ChEMBL database is the primary source of data for our model. A sizable manual library of bioactive compounds with drug-like characteristics is called ChEMBL. It is a database that combines chemical, bioactivity, and genetic information to help with the curation and upkeep of new medications developed using genomic information. The curators of the dataset manually extract chemical, test, and bioactivity information from scientific publications . 
For our model, we can extract and have extracted information on several types of diseases from the database, which is also available for different organisms and not just for humans. Various drugs that have been used for the diseases listed their genomic interactions. The description of the drug, the organism it was used on, and various other factors are listed in the database assays of the various diseases and compounds.
After performing multiple preprocessing activities we have created a preprocessed data set that is used in part2.

PART 2: EDA & lipinski descriptor calculation:
Here we have done a lot of exploratory data analysis and calculated lipinski descriptors
Lipinski's descriptors are calculated thereafter, which define how druglike compounds in the data are, based on the Absorption, Distribution, Metabolism, and 
Excretion (ADME) which is also known as the pharmacokinetic profile.
These are analyzed based on Lipinski’s rule of 5 which are:
Molecular weight < 500 Dalton
Octanol-water partition coefficient (LogP) < 5
Hydrogen bond donors < 5
Hydrogen bond acceptors < 10

PART  3: calculating PADEL descriptors and creating data set:
PaDEL-Descriptor is a software for calculating molecular descriptors and fingerprints. 
The software currently calculates 797 descriptors (663 1D, 2D descriptors, and 134 3D descriptors) and 10 types of fingerprints. 
These descriptors and fingerprints are calculated mainly using The Chemistry Development Kit. Some additional descriptors and fingerprints were added, 
which include atom type electrotopological state descriptors, McGowan volume, molecular linear free energy relation descriptors, ring counts, 
count of chemical substructures identified by Laggner, and binary fingerprints and count of chemical substructures identified by Klekota and Roth.
And after all of these we have prepared final datasets to apply on predictive machine learning models.

PART 4: Testing of Decision tree algorithms and Multiclass logistic regression:
Here we have applied Random forest algorithm  that was giving around 69% accuracy score.
Whereas Multiclass logistic regression algorithm  that has given accuracy around 73%.

PART 5: Applying deep learning and Boosting algorithms to improve accuracy:
Here with multiclass dataset where active,inactive and intermediate classes are present, Adaboost algorithm has given nearly 81% accuracy score and
Adaboost algorithm has shown 83% accuracy score.
Later on to improve more we have eliminated intermediate class from the data set and finally have got around 84% accuracy score.
