Basic analysis of public skin scRNA-seq data using Seurat.
Reads aligned and cells hashed using nf-core scrnaseq pipeline (STARsolo workflow)

Scripts:
1_Seurat_process: Import counts matrices from nf-core scRNAseq, basic QC (globin/mitochondrial filtering), integrate across individuals, create seurat object.

1.1_Seurat_cluster: Dimensionality reduction and clustering

1.2_Seurat_annotate: Annotate with SingleR using celldex resource. 

    adapts https://www.singlecellcourse.org/single-cell-rna-seq-analysis-using-seurat.html#cell-type-annotation-using-singler
    remember to set the ExperimentHub cache location when caching the celldex resources:
    setExperimentHubOption('cache', '/well/fullerton/users/rxw025/software/R/ExperimentHub')