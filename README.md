# 🧬 Needleman-Wunsch Dynamic Programming Aligner: TP53 Mutation Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lRDiGK7fu7zWZAFQmKLGOii05rLullp5?usp=sharing)

## 📌 Project Overview
This repository contains a pure Python implementation of the foundational **Needleman-Wunsch global sequence alignment algorithm**. Built entirely from scratch without relying on external packages (such as Biopython), this project demonstrates core proficiency in computer science fundamentals applied directly to molecular oncology.

The tool constructs a two-dimensional scoring matrix, executes dynamic programming path-finding optimization, and performs a matrix traceback to map sequence variations between reference sequences and clinical variants.

## 🔬 Biological Application: TP53 & Oncology
In cancer biology, pinpointing the exact location of structural variants is critical. This aligner is configured to scan sequence segments of the **TP53 tumor suppressor gene** to identify somatic hypermutations, substitutions, and frame-shift deletions. 

By applying a custom scoring matrix (Match: +1, Mismatch: -1, Gap: -2), the algorithm mathematically determines the optimal alignment, accurately placing insertion/deletion gaps (`-`) to restore the correct reading frame comparison—mirroring the alignment mechanics used in large-scale pipelines like BLAST.

## 📊 Sample Diagnostic Readout
When processing batch patient samples, the pipeline outputs structured analysis summaries:

```text
RUNNING AUTOMATED SCREENING PIPELINE...

🧬 PATIENT RUN: Biopsy B (Lymphoma Clone)
-----------------------------------
Wild-Type TP53: SQKTYQGSYGFRLGFLHSGTAKSVTCTYSPA
                ||||||||||||| |*||||||||||||*||
Tumor Target:   SQKTYQGSYGFRL-FLHSGTAKSVTCTHSPA
-----------------------------------
Sequence Identity: 90.3% | Total Alterations: 3
-----------------------------------
