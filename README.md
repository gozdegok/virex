# virex
A data pre-processing tool for virus-host protein interactions with a high usability for ML prediction algorithms

Upload following files in order to be able to run the codes:
"phi_data.csv","HumanData.csv", "VirusData.csv",
"CorrHumanData.txt", "CorrVirusData.txt" 

"gatherVirusData" and "gatherHumanData" methods will be working on another method named "runPools"
Method "runpools" was implemented for gathering data from web. 

Due to performance upgrade issues after "runPools" and "cleaning" methods are run, the extracted data is stored on two CSV files named
"HumanData.csv", "VirusData.csv" and read from that CSVs.

Corrupted protein IDs are also stored in two txt files which are:
"CorrHumanData.txt", "CorrVirusData.txt" and read from that txts.

Running orders of the blocks must be as follows:

1.Import the libraries (If not edited on Google Colab pip install the libraries)
2.Run the variables
3.Read the initial file (Phi_data)
4.Run the experimental method graph block
5.Run the most infectious pathogens block
6.If you want to continue with all the data then skip "gatherVirusData","gatherHumanData",
"runpools" and "cleaning" methods. And directly run the next block(not commented) starting with the ("IDs that cannot be scraped from web") title.
If you dont want to extract sequence data for all proteins, you can first run "gatherVirusData","gatherHumanData",
"runpools" and "cleaning" methods and then run next two block which are commented and seen green. 
You can observe that it can gather the data and clean. But if you choose the second option and run those methods, 
you must be aware that gtahering and cleaning methods rewrites on the file which keeps us doing prediction on 100.000 rows of data.
7.Assuming you skipped those methods continue by joining the sequences of positive matches.
8.Run the block with cartesian product.
9.Run the merging negative infections
10.Run virus sequence vectorization block
11. Run human sequence vectorization block
12. Run labels binarization block
13. Run Average vector block
14.Run the RF classifier block
15.Run the SVC block
16. Run the Naive Bayes block
