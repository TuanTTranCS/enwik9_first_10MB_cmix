# enwik9.head_10MB_cmix
Compressed and decompressed file using cmix-v18 on the first 10 MB of the enwik9 file

You can try download the source code from https://www.byronknoll.com/cmix.html and compile to run on a computer with >32GB of RAM.
Instruction to run compression (using cmix-v18):
1. Copy the file to be compressed (*enwik9.head*) into the cmix folder
2. Run the cmix command on terminal (Linux/OSX) or command line (Windows):

        In linux/OSX:
        ./cmix -c ./dictionary/english.dic enwik9.head enwik9.head_cmix
        
        
        In Windows:
        cmix -c dictionary\english.dic enwik9.head enwik9.head_cmix
