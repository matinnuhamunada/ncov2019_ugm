# ncov2019_ugm
## Project Description
* This project started in early 2020, where at that point, the SARS-CoV-2 that we know of were still called Novel Coronavirus (2019-nCoV).
* This project aims to gain insight on the motifs / conserved sequence of the spike-gene from nCoV 2019 by comparing sequences from various location.
* Once the consensus sequence were obtained, the team at UGM can start designing primers for early detection of the nCoV 2019.

## Brief method overview
* A list of 2434 SARS-CoV-2 genome sequences with human hosts was retrieved from NCBI Genbank on the 8th of May 2020.
* The sequences and metadata were fetched using this particular query: https://www.ncbi.nlm.nih.gov/labs/virus/vssi/#/virus?SeqType_s=Nucleotide&VirusLineage_ss=SARS-CoV-2,%20taxid:2697049. The resulting table can be accessed [here](spike_project/dataset/ncov2019_ncbi08052020.csv)
* The dataset is further filtered to only have a complete S-gene sequence (3822 bp), retaining 2283 samples for further sub-selection. The consensus sequence of the S-gene was created by sub-sampling up to 10 sequences from each geo-location tag (countries). Samples with ambiguous nucleotides were further filtered, resulting in 121 representatives of SARS-CoV-2 S-gene. This step is described in this [notebook](spike_project/01_fetch_sequence.ipynb)
* A degenerate consensus of the 121 sequences is then created to design primers to target S-gene, as describe in this [notebook](spike_project/02_analysis.ipynb). Multipe fasta file of the 121 sequence can be found [here](spike_project/output/spike_nucleotide.fna)