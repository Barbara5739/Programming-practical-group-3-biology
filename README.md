# Programming-practical-group-3-biology
### To move or not to move: which nutrient conditions affect the movement of various types of bacteria the most?
This is the GitHub repository created for the programming practical PRA2003. It contains a programming project about a fictional experiment on bacteria. In the simulation, each type of bacteria has a 'normal' or wild type (marked by a positive number in the database), and also a mutant type (marked by a negative number in the same database), which may or may not move and proliferate differently under different nutrient conditions. The Python code uses .txt files that can be downloaded at the provided link. Each file contains data which represents the momentum of each type of baceria from multiple measurements. From this data, the code calculates the total momentum and the statistical uncertainty in every case and also the total uncertainty using a subsampling technique.

## Requirements: 
- VS Code
- The database can be downloaded at: https://surfdrive.surf.nl/index.php/s/7udCnWTk4yMUASD
- Python 3. 14.3 or higher
- Python packages: math, os, numpy, matplotlib, scipy 

## The ID's
The following list explains which ID represents what bacterium:

- 211 E. coli WT (wild type)
- -211 E. coli mutant
- 321 Bacillus subtilis WT
- -321 Bacillus subtilis mutant
- 2212 Pseudomonas aeruginosa WT
- -2212 Pseudomonas aeruginosa antibiotic-resistant
- 3122 Streptococcus pneumoniae
- -3122 Capsule-deficient streptococcus pneumoniae
- 3312 Mycobacterium tuberculosis
- -3312 Drug-resistant mycobacterium tuberculosis
- 3334 Salmonella enteric
- -3334 Salmonella mutant

## Results:

### Plots
The plots for the 2212 and -2212 asymmetry can be seen at: Screenshot 2026-10-13 at 22.18.49.png
The plots for ID 3334 and -3334 asymmetry can be seen at:

## Are these results significant?
The code also calculates whether there is a significant asymmetry in the case of any of the data points.
For Pseudomonas aeruginosa, no significant asymmetry in the momentum was found:

Statistical Significance calculation using an unpaired t-test: 
Range [  0 -  10]: p-value = 0.6038 (Not Significant)
Range [ 10 -  25]: p-value = 0.8907 (Not Significant)
Range [ 25 -  45]: p-value = 0.8640 (Not Significant)
Range [ 45 -  70]: p-value = 0.7266 (Not Significant)
Range [ 70 - 100]: p-value = 0.5272 (Not Significant)
Range [100 - 135]: p-value = 0.4329 (Not Significant)
Range [135 - 175]: p-value = 0.3624 (Not Significant)

The same was the case for Salmonella:

Statistical Significance calculation using an unpaired t-test: 
Range [  0 -  10]: p-value = 0.5295 (Not Significant)
Range [ 10 -  25]: p-value = 0.9738 (Not Significant)
Range [ 25 -  45]: p-value = 0.9379 (Not Significant)
Range [ 45 -  70]: p-value = 0.7767 (Not Significant)
Range [ 70 - 100]: p-value = 0.1401 (Not Significant)
Range [100 - 135]: p-value = 0.6317 (Not Significant)
Range [135 - 175]: p-value = 1.0000 (Not Significant)


