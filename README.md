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

## Bioinformatics workflows

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

## Working approach

I document inputs, execution steps, tested environments and interpretation limits. Each featured repository identifies contribution scope, source provenance, and tested execution steps. Synthetic examples are labelled explicitly, and original participant records are excluded from the public study repositories.
