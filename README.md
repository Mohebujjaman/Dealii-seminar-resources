Dealii website: https://dealii.org/
Download link: https://dealii.org/current_release/download/
For Mac OS X with M1, M2, etc chips, follow the installation instructions: https://github.com/dealii/dealii/wiki/MacOSX

Tutorials:

Step1: https://www.dealii.org/current/doxygen/deal.II/step_1.html
Step2: https://www.dealii.org/current/doxygen/deal.II/step_2.html
Step3: https://www.dealii.org/current/doxygen/deal.II/step_3.html

Run dealii codes in Alabama Supercomputer:
Say your code file name mydealiicode.cc

Go to the folder where you have all the source codes, for example, mydealiicode.cc, CMakeLists.txt, mesh file, parameter file etc



Make a .sh file say "dealii.sh" and  which contains the following:


#!/bin/bash
#
#  load the module
source /apps/profiles/modules_asax.sh.dyn
module load dealii/9.6.0
#
#  place commands here
run_dealii mydealiicode

Then do the following:

 module load gcc
 module load dealii
 cmake .
 make 

 For interactive mode running:
 make run

 If you want to submit jobs:

 chmod + dealii.sh
 run_script dealii.sh

 Then follow the directions.
