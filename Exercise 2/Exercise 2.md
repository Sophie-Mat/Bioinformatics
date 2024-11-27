# Sequencing, alignment

## Part 1

For the first part, you must use the online version of [BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi), for the following DNA sequence:

ATGGGAAAGGAGAAGACCCACATCAACATCGTTGTCATTGGGCACGTAGATTCAGGGAAGTCTACCACGACTGGCCATCTGATCTATAAATGTGGCGGGATCGACAAGAGAACAATTGAAAAGTTCGAGAAGGAGGCTGCCGAGATGGGAAAGGGCTCCTTCAAATATGCCTGGGTCTTGGACAAACTTAAAGCTGAACGTGAGCGTGGTATCACCATTGATATCTCCCTGTGGAAATTTGAGACCAGCAAGTACTATGTTACCATCATTGATGCCCCAGGACACAGAGACTTCATCAAAAACATGATTACAGGCACATCCCAGGCTGACTGTGCTGTCCTGATCGTTGCTGCTGGTGTTGGTGAATTTGAAGCCGGTATCTCCAAGAACGGGCAGACCCGTGAGCATGCCCTTTTGGCTTACACCCTGGGTGTGAAACAACTAATTGTTGGCGTTAACAAAATGGATTCCACTGAGCCACCCTATAGCCAGAAGAGATACGAAGAAATTGTTAAGGAAGTCAGCACCTATATTAAGAAAATTGGCTACAACCCCGACACAGTAGCATTTGTGCCAATTTCTGGCTGGAATGGTGACAACATGCTAGAACCAAGTGCTAATATGCCATGGTTCAAGGGATGGAAAGTCACCCGTAAGGACGGCAATGCCAGTGGAACCACCCTGCTTGAAGCTCTGGATTGCATTCTGCCACCAACTCGCCCAACTGACAAACCCTTGCGTTTGCCTCTCCAGGATGTCTATAAAATTGGTGGTATTGGTACTGTCCCTGTGGGTCGTGTGGAGACTGGTGTTCTCAAACCTGGCATGGTGGTCACCTTTGCTCCAGTCAATGTAACAACTGAAGTGAAGTCTGTAGAAATGCACCATGAAGCATTGAGTGAAGCCCTTCCTGGGGACAATGTGGGCTTTAATGTCAAAAACGTGTCTGTCAAAGATGTCCGTCGTGGCAATGTGGCTGGTGACAGCAAAAATGATCCACCCATGGAAGCTGCTGGCTTCACAGCTCAGGTGATTATTTTGAACCATCCAGGCCAAATCAGTGCTGGATATGCACCTGTGCTGGATTGTCACACAGCTCACATTGCTTGCAAGTTTGCTGAGCTGAAGGAGAAGATTGATCGTCGTTCTGGGAAAAAGCTGGAAGATGGCCCTAAATTCTTGAAATCTGGTGACGCTGCCATCGTTGATATGGTTCCTGGCAAGCCCATGTGTGTCGAGAGCTTCTCTGATTATCCTCCCCTGGGCCGTTTTGCTGTGCGTGACATGAGACAGACAGTCGCTGTGGGTGTCATCAAAGCAGTGGACAAGAAGGCAGCTGGAGCTGGCAAGGTCACCAAGTCTGCCCAGAAAGCTCAGAAGGCTAAATGA

1. Identify the species and the gene that the following DNA sequence belongs to. 
2. Using the filters of online BLAST narrow down your search to the species Bison (taxid:9900). Are there sequences with high similarity?
3. Repeat the procedure for the species Mus musculus (taxid:10090).
4. You can translate your DNA sequence to Amino Acid sequences using the online tool [expasy translate](https://web.expasy.org/translate/). Translate your DNA sequence to Amino Acids sequence and select the results of the first frame. Go to the BLAST again and run the protein-protein version of the tool.
5. Again, using the filters of online BLAST narrow down your search to the species Bison (taxid:9900). Are there sequences with high similarity? Repeat the procedure for the species Mus musculus (taxid:10090). 

Write your answers as Markdowns in the Jupiter Notebook.

## Part 2

For part 2 you will use sequences of CTCF gene. Specifically, you will use the DNA sequence of CTCF gene for [homo sapiens](https://github.com/Sophie-Mat/Bioinformatics/blob/main/Exercise%202/CTCF_DNA_HOMO.fna) and for [mus musculus](https://github.com/Sophie-Mat/Bioinformatics/blob/main/Exercise%202/CTCF__DNA_MUS.fna) and the protein sequence (amino acid) of CTCF gene for [homo sapiens](https://github.com/Sophie-Mat/Bioinformatics/blob/main/Exercise%202/CTCF_AA_HOMO.faa) and for [mus musculus](https://github.com/Sophie-Mat/Bioinformatics/blob/main/Exercise%202/CTCF_AA_MUS.faa). 
1. Use the first 100 nucleotides from the DNA sequence of CTCF gene for human and mouse to create a Dot Matrix with k-mer k=6.
2. Use the protein sequence of CTCF gene for human and mouse to create a Dot Matrix with k-mer k=3.

## Part 3

1. Using the datasets from part 2, implement your own Smith-Waterman Algorithm for global alignment of the Amino Acid sequences with the following parameters: Identical = +2, substitution = -2 and gap penalty = -1. Print the final scoring matrix and find the position of the highest value.

## Part 4

1. Using the datasets from part 2, implement your own Smith-Waterman Algorithm for global alignment of the Amino Acid sequences that will score the identical and substitutions based on the [BLOSUM62 scoring matrix](https://github.com/Sophie-Mat/Bioinformatics/blob/main/Exercise%202/BLOSUM62.txt) (tab delimeted file). For gap penalty use -10. Print the final scoring matrix and find the position of the highest value.
