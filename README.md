# Playing with the CMIX compression algorithm on the enwik9 dataset
Compressed and decompressed the first 10 MB of the enwik9 file using cmix-v18 

You can try downloading the source code from https://www.byronknoll.com/cmix.html and compile it to run on a computer with at least 32GB of RAM (recommended). Windows users can download the already compiled version instead and run directly.

### Instruction to run compression (using cmix-v18)
1. Copy the file to be compressed (*enwik9.head*) into the cmix folder

   The data file can be download from [/files](https://github.com/littleghost1712/enwik9_first_10MB_cmix/tree/main/files) folder, or can be auto-generated using the Notebook ***Data_prep_enwik9_head_10mb.ipynb***
2. Run the cmix command on terminal (Linux/OSX) or command line (Windows):

        In Linux/OSX:
        ./cmix -c ./dictionary/english.dic enwik9.head enwik9.head_cmix
        
        In Windows:
        cmix -c dictionary\english.dic enwik9.head enwik9.head_cmix
        
   The compression algorithm will take some time to complete, nearly 4 hours for a Google compute instance with type n1-standard-16 (16 vCPUs, 60 GB memory). However, the compression ratio is state-of-the-art (SOTA) these days.
   
   ![compress_cmix](/img/cmix_compress.png)
   
***However***, with a computer with 16GB, the author experienced the compression process get killed in the middle (at about 89%)!!!

   
### Instruction to run decompression (using cmix-v18)

To decompress file ***enwik9.head_cmix*** and retrieve back the original file with a new name ***enwik9.head_cmix_decompressed***, we need to run the cmix decompress command:
      
      In Linux/OSX:
      ./cmix -d ./dictionary/english.dic enwik9.head_cmix enwik9.head_cmix_decompressed

      In Windows:
      cmix -d dictionary\english.dic enwik9.head_cmix enwik9.head_cmix_decompressed
      
   Decompression result:
   
   ![compress_cmix](/img/cmix_decompress.png)
