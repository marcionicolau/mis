Installing MIS
--------------
MIS must be built using GCC 4.8.x or higher and requires libz.

To build MIS:

1) First compile MUser2 (refer to MUser2's README for further details):
   
   cd Muser2-Source/src/tools/muser2/
   make allclean
   make
   
2) Install libz if required:

   sudo apt-get install zlib1g-dev
   
3) Compile togmus:

   cd -
   g++  -o -togmus togmus.cpp -lz   

As described below, we provide the wrapper script 'ComputeMinimalIndependentSupport.py' in this directory as an easy way to invoke MIS.



Running MIS
---------------
You can run MIS using the 'ComputeMinimalIndependentSupport.py' Python script in this directory.
For example, the command

   python ComputeMinimalIndependentSupport.py formula.cnf formula.out log.txt 300

runs MIS on the DIMACS CNF file 'formula.cnf', writing the generated minimal independent support to a file called 'formula.out' with logfile log.txt and a timeout of 300 seconds.


---
Contact
---
Kuldeep Meel (kuldeep@rice.edu)