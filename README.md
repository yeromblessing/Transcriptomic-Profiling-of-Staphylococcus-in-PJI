# Transcriptomic-Profiling-of-Staphylococcus-in-PJI
Background & Rationale
Periprosthetic joint infections (PJIs) are among the most devastating complications of orthopedic implants. They increase morbidity, prolong hospital stays, and often require costly revision surgeries.
Staphylococcus aureus particularly methicillin-resistant strains (MRSA) is a leading cause of PJIs. S. aureus pathogenesis stems from its ability to switch between acute and chronic infection phases. This ability contributes to treatment failure and persistent infections. 
RNA sequencing (RNA-seq) provides a systems-level approach to uncover the transcriptional programs driving this acute to chronic shift. By profiling gene expression across phases, we can:
•	Identify virulence genes unique to acute infection.
•	Detect persistence-related pathways in chronic infection.
•	Reveal regulatory RNAs linked to biofilm formation.
Project Goals
1.	Preprocessing & Quality Control
o	Trimming raw reads, quality assessment, and alignment to the S. aureus reference genome.
o	Generate count matrices for acute vs chronic isolates.
2.	Differential Gene Expression (DGE) Analysis
o	Compare acute vs chronic transcriptomes.
o	Identify virulence, stress response, and metabolic genes that are significantly up/downregulated.
3.	Functional Enrichment & Pathway Mapping
o	Conduct GO/KEGG enrichment.
o	Highlight biofilm, immune evasion, and antibiotic resistance pathways.
4.	Regulatory & Adaptation Insights
o	Explore small RNAs and transcriptional regulators shaping chronic persistence.
5.	Visualization & Communication
o	PCA plots, volcano plots, and heatmaps of DEGs.
o	Draft a clinical microbiology-style report summarizing molecular strategies of S. aureus.
Analysis Workflow
The pipeline consists of the following steps:
1.	Download raw data from ENA/SRA.
2.	Quality control using FASTQC and MultiQC.
3.	Read trimming with fastp.
4.	Reference genome download from Ensembl Bacteria (FASTA + GFF3).
5.	Genome index building with STAR.
6.	Read alignment with STAR → sorted BAM files.
7.	Read quantification using featureCounts.
8.	Differential expression analysis with DESeq2 in R.
9.	Visualization: volcano plots, heatmaps.
