# Longest Common Subsequence (LCS) Solver

## Overview

This repository contains an implementation of a dynamic programming algorithm for solving the Longest Common Subsequence (LCS) problem. The LCS problem is crucial in bioinformatics for finding similarities between two DNA sequences represented as strings of A, C, G, and T characters, which represent nucleotides.

## Problem Definition

Given two DNA sequences, the goal is to find the longest common subsequence shared by both sequences. A subsequence is a sequence that appears in the same relative order, but not necessarily contiguous. The LCS problem is essential for comparing DNA sequences and understanding their evolutionary relationships.

## Input

- **DNA Sequences**: Two DNA sequences represented as strings of characters A, C, G, and T.

## Output

- **Length of LCS**: The length of the longest common subsequence shared by the two DNA sequences.
- **LCS Sequence**: The longest common subsequence itself.

## Approach

### Function `findLCS`

This function computes the length of the Longest Common Subsequence (LCS) for two given DNA sequences represented as strings `a` and `b`.

- **Inputs**:
  - `a`: String representing the first DNA sequence.
  - `b`: String representing the second DNA sequence.

- **Output**:
  - A 3-dimensional matrix `c`, where each cell contains:
    - The length of the LCS up to that position.
    - A direction indicator ('H', 'D', 'U', or 'S') representing the movement direction in the dynamic programming table.

- **Approach**:
  - Initializes a 3-D matrix `c` with dimensions `(m+1) x (n+1)`, where `m` and `n` are the lengths of strings `a` and `b` respectively.
  - Iterates through each character of both sequences.
  - If characters at the current positions are not equal, chooses the maximum LCS length from either moving up or moving left in the matrix.
  - If characters are equal, increments the LCS length by 1 and marks the diagonal move.
  - Returns the computed matrix `c`.

### Function `printLCS`

This function prints the Longest Common Subsequence (LCS) for two given DNA sequences represented as strings `a` and `b` based on the computed matrix `c`.

- **Inputs**:
  - `a`: String representing the first DNA sequence.
  - `c`: Computed matrix containing LCS length and direction indicators.
  - `i`: Current row index in the matrix `c`.
  - `j`: Current column index in the matrix `c`.

- **Output**:
  - Prints the LCS sequence.

- **Approach**:
  - Recursively traverses the matrix `c` from the bottom-right corner.
  - Prints characters from sequence `a` corresponding to the 'D' (diagonal) direction indicators in the matrix, representing matches in the LCS.
  - Continues recursively based on the direction indicators ('U' for moving up, 'S' for moving side) until reaching the top-left corner of the matrix.

## Real-life Use Cases

1. **Genomic Sequence Analysis**: Biologists and bioinformaticians use the LCS algorithm to compare genomic sequences from different organisms. Understanding similarities and differences in DNA sequences helps in studying genetic variations and evolutionary relationships.

2. **Phylogenetic Analysis**: The LCS algorithm is employed in phylogenetic analysis to infer evolutionary relationships between species based on their DNA sequences. Identifying common subsequences assists in constructing phylogenetic trees and understanding evolutionary divergence.

3. **Drug Discovery**: In drug discovery, researchers use LCS algorithms to compare DNA sequences of pathogens, such as viruses and bacteria, with host DNA. Identifying conserved regions can aid in developing targeted therapeutics and vaccines.
4. 
