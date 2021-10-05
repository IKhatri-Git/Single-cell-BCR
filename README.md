# Single-cell-BCR
B-cell receptor repertoire analysis from single-cell

Two python notebooks for following Methods section are provided in separate folders.

###Identification of B cell clonotypes
Multiple files obtained from the IMGT HighV-Quest were combined using an in-house Python script. The B cell clonotypes were identified with the same V family, J family, and 80% nucleotide identity in IG heavy chain CDR3 as computed by Levenshtein distance {Python}. As V gene assignment might be flawed by the assignment methods, we used the V family to call clonotypes which avoids inaccurate grouping of the clones in the first place. Also, a comparative assessment was performed of the clonotypes obtained when using V genes versus V family in assigning B cell clonotypes.


##Query tool to identify anti-toxoid BCRs

The currently profiled BCRs comprise of all the PB/PCs raised in response to the vaccine which comprises of multiple components. To identify the contribution of each component of the vaccine, we developed an in-house tool using Python. To show its functionality, junction sequences related to anti-TT, anti-DT, anti-FHA, anti-Prn and anti-PT were searched in the literature. We could only identify the CDR3 sequences for anti-TT, anti-DT and anti-PT. These sequences were searched in the Boostrix-specific BCR-rep obtained in this study. The search was not only performed based on the percentage identity, but a parameter of length flexibility was also incorporated; i.e. the search space will include junction sequences that are longer or shorter by a user defined length. The sequence similarity is calculated based on the Levenshtein distance of the junction sequences.
