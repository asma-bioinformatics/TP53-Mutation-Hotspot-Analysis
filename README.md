TP53 Mutation Hotspot Analysis

Project Overview

This project aims to identify mutation hotspots in the TP53 gene using a simulated tumor mutation dataset. The analysis reproduces a simplified version of approaches commonly used in cancer genomics studies.

TP53 is one of the most frequently mutated genes in human cancers. Identifying recurrent mutations (hotspots) is essential to understand tumor biology and functional impact.

Biological Background

The TP53 gene encodes the p53 protein, a key tumor suppressor involved in:

- DNA damage response
- cell cycle regulation
- apoptosis

Mutations in TP53 often occur at specific positions known as hotspots, such as:

- codon 175
- codon 248
- codon 273

These mutations can disrupt p53 function and promote tumor progression.

Objectives

- Identify recurrent mutations in TP53
- Detect mutation hotspots
- Quantify mutation frequency per position
- Interpret biological significance of hotspots

Dataset

The dataset contains simulated TP53 mutations derived from tumor samples.

Columns include:

- Sample ID
- Mutation
- Position

Bioinformatics Workflow

The analysis pipeline includes:

1. Removing the header
2. Extracting mutation positions
3. Counting occurrences of each position
4. Sorting results by frequency

Script Example

cut -d " " -f3 ../data/tp53_mutations.txt | tail -n +2 | sort | uniq -c | sort -nr > ../results/hotspot_counts.txt

Results

Example output:

4 248
3 175
3 273

These results indicate that codons 248, 175, and 273 are mutation hotspots.

Scientific Interpretation

The identified hotspots correspond to well-known TP53 mutation sites reported in cancer genomics studies. These positions are critical for DNA binding and protein function.

Mutations at these sites are frequently observed in:

- colorectal cancer
- lung cancer
- breast cancer

Technologies Used

- Linux command line
- Bash scripting
- Data processing (cut, sort, uniq)

Author

Asma Bouafif
Master’s degree in Biomedical Sciences
Specialization in Molecular Biology and Oncogenetics

This project is part of a bioinformatics training program focused on cancer genomics and precision medicine.

