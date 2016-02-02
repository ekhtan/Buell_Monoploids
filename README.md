# Dosage Analysis of Buell Monoploids

Dataset for monoploids acquired from <a href='http://www.plantcell.org/content/early/2016/01/14/tpc.15.00538.abstract'> Hardigan et al., *Plant Cell* 2016</a>.

The plan is to generate bin-by-sam dosage plots.

-------

## A. Download data

We are only interested in genome data for this analysis. Also note that we took just Read 1 for this analysis.

      
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/006/SRR2067676/SRR2067676_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/006/SRR2067686/SRR2067686_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/009/SRR2067779/SRR2067779_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/007/SRR2065337/SRR2065337_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/009/SRR2065339/SRR2065339_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/007/SRR2069937/SRR2069937_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/001/SRR2067791/SRR2067791_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/002/SRR2067802/SRR2067802_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/004/SRR2068304/SRR2068304_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/002/SRR2068242/SRR2068242_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/000/SRR2068260/SRR2068260_1.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/002/SRR2069932/SRR2069932_1.fastq.gz .
      


## B. Data download, prep and alignment

Link the correct genotypes to each fastq file.

      
      ln -s SRR2067676_1.fastq.gz M01-1x.fastq.gz
      ln -s SRR2067686_1.fastq.gz M02-1x.fastq.gz
      ln -s SRR2067779_1.fastq.gz M03-1x.fastq.gz
      ln -s SRR2065337_1.fastq.gz M04-1x.fastq.gz
      ln -s SRR2065339_1.fastq.gz M05-1x.fastq.gz
      ln -s SRR2069937_1.fastq.gz M06-1x.fastq.gz
      ln -s SRR2067791_1.fastq.gz M07-1x.fastq.gz
      ln -s SRR2067802_1.fastq.gz M08-1x.fastq.gz
      ln -s SRR2068304_1.fastq.gz M09-1x.fastq.gz
      ln -s SRR2068242_1.fastq.gz M10-2x.fastq.gz
      ln -s SRR2068260_1.fastq.gz M11-2x.fastq.gz
      ln -s SRR2069932_1.fastq.gz DM-2x.fastq.gz
      

Filter and cleanup the data for alignment.


## C. Run bin-by-sam analysis

## D. Plot data

