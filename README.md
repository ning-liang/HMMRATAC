# HMMRATAC

Quick Start:

$ python Make_HMMR_Files.py ExampleFile.bam hg19.genome ExampleFile.processed

$ java -jar HMMRATAC_V1.0_exe.jar -b ExampleFile.processed.bam -i ExampleFile.processed.bam.bai -g hg19.genome -w ExampleFile.processed_fromBedtools.bw 

The above command uses the bedtools-generated bigWig file. This may not be ideal (See section 1.4 of HMMRATAC_Guide.txt). 
The better way is to use the bigWig file generated by MACS2. If you have MACS2 installed, the resulting bigWig is created by 
Make_HMMR_Files.py.

$ java -jar HMMRATAC_V1.0_exe.jar -b ExampleFile.processed.bam -i ExampleFile.processed.bam.bai -g hg19.genome -w ExampleFile.processed_fromMACS2.bw

To use Make_HMMR_Files.py, you must have samtools, UCSC's bedGraphToBigWig and either bedtools or macs2 installed. Please open the file
and insert the correct path to each required tool. Alternatively, you can manually create the required input files (See section 1 of HMMRATAC_Guide.txt).

Be sure to run HMMRATAC using the executable file, found here: 
https://github.com/LiuLabUB/HMMRATAC/releases
The source files are uploaded for users to see how the program works.  They do not contain the required manifest file needed to actually
run.  For details on HOW to run HMMRATAC, see HMMRATAC_Guide.txt, which contains a thorough runthrough of all parameters, output files and input
requirements and troubleshooting.
