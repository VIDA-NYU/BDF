---
title: Benchmarks
permalink: /benchmarks/
---

### GDC-SM: The GDC Schema Matching Benchmark
<div style="display: flex; align-items: flex-start; margin-bottom: 2em;">
  <div style="flex: 2; text-align: justify;">
    GDC-SM is a schema matching benchmark derived from a real-world biomedical data harmonization scenario in cancer genomics. It is based on the study by <a href="https://pubmed.ncbi.nlm.nih.gov/37582339/">Li et al. (2023)</a>, where datasets from ten independent tumor-related studies were integrated and mapped to the <a href="https://gdc.cancer.gov/">Genomics Data Commons (GDC)</a> standard used by the U.S. National Cancer Institute. To support schema matching research, the original GDC graph-based model was transformed into a simplified relational schema containing only column names and value domains, producing a unified target table with 736 attributes.
    <br><br>
    The benchmark includes 10 source-to-target table pairs with heterogeneous schemas (16–179 columns per source and 93–225 rows). Ground truth matches were manually curated by at least three biomedical experts per dataset, combining automated candidate generation with careful expert validation and consensus-based decision-making, reflecting the inherent ambiguity and difficulty of real biomedical schema alignment tasks.
    <br><br>
    <p>
      <a href="https://zenodo.org/records/14963588"><i class="fa fa-folder-open"></i> Benchmark</a>&nbsp;&nbsp;&nbsp;
    </p>
  </div>
</div>

<hr>

### GDC-VM: The GDC Value Matching Benchmark
<div style="display: flex; align-items: flex-start; margin-bottom: 2em;">
  <div style="flex: 2; text-align: justify;">
    GDC-VM extends GDC-SM by introducing a value-level matching benchmark that provides curated correspondences for attribute values in addition to schema-level mappings. Built on the same biomedical harmonization setting from <a href="https://pubmed.ncbi.nlm.nih.gov/37582339/">Li et al. (2023)</a>, it focuses on aligning source data values from ten cancer-related studies to standardized values in the <a href="https://gdc.cancer.gov">Genomics>Data Commons (GDC)</a> model. This enables fine-grained evaluation of value matching tasks in realistic clinical and genomic datasets.
    <br><br>
    The benchmark was built through a multi-stage process combining automated matching with BDI-Kit and independent review by three annotators per dataset. All disagreements were resolved through consensus, producing a final ground truth with 100% agreement after reconciliation. It includes datasets with 5–29 attributes and 117–524 unique values, resulting in 182–840 curated value-level matches per dataset and reflecting realistic complexity in biomedical data harmonization tasks.
    <br><br>
    <p>
      <a href="https://zenodo.org/records/18557064"><i class="fa fa-folder-open"></i> Benchmark</a>&nbsp;&nbsp;&nbsp;
    </p>
  </div>
</div>

<hr>

### DataRef: A Dataset of Data Citations
<div style="display: flex; align-items: flex-start; margin-bottom: 2em;">
  <div style="flex: 2; text-align: justify;">
    DataRef Benchmark was created during the development of Data Gatherer, an LLM-based system for automatically detecting dataset mentions and extracting structured dataset citation records from scientific publications. All underlying publications and repositories are open-access, ensuring reproducibility and transparency.
    <br><br>
    The benchmark consists of two complementary datasets. DataRef-EXP contains manually curated dataset references from 21 PubMed Central articles, selected to capture diverse citation styles and common extraction challenges, including incomplete or erroneous dataset mentions. DataRef-REV is derived through a reverse-engineering approach using large-scale repository metadata from ProteomeCentral and the Gene Expression Omnibus (GEO), providing a broad set of publication–dataset links grounded in real repository records. A sampled subset ensures balance across sources, while the full dataset spans hundreds of thousands of dataset references across hundreds of thousands of papers and over 100,000 datasets, offering a large-scale benchmark for dataset mention extraction and linking tasks.
    <br><br>
    <p>
      <a href="https://zenodo.org/records/15549086"><i class="fa fa-folder-open"></i> Benchmark</a>&nbsp;&nbsp;&nbsp;
    </p>
  </div>
</div>

<hr>
