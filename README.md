# Hayoung Anna Cho

**Bioinformatics at Georgia Tech · Python, R and reproducible research workflows**

I work on computational biology, simulation and data analysis. My projects connect biological questions with configurable models, statistical workflows and usable research software.

## Selected projects

### [Macaque Social Dynamics](https://github.com/hayannacho/macaque-social-dynamics)
Explore how grooming strategies and alliance dynamics shape simulated dominance hierarchies.

- **Focus:** configuration, grooming matrices and biological initialization within a six-person team project.
- **See it run:** three-strategy demo, matrix visualization and a locally verified 281-test suite.
- **Stack:** Python · NumPy · SciPy · simulation

### [PostureAware](https://github.com/hayannacho/posture-aware-study)
A team course project implementing a local webcam application for immediate versus adaptive posture feedback.

- **Focus:** webcam calibration, posture monitoring and adaptive feedback; application code developed with AI assistance.
- **Explore:** personal calibration, posture monitoring, feedback and session summaries. Four hardware-free checks passed; live camera/audio behavior requires separate verification.
- **Stack:** Python · MediaPipe · Flask · Socket.IO
- **Data:** original participant data excluded.

### [Missing-data Sensitivity Analysis](https://github.com/hayannacho/missing-data-sensitivity-analysis)
Compare complete-case regression, multiple imputation and measurement-handling scenarios.

- **Focus:** missingness analysis, pooled regression and measurement-handling sensitivity checks.
- **See it run:** generated data, pooled estimates and a validated HTML report; both scenarios complete 20 imputations × 10 iterations.
- **Stack:** R · mice · R Markdown · Python
- **Data:** synthetic demonstration only; no real ADNI data or clinical findings.

## Statistical learning

### [Bayesian regression workflows](https://github.com/hayannacho/bayesian-regression-workflows)
Compare slope priors, fit random-intercept/random-slope growth curves, and estimate binary-outcome probabilities with brms and Stan.

- **Verified:** five real MCMC fits, four chains each, and 10 passing checks; maximum R-hat 1.0042 and zero divergences. [Results and plots](https://github.com/hayannacho/bayesian-regression-workflows).
- **Synthetic result:** population time slope −0.355 for a generating value of −0.35; fictional observations only, with no clinical or original-course-data results.
- **Context:** individual PSYC 8803 coursework, Fall 2025; model specification, prior comparison, and posterior interpretation.
- **Stack:** R · brms · Stan · Docker

### [Gaussian mixture clustering with EM](https://github.com/hayannacho/gmm-em-clustering)
Fit a full-covariance Gaussian mixture in NumPy and export assignments and likelihood traces.

- **Verified:** seven independent tests and seven course tests passed; a 600-point synthetic demo converged in 11 iterations.
- **Implementation:** individual CSE 6740 coursework implementing initialization, covariance estimation, Gaussian density, E/M updates and model training.
- **Data:** synthetic observations only.
- **Stack:** Python · NumPy

## Bioinformatics workflows

### [ESM2 variant prediction](https://github.com/hayannacho/esm2-variant-prediction)
Score single amino-acid substitutions with frozen ESM2 embeddings and a neural regression head; export validation metrics and candidate rankings.

- **Verified:** real ESM2 8M CPU inference for 80 synthetic variants, five training epochs, a 48/12 position-held-out split, 20 candidate predictions, and 12 passing tests. [Results](https://github.com/hayannacho/esm2-variant-prediction/blob/main/docs/VALIDATION.md).
- **Result limits:** synthetic validation MSE 0.232305 and Spearman −0.293706; an execution demo, not evidence of useful biological ranking.
- **Context:** CX 4803 · Spring 2025 · team project; frozen protein embeddings, regression, validation, and ranking.
- **Stack:** Python · PyTorch · fair-esm · NumPy · SciPy

### [Local alignment path counter](https://github.com/hayannacho/local-alignment-path-counter)
Compute optimal local DNA-alignment scores and count coordinate-distinct traceback paths; export total and endpoint counts as JSON.

- **Verified:** seven tests passed, including 1,922 score/count comparisons against independent exhaustive enumeration. Archive-compatible mode also matched the original function on 961 short sequence pairs. [Validation](https://github.com/hayannacho/local-alignment-path-counter/blob/main/docs/VALIDATION.md).
- **Scope:** individual coursework implementing score/count dynamic programming and tied-path aggregation. Scoring correction, CLI and tests are documented as current maintenance. [Source and changes](https://github.com/hayannacho/local-alignment-path-counter/blob/main/docs/PROVENANCE.md).
- **Data:** synthetic toy sequences only; short-sequence algorithm demonstration, not a biological significance test.
- **Context:** CSE 6301 · Fall 2025 · Homework 1
- **Stack:** Python standard library

### [RAD-seq coverage demo](https://github.com/hayannacho/rad-seq-coverage-demo)
Compare educational Single RAD, ddRAD and 2bRAD coverage windows with two-sample variant positions; export BED, TSV and JSON results.

- **Verified:** eight tests passed across all three modes, coordinate boundaries, overlapping intervals and repeatability. The synthetic example produces 3 / 8 / 1 windows and covers 3 / 4 / 1 variant records respectively. [Validation](https://github.com/hayannacho/rad-seq-coverage-demo/blob/main/docs/VALIDATION.md).
- **Scope:** team coursework covering motif matching, interval construction and genotype filtering. Current maintenance changes are documented separately. [Source and changes](https://github.com/hayannacho/rad-seq-coverage-demo/blob/main/docs/PROVENANCE.md).
- **Data:** entirely synthetic FASTA/VCF examples; a simplified recognition-start model, not a physical digestion or sequencing-yield simulator.
- **Context:** BIOL 6505 · Fall 2025 · team project
- **Stack:** Python · Biopython

### [Alignment variability profiler](https://github.com/hayannacho/alignment-variability-profiler)
Summarize variable columns in aligned protein sequences and export per-column counts, fractions and a ranked plot.

- **Verified:** seven tests passed, including agreement with the archived script on the synthetic example; a Linux Python 3.12 smoke run also generated CSV and PNG. [Validation](https://github.com/hayannacho/alignment-variability-profiler/blob/main/docs/VALIDATION.md).
- **Scope:** aligned-FASTA parsing, per-column residue counting, ranking and plotting, based on the named coursework script; current CLI, validation and output additions are documented separately. [Source and changes](https://github.com/hayannacho/alignment-variability-profiler/blob/main/docs/PROVENANCE.md).
- **Data:** synthetic example only—four artificial sequences, ten alignment columns, three variable columns. Counts describe observed sequence variation, not evolutionary mutation events.
- **Context:** BIOL 7200 · Fall 2024
- **Stack:** Python · Biopython · Matplotlib

### [Genome sequence analysis](https://github.com/hayannacho/genome_sequence_analysis)
Search exact nucleotide matches and protein-to-genome candidates, extract repeat-flanked spacer candidates, and map alignments to annotated genes.

- **Verified:** five synthetic integration tests passed with real BLAST+ and seqtk, covering reverse-strand/BED boundaries, spacer extraction, paths with spaces, and failure handling. [Validation](https://github.com/hayannacho/genome_sequence_analysis/blob/main/docs/VALIDATION.md).
- **Scope:** Bash workflow integration, sequence filtering and coordinate handling, with archived coursework separated from current corrections. [Source and changes](https://github.com/hayannacho/genome_sequence_analysis/blob/main/docs/PROVENANCE.md).
- **Context:** BIOL 7200 · Fall 2024
- **Stack:** Bash · BLAST+ · seqtk · Docker

### [Paired-end processing with Nextflow](https://github.com/hayannacho/my_first_wf)
Trim paired reads with fastp, then run SPAdes assembly and SeqKit statistics as parallel downstream branches.

- **Verified:** all three stages completed on the archived read subset, synthetic inputs, and inputs with spaces in their filenames; output checks confirmed paired FASTQ, statistics and nonempty assemblies. [Validation](https://github.com/hayannacho/my_first_wf/blob/main/docs/VALIDATION.md).
- **Scope:** composing the three-tool workflow and configuring inputs, execution and outputs; archived coursework and current maintenance changes are documented separately. [Source and changes](https://github.com/hayannacho/my_first_wf/blob/main/docs/PROVENANCE.md).
- **Context:** BIOL 7210 · Spring 2025
- **Stack:** Nextflow DSL2 · fastp · SPAdes · SeqKit · Docker

These checks demonstrate execution, not biological accuracy or genome-assembly quality. The underlying bioinformatics tools are external software; the contribution described here is their workflow integration.

## More computational projects

Runnable coursework implementations with synthetic examples. Checks below describe local execution and algorithm behavior; tiny training fixtures are not benchmark accuracy results.

| Project | Function | Verified result |
|---|---|---|
| [Six-frame DNA translation](https://github.com/hayannacho/six-frame-dna-translator) | Standard-code translation on both strands | 64 codons and six-frame fixtures; 3 tests |
| [Affine-gap global alignment](https://github.com/hayannacho/affine-global-alignment) | Three-state dynamic programming and traceback | 225 short pairs vs exhaustive oracle; 2 tests |
| [Hidden-state inference](https://github.com/hayannacho/hmm-state-inference) | Scaled forward–backward posterior probabilities | Hidden-state enumeration and normalization; 2 tests |
| [Matrix factorization](https://github.com/hayannacho/matrix-factorization-recommender) | Biased low-rank SGD for missing ratings | Synthetic training RMSE 1.69967 → 1.55173; 2 tests |
| [Bacterial competition](https://github.com/hayannacho/bacterial-competition-simulator) | Seeded killing/reproduction on a lattice | Population and event accounting; 3 tests |
| [Climate finance demo](https://github.com/hayannacho/climate-finance-demo) | Country joins, coal shares, CSV and scatter plot | 6 fictional countries; 3 tests |
| [Graph learning baselines](https://github.com/hayannacho/graph-learning-baselines) | MLP/GCN node and pooled graph classification | CPU training and permutation equivariance; 3 tests |
| [Primer design](https://github.com/hayannacho/primer-design-demo) | Primer3 pairs around a genomic position | Binding coordinates and 600–800 bp products; 3 tests |
| [K-means / K-medoids](https://github.com/hayannacho/kmeans-kmedoids-comparison) | Mean and medoid clustering with outliers | Known clusters and duplicate-point behavior; 3 tests |
| [Protein attention classifier](https://github.com/hayannacho/protein-attention-classifier) | Amino-acid self-attention and masked pooling | Padding invariance and CPU backpropagation; 3 tests |

### [Perceptual Sense Lab](https://github.com/hayannacho/perceptual-sense-lab)
Run six local sight/hearing tasks with generated visual and audio stimuli, adaptive 3-AFC trials and threshold plots.

- **Verified:** seven automated tests passed, covering all six pages, adaptive response recording, staircase reversals, WAV frequency and amplitude, gap timing and screen calculations.
- **Context:** individual Human–Systems Integration coursework, Summer 2026, Assignment 2.
- **Data:** synthetic signals and scripted test responses; personal measurements and the original report are excluded. Hardware calibration and human thresholds were not validated by these software checks.
- **Stack:** Python · Streamlit · NumPy · Matplotlib · Pillow

## Working approach

I document inputs, execution steps, tested environments and interpretation limits. Each featured repository documents implementation and tested execution steps. Synthetic examples are labelled explicitly, and original participant records are excluded from the public study repositories.
