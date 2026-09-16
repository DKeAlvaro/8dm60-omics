

# Omics models

Federica Eduati

Eindhoven University of Technology  
Department of Biomedical Engineering

2026

Which type(s) of omics data are covered in the papers?

![QR code linking to the Menti poll.](c803f6f6e2c49429d2951832bd0f208d_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

## What is RNAseq and how is scRNAseq measured

![Diagram of a cell nucleus with chromosomes and a DNA strand showing Gene A, Gene B, and Gene C. Diagram showing Gene A mRNA, Gene B mRNA, and Gene C mRNA as wavy lines. Diagram of a sequencing machine and short sequencing reads. Lightbulb icon](1b7d539e02a202c2cf2d97698b911447_img.jpg)

### 1 What RNA-seq measures

**1** DNA in the nucleus contains genes

Genes in DNA can be transcribed

**2** Genes are transcribed into mRNA transcripts

mRNA reflects which genes are active

**3** RNA-seq sequences many RNA molecules

Sequencing reads sample RNA molecules

**4** The output is a table of counts

|        | Sample 1 | Sample 2 | Sample 3 |
|--------|----------|----------|----------|
| Gene A | 17       | 0        | 5        |
| Gene B | 3        | 28       | 1        |
| Gene C | 0        | 2        | 14       |
| Gene D | 8        | 0        | 0        |
| ...    | ...      | ...      | ...      |

Data are summarized as gene-expression counts

Higher counts usually indicate more detected transcripts, not direct absolute abundance.

Diagram of a cell nucleus with chromosomes and a DNA strand showing Gene A, Gene B, and Gene C. Diagram showing Gene A mRNA, Gene B mRNA, and Gene C mRNA as wavy lines. Diagram of a sequencing machine and short sequencing reads. Lightbulb icon

## What is RNAseq and how is scRNAseq measured

### 1 What RNA-seq measures

![A four-step diagram showing the RNA-seq process: 1. DNA in the nucleus contains genes (Gene A, B, C). 2. Genes are transcribed into mRNA transcripts (Gene A, B, C mRNA). 3. RNA-seq sequences many RNA molecules. 4. The output is a table of counts for Gene A, B, C, D across Sample 1, 2, 3.](9e6062272bbe3ddbb7c0606721d64cf0_img.jpg)

**1 DNA in the nucleus contains genes**  
Genes in DNA can be transcribed

**2 Genes are transcribed into mRNA transcripts**  
mRNA reflects which genes are active

**3 RNA-seq sequences many RNA molecules**  
Sequencing reads sample RNA molecules

**4 The output is a table of counts**  
Data are summarized as gene-expression counts

|        | Sample 1 | Sample 2 | Sample 3 |
|--------|----------|----------|----------|
| Gene A | 17       | 0        | 5        |
| Gene B | 3        | 28       | 1        |
| Gene C | 0        | 2        | 14       |
| Gene D | 8        | 0        | 0        |
| ...    | ...      | ...      | ...      |

A four-step diagram showing the RNA-seq process: 1. DNA in the nucleus contains genes (Gene A, B, C). 2. Genes are transcribed into mRNA transcripts (Gene A, B, C mRNA). 3. RNA-seq sequences many RNA molecules. 4. The output is a table of counts for Gene A, B, C, D across Sample 1, 2, 3.

Higher counts usually indicate more detected transcripts, not direct absolute abundance.

### 2 How single-cell RNA-seq is measured

![A six-step diagram showing the scRNA-seq process: 1. Tissue or cell mixture. 2. Dissociate into individual cells. 3. Isolate single cells (droplets or wells). 4. Add cell barcodes and convert RNA to cDNA. 5. Sequence the pooled library. 6. Build a gene-by-cell count matrix for Cell 1, 2, 3... N.](f0bae10b54c4f3cf8d0e33f5e2fb7cfa_img.jpg)

**1 Tissue or cell mixture**  
Start with many cells

**2 Dissociate into individual cells**  
Separate individual cells

**3 Isolate single cells (droplets or wells)**  
Capture one cell per droplet/well

**4 Add cell barcodes and convert RNA to cDNA**  
Barcode molecules by cell (different colors = different cells)

**5 Sequence the pooled library**  
Sequence the pooled library

**6 Build a gene-by-cell count matrix**  
Count genes in each cell (rows = genes, columns = cells)

|        | Cell 1 | Cell 2 | Cell 3 | ... | Cell N |
|--------|--------|--------|--------|-----|--------|
| Gene A | 3      | 0      | 12     | ... | 1      |
| Gene B | 0      | 7      | 0      | ... | 4      |
| Gene C | 5      | 1      | 0      | ... | 0      |
| Gene D | 0      | 0      | 2      | ... | 0      |
| ...    | ...    | ...    | ...    | ... | ...    |

A six-step diagram showing the scRNA-seq process: 1. Tissue or cell mixture. 2. Dissociate into individual cells. 3. Isolate single cells (droplets or wells). 4. Add cell barcodes and convert RNA to cDNA. 5. Sequence the pooled library. 6. Build a gene-by-cell count matrix for Cell 1, 2, 3... N.

![Clipboard icon with checklist.](d0baec9a9191662196c3f3be304ee01c_img.jpg)

Clipboard icon with checklist.

- RNA-seq measures gene-expression through sequenced RNA molecules.
- scRNA-seq measures this separately for many individual cells.
- The final data are sparse count matrices: genes × cells.

## What can we learn from scRNAseq data?

### 1 Identify cell types and diversity Which cell types are present?

![UMAP plot showing distinct clusters of cell types.](7a3561af571faf036baa93f5f4b1bdb9_img.jpg)

A UMAP plot with UMAP 1 on the x-axis and UMAP 2 on the y-axis. The plot shows several distinct clusters of cells, each color-coded: blue for T cells, orange for B cells, green for Myeloid cells, red for Epithelial cells, and purple for Stromal cells. A legend on the right lists these cell types with their corresponding colors.

UMAP plot showing distinct clusters of cell types.

### 2 Characterize cell states How do cells of the same type differ?

![UMAP plot showing a continuum of cell states.](b15e3860e0c96ed16ce77f032da6f107_img.jpg)

A UMAP plot with UMAP 1 on the x-axis and UMAP 2 on the y-axis. The data points form a continuous arc, transitioning from purple/blue on the left to yellow/red on the right. An arrow labeled "Activation / differentiation" points along this arc from left to right, indicating a progression of cell states.

UMAP plot showing a continuum of cell states.

### 3 Discover markers and pathways What genes or programs define cell types or states?

![Heatmap of gene expression across cell types.](6f1efa91fb9b476380af7a35db4f14bf_img.jpg)

A heatmap comparing gene expression between Cell type A and Cell type B. The columns are labeled "Cell type A" and "Cell type B". The rows are labeled "Gene 1", "Gene 2", "Gene 3", "Gene 4", and "Gene 5". A color scale on the right indicates expression levels, from blue (Low expression) to red (High expression). Cell type A shows high expression (red) for Genes 1, 2, and 3, while Cell type B shows high expression (red) for Genes 4 and 5.

Heatmap of gene expression across cell types.

### 6 Infer trajectories and communication How do cells develop and interact?

![Diagram of cell differentiation trajectory and communication.](bc04d002fc79e8a3637b1552ac3361e6_img.jpg)

A diagram illustrating cell development and interaction. On the left, a "Differentiation trajectory" is shown as a curved path of colored dots. On the right, "Cell-cell communication" is depicted between a "Sender cell" (purple) and a "Receiver cell" (green), with yellow dots representing signaling molecules being transferred between them.

Diagram of cell differentiation trajectory and communication.

### 4 Compare conditions How do cells and states change across disease, treatment or time?

![UMAP plots comparing healthy and diseased/treated conditions.](1a6d75c94d3fd49936527eadd25e9278_img.jpg)

Two UMAP plots side-by-side, both with UMAP 1 on the x-axis and UMAP 2 on the y-axis. The left plot, labeled "Healthy", shows a standard distribution of cell clusters. The right plot, labeled "Diseased / Treated", shows a similar distribution but with some shifts and changes in the relative positions and densities of the clusters, indicating cellular changes due to the condition.

UMAP plots comparing healthy and diseased/treated conditions.

### 5 Predict treatment response Can we identify responders and resistant cells?

![Diagram of predicting treatment response from patient data.](867fce43c58fda6178b06e454b4ed73a_img.jpg)

A diagram showing the process of predicting treatment response. It starts with "Patients" (represented by icons). An arrow points to a box labeled "scRNA-seq + models". From this box, two arrows point to different outcomes: a green figure labeled "Responder" and a red figure labeled "Resistant". Next to each figure is a line graph of "Responses" over "Time". The "Responder" graph shows a green line that decreases over time, while the "Resistant" graph shows a red line that remains relatively flat.

Diagram of predicting treatment response from patient data.

Single-cell RNA-seq reveals cellular diversity, function and response, opening new opportunities for understanding biology and improving treatment.

What are key characteristics of single cell RNAseq data that scVI is dealing with?

## Key challenges in scRNAseq

### 1 Sparsity

Only a fraction of transcripts present in a cell are detected.

Transcripts in a cell (many genes) → Capture & sequencing detect a subset → Observed counts (many zeros)

| Gene   | Count |
|--------|-------|
| Gene 1 | 1     |
| Gene 2 | 0     |
| Gene 3 | 4     |
| Gene 4 | 0     |
| ...    | ...   |
| Gene G | 0     |

![](c0843c6d138705289960d9f53a6e72a1_img.jpg)

### Single-cell RNA-seq data matrix

Cells (columns) →

Genes (rows) ↓

|        | Cell 1 | Cell 2 | Cell 3 | ... | Cell j | ... | Cell N |
|--------|--------|--------|--------|-----|--------|-----|--------|
| Gene 1 | 0      | 0      | 12     | 0   | 3      | 0   | 25     |
| Gene 2 | 5      | 0      | 0      | 1   | 0      | 0   | 3      |
| Gene 3 | 0      | 7      | 0      | 0   | 0      | 2   | 0      |
| Gene 4 | 32     | 0      | 8      | 0   | 15     | 0   | 42     |
| Gene 5 | 0      | 0      | 0      | 0   | 0      | 0   | 0      |
| ...    | ...    | ...    | ...    | ... | ...    | ... | ...    |
| Gene i | 0      | 1      | 4      | 0   | 0      | 0   | 6      |
| ...    | ...    | ...    | ...    | ... | ...    | ... | ...    |
| Gene G | 18     | 0      | 0      | 9   | 0      | 1   | 0      |

UMI counts color scale: 0, 1, 3, 10, 30, 100

![Bar chart showing UMI counts (library size) for Cell X and Cell Y. Cell X has a low bar (~1.2K) and Cell Y has a high bar (~22.4K).](a6a8016b231533e7f34b550f4676afc6_img.jpg)

### 2 Sequencing depth

Total counts (library size) vary widely across cells.

Cell X (low depth): Total UMI count: 1,242

Cell Y (high depth): Total UMI count: 22,387

Bar chart showing UMI counts (library size) for Cell X and Cell Y. Cell X has a low bar (~1.2K) and Cell Y has a high bar (~22.4K).

![UMAP plot showing two clusters of cells, Batch 1 (green) and Batch 2 (orange), separated by a dashed line labeled 'Unwanted technical separation'.](c64e9e9f3b0b828a5f6ac70441877764_img.jpg)

### 3 Batch effect

Same cell types, different batches (technical separation, not biology).

UMAP 2

UMAP 1

Batch 1 Batch 2

UMAP plot showing two clusters of cells, Batch 1 (green) and Batch 2 (orange), separated by a dashed line labeled 'Unwanted technical separation'.

![Diagram showing the growth of cell clusters from 10^2 to 10^6-10^7 cells.](4279c8be6ec4ed56f4b3349be98bb426_img.jpg)

### 5 Increasingly large datasets

Number of cells grows from hundreds to millions, increasing computational burden.

Hundreds of cells → Thousands of cells → Hundreds of thousands of cells → Millions of cells

10<sup>2</sup> 10<sup>3</sup> 10<sup>5</sup> 10<sup>6</sup>-10<sup>7</sup>

Number of cells

Diagram showing the growth of cell clusters from 10^2 to 10^6-10^7 cells.

![Violin plots for Gene A, Gene B, and Gene C showing stochastic expression across cells. Each dot represents one cell.](01da0d212fb571933f10f96556157745_img.jpg)

### 4 Transcriptional noise

Expression of the same gene varies stochastically across similar cells.

Expression across similar cells

Gene A Gene B Gene C

Expression (UMI)

Each dot = one cell

Violin plots for Gene A, Gene B, and Gene C showing stochastic expression across cells. Each dot represents one cell.

# Which architecture best describes the core of scVI?

![QR code linking to the Menti poll.](892f25e3d71d8e315a2a51092a8a8da7_img.jpg)

A QR code is displayed in the bottom right corner of the slide, which when scanned, would direct the user to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

What are the main components and what is their role?

### The scVI architecture

![A schematic diagram of the scVI architecture showing the flow from raw expression data through variational posterior and generative model blocks to final tasks like imputation and clustering.](f4fdd410cdb84df81274da55721e56fb_img.jpg)

The diagram illustrates the scVI architecture, which is divided into several functional blocks:

- Raw expression data + batch ID (Block a):** This block contains the input data, represented by orange circles for expression values ( $x_{n,1}, \dots, x_{n,G}$ ) and a green circle for the batch ID ( $s_n$ ).
- Variational posterior  $q(z_n, l_n | x_n, s_n)$  (Blue block):** This block performs nonlinear mapping using neural networks NN1, NN2, NN3, and NN4. NN1 and NN2 map to the **Size factor** (Mean and S.d.), while NN3 and NN4 map to the **Latent space** (Mean and S.d.).
- Sampling (Green block):** This block shows the sampling of latent variables:  $l_n$  (library size / depth),  $z_{n,1}, \dots, z_{n,d}$  (latent cell state), and  $s_n$  (batch).
- Generative model  $p(x_n | z_n, s_n, l_n)$  (Orange block):** This block performs nonlinear mapping using NN5 and NN6. NN5 maps to the **Expected frequency** ( $f_w(z_n, s_n)$ ), and NN6 maps to the **Expected dropout** ( $f_h(z_n, s_n)$ ). The library size  $l_n$  is used for **Cell-specific scaling**. These components combine to produce the **Expected counts**.
- Downstream tasks:** The expected counts are used for **Imputation** and **Differential expression**. The latent variables  $z_n$  and  $s_n$  are used for **Clustering**, **Visualization**, and **Batch removal**.

A schematic diagram of the scVI architecture showing the flow from raw expression data through variational posterior and generative model blocks to final tasks like imputation and clustering.

### The scVI architecture

![A detailed diagram of the scVI architecture showing the flow from raw expression data through an encoder (NN1-NN4) to a variational posterior, then to sampling of latent variables (l, z, s), and finally through a generative model (NN5-NN6) to produce expected counts for downstream tasks like imputation and differential expression.](5b4e774d63e0e0ed73801a9247755e5f_img.jpg)

**Infer state**  
Encoder maps noisy counts to distributions over  $z$  and  $l$ .

**Model how counts are generated**  
Decoder predicts parameters of an NB/ZINB count distribution.

**a**

Raw expression data + batch ID:  $x_{n,1}, \dots, x_{n,G}, s_n$

**Variational posterior**  
 $q(z_n, l_n | x_n, s_n)$

Nonlinear mapping: NN1, NN2, NN3, NN4

Variational distribution:

- Size factor**: Mean, S.d.
- Latent space**: Mean, S.d.

**Sampling**

- $l$ : library size / depth  $\rightarrow l_n$
- $z$ : latent cell state  $\rightarrow z_{n,1}, \dots, z_{n,d}$
- $s$ : batch  $\rightarrow s_n$

**Generative model**  
 $p(x_n | z_n, s_n, l_n)$

Nonlinear mapping: NN5, NN6

Generative distribution parameters:

- Cell-specific scaling:  $l_n$
- Expected frequency:  $f_w(z_n, s_n)$  (from NN5)
- Expected dropout:  $f_h(z_n, s_n)$  (from NN6)

Expected counts

Downstream tasks: Imputation, Differential expression

Additional outputs: Clustering, Visualization, Batch removal

**Separate biology from known technical factors**  
 $z$  represents latent cell state;  $l$  represents sequencing depth;  $s$  identifies batch.

A detailed diagram of the scVI architecture showing the flow from raw expression data through an encoder (NN1-NN4) to a variational posterior, then to sampling of latent variables (l, z, s), and finally through a generative model (NN5-NN6) to produce expected counts for downstream tasks like imputation and differential expression.

# What is the main training objective in scVI?

![QR code linking to the Menti poll.](ec0158057f8ccaf74edba16682ec5444_img.jpg)

A QR code is displayed in the bottom right corner of the slide, which likely links to the Menti poll for the question.

QR code linking to the Menti poll.

menti.com  
1943 3368

### The ELBO objective

![A 5-step diagram of the ELBO objective process: 1. Observed data (input), 2. Encoder / variational posterior, 3. Sample latent variables from q, 4. Generative model (decoder / observation model), 5. Observation model (evaluate data likelihood). Encoder neural network diagram Decoder neural network diagram](4e4be0bd8b235167902f2c03e41da651_img.jpg)

**1 Observed data (input)**  
Observed gene counts and batch for cell  $n$ .

$x_n^{\text{obs}}$  (counts)  $\left\{ \begin{array}{c} x_{n1} \\ x_{n2} \\ \vdots \\ x_{nG} \end{array} \right.$

$s_n$  (batch) e.g. 0, 1, ..., S

**2 Encoder / variational posterior**  
Neural network takes observed counts and batch as input and outputs a distribution over latent variables.

$x_n^{\text{obs}}$   $s_n$   $q(z_n, l_n | x_n^{\text{obs}}, s_n)$

Encoder  $q_\phi$  Variational posterior over latent variables  $(z_n, l_n)$

**3 Sample latent variables from  $q$**   
Draw samples of  $z_n$  and  $l_n$  using the reparameterization trick (differentiable sampling).

$z_n, l_n \sim q(z_n, l_n | x_n^{\text{obs}}, s_n)$

$z_n$  Latent biological state (low-dimensional)  
 $l_n$  Library size / depth (cell-specific)

**4 Generative model (decoder / observation model)**  
Use  $z_n$ ,  $s_n$  and  $l_n$  to produce ZINB distribution parameters for each gene.

$z_n$   $s_n$   $l_n$  **Decoder**  $p_\theta$

**ZINB parameters** (for each gene  $g$ )

- $\mu_{ng}$  (mean expression)
- $\theta_g$  (dispersion)
- $\pi_{ng}$  (dropout probability)

**5 Observation model (evaluate data likelihood)**  
Observed counts are modeled with a zero-inflated negative binomial (ZINB).

$x_{ng} \sim \text{ZINB}(\mu_{ng}, \theta_g, \pi_{ng})$

$p(x_n^{\text{obs}} | z_n, l_n, s_n)$   
Probability of observed counts under the ZINB model

A 5-step diagram of the ELBO objective process: 1. Observed data (input), 2. Encoder / variational posterior, 3. Sample latent variables from q, 4. Generative model (decoder / observation model), 5. Observation model (evaluate data likelihood). Encoder neural network diagram Decoder neural network diagram

#### Training objective (ELBO)

For each cell  $n$ :

$$\text{ELBO}_n = \mathbb{E}_{q(z_n, l_n | x_n^{\text{obs}}, s_n)} \left[ \log p(x_n^{\text{obs}} | z_n, l_n, s_n) \right] - \text{KL} \left( q(z_n, l_n | x_n^{\text{obs}}, s_n) \parallel p(z_n, l_n | s_n) \right)$$

#### Likelihood / reconstruction term

How probable are the observed counts  $x_n^{\text{obs}}$  under the predicted ZINB distribution (with parameters  $\mu_{ng}, \theta_g, \pi_{ng}$ )?

#### KL regularization term

Keeps the inferred latent variables close to the prior  $p(z_n, l_n | s_n)$  and encourages a smooth, well-behaved latent space across cells.

What are advantages and limitations of scVI?

### scVI: main applications, advantages and limitations

#### Applications

- **Latent representation**  
Dimensionality reduction, visualization and clustering of cell states.
- **Data integration**  
Combine datasets and reduce known batch effects using batch covariates.
- **Expression analysis**  
Denoised/normalized expression estimates and differential-expression testing.
- **Large atlases**  
Learn a common representation across very large single-cell datasets.

#### Advantages

- **Count-aware**  
Models raw scRNA-seq counts probabilistically rather than treating them as Gaussian data.
- **Uncertainty-aware**  
Represents each cell by a posterior distribution, not only a point estimate.
- **Separates factors**  
Models latent state, library size and known technical covariates separately.
- **Scalable**  
Amortized inference and mini-batch optimization scale to large numbers of cells.

#### Limitations

- **Latent  $\neq$  biology**  
A useful latent space is not automatically interpretable or mechanistic.
- **Model assumptions**  
Results depend on choices of count distribution, priors and covariates.
- **Batch correction**  
Can fail when batch and biology are confounded, and may remove real biological signal.
- **Not causal**  
Primarily represents observed variation; it does not by itself predict responses to unseen perturbations.

Why use transformer-based foundation models for scRNAseq data?

## Why use transformer-based foundation models for scRNAseq data?

- ▶ **Scale:** exploit very large collections of single-cell data rather than training separate models from scratch.
- ▶ **Reuse across tasks and datasets:** learn a general representation that can support many downstream tasks and potentially generalize to new biological contexts.
- ▶ **Context-dependent representations:** learn how the meaning of a gene depends on the expression state of other genes in the same cell.

### How can we adapt Transformers to scRNAseq?

Select all that apply

![QR code linking to the Menti poll.](97fe9069356cc2a84e8e70673e405958_img.jpg)

A QR code is displayed in the bottom right corner of the slide, which when scanned, would direct the user to the Menti poll interface.

QR code linking to the Menti poll.

menti.com  
1943 3368

### What makes it non-trivial?

#### ▶ **Non-sequential nature:**

- ▶ In natural language: text token sequences have a strict directional flow, where sequence order dictates meaning
- ▶ In biology: A cell's transcriptome is non-sequential—a "bag-of-genes" that express transcripts simultaneously

#### ▶ **Quantitative values:**

- ▶ In natural language: a word token in a sentence is a discrete, categorical unit. It is either present or absent.
- ▶ Every gene token in a cell possesses a continuous, quantitative expression value indicating transcript abundance

How is a cell converted into tokens in scGPT?

### How is a cell converted into tokens in scGPT?

#### Analogy to Lecture 1: language models

#### A sentence (raw text)

The biopsy showed invasive carcinoma .

![Downward arrow indicating the process of tokenization.](cc777601b892d144a2c0b69f56ef03bf_img.jpg)

Downward arrow indicating the process of tokenization.

#### Tokenization

The

biopsy

showed

invasive

carcinoma

.

In language, tokens are words or subwords  
in sequence.

#### scGPT: one cell

#### Example cell (gene expression)

| Gene | Expression (bin) | Condition (optional) |
|------|------------------|----------------------|
| TP53 | 3                | disease              |
| EGFR | 0                | disease              |
| MYC  | 6                | disease              |
| CD3D | 2                | disease              |
| ...  | ...              | ...                  |

![Icon of a document with lines of text.](906b2c6ba479621b00429a51cbcce897_img.jpg)

Icon of a document with lines of text.

A condition token can include metadata, e.g., batch, perturbation, or modality.

#### How each input token is represented

Each gene token includes three pieces of information:

(1) gene identity, (2) expression value (discretized into a bin), and (3) condition/metadata.

These embeddings are combined to form the input representation for token  $i$ :

$$h_i = \mathbf{emb}_g(g_i) + \mathbf{emb}_x(x_i) + \mathbf{emb}_c(c_i)$$

where  $h_i$  is the combined input embedding for token  $i$ .

# How can scGPT learn context between genes?

![QR code linking to the Menti poll.](55d74563d1b88865295879cdaffce3ff_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

### How can the model learn context between genes?

#### Analogy to Lecture 1: language models

#### A sentence (raw text)

The biopsy showed invasive carcinoma .

#### Tokenization (sequence order matters)

|     |        |        |          |           |   |
|-----|--------|--------|----------|-----------|---|
| The | biopsy | showed | invasive | carcinoma | . |
| 1   | 2      | 3      | 4        | 5         | 6 |

#### Causal mask (autoregressive)

![](d369dc114803a761d452c13ee58ed579_img.jpg)

Key token (can attend to)

| Query token | 1          | 2          | 3          | 4          | 5          | 6          |
|-------------|------------|------------|------------|------------|------------|------------|
| 1           | can attend | blocked    | blocked    | blocked    | blocked    | blocked    |
| 2           | can attend | can attend | blocked    | blocked    | blocked    | blocked    |
| 3           | can attend | can attend | can attend | blocked    | blocked    | blocked    |
| 4           | can attend | can attend | can attend | can attend | blocked    | blocked    |
| 5           | can attend | can attend | can attend | can attend | can attend | blocked    |
| 6           | can attend | can attend | can attend | can attend | can attend | can attend |

can attend = blue, blocked = grey

Predict next token from left to right.

#### scGPT: one cell

#### A single cell (gene expression)

![red hatched box red hatched box](86d30a7d5a9cd4ee5456b5962ae3420a_img.jpg)

| cell token | TP53 | EGFR | CD3D | MYC | GATA3 |
|------------|------|------|------|-----|-------|
| -          | 3    | 0    | 2    |     |       |

Known genes (expression available): cell token, TP53, EGFR, CD3D

Target genes (expression masked): MYC, GATA3

Example target: MYC (gene ID visible; expression masked)

Mask some gene expression values, then predict them from the remaining known genes in the same cell.

red hatched box red hatched box

#### Generative attention mask during training

![](356ab6a9298284115a7334b1b56d59e2_img.jpg)

| Query token (attends to →) | <cls>             | TP53              | EGFR              | CD3D              | MYC       | GATA3     |
|----------------------------|-------------------|-------------------|-------------------|-------------------|-----------|-----------|
| <cls>                      | attention allowed | attention allowed | attention allowed | attention allowed | blocked   | blocked   |
| TP53                       | attention allowed | attention allowed | attention allowed | attention allowed | blocked   | blocked   |
| EGFR                       | attention allowed | attention allowed | attention allowed | attention allowed | blocked   | blocked   |
| CD3D                       | attention allowed | attention allowed | attention allowed | attention allowed | blocked   | blocked   |
| MYC                        | attention allowed | attention allowed | attention allowed | attention allowed | self only | blocked   |
| GATA3                      | attention allowed | attention allowed | attention allowed | attention allowed | blocked   | self only |

- = attention allowed
- = self only — gene ID visible, expression masked
- = blocked

Known genes attend to all known genes. Each target gene can attend to the cell token, all known genes, and its own gene identity, but not to other target genes.

##### What does it mean?

To predict MYC, the model can attend to:

- cell token
- known genes (TP53, EGFR, CD3D)
- MYC itself (gene ID only)

##### It cannot attend to:

- other masked targets (e.g. GATA3)

After the Transformer has learned context between genes, what representations do you think we can extract from the model?

### From gene tokens to contextual representation

![](a74294f34a0c736b7ee0f5f0cdca7e28_img.jpg)

**1 Input: one cell (gene tokens)**

**<cls>** TP53 3 EGFR 0 CD3D 2 MYC ? GATA3 ?

cell token

known genes (expression available)

target genes (expression masked)

**2 scGPT (Transformer)**

Multi-head self-attention

Feed-forward networks

× L layers

**3 Output: contextual representations**

$h_{\text{cell}}$  (d-dim) Cell representation (whole cell)

$h_{\text{TP53}}$  (d-dim)

$h_{\text{EGFR}}$  (d-dim)

$h_{\text{CD3D}}$  (d-dim)

$h_{\text{MYC}}$  (d-dim)

$h_{\text{GATA3}}$  (d-dim)

Contextual gene representations (depend on the other genes in the same cell)

![](552265bdbcf6d43d341fd018a9076269_img.jpg)

**4 Same gene, different representations**

TP53 in a T cell

TP53 in a cancer cell

$h_{\text{TP53}}^{(T)}$

$h_{\text{TP53}}^{(C)}$

Same gene (TP53), different representation because the cellular context is different.

![UMAP plot showing cell clusters: Cancer cells (red), T cells (blue), B cells (orange), and Myeloid (green).](a1545557e366b6302109d13360b199c3_img.jpg)

**5 Cell representation captures cell state**

UMAP 2

UMAP 1

$h_{\text{cell}}$

Can support cell-level tasks (e.g. annotation, clustering, integration).

UMAP plot showing cell clusters: Cancer cells (red), T cells (blue), B cells (orange), and Myeloid (green).

![](e354b57563dae469c00b412b2abdf765_img.jpg)

**6 Which representation to use?**

**Cell-level question**

- What cell type is this?
- Use the cell representation ( $h_{\text{cell}}$ ).

**Gene-level question**

- How does TP53 behave in this cell?
- Use the contextual gene representation ( $h_{\text{TP53}}$ ).

How is the pretrained scGPT model adapted for downstream tasks?

### From pretrained scGPT to downstream task prediction

![A flow diagram showing the process from pretrained scGPT to downstream task prediction. It consists of three main stages: Pretrained scGPT, Task-specific adaptation, and Downstream predictions / representations.](043e64d41a3368d138ace3816fd26469_img.jpg)

The diagram illustrates the workflow of using a pretrained single-cell Generative Pre-trained Transformer (scGPT) for various biological tasks. It is divided into three main stages:

- Pretrained scGPT**: This stage shows a group of diverse, colored cells (blue, purple, green, orange) being processed by a **Transformer** block. Below this, it states: "Pretrained on >33 million cells" and "general gene + cell representations".
- Task-specific adaptation**: This stage shows the **Pretrained Transformer** (represented by a blue trapezoid) connected to a **Task-specific head** (represented by a green rounded rectangle). Below this, it explains: "Initialize from pretrained weights", "→ fine-tune on task-specific data/objective", and "what is adapted / read out depends on the task".
- Downstream predictions / representations**: This stage lists four applications of the adapted model:
  - cell type annotation**: Represented by a cluster of colored circles.
  - data integration**: Represented by two distinct clusters of blue and orange dots.
  - perturbation response**: Represented by a red pill icon pointing to a purple cell.
  - gene network inference**: Represented by a network graph with blue nodes and edges.

A flow diagram showing the process from pretrained scGPT to downstream task prediction. It consists of three main stages: Pretrained scGPT, Task-specific adaptation, and Downstream predictions / representations.

**Pretrain once at scale → adapt the same model to different biological tasks.**

Which result would provide the strongest evidence that scGPT has learned a transferable foundation-model representation?

![QR code linking to the Menti poll.](b8e33e88baf855d3881d2f32fb17b60a_img.jpg)

A QR code is displayed in the bottom right corner of the slide, which likely links to the Menti poll interface for the question.

QR code linking to the Menti poll.

menti.com  
1943 3368

### What would demonstrate foundation-model capabilities?

- ▶ transfer across datasets or biological contexts,
- ▶ usefulness across multiple tasks,
- ▶ strong zero-shot or few-shot performance,
- ▶ improvement over non-pretrained baselines.

### Fine-tuning vs zero-shot

![Diagram comparing Fine-tuning and Zero-shot transfer learning processes.](5414f65867392f05ba0063b208eeb5e1_img.jpg)

The diagram illustrates two transfer learning approaches: Fine-tuning and Zero-shot.

**Fine-tuning** (blue box):

- Starts with a **Pretrained model** (represented by a network icon).
- Followed by **New labeled dataset + task objective** (represented by a database icon).
- Then **Adapt model parameters** (represented by a gear icon).
- Finally, **Task prediction** (represented by a bar chart icon).
- A note below the third step states: **Model changes during downstream training**.

**Zero-shot** (green box):

- Starts with a **Pretrained model** (represented by a network icon).
- Followed by **Frozen representation / no task-specific training** (represented by a padlock icon).
- Finally, **Direct evaluation (or downstream prediction)** (represented by a bar chart icon).
- A note below the second step states: **No parameter updates**.

Diagram comparing Fine-tuning and Zero-shot transfer learning processes.

- ▶ Full fine-tuning tests whether pretraining is a useful starting point
- ▶ Zero-shot tests whether the pretrained representation itself transfers
- ▶ Strong transfer should hold on genuinely new data and against strong baselines

What should a good single-cell embedding preserve,  
and what should it be invariant to?

### How do we measure a good cell embedding?

#### Biological conservation

- ▶ cell-type separability / clustering
- ▶ neighborhood purity
- ▶ preservation of known biological structure

#### Batch integration

- ▶ mixing of batches within biological populations
- ▶ reduced predictability of batch from the embedding

A strong embedding should score well on both, not optimize one at the expense of the other.

### How do zero-shot foundation-model embeddings compare with established baselines?

1A

![](a844248c1fa0a79f187fc9aa111182f7_img.jpg)

### Average BIO (AvgBIO) score

| Method      | Pancreas (16k) | PBMC (95k) | Tabula Sapiens (483k) | PBMC (12k) | Immune (330k) |
|-------------|----------------|------------|-----------------------|------------|---------------|
| HVG         | 0.68           | 0.53       | 0.45                  | 0.63       | 0.53          |
| Harmony     | 0.82           | 0.63       | 0.39                  | 0.72       | 0.57          |
| scVI        | 0.81           | 0.67       | 0.57                  | 0.74       | 0.53          |
| Geneformer  | 0.26           | 0.52       | 0.30                  | 0.59       | 0.36          |
| scGPT human | 0.44           | 0.55       | 0.43                  | 0.78       | 0.51          |

Dataset: Pancreas (16k), PBMC (95k), Tabula Sapiens (483k), PBMC (12k), Immune (330k)

1E

![](5dc5581cd2aad0e683c73b959f637b31_img.jpg)

### Average batch score

| Method      | Pancreas (16k) | PBMC (95k) | Tabula Sapiens (483k) | PBMC (12k) | Immune (330k) |
|-------------|----------------|------------|-----------------------|------------|---------------|
| HVG         | 0.77           | 0.58       | 0.47                  | 0.65       | 0.51          |
| Harmony     | 0.79           | 0.77       | 0.41                  | 0.89       | 0.74          |
| scVI        | 0.86           | 0.73       | 0.61                  | 0.85       | 0.43          |
| Geneformer  | 0.30           | 0.41       | 0.45                  | 0.49       | 0.38          |
| scGPT human | 0.43           | 0.47       | 0.45                  | 0.49       | 0.59          |

Dataset: Pancreas (16k), PBMC (95k), Tabula Sapiens (483k), PBMC (12k), Immune (330k)

1C-D

![Four UMAP plots comparing scVI and scGPT_human embeddings across different cell types and batches. The top row shows embeddings colored by cell type, and the bottom row shows embeddings colored by batch. scGPT_human shows better separation of cell types and batches compared to scVI.](6fe536731996880570f251da168376cf_img.jpg)

Cell type: acinar, alpha, beta, delta, ductal, endothelial, gamma

Batch: celseq, celseq2, fluidigm1, inDrop, smarter, smartseq2

Four UMAP plots comparing scVI and scGPT\_human embeddings across different cell types and batches. The top row shows embeddings colored by cell type, and the bottom row shows embeddings colored by batch. scGPT\_human shows better separation of cell types and batches compared to scVI.

#### What do we learn from the zero-shot evaluation?

- ▶ Foundation-model embeddings capture biological structure, but are not consistently superior to HVG, Harmony or scVI.
- ▶ Batch effects remain a challenge in zero-shot embeddings.
- ▶ Large-scale pretraining does not automatically produce a better off-the-shelf representation.
- ▶ Strong performance after fine-tuning and strong zero-shot transfer are different claims.
- ▶ Evaluation needs strong baselines and biologically meaningful held-out settings.

### An outlook on foundation models in biology

- ▶ Foundation models remain promising for learning reusable representations from large biological datasets.
- ▶ Scale is not enough: we need to test what biology is actually learned and how well it transfers.
- ▶ Strong simple baselines are essential to judge whether pretraining adds real value.
- ▶ Benchmarking is becoming increasingly important for evaluating zero-shot transfer, fine-tuning and robustness.

## Why predict perturbation responses from single-cell data?

### Why it matters

- Many possible drugs, targets, doses and combinations

![Diagram showing four categories of perturbations: Drugs (represented by various colored capsules), Targets (e.g. CRISPR, represented by a DNA helix and scissors), Doses (represented by a series of increasing blue circles), and Combinations (represented by two pairs of capsules with plus signs).](2837ffdadcdb1e5bababa56b564e56ed_img.jpg)

Diagram showing four categories of perturbations: Drugs (represented by various colored capsules), Targets (e.g. CRISPR, represented by a DNA helix and scissors), Doses (represented by a series of increasing blue circles), and Combinations (represented by two pairs of capsules with plus signs).

- Experimental testing is expensive and incomplete

![Diagram illustrating the challenges of experimental testing. It shows a multi-well plate, stacks of gold coins, and a money bag with a dollar sign. A text box states: 'Many conditions, high cost, limited throughput. We can't test everything.'](fcbc3c31776721edc98ceb1944ec438f_img.jpg)

Diagram illustrating the challenges of experimental testing. It shows a multi-well plate, stacks of gold coins, and a money bag with a dollar sign. A text box states: 'Many conditions, high cost, limited throughput. We can't test everything.'

- Goal: predict how cellular state changes after an intervention

![Diagram showing a cell state transition. A blue cell labeled 'Cell state (before treatment)' is subjected to 'Drug / genetic perturbation' (indicated by an arrow with a red capsule icon), resulting in a green cell labeled 'Cell state (after treatment)'.](315bdbeafb39026e19b77c26b19d9d1f_img.jpg)

Diagram showing a cell state transition. A blue cell labeled 'Cell state (before treatment)' is subjected to 'Drug / genetic perturbation' (indicated by an arrow with a red capsule icon), resulting in a green cell labeled 'Cell state (after treatment)'.

### Why it is difficult

- scRNA-seq is destructive: cells are lysed during measurement

![Diagram showing the destructive nature of scRNA-seq. A 'Single cell' (purple) undergoes 'Cell lysis and RNA sequencing', resulting in a state where the 'Cell is destroyed (only RNA remains)' (represented by scattered RNA strands).](3db5d62ad46e33647ec2b1ad6d2703bb_img.jpg)

Diagram showing the destructive nature of scRNA-seq. A 'Single cell' (purple) undergoes 'Cell lysis and RNA sequencing', resulting in a state where the 'Cell is destroyed (only RNA remains)' (represented by scattered RNA strands).

- We cannot observe the same cell before and after treatment

![Diagram showing that the same cell cannot be tracked over time in scRNA-seq. A blue cell ('Same cell (before treatment)') is followed by a dashed arrow with a red 'X' over it, labeled 'We cannot follow the same cell over time in scRNA-seq', leading to a green cell ('Same cell (after treatment)').](1dc5e74b1032f935e1b1ea3a9c876ac6_img.jpg)

Diagram showing that the same cell cannot be tracked over time in scRNA-seq. A blue cell ('Same cell (before treatment)') is followed by a dashed arrow with a red 'X' over it, labeled 'We cannot follow the same cell over time in scRNA-seq', leading to a green cell ('Same cell (after treatment)').

- Control and treated conditions therefore contain different cells

![Diagram comparing control and treated cell sets. The 'Control (untreated)' group contains a set of cells (A, B, C, ...). The 'Treated (e.g. drug)' group contains a different set of cells (D, E, F, ...).](e038bf4fcea08f51944b4a2dd6e197a5_img.jpg)

Diagram comparing control and treated cell sets. The 'Control (untreated)' group contains a set of cells (A, B, C, ...). The 'Treated (e.g. drug)' group contains a different set of cells (D, E, F, ...).

![A yellow lightbulb icon.](9502b9363b8a9a6f0a9a321ac874785b_img.jpg)

A yellow lightbulb icon.

**Perturbation-response prediction is inherently counterfactual:**  
what would this cell have looked like under another treatment?

What determines perturbation response?

### What determines perturbation response?

- ▶ Baseline cellular state
- ▶ Perturbation identity
- ▶ Dose
- ▶ Cell type / context / covariates
- ▶ Potentially combinations of perturbations

How should we represent these factors? Should cell state, perturbation and dose all be encoded in one latent representation?

### CPA disentangles different sources of variation

![Diagram of the CPA model architecture showing the flow from genes and perturbations through an encoder and composition block to a decoder, which then outputs genes.](67114ecf6da13c97a89aeff0d86885d5_img.jpg)

The diagram illustrates the CPA model architecture. On the left, a blue vertical bar labeled 'genes' is connected by a dotted line to a box labeled 'z basal state'. This box is the output of an 'encoder' (represented by a trapezoid). Below the encoder, a 'dosage encoder' (a hexagon labeled  $f(d)$ ) takes 'perturbations  $d$ ' (represented by two pill icons) as input. The 'z basal state' is then combined with perturbation embeddings and covariate embeddings in a 'composition' block. The composition block contains the expression  $z + f_1(d_1) * \text{pill}_1 + f_2(d_2) * \text{pill}_2 + c_1 * \text{cell}_1 + c_2 * \text{cell}_2$ . The perturbation embeddings are shown as a green bar with four segments, and the covariate embeddings are shown as a red bar with four segments. The output of the composition block is fed into a 'decoder' (represented by a trapezoid), which then outputs a blue vertical bar labeled 'genes' on the right. A dotted line labeled  $\approx$  connects the input and output gene bars.

Diagram of the CPA model architecture showing the flow from genes and perturbations through an encoder and composition block to a decoder, which then outputs genes.

**Basal latent state:** underlying cell state before perturbation

**Perturbation embedding:** effect associated with the drug / intervention

**Dose embedding:** controls perturbation strength

**Covariate embeddings:** cell type, batch, condition, etc.

Combine these factors to reconstruct the treated state

# How does CPA prevent the basal state from encoding treatment?

![QR code linking to the Menti poll.](7f78becb007c69a3a1b4aef8edc0e328_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

#### Adversarial disentanglement

![Diagram of an adversarial disentanglement architecture for gene expression.](4ae4505e885586e481a3ad3bff5198b7_img.jpg)

The diagram illustrates an adversarial disentanglement framework for gene expression. It consists of the following components:

- Input:** A vertical blue bar labeled "genes" on the left.
- Encoder:** A trapezoidal block that maps the input genes to a latent representation  $z$ .
- Latent State:** A box labeled  $z$  basal state.
- Discriminators:** A red box containing two discriminators:
  - perturbation discriminator:** Takes the latent state  $z$  and a perturbation (represented by a capsule icon) as input and outputs a prediction (indicated by a question mark).
  - covariate discriminator:** Takes the latent state  $z$  and a covariate (represented by a circular icon) as input and outputs a prediction (indicated by a question mark).
- Composition:** A central box where the latent state is combined with perturbations and covariates:
$$z + f_1(d_1) * \text{perturbation}_1 + f_2(d_2) * \text{perturbation}_2 + c_1 * \text{covariate}_1 + c_2 * \text{covariate}_2$$
- Decoder:** A trapezoidal block that maps the composed representation back to genes.
- Output:** A vertical blue bar labeled "genes" on the right.
- External Components:**
  - perturbations  $d$ :** Represented by capsule icons and a green bar. A hexagonal block labeled  $f(d)$  and "dosage encoder" maps these to perturbation embeddings (green and grey bars).
  - covariates  $c$ :** Represented by circular icons and a red bar. These map to covariate embeddings (red and grey bars).

Diagram of an adversarial disentanglement architecture for gene expression.

Encoder maps each observed cell to a latent basal state.

A discriminator tries to predict perturbation / covariates from that latent state.

The encoder is trained to make this prediction difficult.

Therefore the basal latent representation is encouraged to be less informative about treatment identity.

Treatment and covariate information are added back explicitly before decoding.

# What can CPA generalize to?

![QR code linking to the Menti poll.](023d970f080d18a5ec7578ebb73205b4_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

#### What can CPA generalise to?

##### Can predict:

- ▶ New drug combinations when the individual drugs were seen during training.
- ▶ A known drug in a new cellular context when that drug–cell context combination was not observed during training.
- ▶ Unseen doses of a known perturbation.
- ▶ More generally, new combinations of factors that were observed separately during training.

##### Cannot directly predict

- ▶ The effect of a completely unseen perturbation.
- ▶ The response of a cell type / cell line never seen during training.
- ▶ Synergistic/antagonistic combinatorial effects can be predicted only if combinatorial perturbation was already in the training set

### Use prior biological relationships to generalize to unseen perturbations

- ▶ A completely unseen perturbation has no learned experimental effect of its own.
- ▶ But the perturbed gene may be related to genes seen during training.
- ▶ GEARs uses gene–gene relationship graphs to transfer information from related genes.
- ▶ Goal: predict both unseen single-gene perturbations and new combinations.

What allows GEARS to represent a perturbation  
never seen during training?

![QR code linking to the Menti poll.](b73e15bd8ab2756cf10f9344fe551227_img.jpg)

A square QR code with a black and white pixelated pattern, used for linking to an external poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

### What prior knowledge does GEARS use?

#### Gene co-expression graph

Edges link genes with high coexpression similarity  
(illustration: top-2 correlated neighbors above a threshold)

![Three small network diagrams showing gene neighborhoods. Neighborhood 1: ACTB, GAPDH, RPS3, RPL13A, RPLP0. Neighborhood 2: STAT1, IFIT1, OAS1, MX1, ISG15. Neighborhood 3: MKI67, PCNA, CDK1, TOP2A, TYMS.](77a781dfb114c3e2b399f876f1808cfd_img.jpg)

Three small network diagrams showing gene neighborhoods. Neighborhood 1: ACTB, GAPDH, RPS3, RPL13A, RPLP0. Neighborhood 2: STAT1, IFIT1, OAS1, MX1, ISG15. Neighborhood 3: MKI67, PCNA, CDK1, TOP2A, TYMS.

Gene-gene correlation matrix (|Pearson correlation|)

![Heatmap showing the absolute Pearson correlation between 15 genes. The color scale ranges from 0.0 (white) to 1.0 (dark red). The genes listed on both axes are ACTB, GAPDH, RPLP0, RPL13A, RPS3, STAT1, IFIT1, ISG15, MX1, OAS1, MKI67, PCNA, TYMS, TOP2A, and CDK1.](07c5a1c0fddd7da92a8427f5af840ffa_img.jpg)

Heatmap showing the absolute Pearson correlation between 15 genes. The color scale ranges from 0.0 (white) to 1.0 (dark red). The genes listed on both axes are ACTB, GAPDH, RPLP0, RPL13A, RPS3, STAT1, IFIT1, ISG15, MX1, OAS1, MKI67, PCNA, TYMS, TOP2A, and CDK1.

The gene co-expression graph above is derived from the correlation structure shown below (using a threshold on |Pearson correlation|).

#### GO-derived perturbation graph

Edges link genes with similar GO-term annotations  
(illustration: top-2 Jaccard-similarity neighbors)

![Three small network diagrams showing gene neighborhoods based on GO terms. Immune-related: STAT1, IFIT1, MX1, ISG15. MAPK-related: EGFR, GRB2, RAF1, MAPK1. Cell-cycle-related: MKI67, PCNA, CDK1, TOP2A.](9d68fb624003177408b9d49ff8a6953a_img.jpg)

Three small network diagrams showing gene neighborhoods based on GO terms. Immune-related: STAT1, IFIT1, MX1, ISG15. MAPK-related: EGFR, GRB2, RAF1, MAPK1. Cell-cycle-related: MKI67, PCNA, CDK1, TOP2A.

Example GO annotations used to derive gene similarity

| Gene  | Representative GO terms                                                      |
|-------|------------------------------------------------------------------------------|
| STAT1 | cytokine-mediated signaling, defense response to virus, interferon signaling |
| IFIT1 | defense response to virus, innate immune response, interferon signaling      |
| ISG15 | innate immune response, interferon signaling, protein modification           |
| MX1   | antiviral response, defense response to virus, innate immune response        |
| EGFR  | MAPK cascade, cell proliferation, receptor signaling                         |
| GRB2  | MAPK cascade, receptor signaling, signal transduction                        |
| MAPK1 | MAPK cascade, cell communication, signal transduction                        |
| RAF1  | MAPK cascade, protein kinase activity, signal transduction                   |
| MKI67 | cell cycle, cell proliferation, mitotic nuclear division                     |
| PCNA  | DNA repair, DNA replication, cell cycle                                      |
| TOP2A | DNA replication, cell cycle, chromosome segregation                          |
| CDK1  | cell cycle, mitotic nuclear division, protein kinase activity                |

Gene similarity is based on the Jaccard overlap of GO-term sets; the graph keeps only a few highest-similarity neighbors.

### GEARS architecture

**1** Initialize embeddings

**2** Graph-informed embeddings

![Diagram of GEARS architecture showing gene and perturbation embeddings and their relationship graphs.](a003ffe7299e0a48bceb7f1e45a4f1a3_img.jpg)

The diagram illustrates the GEARS architecture, which consists of two main components: **1 Initialize embeddings** and **2 Graph-informed embeddings**.

**1 Initialize embeddings:** This section shows the initialization of gene and perturbation embeddings. On the left, a list of genes  $g_1, g_2, g_3, g_4, \dots, g_n$  is shown, each associated with a vertical stack of small squares representing its initial embedding. Below this, the **Unperturbed state** is shown, with a list of perturbations  $p_1, p_2, p_3, p_4, \dots, p_n$ , each also associated with a vertical stack of small squares. A lightning bolt icon labeled  $p_2$  is next to  $p_2$ , and another lightning bolt icon labeled  $p_4$  is next to  $p_4$ , indicating genetic perturbations.

**2 Graph-informed embeddings:** This section shows the graph-informed embeddings. It includes two graphs: the **Genetic relationship graph (gene coexpression)** and the **Perturbation relationship graph (GO)**. The Genetic relationship graph is a network of nodes  $g_1, g_2, g_3, g_4, g_5, g_6, g_7, g_8, g_9$  connected by green lines, with each node having a vertical stack of small squares. The Perturbation relationship graph is a network of nodes  $p_1, p_2, p_3, p_4, p_5, p_6, p_7, p_8, p_9$  connected by red lines, with each node having a vertical stack of small squares.

Labels at the bottom indicate the components: **Genetic perturbation**, **Initialize embedding**, and **Perturbation relationship graph (GO)**.

Diagram of GEARS architecture showing gene and perturbation embeddings and their relationship graphs.

### GEARS architecture

**1** Initialize embeddings

**2** Graph-informed embeddings

![Diagram of the GEARS architecture showing gene and perturbation embeddings and their relationship graphs.](8d66c9c295023a1380f9986d3663bb1e_img.jpg)

The diagram illustrates the GEARS architecture. On the left, a list of genes  $g_1, g_2, g_3, g_4, \dots, g_n$  is shown, each associated with an initial embedding vector (represented by a small grid). Below this, a list of perturbations  $p_1, p_2, p_3, p_4, \dots, p_n$  is shown, also with initial embeddings. A lightning bolt icon next to  $p_2$  and  $p_4$  indicates a genetic perturbation. The central part of the diagram shows two graphs: a green 'Genetic relationship graph (gene coexpression)' and a red 'Perturbation relationship graph (GO)'. Each graph node is connected to its corresponding gene or perturbation embedding vector. The graphs are overlaid on a background of curved, colored bands.

Genetic relationship graph (gene coexpression)

Perturbation relationship graph (GO)

Genetic perturbation

Initialize embedding

Diagram of the GEARS architecture showing gene and perturbation embeddings and their relationship graphs.

**1** Each gene has two learnable embeddings:

$x_u^{\text{gene}}$  : gene embedding

$x_u^{\text{pert}}$  : perturbation embedding

**2** Two GNNs incorporate different notions of gene similarity:

$h_u^{\text{gene}} = \text{GNN}_{\text{gene}}(x_u^{\text{gene}}, G_{\text{gene}})$

$h_u^{\text{pert}} = \text{GNN}_{\text{pert}}(x_u^{\text{pert}}, G_{\text{pert}})$

Co-expression graph: observed similarity

GO graph: functional similarity

### GEARS architecture

**1** Initialize embeddings

**2** Graph-informed embeddings

![Diagram of the GEARS architecture showing the flow from gene initialization to graph-informed embeddings and composition.](3442f31a562d1ef45bfa18b18a6a1ddc_img.jpg)

The diagram illustrates the GEARS architecture. It starts with a list of genes  $g_1, g_2, g_3, g_4, \dots, g_n$  and perturbations  $p_1, p_2, p_3, p_4, \dots, p_n$ . Each gene and perturbation is initialized with an embedding vector (represented by small squares). The genes are connected by a 'Genetic relationship graph (gene coexpression)' and the perturbations by a 'Perturbation relationship graph (GO)'. These graphs are used to refine the initial embeddings. Finally, a 'Composition operator' combines the gene and perturbation embeddings for each gene, shown as  $g_i + p_2 + p_4$  for genes  $g_1, g_2, g_3, g_4$  and  $g_n$ . The labels at the bottom are: 'Genetic perturbation' (red), 'Initialize embedding' (black), 'Perturbation relationship graph (GO)' (red), and 'Composition operator' (black).

Diagram of the GEARS architecture showing the flow from gene initialization to graph-informed embeddings and composition.

**1** Each gene has two learnable embeddings:

- $x_u^{\text{gene}}$  : gene embedding
- $x_u^{\text{pert}}$  : perturbation embedding

**2** Two GNNs incorporate different notions of gene similarity:

$$h_u^{\text{gene}} = \text{GNN}_{\text{gene}}(x_u^{\text{gene}}, G_{\text{gene}})$$

$$h_u^{\text{pert}} = \text{GNN}_{\text{pert}}(x_u^{\text{pert}}, G_{\text{pert}})$$

Co-expression graph: observed similarity  
GO graph: functional similarity

### GEARS architecture

**1** Initialize embeddings

**2** Graph-informed embeddings

**3** Compose perturbation

![Diagram of the GEARS architecture showing the flow from genetic relationship graph to perturbation relationship graph and finally to the composition operator.](08f6ace0c83e7394657fa372b47aec04_img.jpg)

The diagram illustrates the GEARS architecture's three main components:

- Genetic relationship graph (gene coexpression):** A green graph showing relationships between genes  $g_1, g_2, g_3, g_4, \dots, g_n$ . Each gene is associated with an initial embedding vector (green squares).
- Perturbation relationship graph (GO):** A red graph showing relationships between perturbations  $p_1, p_2, p_3, p_4, \dots, p_n$ . Each perturbation is associated with an initial embedding vector (red squares).
- Composition operator:** This section shows how gene embeddings are updated by incorporating perturbation information. For each gene  $g_i$ , its initial embedding is combined with perturbation embeddings  $p_2$  and  $p_4$  (indicated by lightning bolts). The resulting perturbed gene embeddings are then passed to the composition operator.

Labels at the bottom indicate the stages: Genetic perturbation, Initialize embedding, Perturbation relationship graph (GO), and Composition operator.

Diagram of the GEARS architecture showing the flow from genetic relationship graph to perturbation relationship graph and finally to the composition operator.

**1** Each gene has two learnable embeddings:

- $x_u^{\text{gene}}$  : gene embedding
- $x_u^{\text{pert}}$  : perturbation embedding

**2** Two GNNs incorporate different notions of gene similarity:

$$h_u^{\text{gene}} = \text{GNN}_{\text{gene}}(x_u^{\text{gene}}, G_{\text{gene}})$$

$$h_u^{\text{pert}} = \text{GNN}_{\text{pert}}(x_u^{\text{pert}}, G_{\text{pert}})$$

Co-expression graph: observed similarity  
GO graph: functional similarity

**3** Combine the applied perturbations into one representation:

$$h^P = \text{MLP}_c \left( \sum_{p \in P} h_p^{\text{pert}} \right)$$

Then combine the same perturbation representation with every gene:

$$h_u^{\text{post}} = \text{MLP}_{\text{pp}}(h_u^{\text{gene}} + h^P)$$

Same  $h^P$  is applied to all genes.

### GEARS architecture

**1** Initialize embeddings

**2** Graph-informed embeddings

**3** Compose perturbation

![Main diagram of the GEARS architecture showing the flow from gene initialization and graph-informed embeddings to perturbation composition and final MLP layers.](fb4274c4b7882a4059103f1dbca9b111_img.jpg)

The diagram illustrates the GEARS architecture. It starts with an 'Unperturbed state' where genes  $g_1, g_2, g_3, g_4, \dots, g_n$  are initialized with embeddings  $g_1, g_2, g_3, g_4, \dots, g_n$ . These are processed through a 'Genetic relationship graph (gene coexpression)' and a 'Perturbation relationship graph (GO)'. The 'Composition operator' combines these with perturbations  $p_2, p_4$  (indicated by lightning bolts) to produce perturbation embeddings  $p_1, p_2, p_3, p_4, \dots, p_n$ . These are then passed through a 'Cross-gene MLP layer' and a 'Gene-specific MLP layer' to yield final gene representations.

Main diagram of the GEARS architecture showing the flow from gene initialization and graph-informed embeddings to perturbation composition and final MLP layers.

**1** Each gene has two learnable embeddings:

$x_u^{\text{gene}}$  : gene embedding  
 $x_u^{\text{pert}}$  : perturbation embedding

**2** Two GNNs incorporate different notions of gene similarity:

$h_u^{\text{gene}} = \text{GNN}_{\text{gene}}(x_u^{\text{gene}}, G_{\text{gene}})$   
 $h_u^{\text{pert}} = \text{GNN}_{\text{pert}}(x_u^{\text{pert}}, G_{\text{pert}})$

Co-expression graph: observed similarity  
 GO graph: functional similarity

**3** Combine the applied perturbations into one representation:

$h^P = \text{MLP}_c \left( \sum_{p \in P} h_p^{\text{pert}} \right)$

Then combine the same perturbation representation with every gene:

$h_u^{\text{post}} = \text{MLP}_{\text{pp}}(h_u^{\text{gene}} + h^P)$

Same  $h^P$  is applied to all genes.

### GEARS architecture

![Main diagram of the GEARS architecture showing the flow from gene initialization and graph-informed embeddings to perturbation composition and cross-gene effects.](fc02903382cebe6fc11e4c0d74b5313f_img.jpg)

The main diagram illustrates the GEARS architecture flow:

- 1 Initialize embeddings:** Genes  $g_1, g_2, g_3, g_4, \dots, g_n$  are initialized with embeddings  $g_1, g_2, g_3, g_4, \dots, g_n$ .
- 2 Graph-informed embeddings:** A **Genetic relationship graph (gene coexpression)** is used to refine gene embeddings.
- 3 Compose perturbation:** Perturbations  $p_1, p_2, p_3, p_4, \dots, p_n$  are initialized. A **Perturbation relationship graph (GO)** is used to compose perturbations. For each gene  $g_i$ , the composition operator combines the gene embedding  $g_i$  with relevant perturbation embeddings  $p_2, p_4$  (indicated by lightning bolts).
- 4 Cross-gene effects:** The composed representations pass through a **Cross-gene MLP layer** and then a **Gene-specific MLP layer** to produce final outputs.

Labels at the bottom: Genetic perturbation, Initialize embedding, Perturbation relationship graph (GO), Composition operator, Cross-gene MLP layer, Gene-specific MLP layer.

Main diagram of the GEARS architecture showing the flow from gene initialization and graph-informed embeddings to perturbation composition and cross-gene effects.

**1** Each gene has two learnable embeddings:

$x_u^{\text{gene}}$  : gene embedding  
 $x_u^{\text{pert}}$  : perturbation embedding

**2** Two GNNs incorporate different notions of gene similarity:

$h_u^{\text{gene}} = \text{GNN}_{\text{gene}}(x_u^{\text{gene}}, G_{\text{gene}})$   
 $h_u^{\text{pert}} = \text{GNN}_{\text{pert}}(x_u^{\text{pert}}, G_{\text{pert}})$

Co-expression graph: observed similarity  
 GO graph: functional similarity

**3** Combine the applied perturbations into one representation:

$h^P = \text{MLP}_c \left( \sum_{p \in P} h_p^{\text{pert}} \right)$

Then combine the same perturbation representation with every gene:

$h_u^{\text{post}} = \text{MLP}_{\text{pp}}(h_u^{\text{gene}} + h^P)$

Same  $h^P$  is applied to all genes.

**4** First predict a preliminary effect for each gene:

$z_u = w_u^T h_u^{\text{post}} + b_u$

Then summarize effects across the transcriptome:

$h^{cg} = \text{MLP}_{\text{cg}}(z_1, \dots, z_K)$

$h^{cg}$  captures transcriptome-wide context and secondary effects.

### GEARS architecture

![GEARS architecture diagram showing the flow from gene initialization to perturbation prediction.](b898dcb574f08ea237dd3326abecd185_img.jpg)

The diagram illustrates the GEARS architecture, which consists of five main steps:

- Initialize embeddings**: Each gene  $g_i$  is initialized with a gene embedding  $x_u^{\text{gene}}$  and a perturbation embedding  $x_u^{\text{pert}}$ .
- Graph-informed embeddings**: Two Graph Neural Networks (GNNs) incorporate different notions of gene similarity (co-expression graph and GO graph) to produce gene embeddings  $h_u^{\text{gene}}$  and perturbation embeddings  $h_u^{\text{pert}}$ .
- Compose perturbation**: The applied perturbations  $p_2$  and  $p_4$  are combined into a single representation  $h^P$  using a composition operator.
- Cross-gene effects**: A cross-gene MLP layer processes the gene embeddings and the composed perturbation representation to capture transcriptome-wide context and secondary effects, resulting in  $h^{cg}$ .
- Predict response**: A gene-specific decoder combines the local and cross-gene information to predict the post-perturbation expression  $\hat{g}_u$ .

The diagram also shows the flow of data from the unperturbed state to the perturbed state, including the genetic perturbation, initialization, graph-informed embeddings, composition operator, cross-gene MLP layer, gene-specific MLP layer, and the final perturbed state.

GEARS architecture diagram showing the flow from gene initialization to perturbation prediction.

**1** Each gene has two learnable embeddings:

$$x_u^{\text{gene}} : \text{gene embedding}$$

$$x_u^{\text{pert}} : \text{perturbation embedding}$$

**2** Two GNNs incorporate different notions of gene similarity:

$$h_u^{\text{gene}} = \text{GNN}_{\text{gene}}(x_u^{\text{gene}}, G_{\text{gene}})$$

$$h_u^{\text{pert}} = \text{GNN}_{\text{pert}}(x_u^{\text{pert}}, G_{\text{pert}})$$

Co-expression graph: observed similarity  
GO graph: functional similarity

**3** Combine the applied perturbations into one representation:

$$h^P = \text{MLP}_c \left( \sum_{p \in P} h_p^{\text{pert}} \right)$$

Then combine the same perturbation representation with every gene:

$$h_u^{\text{post}} = \text{MLP}_{pp}(h_u^{\text{gene}} + h^P)$$

Same  $h^P$  is applied to all genes.

**4** First predict a preliminary effect for each gene:

$$z_u = w_u^T h_u^{\text{post}} + b_u$$

Then summarize effects across the transcriptome:

$$h^{cg} = \text{MLP}_{cg}(z_1, \dots, z_K)$$

$h^{cg}$  captures transcriptome-wide context and secondary effects.

**5** The final gene-specific decoder combines the local and cross-gene information:

$$\hat{z}_u = \text{Decoder}_u(z_u \parallel h^{cg})$$

Add the predicted perturbation effect to the control expression:

$$\hat{g}_u = g_{u,\text{ctrl}} + \hat{z}_u$$

**Output:** predicted post-perturbation expression.

# How is GEARS trained?

#### How is GEARS trained?

- ▶ **Input:** control expression profile + perturbation set
- ▶ **Prediction:** post-perturbation gene expression
- ▶ **Training target:** measured expression under the perturbation
- ▶ **Loss:** compares predicted vs. measured post-perturbation expression
- ▶ **Autofocus direction-aware loss:** emphasizes informative perturbation-induced changes. Most genes change little after perturbation, so standard MSE can underweight the genes with the strongest biological response.

# What can GEARS generalise to?

![QR code linking to the Menti poll.](8f068da8e4726d3b832b19aa37b1d162_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

#### What can GEARS generalise to?

##### Can:

- ▶ Predict effects of genes never experimentally perturbed during training
- ▶ Predict new combinations, including combinations containing unseen genes
- ▶ Use prior biological relationships to extrapolate beyond observed perturbations

##### Cannot/limitations:

- ▶ Not originally designed for new cell types / cross-cell-type transfer
- ▶ Combination prediction still benefits from / requires exposure to combinatorial perturbation data
- ▶ Performance depends on the quality and relevance of the prior graphs

How can we tell whether a complex perturbation model is really learning something beyond simple patterns in the data?

## Benchmark complex models against strong simple alternatives

- ▶ Use the same datasets, train/test splits and metrics
- ▶ Include simple baselines that capture dominant structure in the data
- ▶ Test the specific generalization claim of the model
- ▶ Ask whether complexity improves prediction beyond additive or linear effects

### How do they benchmark added value?

Benchmark complex models against strong simple alternatives

#### 1. Unseen combinations

- ▶ Train on single perturbations + some combinations
- ▶ Test on held-out double perturbations

*Question tested:* Can the model predict non-additive structure beyond what additivity already explains?

#### 2. Unseen perturbations

- ▶ Hold out entire single-gene perturbations
- ▶ Test on genes never perturbed during training

*Question tested:* Can the model extrapolate to a new perturbation identity better than simple structured predictors?

Different generalisation claims require different baselines.

What is the best simple baseline for predicting an unseen combination of two perturbations?

![QR code linking to the Menti poll.](e559cb8d15d95b7f4c5761d295051cc0_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

What is the best simple baseline for predicting a completely unseen perturbation?

![QR code linking to the Menti poll.](26e59f6e6ab842a448d8270473d5c8a8_img.jpg)

A square QR code with a black and white pixelated pattern, used for quick access to the Menti poll.

QR code linking to the Menti poll.

menti.com  
1943 3368

### How do they benchmark added value?

Benchmark complex models against strong simple alternatives

#### 1. Unseen combinations

- ▶ Train on single perturbations + some combinations
- ▶ Test on held-out double perturbations
- ▶ Simple baseline: add the two single-perturbation effects
- ▶ Models: CPA, GEARS, scGPT (among others)

*Question tested:* Can the model predict non-additive structure beyond what additivity already explains?

#### 2. Unseen perturbations

- ▶ Hold out entire single-gene perturbations
- ▶ Test on genes never perturbed during training
- ▶ Simple baselines: mean / linear predictors
- ▶ Models include GEARS, scGPT (not CPA)

*Question tested:* Can the model extrapolate to a new perturbation identity better than simple structured predictors?

Different generalisation claims require different baselines.

### Benchmarking double perturbation prediction task

Can complex models improve on simple additivity for unseen combinations?

Prediction error

$$L_2(\hat{\mathbf{y}}, \mathbf{y}) = \sqrt{\sum_{g=1}^{1000} (\hat{y}_g - y_g)^2}$$

![Violin plot showing prediction error (L2) for various models. The y-axis ranges from 0 to 12.5. The x-axis is divided into three groups: Baselines (No change, Additive), Foundation models (scGPT, scFoundation, UCE*, scBERT*, Geneformer*), and Other deep learning models (GEARS, CPA). Each violin plot shows the distribution of errors, with a red horizontal line indicating the median error. An orange dot in each plot represents the error for the CEBPE+CEBPB combination. The 'No change' baseline has a median error around 5.5, while 'Additive' is around 2.5. Foundation models generally show lower median errors, with Geneformer* being the lowest at approximately 3.5. GEARS also shows a low median error around 4.0. CPA has a significantly higher median error around 11.5.](509a054727400bc6d424bb2a559b8cfc_img.jpg)

| Model Group                | Model        | Median Error (approx.) | CEBPE+CEBPB Error (approx.) |
|----------------------------|--------------|------------------------|-----------------------------|
| Baselines                  | No change    | 5.5                    | 8.5                         |
|                            | Additive     | 2.5                    | 4.5                         |
| Foundation models          | scGPT        | 4.5                    | 7.0                         |
|                            | scFoundation | 4.5                    | 4.5                         |
|                            | UCE*         | 4.0                    | 6.5                         |
|                            | scBERT*      | 4.0                    | 6.5                         |
|                            | Geneformer*  | 3.5                    | 3.0                         |
| Other deep learning models | GEARS        | 4.0                    | 6.5                         |
|                            | CPA          | 11.5                   | 11.5                        |

Violin plot showing prediction error (L2) for various models. The y-axis ranges from 0 to 12.5. The x-axis is divided into three groups: Baselines (No change, Additive), Foundation models (scGPT, scFoundation, UCE\*, scBERT\*, Geneformer\*), and Other deep learning models (GEARS, CPA). Each violin plot shows the distribution of errors, with a red horizontal line indicating the median error. An orange dot in each plot represents the error for the CEBPE+CEBPB combination. The 'No change' baseline has a median error around 5.5, while 'Additive' is around 2.5. Foundation models generally show lower median errors, with Geneformer\* being the lowest at approximately 3.5. GEARS also shows a low median error around 4.0. CPA has a significantly higher median error around 11.5.

#### Baseline models

##### No change

$$\hat{\mathbf{y}}^{A+B} = \mathbf{y}^\emptyset$$

Assumes no perturbation effect

### Additive

$$\hat{\mathbf{y}}^{A+B} = \mathbf{y}^A + \mathbf{y}^B - \mathbf{y}^\emptyset$$

Assumes the effect of A and B add linearly

### Benchmarking unseen perturbation prediction

Can complex models extrapolate to a perturbation never seen during training better than simple predictors?

#### Baseline models

![Violin plot for Replogle K562 showing prediction error (L2) for various models. The y-axis ranges from 0 to 10.0. Models include Mean, LM based on training, scGPT, UCE*, scBERT*, Geneformer*, and GEARS. A red horizontal line indicates the mean error for each model.](835ebc0e9ec15eea8eadc15448249226_img.jpg)

Replogle K562

Prediction error ( $L_2$ )

Mean LM based on training scGPT UCE\* scBERT\* Geneformer\* GEARS

Baselines Foundation models Other DL models

Violin plot for Replogle K562 showing prediction error (L2) for various models. The y-axis ranges from 0 to 10.0. Models include Mean, LM based on training, scGPT, UCE\*, scBERT\*, Geneformer\*, and GEARS. A red horizontal line indicates the mean error for each model.

![Violin plot for Replogle RPE1 showing prediction error (L2) for various models. The y-axis ranges from 0 to 10.0. Models include Mean, LM based on training, scGPT, UCE*, scBERT*, Geneformer*, and GEARS. A red horizontal line indicates the mean error for each model.](0775f419af4e481eea2fb9706fe0b035_img.jpg)

Replogle RPE1

Prediction error ( $L_2$ )

Mean LM based on training scGPT UCE\* scBERT\* Geneformer\* GEARS

Baselines Foundation models Other DL models

Violin plot for Replogle RPE1 showing prediction error (L2) for various models. The y-axis ranges from 0 to 10.0. Models include Mean, LM based on training, scGPT, UCE\*, scBERT\*, Geneformer\*, and GEARS. A red horizontal line indicates the mean error for each model.

##### Mean

$$\hat{\mathbf{y}}^{(p)} = \bar{\mathbf{y}}_{\text{train}}$$

Predicts the average expression profile across training perturbations

#### Linear model

$$\hat{\mathbf{Y}} = \mathbf{G}\mathbf{W}\mathbf{P}^{\top} + \mathbf{b}$$

Predict response from gene representations with a linear model

- $\mathbf{G}$ : read-out gene embeddings
- $\mathbf{P}$ : perturbation gene embeddings
- $\mathbf{W}$ : learned linear mapping
- $\mathbf{b}$ : gene-wise intercept

### How should we benchmark perturbation models?

- ▶ **Use strong simple baselines:** Ask whether model complexity adds predictive value beyond mean, linear or additive structure (*Ahlmann-Eltze et al., Nature Methods, 2025*)
- ▶ **Match the metric to the biological question:** Good whole-transcriptome prediction does not necessarily mean good prediction of perturbation-specific effects. (*SYSTEMA, Nature Biotechnology, 2025*)
- ▶ **Check that the metric is informative:** A useful metric should distinguish meaningful predictions from null predictors. (*Miller et al., bioRxiv, 2025*)
- ▶ **Benchmark the actual generalization claim:** Be explicit about what is held out: perturbations, combinations, cell types, contexts, or patients. (*Saez-Rodriguez et al., Nature Methods, 2026*)
- ▶ **Test robustness across datasets and splits:** Conclusions should not depend on one dataset or one favorable train/test split.

## Takeaways

- ▶ **Different models solve different generalization problems:** Representing observed states, recombining known perturbations, and predicting completely unseen perturbations are fundamentally different tasks.
- ▶ **Simple biological structure already goes a long way:** Much of the predictable response can be additive, low-dimensional or shared across perturbations.
- ▶ **Complex models are most valuable when they capture what simple models miss:** Non-additive interactions, context dependence, multimodal information, transferable biological relationships.
- ▶ **More complexity also means greater data demands:** Large numbers of cells do not necessarily mean many independent perturbation examples; learning interactions and extrapolation may require much richer perturbation coverage.
- ▶ **Biological priors can help extrapolation:** Especially when the perturbation itself has not been observed, but their value depends on how informative and relevant the prior is.

## References

## Lecture papers

- **Lopez et al.** *Deep generative modeling for single-cell transcriptomics.* **Nature Methods**, 2018.
- **Cui et al.** *scGPT: toward building a foundation model for single-cell multi-omics using generative AI.* **Nature Methods**, 2024.
- **Kedzierska et al.** *Zero-shot evaluation reveals limitations of single-cell foundation models.* **Genome Biology**, 2025.
- **Lotfollahi et al.** *Predicting cellular responses to complex perturbations in high-throughput screens.* **Molecular Systems Biology**, 2023.
- **Roohani et al.** *Predicting transcriptional outcomes of novel multigene perturbations with GEARS.* **Nature Biotechnology**, 2024.
- **Ahlmann-Eltze et al.** *Deep-learning-based gene perturbation effect prediction does not yet outperform simple linear baselines.* **Nature Methods**, 2025.

### Additional benchmarking / perspective

- **Viñas Torné et al.** *Systema: a framework for evaluating genetic perturbation response prediction beyond systematic variation.* **Nature Biotechnology**, published online 2025.
- **Miller et al.** *Deep Learning-Based Genetic Perturbation Models Do Outperform Uninformative Baselines on Well-Calibrated Metrics.* **bioRxiv**, 2025.
- **Saez-Rodriguez et al.** *Benchmarking biomedical foundation models.* **Nature Methods**, 2026.