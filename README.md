# JCVI-Syn3A Minimal Genome Browser

An interactive genome browser for the minimal synthetic bacterium **JCVI-Syn3A** (CP016816.2, 543,379 bp).
https://shotaharry.github.io/MinimumGenomeViewer/

## Features

- **Gene visualization** — Color-coded display of CDS, tRNA, rRNA, ncRNA, and misc_RNA
- **RNA-seq coverage** — Overlay of 4 samples from GSE205017 (normal / stationary × 2)
- **GM12 comparison** — Side-by-side comparison with the JCVI-syn1.0 (GM12) genome using BLASTn/BLASTp results
- **Gene info panel** — Click any gene to view its function, sequence, and links to NCBI / UniProt / AlphaFold
- **Search** — Jump to any gene by name or locus tag
- **Circular view** — Whole-genome circular visualization
- **Gene groups & markers** — Annotate genes with custom groups and markers (○△□★)
- **Gene comments** — Add personal notes to individual genes
- **Sequence copy** — Copy nucleotide sequence of any selected region
- **Random gene picker** — Randomly select a gene for exploration

## Usage

Open `index.html` directly in a browser — no server required.

```
open syn3A_genome_browser/index.html
```

## Data sources

| Data | Source |
|---|---|
| Genome annotation | CP016816.2 (NCBI) |
| RNA-seq | GSE205017 (SRR19432056–59) |
| GM12 comparison | CP001668 / NZ_CP001668.1 |

## Repository structure

```
syn3A_genome_browser/
├── index.html          # Main browser (self-contained)
├── genes.json          # Gene annotations
├── compare/            # GM12 comparison data (BLAST results, PAF, FASTA)
└── rnaseq/
    ├── coverage.json   # RNA-seq coverage (4 samples)
    └── genome/         # Syn3A genome sequence
```
