# Hayoung Anna Cho

**MS in Bioinformatics & MS in Computational Science and Engineering at Georgia Tech**

I work on bacterial genomics, protein and expression modeling, and the statistics that decide what those results mean. My projects run end to end: raw data to assemblies and alignments, models with held-out evaluation, and documented limits.

[Selected work](#selected-work) · [Bioinformatics](#bioinformatics) · [Statistical analysis](#statistical-analysis) · [Simulation and applications](#simulation-and-applications)

## Selected work

### 01 · [Outbreak genomics of 34 *N. gonorrhoeae* isolates](https://github.com/hayannacho/gonorrhoeae-outbreak-genomics)
**Which isolates belong to the same outbreak, and how much does that answer depend on recombination?**

Raw Illumina reads to assemblies, a core-genome phylogeny, and SNP-distance clusters for 34 clinical isolates. I ran the Trimmomatic/SPAdes assembly arm of the course project, then rebuilt the comparative step as one containerized pipeline.

[![Pairwise SNP distances before and after recombination filtering](https://raw.githubusercontent.com/hayannacho/gonorrhoeae-outbreak-genomics/main/results/figures/snp_distances.png)](https://github.com/hayannacho/gonorrhoeae-outbreak-genomics)

**Read the figure:** the team's 50-SNP threshold separates outbreak clusters cleanly on all core SNPs (left). After Gubbins masks recombinant regions (right), every isolate falls within 43 SNPs of every other and only one of the three clusters survives as a supported clade.

**Found:** 1,170 of 1,355 SNPs (86%) sit in 74 recombination blocks, so the outbreak/sporadic split rests mostly on imported DNA rather than clonal divergence. **Stack:** ParSNP · Gubbins · IQ-TREE 2 · snp-dists · Docker.

[Explore the analysis](https://github.com/hayannacho/gonorrhoeae-outbreak-genomics) · [Pipeline](https://github.com/hayannacho/gonorrhoeae-outbreak-genomics/tree/main/pipeline) · [Assembly QC for 34 isolates](https://github.com/hayannacho/gonorrhoeae-outbreak-genomics/blob/main/results/assembly_qc.tsv)

### 02 · [Prognosis prediction from breast cancer gene expression](https://github.com/hayannacho/metabric-npi-prediction)
**Can tumor expression alone recover the Nottingham Prognostic Index risk group?**

A residual network on 489 METABRIC expression features, built with a teammate for a course project and re-evaluated afterwards on a clean split.

[![Held-out ROC curves and confusion matrix](https://raw.githubusercontent.com/hayannacho/metabric-npi-prediction/main/results/test_performance.png)](https://github.com/hayannacho/metabric-npi-prediction)

**Found:** expression carries a real but modest signal, and L2 logistic regression (71.7%, AUC 0.756) beats the residual network (68.3 ± 2.1%, AUC 0.699) on 381 held-out patients. The original notebook selected hyperparameters on the test split; this version searches on a separate validation split and scores the test set once. **Stack:** PyTorch · scikit-learn · pandas.

[Explore the model](https://github.com/hayannacho/metabric-npi-prediction) · [Metrics and search](https://github.com/hayannacho/metabric-npi-prediction/blob/main/results/metrics.json) · [Original team notebook](https://github.com/hayannacho/metabric-npi-prediction/blob/main/notebooks/ResNet.ipynb)

### 03 · [ESM2 variant prediction](https://github.com/hayannacho/esm2-variant-prediction)
**Frozen protein language-model embeddings, a trainable regression head, and candidate ranking.**

A command-line workflow adapted from a team project notebook, with position-held-out splitting, batched embedding extraction, input validation, and a reproducible synthetic example.

| Verified CPU run | Result |
|---|---|
| Backbone | `esm2_t6_8M_UR50D`, frozen, 320-dimensional |
| Labeled variants | 48 training / 12 validation, disjoint mutation positions |
| Validation MSE | 0.232305 (training-mean baseline 0.240686) |
| Spearman correlation | −0.293706 |
| Automated checks | 12 tests |

The negative rank correlation on arbitrary synthetic labels verifies the workflow, not biological ranking. **Stack:** PyTorch · fair-esm · NumPy.

[Explore the workflow](https://github.com/hayannacho/esm2-variant-prediction) · [Validation](https://github.com/hayannacho/esm2-variant-prediction/blob/main/docs/VALIDATION.md)

## Bioinformatics

| Project | What it does | Verified execution |
|---|---|---|
| [Genome sequence analysis](https://github.com/hayannacho/genome_sequence_analysis) | Exact matches, protein-to-genome candidates, spacer extraction, and annotation mapping | Five integration tests using real BLAST+ and seqtk |
| [Nextflow paired-end workflow](https://github.com/hayannacho/my_first_wf) | fastp trimming with parallel SPAdes assembly and SeqKit statistics | All three stages ran on archived and synthetic inputs, including paths with spaces |
| [Amplicon workflow](https://github.com/hayannacho/amplicon-workflow) | Extract and orient amplicons from assemblies or mapped paired reads | Four tests with real BLAST/minimap2/samtools; 192-base synthetic output |

These checks establish software behavior rather than biological accuracy or assembly quality. Each repository describes its coursework context and implementation scope.

## Statistical analysis

| Project | What it does | Verified execution |
|---|---|---|
| [Missing-data sensitivity analysis](https://github.com/hayannacho/missing-data-sensitivity-analysis) | Compare complete-case regression, multiple imputation, and alternative handling of zero-valued measurements | 400 synthetic rows, 69 screened features, two scenarios of 20 imputations × 10 iterations |
| [FIML auxiliary-variable analysis](https://github.com/hayannacho/fiml-auxiliary-variable-analysis) | Compare FIML regression with and without auxiliary variables; export robust intervals and Wald tests | Two fits converged on 800 synthetic rows; 8 checks |
| [Bayesian regression workflows](https://github.com/hayannacho/bayesian-regression-workflows) | Compare priors, fit growth curves, and estimate binary-outcome probabilities with brms/Stan | Five MCMC fits, four chains each; max R-hat 1.0042, zero divergences; 10 checks |

The public missing-data workflow uses generated observations only; no original participant records or clinical results are included.

## Simulation and applications

| Project | What it does | Verified execution |
|---|---|---|
| [Macaque social dynamics](https://github.com/hayannacho/macaque-social-dynamics) | Agent-based model of grooming, alliances, and rank change; I led configuration, grooming matrices, and biological initialization in a six-person team | Three 30-agent runs, 1,800 exported state values; 281 team tests pass |
| [PostureAware](https://github.com/hayannacho/posture-aware-study) | Webcam posture feedback with personal calibration and adaptive alert timing, from a team study | Four hardware-free tests plus a synthetic timing demo |
| [Perceptual Sense Lab](https://github.com/hayannacho/perceptual-sense-lab) | Six sight and hearing tasks with generated stimuli and adaptive staircases | Seven software and signal tests; no participant data |
| [Coursework algorithms](https://github.com/hayannacho/coursework-algorithms) | Thirteen implementations in one repository: affine-gap and local alignment, six-frame translation, primer design, RAD-seq coverage, attention and graph classifiers, HMM smoothing, clustering, Gaussian mixtures, matrix factorization | 49 tests on Python 3.11 |

Participant records are excluded from the two study repositories. Team projects identify the relevant implementation scope.

## How I work

**Explicit assumptions. Reproducible runs. Results you can inspect.**

I document inputs, commands, tested environments, and interpretation limits alongside the code. Synthetic examples are labeled as such, original participant records stay out of public repositories, and where a result depends on an analysis choice, I say which choice and show the alternative.
