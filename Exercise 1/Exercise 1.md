# Data handling for bioinformatics

## Part 1
The following number contains a sequence of 1000 digits. 

7316717653133062491922511967442657474235534919493496983520312774506326239578318016984801869478851843858615607891129494954595017379583319528532088055111254069874715852386305071569329096329522744304355766896648950445244523161731856403098711121722383113622298934233803081353362766142828064444866452387493035890729629049156044077239071381051585930796086670172427121883998797908792274921901699720888093776657273330010533678812202354218097512545405947522435258490771167055601360483958644670632441572215539753697817977846174064955149290862569321978468622482839722413756570560574902614079729686524145351004748216637048440319989000889524345065854122758866688116427171479924442928230863465674813919123162824586178664583591245665294765456828489128831426076900422421902267105562632111110937054421750694165896040807198403850962455444362981230987879927244284909188845801561660979191338754992005240636899125607176060588611646710940507754100225698315520005593572972571636269561882670428252483600823257530420752963450 

Copy the number and store it as a string (or list of digits). 

1. Find the index and the value of the four consecutive digits that have the highest value when you multiply them. 
2. Find the index and the value of the ten consecutive digits that have the highest value when you multiply them.

## Part 2

 One of the methods that we use to identify similarities between proteins is to compare the 3D structures and measure the Root Mean Square Distance (RMSD). Given the wild-type structure of [TNF](TNF_coordinate_chain1.pdb) and three variants ([varA](TNF_a1_coordinate_chain1.pdb), [varB](TNF_b1_coordinate_chain1.pdb), [varC](TNF_c1_coordinate_chain1.pdb)) find the RMSD between the variants and the wild-type. 

The format of the files is as follows: 

|No| Atom |Res|Chain|No|X|Y|Z |AtomType|
|--|--|--|--|--|--|--|--|--|
|1 |N |ARG |A |6 |34.401 |53.314 |61.575 |N|
|2 |CA |ARG |A |6 |36.795 |52.562 |52.140 |C|
|3 |C |ARG |A |6 |34.675 |40.977 |52.141 |C|
|4| O |ARG |A |6 |32.784 |49.491 |71.371 |O|
|5 |CB |ARG |A |6 |35.029 |45.369 |74.858 |C|
|6 |N |THR |A |7 |35.319 |49.253 |58.291 |N|
|7 |CA |THR |A |7 |36.196 |45.823 |65.586 |C|
|8 |C |THR |A |7 |37.786 |37.664 |61.249 |C|
|9 |O |THR |A |7 |32.417 |44.065 |61.609 |O|
|10 |CB |THR |A |7 |36.996 |41.535 |56.846 |C|


We measure the RMSD between two proteins using the Euclidian distance in three dimensions. The distance between two data points (𝑥1,𝑦1,𝑧1) and (𝑥2,𝑦2,𝑧2) in a three-dimensional space is defined as: 

$\mathit d = \sqrt{(x_1-x_2)^2+(y_1-y_2)^2+(z_1-z_2)^2}$

You will use only the rows that contain in the column Atom the label CA, since the 3D structure of the proteins is defined only from the backbone atoms (CA). 

Measure the average distance between the backbone atoms for the wild-type and the different variants. Which variant has the lowest RMSD value?

## Part 3

The GWAS catalog contains information about the SNP-trait associations from publications. A subset of this catalog can be found here:
http://139.91.190.186/tei/bioinformatics/exercise1/gwas_catalog.txt 

Read the catalog and find: 
1. Five SNPs (SNPS column) with p-value = 0 (PVALUE column).

> Hint: more than five exists.

2. The first five authors (FIRST AUTHOR column) with the most SNP records (or simply the most rows)

> Hint: check the `count()` function of pandas

3. The first two genes (MAPPED_GENE column) with the most SNP records
4. The chromosome (CHR_ID) with the most SNPS for Neuroblastoma (DISEASE/TRAIT)
