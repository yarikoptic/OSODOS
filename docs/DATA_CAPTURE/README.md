
This module will show you ways to ensure that capturing data operations will produce reliable records
=====================================================================================================

Capturing data in a laboratory is a daily operation that easily falls in routine chores. Something 
that can be a way to pile-up habits, both good and bad. Good data capture habits result in organised 
datasets in which one can find the means to reconstruct the capture itself, identify the instruments 
that were used, the reactants, the people intervening, etc. For a scientist, even if working alone, 
good datasets are an assurance that his/her attitude towards a rigorous relationship with the experiments 
started correctly. To the questions who, where, when and how (WWWH) did you get your data, one can exect to be 
able to answer unequivocally. 

It is relatively easy to produce and accumulate bad records and store bad datasets that have little 
or zero scientific value. Apparently good practices like keeping a lab-book, usually mandatory nowadays, 
are NOT a guarantee that experiments are properly recorded into datasets that allow anyone, including
the original researcher, to fully address the WWWH questions, to start with. For example, a bad habit 
that apparently looks good is to record data in spreadsheets, occasionally print parts of spreadsheets on 
paper and glue tables in the lab-book. Easily the WWWH questions become unanswerable, the content of such a 
table becomes artificially dependent from other recorded information in the lab-book but it easily detaches 
from it with a simple annotation mistake. Highly dangerous, yet quite common practice. Worse than just 
being bad, it can "look" good, misleadingly!

In Data Science, the the WWWH question is usually referred to as **provenance**. Provenance in data is tied 
not only to the Data Collection act but also to the its futher movements between databases. 

Provenance may or not entail ownership and licensing of its use. If the appropriate steps, as will be explained below, 
are taken, authenticated provenance implies authorship. 

When Data Collection is performed via a service of some kind, such as the work from a Core Facility or Analytics 
provider, even more care must be put into fully describing the provenance. The reliability of a good provider is
measurable, as described in the REPRODUCIBILTY part of this course. This should not be confused with the reliability of 
a specific set of measurements. Here the evaluation of data quality should be intrinsic to each dataset, and taken into 
consideration in the analytical steps that follow.

For example, in a sequencing project, the final preparation of the samples and the actual running of the sequencing 
job is not usually in the hands of the experimentalist, and is handled by service personnel in a facility. The results 
of a sequencing run are usually handed to the requester via a usually large amount of files, either in a folder deposited 
in a server or in a hard disk that can be shipped. Either way care is taken to use standardised formats and keep data 
integrity. The fist thing that the experimenter should do is assess data quality and decide on a strategy to accept or
rejecty records and to clean-up the artifacts. In sequencing data, whichever instrumental platform is used, data quality 
will not be uniform and tends to be worse at least at the end of each read. This is the result of a natural penomenon 
that is tied to the measurement process. So, removing the tails of the reads, as much as removing traces from sequencing 
adaptors, for example, is a normal task that lies in the hands of the experimentalist.

Data from a sequencing run can be inspected with a widely used public tool called [FastQC] 
(https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) produced at the Babraham Institute, Cambridge, UK


<a name="FastQC1"></a>
![A very good dataset can look like this:](fastqc1.png)

<a name="FastQC2"></a>
![A very bad dataset can look like this:](fastqc2.png)

A program like FastQC can look at the dataset from a varietey of different perspectives, other than the above quality score 
and allows the experimenter to find support fro accepting or rejecting a dataset and also to diagnose possible sources of
disturbance, figuring out strategies to clean it up and checking for the effectiveness of such clean-up processes.

The above example shows an instance of data capture where, because we have large datasets in hands, a statistical assessment
of quality may be comfortable or easy to perform. Also, this step in the provenance comes from a single machine, run by
an identifiable team of professionals that, in principle, checks the ientire service provision regularly for the quality
of the service itself. That is obvously not the case if we are dealing with field work, for example, where sample are collected 
by human agents that we barely know, over a large geographical area in a long period. It is very different if samples travel 
at different times and via different routes. It is very different if samples are measured with different instruments with 
different checking and calibrtation routines. In such cases, finding commonality is an issue, uncontrollable sources of variation 
in measurements can occur, even if we are only measuring weight with a scale or length with a ruler!

I cooperative work, the need for adoption of standards and formats is even higher and simple things like the reliable time 
stamping of the datasets can serously compromise the accreditation of datasets. Likewise, as the result of serious efforts in 
standardisation, consortia have worked on the definition of stanadrdised ways of describing experiments, and managed to reduce 
their summarised information to minimum sets of descriptors. Here are some examples:

[Minimum information about a microarray experiment (MIAME)] (https://www.nature.com/ng/journal/v29/n4/pdf/ng1201-365.pdf)
[The minimum information about a proteomics experiment (MIAPE)] (https://www.nature.com/nbt/journal/v25/n8/pdf/nbt1329.pdf)


[Data Provenance: Some Basic Issues] (http://db.cis.upenn.edu/DL/fsttcs.pdf)
