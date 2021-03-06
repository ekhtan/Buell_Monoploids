# SNP Analysis


## A. Download data

Will require both R1 and R2 reads in this case.

      
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
      
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/006/SRR2067676/SRR2067676_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/006/SRR2067686/SRR2067686_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/009/SRR2067779/SRR2067779_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/007/SRR2065337/SRR2065337_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/009/SRR2065339/SRR2065339_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/007/SRR2069937/SRR2069937_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/001/SRR2067791/SRR2067791_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/002/SRR2067802/SRR2067802_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/004/SRR2068304/SRR2068304_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/002/SRR2068242/SRR2068242_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/000/SRR2068260/SRR2068260_2.fastq.gz .
      wget ftp.sra.ebi.ac.uk/vol1/fastq/SRR206/002/SRR2069932/SRR2069932_2.fastq.gz .
      


## B. Prepare files for analysis

Move downloaded files to a folder called /Original_files/ and make symlinks to the appropriate genotypes.

      
      ln -s Original_files/SRR2067676_1.fastq.gz M01-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2067686_1.fastq.gz M02-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2067779_1.fastq.gz M03-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2065337_1.fastq.gz M04-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2065339_1.fastq.gz M05-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2069937_1.fastq.gz M06-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2067791_1.fastq.gz M07-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2067802_1.fastq.gz M08-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2068304_1.fastq.gz M09-1x_R1_001.fastq.gz
      ln -s Original_files/SRR2068242_1.fastq.gz M10-2x_R1_001.fastq.gz
      ln -s Original_files/SRR2068260_1.fastq.gz M11-2x_R1_001.fastq.gz
      ln -s Original_files/SRR2069932_1.fastq.gz MDM-2x_R1_001.fastq.gz
      
      ln -s Original_files/SRR2067676_2.fastq.gz M01-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2067686_2.fastq.gz M02-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2067779_2.fastq.gz M03-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2065337_2.fastq.gz M04-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2065339_2.fastq.gz M05-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2069937_2.fastq.gz M06-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2067791_2.fastq.gz M07-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2067802_2.fastq.gz M08-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2068304_2.fastq.gz M09-1x_R2_001.fastq.gz
      ln -s Original_files/SRR2068242_2.fastq.gz M10-2x_R2_001.fastq.gz
      ln -s Original_files/SRR2068260_2.fastq.gz M11-2x_R2_001.fastq.gz
      ln -s Original_files/SRR2069932_2.fastq.gz MDM-2x_R2_001.fastq.gz
      

Unzip files for the next bash script to work.

      
      gunzip -f *R1*
      
      gunzip -f *R2*
      

Interleave, filter and trim files in paired-end mode.

      
      #################
      # First, interleave raw fastq files
      #################
      
      for i in *_R1_001.fastq
      do
        BASE=$(basename $i _R1_001.fastq)
        echo 'processing' $BASE
        interleaveSwitcher.py i $BASE'_R1_001.fastq' $BASE'_R2_001.fastq' $BASE.fastq
        echo 'gzip' $BASE
        gzip $BASE.fastq
        echo 'done'
      done
      
      ################
      # Second, filter and trim using pair-mode 
      # This script takes .gz files
      ################
      
      N_Adapter_Trim_Batchmode.py 45 -p
      

Interleaved files were kept and single R1 and R2 files were removed to conserve space.

## C. Alignment using bwa

      
      bwa-doall-vModules-current.py -d ~ekhtan/genomes/PGSC_DM_v4.03_pseudomolecules.fasta -t 20
      

This took about a week, considering the large file sizes.

## D. Test case using the M04 monoploid

Will look at SNPs from two file types: 
(a) uniquely mapping reads that are with the sam cigar string: XT:A:U 
(b) usam files, which are 'unique' reads that were isolate by having different start and end mapping positions, seen as a result of PCR duplicates

These .bam files were sorted and an mpileup file generated, and parsed using two scripts that support threading.

      
      beta-run-mpileup.py
      
      beta-mpileup-parser.py
      

Look to see if we have SNPs with 100% coverage in M04 vs MDM

      
      # This awk command line looks at the 100% mapped nucleotide for M04 (column 4), 
      # compared to unmatched 100% mapped nucleotide of MDM (column 8)
      
      awk -F'\t' '$4 != $8 && $4 ~ /100.0/ && $8 ~ /100.0/' parsed_mpileup_testM04.txt
      


