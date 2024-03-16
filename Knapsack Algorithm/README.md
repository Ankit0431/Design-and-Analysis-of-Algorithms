# Fractional Knapsack Problem Solver

## Overview

This repository contains a solution for the Fractional Knapsack problem. The problem involves selecting a subset of files for compression while adhering to a given storage capacity constraint. Each file is characterized by its compression ratio (weight) and priority (profit).

## Problem Definition

You are provided with:
- A set of files, each represented by a pair of attributes: compression ratio (weight) and priority (profit).
- A storage capacity, which limits the total size of the selected files.

## Input

- **Files**: Each file is represented by a pair of attributes - compression ratio (weight) and priority (profit).
- **Storage Capacity**: A maximum storage capacity limiting the selected files' total size.

## Output

- **Selected Files**: The subset of files chosen for compression, optimized for maximum priority and minimum compression ratio.

## Constraints

- The number of files is between 1 and 1000.
- Each file's compression ratio and priority are positive integers.
- The storage capacity is a positive integer.

## Approach

To solve the Fractional Knapsack problem for file compression, we employ a systematic approach that optimizes for both maximum priority and minimum compression ratio. Here's a breakdown of our methodology:

1. **Representation of Files**: Each file in the input set is represented as a pair of values: (compression ratio, priority). This representation allows us to evaluate each file's importance and impact on storage capacity independently.

2. **Sorting Algorithm**: We utilize a sorting algorithm to arrange the files based on either their compression ratios or priorities. Sorting the files enables us to efficiently process them in an order that maximizes our objective.

3. **Three Computation Methods**:
   - **Minimum Compression Ratio**: In this method, we prioritize files with the lowest compression ratios, aiming to utilize storage space efficiently. By selecting files with minimal compression ratios, we ensure that the resulting compressed data occupies as little space as possible.
   
   - **Maximum Priority**: Here, we focus on files with the highest priorities. Prioritizing files with maximum priority values ensures that important data is preserved and compressed with high fidelity. This method aims to maximize the overall value gained from file compression.
   
   - **Ratio (Priority/Compression Ratio)**: This approach calculates the ratio of priority to compression ratio for each file. By selecting files based on this ratio, we aim to strike a balance between preserving high-priority data and optimizing storage space utilization. Files with higher priority-to-compression ratio ratios are given precedence, as they offer greater value relative to their size.

4. **Performance Evaluation**: After applying each computation method, we measure the time required for computation. This evaluation allows us to assess the efficiency of each approach and compare their performance. Additionally, we plot the results to visualize the effectiveness of different methods in achieving our objectives.

## Real-life Use Cases

1. **Cloud Storage Optimization**: Companies managing cloud storage can use the algorithm to prioritize and compress files efficiently, reducing storage costs while preserving critical data integrity.

2. **Mobile Device Storage Management**: Mobile device operating systems can employ the algorithm to optimize storage usage by selecting and compressing files based on their importance and compression ratios, improving device performance and user experience.

4. **Data Backup Solutions**: Backup software can apply the algorithm to select and compress files for backup, maximizing storage efficiency and minimizing backup time while ensuring that essential data is preserved.

5. **Content Delivery Networks (CDNs)**: CDNs can use the algorithm to optimize content delivery by selecting and compressing files based on their priority and compression ratios, improving content delivery speed and efficiency.
