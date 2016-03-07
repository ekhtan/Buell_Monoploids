# SNP Analysis


## A. Download both R1 and R2 files from SRA

      
      
      
      


## B. Prepare files for analysis

      
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
      

Also have to unzip files for the next bash script to work.

      
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
      
      Filter_N_Adapter_Trim_Batchmode.py 45 -p
      


