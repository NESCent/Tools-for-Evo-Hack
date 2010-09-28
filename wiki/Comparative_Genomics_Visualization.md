---
title: Comparative Genomics Visualization
---

[GBrowse\_syn](gmod:GBrowse_syn "wikilink") is a popular GMOD component
for viewing comparative genomics data, particularly for viewing synteny
between genomes. It does not currently support the [next-generation
sequencing (NGS) data](gmod:Next_Generation_Sequencing "wikilink")
increasingly available for comparative genomics and emerging model
systems. Support for NGS data was identified by the EMS working group as
a high priority.

In particular, GBrowse\_syn lacks support for the [Sequence Alignment
Format (SAM)](http://samtools.sourceforge.net/), its mechanism of
storing genome comparisons does not scale beyond a few organisms, and
the means for tracking the necessary alignment metadata in
[Chado](gmod:Chado "wikilink") are insufficient.

In addition to filling those gaps, GBrowse\_syn would also particularly
stand to benefit from the event by gaining a more sustainable developer
base.
