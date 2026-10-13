# Programming-practical-group-3-biology
### To move or not to move: how do certain nutrient conditions affect the movement of various types of bacteria?
This is the GitHub repository created for the programming practical PRA2003. It contains a programming project about a fictional experiment on bacteria. In the simulation, each type of bacteria has a 'normal' or wild type (marked by a positive number in the database), and also a mutant type (marked by a negative number in the same database), which may or may not move and proliferate differently under certain nutrient conditions. 

### The question is: is there any asymmetry in the behavior of the wild type and the mutant type?

The Python code uses .txt files that can be downloaded at the provided link. Each file contains data which represents the momentum of each type of baceria from multiple measurements. This code analyzes the files and calculates the asymmetry between the wild type and the mutant type for any ID; this project focused on analyzing the behavior of Pseudomonas aeruginosa (ID's: 2212 (wild type), -2212 (mutant type)) and Salmonella (ID's: 3334 (wild type), -3334 (mutant type)). The total momentum for each bacteria in each measurement is calculated using the formula p = sqrt(px^2+py^2+pz^2). Then the code uses subsampling to calculate the asymmetry, and plots it. The uncertainty is the standard deviation, shown by the y error bars. The x error bars show the bin widths (for the subsampling). After, the code calculates whether the difference is significant for each data point using an unpaired t-test, and prints the result.

## Requirements: 
- VS Code
- The database can be downloaded at: https://surfdrive.surf.nl/index.php/s/7udCnWTk4yMUASD
- Python 3. 14.3 or higher
- Python packages: math, os, numpy, matplotlib, scipy 

## The ID's - what means what in the text files?
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

Each file contains data from multiple experiments. The beginning of every measurement is marked by a header, after which each line contains four numbers: the first three are the x, y, and z components of the momentum for each bacterium, and the last one is the ID, indicating what type and what strain of bacterium we are looking at.

## Results:

### Plots
The plots for the 2212 and -2212 asymmetry can be seen at: Screenshot 2026-10-13 at 22.18.49.png
The plots for ID 3334 and -3334 asymmetry can be seen at: Screenshot 2026-10-13 at 22.50.32.png

## Are these results significant?
The code also calculates whether there is a significant asymmetry in the case of any of the data points.
For Pseudomonas aeruginosa, no significant asymmetry in the momentum was found:

Statistical Significance calculation using an unpaired t-test: 
- Range [  0 -  10]: p-value = 0.6038 (Not Significant)
- Range [ 10 -  25]: p-value = 0.8907 (Not Significant)
- Range [ 25 -  45]: p-value = 0.8640 (Not Significant)
- Range [ 45 -  70]: p-value = 0.7266 (Not Significant)
- Range [ 70 - 100]: p-value = 0.5272 (Not Significant)
- Range [100 - 135]: p-value = 0.4329 (Not Significant)
- Range [135 - 175]: p-value = 0.3624 (Not Significant)

The same was the case for Salmonella:

Statistical Significance calculation using an unpaired t-test: 
- Range [  0 -  10]: p-value = 0.5295 (Not Significant)
- Range [ 10 -  25]: p-value = 0.9738 (Not Significant)
- Range [ 25 -  45]: p-value = 0.9379 (Not Significant)
- Range [ 45 -  70]: p-value = 0.7767 (Not Significant)
- Range [ 70 - 100]: p-value = 0.1401 (Not Significant)
- Range [100 - 135]: p-value = 0.6317 (Not Significant)
- Range [135 - 175]: p-value = 1.0000 (Not Significant)


