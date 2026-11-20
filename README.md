# Hayoung Anna Cho

**MS in Bioinformatics & MS in Computational Science and Engineering at Georgia Tech**

I build research workflows that turn biological questions into configurable models, reproducible analyses, and usable software. My projects span Python and R, sequence analysis, simulation, and interactive research applications.

[Selected work](#selected-work) · [Statistical analysis](#statistical-analysis) · [Bioinformatics](#bioinformatics) · [More implementations](#more-implementations)

## Selected work

### 01 · [Macaque Social Dynamics](https://github.com/hayannacho/macaque-social-dynamics)
**From biological assumptions to a runnable social-dynamics model.**

Compare three grooming strategies and inspect the resulting power trajectories. My focus was configuration, grooming matrices, and biological initialization within a six-person team project.

[![Three seeded macaque simulation outputs](https://raw.githubusercontent.com/hayannacho/macaque-social-dynamics/main/docs/assets/strategy-results.png)](https://github.com/hayannacho/macaque-social-dynamics)

**Verified:** three 30-agent runs; 1,800 exported state values; 281 tests passed. Exploratory simulation, with model assumptions and limits documented. **Stack:** Python · NumPy · Matplotlib.

[Explore the model](https://github.com/hayannacho/macaque-social-dynamics) · [Contribution scope](https://github.com/hayannacho/macaque-social-dynamics/blob/main/docs/CONTRIBUTIONS.md) · [Validation](https://github.com/hayannacho/macaque-social-dynamics/blob/main/docs/VALIDATION.md)

### 02 · [PostureAware](https://github.com/hayannacho/posture-aware-study)
**Personal calibration and adaptive feedback in a local webcam app.**

A team course project connecting MediaPipe pose estimation, baseline calibration, visual/audio feedback, and session summaries. The preview below runs the actual feedback logic with scripted inputs.

[![Immediate and adaptive alert timing on synthetic inputs](https://raw.githubusercontent.com/hayannacho/posture-aware-study/main/docs/assets/feedback-timing.png)](https://github.com/hayannacho/posture-aware-study)

**Verified:** four hardware-free tests plus a synthetic timing demo; first alerts occur after 1s versus 5s of scripted poor posture. Participant data are excluded; camera/audio performance and intervention efficacy are not established by these checks. **Stack:** Python · MediaPipe · Flask · Socket.IO.

[Explore the app](https://github.com/hayannacho/posture-aware-study) · [Validation](https://github.com/hayannacho/posture-aware-study/blob/main/docs/VALIDATION.md) · [Application-code AI disclosure](https://github.com/hayannacho/posture-aware-study/blob/main/AI_USAGE.md)

### 03 · [Missing-data Sensitivity Analysis](https://github.com/hayannacho/missing-data-sensitivity-analysis)
**Make the consequences of missing-data decisions visible.**

Individual coursework comparing complete-case regression, multiple imputation, and alternative handling of zero-valued measurements. The public workflow uses generated observations only.

[![Synthetic regression estimates and analysis populations](https://raw.githubusercontent.com/hayannacho/missing-data-sensitivity-analysis/main/docs/assets/sensitivity-results.png)](https://github.com/hayannacho/missing-data-sensitivity-analysis)

**Verified:** 400 synthetic rows, 69 screened features, and two scenarios with 20 imputations × 10 iterations each; Python checks and the complete R/HTML pipeline passed. **Stack:** R · mice · R Markdown · Python.

[Explore the analysis](https://github.com/hayannacho/missing-data-sensitivity-analysis) · [Exact plotted results](https://github.com/hayannacho/missing-data-sensitivity-analysis/blob/main/docs/demo/coefficient-comparison.csv) · [Validation](https://github.com/hayannacho/missing-data-sensitivity-analysis/blob/main/docs/VALIDATION.md)

## Statistical analysis

| Project | What it does | Verified execution |
|---|---|---|
| [FIML auxiliary-variable analysis](https://github.com/hayannacho/fiml-auxiliary-variable-analysis) | Compare FIML regression with and without auxiliary variables; export robust intervals and Wald tests | Two fits converged on 800 synthetic rows; 8 checks |
| [Bayesian regression workflows](https://github.com/hayannacho/bayesian-regression-workflows) | Compare priors, fit growth curves, and estimate binary-outcome probabilities with brms/Stan | Five MCMC fits, four chains each; max R-hat 1.0042, zero divergences; 10 checks |
| [Gaussian mixture clustering](https://github.com/hayannacho/gmm-em-clustering) | Implement full-covariance Gaussian mixtures and EM in NumPy | 600-point synthetic demo converged in 11 iterations; 7 tests |

## Bioinformatics

| Project | What it does | Verified execution |
|---|---|---|
| [ESM2 variant prediction](https://github.com/hayannacho/esm2-variant-prediction) | Frozen protein embeddings, neural regression, and candidate ranking | Real ESM2 8M inference on 80 synthetic variants; 12 tests |
| [Genome sequence analysis](https://github.com/hayannacho/genome_sequence_analysis) | Exact matches, protein-to-genome candidates, spacer extraction, and annotation mapping | Five integration tests using real BLAST+ and seqtk |
| [Nextflow paired-end workflow](https://github.com/hayannacho/my_first_wf) | fastp trimming with parallel SPAdes assembly and SeqKit statistics | All three stages ran on archived and synthetic inputs, including paths with spaces |
| [Amplicon workflow](https://github.com/hayannacho/amplicon-workflow) | Extract and orient amplicons from assemblies or mapped paired reads | Four tests with real BLAST/minimap2/samtools; 192-base synthetic output |
| [Local alignment path counter](https://github.com/hayannacho/local-alignment-path-counter) | Compute optimal local scores and count tied traceback paths | 1,922 exhaustive-oracle comparisons; 7 tests |
| [RAD-seq coverage demo](https://github.com/hayannacho/rad-seq-coverage-demo) | Compare recognition-window coverage across three RAD modes | Eight tests; synthetic FASTA/VCF examples |
| [Alignment variability profiler](https://github.com/hayannacho/alignment-variability-profiler) | Rank variable aligned-protein columns; export counts and a plot | Seven tests and a Linux smoke run |

ESM2's tiny synthetic run validates execution: validation MSE was 0.232305 and Spearman correlation −0.293706, not evidence of useful biological ranking. Sequence-workflow checks likewise establish software behavior rather than biological accuracy or assembly quality. Each repository describes coursework context and implementation scope.

## More implementations

<details>
<summary><strong>Algorithms, simulations, and research interfaces</strong></summary>

| Project | Function | Verified result |
|---|---|---|
| [Coursework algorithms](https://github.com/hayannacho/coursework-algorithms) | Ten small implementations in one repository: affine-gap alignment, six-frame translation, primer design, attention and graph classifiers, HMM smoothing, K-means / K-medoids, matrix factorization, lattice competition, emissions joins | 27 tests on Python 3.11 |
| [Perceptual Sense Lab](https://github.com/hayannacho/perceptual-sense-lab) | Six sight/hearing tasks with adaptive trials and threshold plots | Seven software tests; generated signals and scripted responses |

Personal measurements and reports are excluded from Perceptual Sense Lab. Software checks do not calibrate human perception or hardware. Small training fixtures in these repositories are execution examples, not benchmark claims.

</details>

## How I work

**Explicit assumptions. Reproducible runs. Results you can inspect.**

I document inputs, commands, tested environments, and interpretation limits alongside the code. Synthetic examples are labeled, original participant records stay out of public repositories, and team projects identify the relevant implementation scope.
