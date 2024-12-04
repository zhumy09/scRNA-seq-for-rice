# scRNA-seq-for-rice
Rice scRNA-seq data analysis, template and final files stoarage  

System requiredments:

All software dependencies and operating systems (including version numbers)

NAME="AlmaLinux"''VERSION="9.4 (Seafoam Ocelot)"''ID="almalinux"''ID_LIKE="rhel centos fedora"''VERSION_ID="9.4"''PLATFORM_ID="platform:el9"''PRETTY_NAME="AlmaLinux 9.4 (Seafoam Ocelot)"''ANSI_COLOR="0;34"''LOGO="fedora-logo-icon"''CPE_NAME="cpe:/o:almalinux:almalinux:9::baseos"''HOME_URL="https://almalinux.org/"''DOCUMENTATION_URL="https://wiki.almalinux.org/"''BUG_REPORT_URL="https://bugs.almalinux.org/"''''ALMALINUX_MANTISBT_PROJECT="AlmaLinux-9"''ALMALINUX_MANTISBT_PROJECT_VERSION="9.4"''REDHAT_SUPPORT_PRODUCT="AlmaLinux"''REDHAT_SUPPORT_PRODUCT_VERSION="9.4"''SUPPORT_END=2032-06-01'

R version 4.2.0 (2022-04-22)



Versions the software has been tested on
R version 4.2.0 (2022-04-22)
Platform: x86_64-conda-linux-gnu (64-bit)
Running under: CentOS Stream 8

Matrix products: default
BLAS/LAPACK: /hpc/group/pbenfeylab/mz187/miniconda3/envs/muscat/lib/libopenblasp-r0.3.21.so

locale:
 [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C              
 [3] LC_TIME=en_US.UTF-8        LC_COLLATE=en_US.UTF-8    
 [5] LC_MONETARY=en_US.UTF-8    LC_MESSAGES=en_US.UTF-8   
 [7] LC_PAPER=en_US.UTF-8       LC_NAME=C                 
 [9] LC_ADDRESS=C               LC_TELEPHONE=C            
[11] LC_MEASUREMENT=en_US.UTF-8 LC_IDENTIFICATION=C       

attached base packages:
[1] stats4    grid      stats     graphics  grDevices utils     datasets 
[8] methods   base     

other attached packages:
 [1] future_1.32.0               scran_1.26.0               
 [3] scuttle_1.8.0               SingleCellExperiment_1.20.0
 [5] SummarizedExperiment_1.28.0 Biobase_2.58.0             
 [7] GenomicRanges_1.50.0        GenomeInfoDb_1.34.9        
 [9] IRanges_2.32.0              S4Vectors_0.36.0           
[11] BiocGenerics_0.44.0         MatrixGenerics_1.10.0      
[13] matrixStats_1.0.0           limma_3.54.0               
[15] muscat_1.12.0               ggrepel_0.9.3              
[17] gprofiler2_0.2.2            GeneOverlap_1.34.0         
[19] circlize_0.4.15             ComplexHeatmap_2.14.0      
[21] cowplot_1.1.1               Seurat_3.1.5               
[23] lubridate_1.9.2             forcats_1.0.0              
[25] stringr_1.5.0               dplyr_1.1.2                
[27] purrr_1.0.1                 readr_2.1.4                
[29] tidyr_1.3.0                 tibble_3.2.1               
[31] ggplot2_3.4.2               tidyverse_2.0.0            

loaded via a namespace (and not attached):
  [1] utf8_1.2.3                reticulate_1.25          
  [3] tidyselect_1.2.0          lme4_1.1-33              
  [5] RSQLite_2.3.1             AnnotationDbi_1.60.0     
  [7] htmlwidgets_1.6.2         BiocParallel_1.32.5      
  [9] Rtsne_0.16                ScaledMatrix_1.6.0       
 [11] munsell_0.5.0             codetools_0.2-19         
 [13] ica_1.0-3                 statmod_1.4.36           
 [15] pbdZMQ_0.3-9              withr_2.5.0              
 [17] colorspace_2.1-0          uuid_1.1-0               
 [19] ROCR_1.0-11               listenv_0.9.0            
 [21] Rdpack_2.4                repr_1.1.6               
 [23] GenomeInfoDbData_1.2.9    bit64_4.0.5              
 [25] glmmTMB_1.1.7             parallelly_1.36.0        
 [27] vctrs_0.6.3               generics_0.1.3           
 [29] timechange_0.2.0          R6_2.5.1                 
 [31] doParallel_1.0.17         ggbeeswarm_0.7.2         
 [33] clue_0.3-64               rsvd_1.0.5               
 [35] locfit_1.5-9.8            bitops_1.0-7             
 [37] cachem_1.0.8              DelayedArray_0.24.0      
 [39] scales_1.2.1              beeswarm_0.4.0           
 [41] gtable_0.3.3              beachmat_2.14.0          
 [43] globals_0.16.2            rlang_1.1.1              
 [45] genefilter_1.80.0         GlobalOptions_0.1.2      
 [47] splines_4.2.0             TMB_1.9.4                
 [49] lazyeval_0.2.2            broom_1.0.5              
 [51] reshape2_1.4.4            backports_1.4.1          
 [53] tools_4.2.0               gplots_3.1.3             
 [55] RColorBrewer_1.1-3        ggridges_0.5.4           
 [57] Rcpp_1.0.10               plyr_1.8.8               
 [59] base64enc_0.1-3           sparseMatrixStats_1.10.0 
 [61] progress_1.2.2            zlibbioc_1.44.0          
 [63] RCurl_1.98-1.12           prettyunits_1.1.1        
 [65] viridis_0.6.3             pbapply_1.7-0            
 [67] GetoptLong_1.0.5          zoo_1.8-12               
 [69] cluster_2.1.4             variancePartition_1.28.0 
 [71] magrittr_2.0.3            data.table_1.14.8        
 [73] lmerTest_3.1-3            lmtest_0.9-40            
 [75] RANN_2.6.1                fitdistrplus_1.1-11      
 [77] hms_1.1.3                 patchwork_1.1.2          
 [79] evaluate_0.21             xtable_1.8-4             
 [81] pbkrtest_0.5.2            RhpcBLASctl_0.23-42      
 [83] XML_3.99-0.9              gridExtra_2.3            
 [85] shape_1.4.6               compiler_4.2.0           
 [87] scater_1.26.0             KernSmooth_2.23-21       
 [89] crayon_1.5.2              minqa_1.2.5              
 [91] htmltools_0.5.5           tzdb_0.4.0               
 [93] geneplotter_1.76.0        DBI_1.1.3                
 [95] MASS_7.3-60               boot_1.3-28.1            
 [97] Matrix_1.5-4.1            cli_3.6.1                
 [99] rbibutils_2.2.13          metapod_1.6.0            
[101] parallel_4.2.0            igraph_1.5.0             
[103] pkgconfig_2.0.3           numDeriv_2016.8-1.1      
[105] IRdisplay_1.1             plotly_4.10.0            
[107] foreach_1.5.2             annotate_1.76.0          
[109] vipor_0.4.5               dqrng_0.3.0              
[111] blme_1.0-5                XVector_0.38.0           
[113] digest_0.6.31             sctransform_0.3.5        
[115] RcppAnnoy_0.0.20          tsne_0.1-3.1             
[117] Biostrings_2.66.0         leiden_0.4.3             
[119] uwot_0.1.14               edgeR_3.40.0             
[121] DelayedMatrixStats_1.20.0 gtools_3.9.4             
[123] rjson_0.2.21              nloptr_2.0.3             
[125] lifecycle_1.0.3           nlme_3.1-157             
[127] jsonlite_1.8.5            aod_1.3.2                
[129] BiocNeighbors_1.16.0      viridisLite_0.4.2        
[131] fansi_1.0.4               pillar_1.9.0             
[133] lattice_0.21-8            KEGGREST_1.38.0          
[135] fastmap_1.1.1             httr_1.4.6               
[137] survival_3.5-5            glue_1.6.2               
[139] png_0.1-8                 iterators_1.0.14         
[141] bluster_1.8.0             bit_4.0.5                
[143] stringi_1.7.6             blob_1.2.4               
[145] BiocSingular_1.14.0       DESeq2_1.38.0            
[147] caTools_1.18.2            memoise_2.0.1            
[149] IRkernel_1.3.2            irlba_2.3.5.1            
[151] future.apply_1.11.0       ape_5.7-1      


Any required non-standard hardware

We used Duke computer cluster to do our bioinformatic analysis. 
To faciliate our scRNA-seq analysis, we often request a 200GB memory: srun -p pbenfeylab --pty --mem=200G bash -i 

Installation guide:
We will include a specific documentation for installing the packages we used. We don't develop any new package for this project. 

Instructions
Typical insall time on a "normal" desktop computer

Demo:
Instruction to run on data
Expected output
Expected run time for demo on a "normal" desktop computer

Please check the included jupyter notebook for data analysis and plot visualization.

Instructions for use:

How to run the software on your data
Reproduction instructions

Please check the included jupyter notebook for data analysis and plot visualization.

Raw sequencing data storage:

Single cell: GSE251706;PRJNA640389
Bulk vs Single-cell: GSE283428;PRJNA1193632
Bulk root dev: GSE260671;PRJNA1082669
Bulk root protoplast: GSE283509;PRJNA1194134


Power Curves

License
This project is covered under the MIT License.

