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

[^1]Reported in 2009 as Ciona intestinalis.

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

In general required reactives to extaction are described in the following Table[^2]:
<p align="center">
  <img width="560" height="300" src="https://github.com/cavelandiah/tunicata_miRNA_seq/blob/master/Figures/lysysprices.png?raw=true">
</p>

[^2] Data from [Exiqon](http://www.exiqon.com/small-rna-ngs)

#### Library preparation and Sequencing

|Requirement(s)|Recommended[^2]|MN kit|Suggested FD|
|-------------:|----------:|-----:|-----------:|
| Expected output | 15-30 nt reads (miRNA-Lib) or 30-200 nt (smallRNA libs)| NA | NA |
| Library construction | 1 x 50 bp, Single End, 7.5 M reads | NA | NA |
| Expected time | After QC, 6 weeks | NA | NA |


Most of the options are Illumina based. Illumina offer the MiniSeq Small RNA-Seq Workflow (takes about $$\sim 1.3$$ days), that includes Library construction, sequencing and analysis of data. For Library construction, they offer the TrueSeq Small RNA Library Prep Kit (G), which have up to $48$ individual indexes. The idea is to multiplex all the possible sequences using those indexes and pool the read from different biiological experiments in the same lane. After that they offer a MiniSeq High/Mid Output Kit (H).  

In this case they offer the machine and obviosly it is completely expensive for
our objectives, for that reason I have to look for a NGS services. There is lot
of options based on user request, but for our idea, I considered the following
hypothetical set-up to request the quotes:
	*Number of species = 3;
	*Replicates (Biological/technical) = 2/2;
	*Total number of samples for specie = $4$.
	*Insert size = $18-25$ bp.
	*Libraries: Single End ($1 \times 50$ bp) OR ($1 \times 75$ bp).
