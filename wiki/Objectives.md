---
title: Objectives
---

Organizers have identified the following broad themes for focusing work
at the event. Before and at the hackathon, the participants will refine
and distill these and other options into concrete implementation
targets. The participants will develop criteria for prioritization, such
as maturity of a target for implementation, availability of test data,
and potential for completing or making significant progress towards the
target during the hackathon. Further ideas and discussion topics can be
found on the [ Supplemental Information
](gmod:GMOD_Evo_Hackathon_Proposal_Supplemental_Information "wikilink")
page.

Viewing tools for comparative genomics data
-------------------------------------------

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

Visualization of phylogenetic data and trees
--------------------------------------------

The [GMOD toolkit](gmod:GMOD_Components "wikilink") at present does not
include web-based alignment viewers, nor can the increasingly popular
[JBrowse](gmod:JBrowse "wikilink") genome browser (the designated
successor of [GBrowse](gmod:GBrowse "wikilink")) display multiple
sequence alignments. GMOD also lacks a phylogenetic tree widget.

Implementing these from scratch would be far beyond a suitable hackathon
target. However, [SGN](http://solgenomics.net) has a relatively mature
[web-based multiple alignment and tree
browser](http://solgenomics.net/tools/align_viewer/) that could be
extracted from SGN's codebase and transformed into a GMOD component, an
add-on for JBrowse. Current Java-based tree viewers (such as
[Archaeopteryx](http://www.phylosoft.org/atv/) or
[PhyloWidget](http://www.phylowidget.org)) could be used as the basis
for a JavaScript-based tree viewer (or an applet that can be controlled
through JavaScript) that integrates with JBrowse.

Population Diversity and Phenotype support
------------------------------------------

GMOD's capabilities in managing phenotype and natural diversity data is
scattered across partially redundant and outdated modules, does not
support modern ontology-based entity-quality data, and lacks a
web-interface. The sophisticated phenotype annotation tools that do
exist cannot interface with Chado, GMOD's central relational data model.
Yet, phenotypic and genetic diversity data are central to many
evolutionary research questions.

A [Natural Diversity Module
initiative](gmod:Chado_Natural_Diversity_Module_Working_Group "wikilink")
to address at least the deficiencies within Chado has already formed
earlier this year. Several key developers (one of the original
developers of the module, and the developer of Phenex, a phenotype
curation tool) are already local to NESCent, and so the hackathon
provides a unique opportunity to review and refine the natural diversity
data model face-to-face, and to integrate it with an updated and
reconciled phenotype module. A recently reported prototype of a Chado
data adapter for Phenote, GMODs phenotype annotation tool, could be
generalized to become the data persistence interface for such data.

Aside from the data model deficiencies, the
[ANISEED](http://aniseed-ibdm.univ-mrs.fr/) project has started efforts
to generalize its sophisticated atlas/image-based web interface for
phenotype data, and to make it operate on top of Chado. The hackathon
could harness this synergy to help this effort leap forward, which could
ultimately provide GMOD with the currently missing web-interface for
such data.
