# EWAS report
- study: Illumina methylation data
- author: Analyst
- date: 18 November, 2026

## Parameters


```
## $sig.threshold
## [1] 0.003221885
## 
## $max.plots
## [1] 1
## 
## $model
## [1] "all"
## 
## $qq.inflation.method
## [1] "median"
## 
## $practical.threshold
##   cg23576855 
## 1.392554e-54 
## 
## $winsorize.pct
## [1] 0.01
## 
## $outlier.iqr.factor
## [1] NA
## 
## $rlm
## [1] TRUE
## 
## $most.variable
## [1] 50000
## 
## $random.seed
## [1] 20161123
## 
## $sample.size
## [1] 188
```

## Sample characteristics

For continuous or ordinal variables, the "mean" column provides the mean
and the "var" column the standard deviation of the variable.
For categorical variables, the "mean" column provides the number
of samples with the given "value" and the
"var" column the percentage of samples with the given "value".


|variable             |value   |mean       |var        |
|:--------------------|:-------|:----------|:----------|
|variable of interest |never   |99         |52.7       |
|variable of interest |current |89         |47.3       |
|Age                  |        |52.73936   |11.63027   |
|Sex                  |F       |144        |76.6       |
|Sex                  |M       |44         |23.4       |
|Bcell                |        |0.06601765 |0.02948774 |
|CD4T                 |        |0.188321   |0.06010949 |
|CD8T                 |        |0.1090449  |0.04596973 |
|Mono                 |        |0.09398571 |0.02091805 |
|Neu                  |        |0.5042772  |0.0978032  |
|NK                   |        |0.08488758 |0.03298624 |

## Covariate associations




### Covariate Age


statistics


|var1     |var2 |         F|   p-value|          R|   p-value|
|:--------|:----|---------:|---------:|----------:|---------:|
|variable |Age  | 0.0001012| 0.9919836| -0.0271044| 0.7119591|

cases


|variable |     mean|      var|  n|     t.stat|   p.value|
|:--------|--------:|--------:|--:|----------:|---------:|
|never    | 52.74747| 156.7621| 99|  0.0101488| 0.9919135|
|current  | 52.73034| 112.8583| 89| -0.0101488| 0.9919135|





![plot of chunk unnamed-chunk-24](figure/unnamed-chunk-24-1.png)


### Covariate Sex


statistics


|var1     |var2 |        R|   p-value|
|:--------|:----|--------:|---------:|
|variable |Sex  | 0.054606| 0.4567064|

frequencies


|        |  F|  M|
|:-------|--:|--:|
|never   | 78| 21|
|current | 66| 23|

enrichment p-values


|        |         F|         M|
|:-------|---------:|---------:|
|never   | 0.2820187| 0.8215467|
|current | 0.8215467| 0.2820187|





![plot of chunk unnamed-chunk-30](figure/unnamed-chunk-30-1.png)


### Covariate Bcell


statistics


|var1     |var2  |         F|   p-value|          R|   p-value|
|:--------|:-----|---------:|---------:|----------:|---------:|
|variable |Bcell | 0.2366181| 0.6272321| -0.1165057| 0.1113357|

cases


|variable |      mean|       var|  n|     t.stat|   p.value|
|:--------|---------:|---------:|--:|----------:|---------:|
|never    | 0.0670116| 0.0004847| 99|  0.4746479| 0.6357655|
|current  | 0.0649121| 0.0013056| 89| -0.4746479| 0.6357655|





![plot of chunk unnamed-chunk-36](figure/unnamed-chunk-36-1.png)


### Covariate CD4T


statistics


|var1     |var2 |        F|   p-value|         R|   p-value|
|:--------|:----|--------:|---------:|---------:|---------:|
|variable |CD4T | 1.708011| 0.1928572| 0.0797971| 0.2763471|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.1828989| 0.0033585| 99| -1.301991| 0.1945799|
|current  | 0.1943523| 0.0038679| 89|  1.301991| 0.1945799|





![plot of chunk unnamed-chunk-42](figure/unnamed-chunk-42-1.png)


### Covariate CD8T


statistics


|var1     |var2 |        F|   p-value|          R|   p-value|
|:--------|:----|--------:|---------:|----------:|---------:|
|variable |CD8T | 3.076023| 0.0811016| -0.1161131| 0.1125543|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.1145895| 0.0023595| 99|  1.766782| 0.0789065|
|current  | 0.1028774| 0.0017899| 89| -1.766782| 0.0789065|





![plot of chunk unnamed-chunk-48](figure/unnamed-chunk-48-1.png)


### Covariate Mono


statistics


|var1     |var2 |        F|   p-value|          R|   p-value|
|:--------|:----|--------:|---------:|----------:|---------:|
|variable |Mono | 6.977278| 0.0089576| -0.1655813| 0.0231534|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.0977469| 0.0004783| 99|  2.660786| 0.0084779|
|current  | 0.0898019| 0.0003635| 89| -2.660786| 0.0084779|





![plot of chunk unnamed-chunk-54](figure/unnamed-chunk-54-1.png)


### Covariate Neu


statistics


|var1     |var2 |        F|   p-value|         R|   p-value|
|:--------|:----|--------:|---------:|---------:|---------:|
|variable |Neu  | 1.790709| 0.1824734| 0.1221984| 0.0948021|

cases


|variable |      mean|       var|  n|    t.stat|  p.value|
|:--------|---------:|---------:|--:|---------:|--------:|
|never    | 0.4952459| 0.0088404| 99| -1.332769| 0.184292|
|current  | 0.5143232| 0.0102878| 89|  1.332769| 0.184292|





![plot of chunk unnamed-chunk-60](figure/unnamed-chunk-60-1.png)


### Covariate NK


statistics


|var1     |var2 |        F|   p-value|          R|   p-value|
|:--------|:----|--------:|---------:|----------:|---------:|
|variable |NK   | 7.140693| 0.0082045| -0.1695074| 0.0200441|

cases


|variable |      mean|       var|  n|    t.stat|   p.value|
|:--------|---------:|---------:|--:|---------:|---------:|
|never    | 0.0908853| 0.0013115| 99|  2.709977| 0.0073742|
|current  | 0.0782160| 0.0007662| 89| -2.709977| 0.0073742|





![plot of chunk unnamed-chunk-66](figure/unnamed-chunk-66-1.png)

## QQ plots






![plot of chunk unnamed-chunk-73](figure/unnamed-chunk-73-1.png)





![plot of chunk unnamed-chunk-76](figure/unnamed-chunk-76-1.png)

## Manhattan plots






![plot of chunk unnamed-chunk-81](figure/unnamed-chunk-81-1.png)





![plot of chunk unnamed-chunk-84](figure/unnamed-chunk-84-1.png)

## Significant CpG sites

There were 3197
CpG sites with association p-values < 0.0032219.
These are listed in the file [associations.csv](associations.csv).



The following table shows overlaps between
associations under different sets of covariates:

|             | p.value.none| p.value.all|
|:------------|------------:|-----------:|
|p.value.none |         1829|        1032|
|p.value.all  |         1032|        2400|



Below are the 1
CpG sites with association p-values < 1.3925537 &times; 10<sup>-54</sup>
in the all regression model.


|           |chromosome | position| p.value.none| p.value.all| coefficient.none| coefficient.all|
|:----------|:----------|--------:|------------:|-----------:|----------------:|---------------:|
|cg05575921 |chr5       |   373378|            0|           0|       -0.2467402|      -0.2459214|

Plots of these sites follow, one for each covariate set.
"p[lm]" denotes the p-value obtained using a linear model
and "p[beta]" the p-value obtained using beta regression.




### CpG site cg05575921




![plot of chunk unnamed-chunk-92](figure/unnamed-chunk-92-1.png)



![plot of chunk unnamed-chunk-92](figure/unnamed-chunk-92-2.png)

## Selected CpG sites

Number of CpG sites selected: 1.


|           |chromosome | position| p.value.none| p.value.all| coefficient.none| coefficient.all|
|:----------|:----------|--------:|------------:|-----------:|----------------:|---------------:|
|cg05575921 |chr5       |   373378|            0|           0|       -0.2467402|      -0.2459214|




### CpG site cg05575921




![plot of chunk unnamed-chunk-101](figure/unnamed-chunk-101-1.png)



![plot of chunk unnamed-chunk-101](figure/unnamed-chunk-101-2.png)

## R session information


```
## R version 4.6.1 (2026-06-24)
## Platform: x86_64-pc-linux-gnu
## Running under: Ubuntu 24.04.5 LTS
## 
## Matrix products: default
## BLAS:   /usr/lib/x86_64-linux-gnu/openblas-pthread/libblas.so.3 
## LAPACK: /usr/lib/x86_64-linux-gnu/openblas-pthread/libopenblasp-r0.3.26.so;  LAPACK version 3.12.0
## 
## locale:
##  [1] LC_CTYPE=en_US.UTF-8       LC_NUMERIC=C              
##  [3] LC_TIME=en_US.UTF-8        LC_COLLATE=en_US.UTF-8    
##  [5] LC_MONETARY=en_US.UTF-8    LC_MESSAGES=en_US.UTF-8   
##  [7] LC_PAPER=en_US.UTF-8       LC_NAME=C                 
##  [9] LC_ADDRESS=C               LC_TELEPHONE=C            
## [11] LC_MEASUREMENT=en_US.UTF-8 LC_IDENTIFICATION=C       
## 
## time zone: Etc/UTC
## tzcode source: system (glibc)
## 
## attached base packages:
## [1] parallel  stats4    stats     graphics  grDevices utils     datasets 
## [8] methods   base     
## 
## other attached packages:
##  [1] meffil_1.6.0           preprocessCore_1.74.0  SmartSVA_0.1.3        
##  [4] RSpectra_0.16-2        isva_1.10              gdsfmt_1.48.2         
##  [7] statmod_1.5.2          quadprog_1.5-8         DNAcopy_1.86.0        
## [10] fastICA_1.2-8          lme4_2.1-0             Matrix_1.7-6          
## [13] multcomp_1.4-32        TH.data_1.1-5          survival_3.8-12       
## [16] mvtnorm_1.4-2          matrixStats_1.5.0      markdown_2.1          
## [19] gridExtra_2.3.1        Cairo_1.7-0            knitr_1.52            
## [22] reshape2_1.4.5         plyr_1.8.9             sva_3.60.0            
## [25] BiocParallel_1.46.0    genefilter_1.94.0      mgcv_1.9-4            
## [28] nlme_3.1-171           limma_3.68.5           sandwich_3.1-3        
## [31] lmtest_0.9-40          zoo_1.9-1              MASS_7.3-66           
## [34] illuminaio_0.54.0      tableone_0.13.2        ggplot2_4.0.4         
## [37] qqman_0.1.9            org.Hs.eg.db_3.23.1    AnnotationDbi_1.74.0  
## [40] IRanges_2.46.0         S4Vectors_0.50.3       clusterProfiler_4.20.3
## [43] ReactomePA_1.56.0      Biobase_2.72.0         BiocGenerics_0.58.1   
## [46] generics_0.1.4        
## 
## loaded via a namespace (and not attached):
##   [1] splines_4.6.1           pbdZMQ_0.3-14           ggplotify_0.1.4        
##   [4] tibble_3.3.1            polyclip_1.10-7         enrichit_0.2.7         
##   [7] graph_1.90.0            XML_3.99-0.25           lifecycle_1.0.5        
##  [10] httr2_1.3.0             Rdpack_2.6.6            edgeR_4.10.7           
##  [13] processx_3.9.0          lattice_0.23-1          base64_2.0.2           
##  [16] survey_4.5              magrittr_2.0.5          yaml_2.3.12            
##  [19] otel_0.2.0              ggtangle_0.1.5          askpass_1.2.1          
##  [22] minqa_1.2.8             DBI_1.3.0               RColorBrewer_1.1-3     
##  [25] purrr_1.2.2             ggraph_2.2.2            JADE_2.0-4             
##  [28] yulab.utils_0.2.5       tweenr_2.0.3            rappdirs_0.3.4         
##  [31] aisdk_1.4.12            labelled_2.16.1         gdtools_0.6.0          
##  [34] enrichplot_1.32.1       ggrepel_0.9.8           tidytree_0.4.9         
##  [37] reactome.db_1.96.0      annotate_1.90.0         codetools_0.2-20       
##  [40] DOSE_4.6.0              ggforce_0.5.0           tidyselect_1.2.1       
##  [43] aplot_0.3.2             farver_2.1.2            viridis_0.6.5          
##  [46] base64enc_0.1-6         Seqinfo_1.2.0           jsonlite_2.0.0         
##  [49] e1071_1.7-17            tidygraph_1.3.1         systemfonts_1.3.2      
##  [52] tools_4.6.1             ggnewscale_0.5.2        treeio_1.36.1          
##  [55] ragg_1.5.2              Rcpp_1.1.2              glue_1.8.1             
##  [58] xfun_0.62               qvalue_2.44.0           MatrixGenerics_1.24.0  
##  [61] IRdisplay_1.1           dplyr_1.2.1             withr_3.0.3            
##  [64] BiocManager_1.30.27     fastmap_1.2.0           mitools_2.7            
##  [67] boot_1.3-32             openssl_2.4.2           callr_3.8.0            
##  [70] digest_0.6.39           R6_2.6.1                gridGraphics_0.5-1     
##  [73] textshaping_1.0.5       GO.db_3.23.1            RSQLite_3.53.3         
##  [76] tidyr_1.3.2             calibrate_1.7.7         fontLiberation_0.1.0   
##  [79] class_7.3-24            graphlayouts_1.2.5      httr_1.4.9             
##  [82] htmlwidgets_1.6.4       scatterpie_0.2.6        graphite_1.58.0        
##  [85] pkgconfig_2.0.3         gtable_0.3.6            blob_1.3.0             
##  [88] S7_0.2.2                XVector_0.52.0          htmltools_0.5.9        
##  [91] fontBitstreamVera_0.1.1 clue_0.3-68             scales_1.4.0           
##  [94] png_0.1-9               reformulas_0.4.4        ggfun_0.2.2            
##  [97] uuid_1.2-2              nloptr_2.2.1            proxy_0.4-29           
## [100] repr_1.1.7              cachem_1.1.0            stringr_1.6.0          
## [103] pillar_1.11.1           grid_4.6.1              vctrs_0.7.3            
## [106] tidydr_0.0.7            xtable_1.8-4            cluster_2.1.8.3        
## [109] evaluate_1.0.5          cli_3.6.6               locfit_1.5-9.12        
## [112] compiler_4.6.1          rlang_1.3.0             crayon_1.5.3           
## [115] labeling_0.4.3          ps_1.9.3                forcats_1.0.1          
## [118] fs_2.1.0                ggiraph_0.9.6           stringi_1.8.9          
## [121] viridisLite_0.4.3       Biostrings_2.80.2       lazyeval_0.2.3         
## [124] GOSemSim_2.38.3         fontquiver_0.2.1        IRkernel_1.3.2         
## [127] hms_1.1.4               patchwork_1.3.2         bit64_4.8.6            
## [130] KEGGREST_1.52.2         haven_2.5.5             rbibutils_2.4.1        
## [133] igraph_2.3.4            memoise_2.0.1           ggtree_4.2.1           
## [136] bit_4.6.0               ape_5.8-1               gson_0.2.2
```
