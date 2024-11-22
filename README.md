# Grace_Fisher_SCIE30001_Project_2024
RNA Seq method for SCIE30001 Project 2024
raw_file_processing: download raw RNA seq files from sequencing company. perform md5 check to ensure data integrity through transfer (integrity was maintained). run fastQC quality checks on raw data files (passed). download version 10 Arabidopsis thaliana reference genome. 
run trimmomatic.sh script. download illumina adaptor file and remove adaptors from reads. remove low quality reads. 
index reference genome using bwa
run bwa_to_bam.sh script. does paired-end alignment of reads. 
run sort_and_index_bam.sh script. sorts reads for downstream analysis and gives quantitative data. 
run stringtie_batch.sh script. directly quantify aligned reads. 
data_normalization_and_anova.R - extract transcript sequences quantification and identities and store in a list. normalize data using DESeq2. perform anova on the 3 treatment levels (col, luh and ABI).sort by significance and fold change. 
volcano plot.R: calculate log2 fold change between all treatment levels. make volcano plots using EnhancedVolcano. 

code courtesy of krodgers20. 
