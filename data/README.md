# Data

No data files are stored in this repository. The notebook downloads everything it needs
on first run into `data_GSE91061/` (created next to the notebook).

| File | Source | Content |
|---|---|---|
| `GSE91061_BMS038109Sample.hg19KnownGene.raw.csv.gz` | [GEO GSE91061](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE91061) | Raw fragment counts (Entrez IDs × 109 samples) |
| `GSE91061_BMS038109Sample.hg19KnownGene.fpkm.csv.gz` | GEO GSE91061 | Robust FPKM |
| `GSE91061_BMS038109Sample.hg19KnownGene.rld.csv.gz` | GEO GSE91061 | Regularised-log expression |
| `GSE91061_BMS038109Sample_Cytolytic_Score_20161026.txt.gz` | GEO GSE91061 | Published cytolytic score |
| `Human.GRCh38.p13.annot.tsv.gz` | NCBI GEO annotation | Entrez ID → gene symbol mapping |
| `h.all.v2023.2.Hs.symbols.gmt` | [MSigDB](https://www.gsea-msigdb.org/) | Hallmark gene sets |
| `c2.cp.reactome.v2023.2.Hs.symbols.gmt` | MSigDB | Reactome gene sets |

Embedded in the notebook (no download required):

- **Clinical annotation** — Table S2 of Riaz et al., *Cell* 2017 (response, prior
  ipilimumab, survival, mutation and neoantigen load). If `data_GSE91061/mmc2.xlsx` is
  present, it is used instead of the embedded copy.
- **TME signatures** — 29 functional gene expression signatures from Bagaev et al.,
  *Cancer Cell* 2021 (`gene_signatures.gmt`), with display order
  (`gene_signatures_order.tsv`). Local files in `data_GSE91061/` take precedence.

If an automatic download fails (e.g. behind a proxy), download the files manually from the
links above and place them in `data_GSE91061/`.

Intermediate result tables (DE results, GSEA, ssGSEA scores, statistical tests) are also
written to `data_GSE91061/` when the notebook runs.
