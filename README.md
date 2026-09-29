# Programming-practical-group-3-biology
### To move or not to move: which nutrient conditions affect the movement of various types of bacteria the most?
This is the GitHub repository created for the programming practical PRA2003. It contains a programming project about a fictional experiment on bacteria. In the simulation, each type of bacteria has a 'normal' or wild type (marked by a positive number in the database), and also a mutant type (marked by a negative number in the same database), which may or may not move and proliferate differently under different nutrient conditions. The Python code uses .txt files that can be downloaded at the provided link. Each file contains data which represents the momentum of each type of baceria from multiple measurements. From this data, the code calculates the total momentum and the statistical uncertainty in every case and also the total uncertainty using a subsampling technique.

## Requirements: 
- VS Code
- The database can be downloaded at: https://surfdrive.surf.nl/index.php/s/7udCnWTk4yMUASD
- Python 3. 14.3 or higher
- Python packages: math, statistics

## Results
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

This is an example of what the code shows when run for one datafile (set1.txt in this case). The total mean and total uncertainty is calculated using the subsampling method:

total calculations   
- ID   211: Mean of Means = 3.52503 | Total Uncertainty = 1.80023
- ID  -211: Mean of Means = 3.51546 | Total Uncertainty = 1.78150
- ID   321: Mean of Means = 4.77971 | Total Uncertainty = 4.67576
- ID  -321: Mean of Means = 4.72950 | Total Uncertainty = 4.53423
- ID  2212: Mean of Means = 6.01319 | Total Uncertainty = 6.39436
- ID -2212: Mean of Means = 5.95920 | Total Uncertainty = 6.29231
- ID  3122: Mean of Means = 7.01459 | Total Uncertainty = 9.24449
- ID -3122: Mean of Means = 6.94246 | Total Uncertainty = 8.96663
- ID  3312: Mean of Means = 8.08212 | Total Uncertainty = 11.24226
- ID -3312: Mean of Means = 8.03394 | Total Uncertainty = 10.96069
- ID  3334: Mean of Means = 9.45021 | Total Uncertainty = 14.08595
- ID -3334: Mean of Means = 9.92836 | Total Uncertainty = 12.34447

