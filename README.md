# Epigenomic-Analysis-IMR90-DNase-seq-Chromatin-Accessibility-Data-GSM468792
Epigenomic Profiling Pipeline Automated Retrieval Processing and MultiMetric Static Visualization of IMR90 DNase seq Chromatin Accessibility Data GSM468792
Static Epigenomic Profiling Pipeline: DNase-seq Chromatin Accessibility Analysis (GSM468792)

This repository contains a complete Python analysis pipeline designed to automatically retrieve, process, and visualize public chromatin accessibility data, specifically DNase-seq data from the Roadmap Epigenomics Project.

The primary dataset analyzed is GSM468792, representing DNase Hypersensitivity Peaks in the IMR90 Fetal Lung Fibroblast Cell Line.

The pipeline focuses on generating static, high-quality visualizations and quantitative summaries of the accessible chromatin landscape.

🔬 Technical Title

Static Epigenomic Profiling Pipeline: Automated Retrieval, Processing, and Multi-Metric Static Visualization of IMR90 DNase-seq Chromatin Accessibility Data (GSM468792)

🚀 Key Features

Automated Data Retrieval: Uses GEOparse to fetch metadata and wget to download the raw supplementary BED file directly from the NCBI GEO database.

Data Processing: Loads, cleans, and filters genomic coordinates, calculates peak lengths, and restricts analysis to standard human chromosomes (chr1-chr22, chrX, chrY).

Static Visualization: Generates three essential static plots using Matplotlib and Seaborn for clear, publication-quality reporting.

Quantitative Summary: Exports detailed descriptive statistics of peak lengths per chromosome to a CSV file.

💾 Repository Contents

Epigenomic_Profiling_Pipeline_Automated_Retrieval_Processing_and_MultiMetric_Static_Visualization_of_IMR90_DNase_seq_Chromatin_Accessibility_Data_GSM468792.ipynb: The main Jupyter Notebook containing the full analysis workflow in runnable cells.

IMR90_DNase.bed: (Generated upon first run) The raw DNase hypersensitivity peaks file.

GSM468792_processed_summary_static.csv: (Generated upon first run) CSV file containing summary statistics (count, mean, median, quartiles, etc.) of peak lengths per chromosome.

🛠️ Setup and Installation

Prerequisites

Python 3.x

Jupyter Notebook or a Python IDE (VS Code, PyCharm, Spyder) that supports running code cells (# %% blocks).

1. Install Python Packages

Run the following command (or run the first cell in the notebook) to install the necessary libraries:

pip install GEOparse matplotlib seaborn pandas


2. Install System Tools (Optional, but recommended for command-line efficiency)

The pipeline uses wget and gunzip for downloading and extracting the .bed.gz file. These are standard on most Linux/Unix/macOS systems. If running on a minimal environment, you may need to ensure they are available:

# Example for Debian/Ubuntu environments
!apt-get install -y wget gunzip


📋 Analysis Workflow

The Jupyter Notebook is organized into logical, runnable cells:

Cell

Purpose

Description

1

Setup & Imports

Installs and imports GEOparse, pandas, matplotlib, and seaborn.

2

Metadata Fetching

Retrieves and prints metadata for GSM468792 to verify the sample source and type.

3

Data Download

Downloads the IMR90_DNase.bed.gz file and extracts the raw IMR90_DNase.bed.

4

Data Loading & Cleaning

Loads the tab-separated BED file, calculates the length of each peak, and filters for standard chromosomes.

5

Static Visualization

Generates the primary static plots (Histogram and Bar Chart).

6

Export Summary

Calculates and exports descriptive statistics of peak lengths per chromosome to CSV.

📊 Key Findings & Static Visualizations

The static plots provide robust evidence regarding the characteristics of accessible chromatin in IMR90 cells.

1. Peak Length Distribution (Histogram)

Finding: The vast majority of DNase peaks cluster tightly around 35 base pairs (bp), indicating high-resolution data and the prevalence of short, precisely defined accessible regions (e.g., transcription factor footprints).

2. Number of Peaks per Chromosome (Bar Chart)

Finding: Peak counts correlate strongly with chromosome size and gene density. Larger chromosomes (e.g., chr1, chr2) harbor the highest number of accessible sites, which is consistent with the genomic landscape of open chromatin.

3. Peak Length Variability by Chromosome (Box Plot)

Finding: The median and interquartile range of peak lengths are remarkably consistent across all chromosomes. This suggests a uniform biological mechanism dictating the size of open chromatin sites throughout the genome.

📝 Citation

The raw data for this analysis pipeline is derived from the Roadmap Epigenomics Project and can be accessed via the NCBI Gene Expression Omnibus (GEO) under the accession ID GSM468792.
