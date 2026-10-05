# NeonDisco Transcript Level Data Schema

## Column Definitions

| Column Name | Data Type | Example Value | Notes |
|-------------|-----------|---------------|-------|
| fusionTranscriptID | string | "TRMT11::SMG6__6:125986622-17:2244719" | Unique identifier for fusion transcript |
| fusionGenePair | string | "TRMT11::SMG6" | Gene pair involved in fusion |
| breakpointID | string | "6:125986622-17:2244719" | Genomic coordinates of breakpoint |
| 5pStrand | string | "+" | Strand orientation of 5' partner |
| 3pStrand | string | "-" | Strand orientation of 3' partner |
| detectedBy | string | "Arriba | STARFusion" | Tools used for detection |
| toolOverlapCount | integer | 2 | Number of tools that detected the fusion |
| sampleID | string | "1T" | Sample identifier |
| sampleNum | integer | 1 | Sample number |
| sampleNum_Padded | string | "0001" | Zero-padded sample number |
| predictedEffect_ARR | string | "CDS/splice-site__CDS/splice-site" | Predicted effect of fusion (ARR format) |
| mutationType_ARR | string | "translocation" | Mutation type (ARR format) |
| confidenceLabel_ARR | string | "high" | Confidence level of prediction (ARR format) |
| readingFrame_ARR | string | "in-frame" | Reading frame status (ARR format) |
| splitReadsTotal_ARR | string | 2 | Total split reads (ARR format) |
| discordantReadPairs_ARR | string | 0 | Discordant read pairs (ARR format) |
| filteredReads_ARR | string | "NA" | Filtered reads information (ARR format) |
| peptideSequence_ARR | string | "ALSCTLNRYLLLMAQEHLEFRLP|LNKRFILSFLHAHGKLFTRIGMETFPAV" | Peptide sequence data (ARR format) |
| predictedEffect_FC | string | "NA" | Predicted effect of fusion (FC format) |
| fusionPairAnnotation_FC | string | "NA" | Fusion pair annotation (FC format) |
| splitReadsTotal_FC | string | "NA" | Total split reads (FC format) |
| discordantReadPairs_FC | string | "NA" | Discordant read pairs (FC format) |
| longestAnchor_FC | string | "NA" | Longest anchor information (FC format) |
| breakpointSpliceType_SF | string | "ONLY_REF_SPLICE" | Breakpoint splice type (SF format) |
| fusionPairAnnotation_SF | string | "\"[\"\"SMG6:Oncogene\"\"];INTERCHROMOSOMAL[chr6--chr17]\"" | Fusion pair annotation (SF format) |
| splitReadsTotal_SF | string | 2 | Total split reads (SF format) |
| discordantReadPairs_SF | string | 0 | Discordant read pairs (SF format) |
| largeAnchorSupport_SF | string | "YES_LDAS" | Large anchor support status (SF format) |
| FFPM_SF | string | 14.7237 | Fragments Per Million (SF format) |
| foundInCCLE&InternalCLs | boolean | false | Found in CCLE and internal cell lines |
| foundInGaoTCGARecurrent | boolean | false | Found in Gao TCGA recurrent fusions |
| foundInMitelmanCancerFusions | boolean | false | Found in Mitelman cancer fusions |
| foundInKlijnCancerCellLineFusions | boolean | false | Found in Klijn cancer cell line fusions |
| GenePairforFusInspector | string | "TRMT11--SMG6" | Gene pair for FusInspector tool |

## Notes
- This is a transcript-level fusion data dataset from the NeonDisco project
- Many columns appear to be formatted using three different annotation systems (ARR, FC, SF) which may represent different data formats or experimental conditions
- Several columns contain repeated information in multiple formats, with many 'NA' values
- The data appears to be from BRCA cancer research focusing on fusion transcripts