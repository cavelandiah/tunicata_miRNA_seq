# tunicata_miRNA_seq
(mi|\*)RNA-seq Project on Tunicates

The current state of _miRNAs-seq_ proyects along tunicates is described in the
following Table:

| Specie   |   Reference(s)   | Method  | Project(s) Accession Number | Samples |
|----------|:----------------:|--------------------:|--------------------:|--------:|
| _Oikopleura dioica_ | [Fu _et al._; 2008](https://academic.oup.com/mbe/article/25/6/1067/1131173) | Cloned miRNAs|NA| NA|
| _Ciona intestinalis_\* | [Shi _et al_., 2009](https://www.nature.com/articles/nsmb.1536) | Illumina sequencing |  [GSE13625](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE13625)| GSM343282, GSM343283, GSM343284 , GSM343285, GSM343286, GSM343287 (Drosophila Toll 10b mutant embryos) |
| _Halocynthia roretzi_ | [Wang _et al_., 2017 ](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-3707-5) | Computational Pred, Mapping _Ciona robusta_ RNA-Seqs (SRR038843, SRR038844, 26 nt) | NA | [GSE21078](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM526915) (small RNA sequencing of two developmental stages of _C. intestinalis_. Public on Mar 27, 2010)|
|_C. robusta_| [Spina _et al_.,2017](http://dev.biologists.org/content/144/10/1787.long) | Ion Torrent Seq | [GSE84837](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE84837) | GSE84836 |
| _Ciona savignyi_ | [Zhang _et al_.,2018](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-4566-4)| Illumina Hiseq | NA | NA | 
| _Salpa thompsoni_ | [Jue _et al_.,2016](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5174732/pdf/evw215.pdf) | Illumina HiSeq 2000| [SRP073811](https://www.ncbi.nlm.nih.gov/Traces/study/?uids=2470099%2C2470098%2C2470097) | SRR3438441, SRR3438440, SRR3438439 |   
\*Reported in 2009 as Ciona intestinalis.

At the same time, current phylogenetic distribution of 16 sequenced tunicates genomes is described as follows:
<p align="center">
  <img width="660" height="500" src="https://github.com/cavelandiah/tunicata_miRNA_seq/blob/master/Figures/treeTunicata.png?raw=true">
</p>

Thus, current set of miRNA-Seq data belongs from solitary tunicates + _S. thompsoni_. The ongoing computational analysis take advantage from these data to find new miRNA families. A current mapping strategy was performed on [Wang _et al_., 2017 ](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-3707-5)], where authors mapped both miRNA-seq raw reads to the _H. roretzi_ genome, but the criteria annotating the _mature_ and _hairpin_ sequences were too strict and more biased to computational parameters.
