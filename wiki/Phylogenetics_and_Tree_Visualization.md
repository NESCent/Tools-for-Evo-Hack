---
title: Phylogenetics and Tree Visualization
---

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
