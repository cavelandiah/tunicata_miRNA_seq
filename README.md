# tunicata_miRNA_seq

## (mi|\*)RNA-seq Project on Tunicates

### Context

The current state of _miRNAs-seq_ proyects along tunicates is described in the
following Table:

| Specie   |   Reference(s)   | Method  | Project(s) Accession Number | Samples |
|----------|:----------------:|--------------------:|--------------------:|--------:|
| _Oikopleura dioica_ | [Fu _et al._; 2008](https://academic.oup.com/mbe/article/25/6/1067/1131173) | Cloned miRNAs|NA| NA|
| _Ciona intestinalis_[^1] | [Shi _et al_., 2009](https://www.nature.com/articles/nsmb.1536) | Illumina sequencing |  [GSE13625](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE13625)| GSM343282, GSM343283, GSM343284 , GSM343285, GSM343286, GSM343287 (Drosophila Toll 10b mutant embryos) |
| _Halocynthia roretzi_ | [Wang _et al_., 2017 ](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-3707-5) | Computational Pred, Mapping _Ciona robusta_ RNA-Seqs (SRR038843, SRR038844, 26 nt) | NA | [GSE21078](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM526915) (small RNA sequencing of two developmental stages of _C. intestinalis_. Public on Mar 27, 2010)|
|_C. robusta_| [Spina _et al_.,2017](http://dev.biologists.org/content/144/10/1787.long) | Ion Torrent Seq | [GSE84837](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE84837) | GSE84836 |
| _Ciona savignyi_ | [Zhang _et al_.,2018](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-4566-4)| Illumina Hiseq | NA | NA | 
| _Salpa thompsoni_ | [Jue _et al_.,2016](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5174732/pdf/evw215.pdf) | Illumina HiSeq 2000| [SRP073811](https://www.ncbi.nlm.nih.gov/Traces/study/?uids=2470099%2C2470098%2C2470097) | SRR3438441, SRR3438440, SRR3438439 |   

[^1]: Reported in 2009 as Ciona intestinalis.

At the same time, current phylogenetic distribution of 16 sequenced tunicates genomes is described as follows:
<p align="center">
  <img width="860" height="500" src="https://github.com/cavelandiah/tunicata_miRNA_seq/blob/master/Figures/treeTunicata.png?raw=true">
</p>

Thus, current set of miRNA-Seq data belongs from solitary tunicates + _S. thompsoni_. The ongoing computational analysis take advantage from these data to find new miRNA families. A current mapping strategy was performed on [Wang _et al_., 2017 ](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-017-3707-5), where authors mapped both miRNA-seq raw reads to the _H. roretzi_ genome, but the criteria annotating the _mature_ and _hairpin_ sequences were too strict and more biased to computational parameters. But the question about the biological realibility remains, focused on the problem to find miRNAs from solitary tuncates and map them on colonial genomes (?).

In this context, we should select a number of species _x_ to extract RNA and build smallRNA-specific libraries to have better representation of data along the Tunicata clade. 

### Experimental design


#### RNA extraction
Based on requested quotes and collected information, the initial set-up for extract RNA for each genome is:

|Requirement(s)|Recommended[^2]|MN kit|Suggested FD|
|-------------:|----------:|-----:|-----------:|
| Collection time | ? | NA | NA |
| Minimum quantity of RNA | 260 ng (160 ng (Seq + QC))| NA | NA |
| Expected time | After QC, 6 weeks | NA | NA |

In general required reactives to extaction are described in the following Table [^2]:
<p align="center">
  <img width="560" height="300" src="https://github.com/cavelandiah/tunicata_miRNA_seq/blob/master/Figures/lysysprices.png?raw=true">
</p>

[^2]: Data from [Exiqon](http://www.exiqon.com/small-rna-ngs)

#### Library preparation and Sequencing

In particular, there is a hypothetical set-up of the experiment that have to be defined before:
	
	*Number of species: _x_
	*Replicates: **0**
	*Number of samples by specie: **4**
	*Libraries: Single End: 1x50 or 1 x 75 bp.
	*Sequencing: NextSeq 500, HiSeq 4000

The idea is to multiplex all the possible sequences using indexes and pool the reads from different species at the same lane. 


An overview of the required quotes calculated for 1 specie with 2 biological replicas and 2 technical replicas is described as follows:

<p align="center">
  <img width="300" height="560" src="https://github.com/cavelandiah/tunicata_miRNA_seq/blob/master/Figures/quoteSeqsmiRNAs.png?raw=true">
</p>

