This repository is related to the thesis project named Virex: 
# A data pre-processing & ML prediction tool for virus-host protein interactions.
-------------------------------------------------

You can find the project summary on Virexposter.pdf file

## First upload the files below to the project folder in order to run the codes:
-------------------------------------------------------------

* "phi_data.csv"
* "HumanData.csv"
* "VirusData.csv"
* "CorrHumanData.txt"
* "CorrVirusData.txt" 

"gatherVirusData" and "gatherHumanData" methods will be working on another method named "runPools"
Method "runpools" was implemented for gathering data from web. 

Due to performance upgrade issues after "runPools" and "cleaning" methods are run, the extracted data is stored on two CSV files named
"HumanData.csv", "VirusData.csv" and read from that CSVs during the development process.

Corrupted protein IDs are also stored in two txt files which are:
"CorrHumanData.txt", "CorrVirusData.txt" and read from that txts.

## Usage

1. Import the libraries (If not edited on Google Colab pip install the necessary libraries)
2. Run the variables
3. Read the initial file (Phi_data.csv)
4. Run the experimental method analysis block
5. Run the most infectious pathogens block
6. A) If you want to skip the data gathering "gatherVirusData","gatherHumanData", "runpools" and "cleaning" methods. And directly run the block starting with the title "IDs that cannot be scraped from web".

  B) If you want to extract sequence data for all proteins once again you must be aware that gtahering and cleaning methods rewrites on the file which keeps us doing prediction on 100.000 rows of data. You need to run "gatherVirusData","gatherHumanData","runpools" and "cleaning" methods firstly and then run the methods that have comments on and can be seen green. You can observe that Virex can successfully gather the sequence data and clean it for the algorithms' usage.  

7. Assuming you skipped those methods continue by joining the sequences of positive matches.
8. Run the block with cartesian product.
9. Run the merging negative infections
10. Run virus protein sequence vectorization block
11. Run human protein sequence vectorization block
12. Run labels binarization block
13. Run Average vector block
14. Run the RF classifier block
15. Run the SVC block
16. Run the Naive Bayes block
