---
title: PhyloXML and NeXML
---

This action item came out of the pre-hackathon [Conference
Calls](Conference_Calls "wikilink"):

  
[Hilmar](Hilmar "wikilink") will contact the developers of NeXML and
PhyloXML to see if they have any suggestions/advice on visualizing
phylogenetic data using those formats, and what if any implementations
have already been built.

PhyloXML
--------

From: Christian M Zmasek <czmasek@sanfordburnham.org>  
Date: October 21, 2010 7:38:09 PM EDT

Hi, Hilmar and Rutger:

I am not entirely clear what you mean by phylogenetic data, but I guess
you mean data (potentially outside of the domain of "evolutionary
biology") associated with tree nodes and branches.

In any case, I think this is quite a challenging problem, especially for
user defined data types, such as by using phyloXML's property element
(http://www.phyloxml.org/documentation/version\_1.10/phyloxml.xsd.html\#h158033242)
and NeXML's triplets.

Clearly, it is straightforward to display this data as text (upon node
or branch clicking or mouse-over, for example); by way of example
"Km=0.1mM" (\*) in an application of phylogenetics in a study of enzyme
kinetics.

On the other hand, most of such associated data might be better
displayed in "graphical" form. For example, by mapping the Michaelis
constant Km to a range of colors. For this, we had the idea of something
like a "stylesheet" which, for example, says to represent gene
duplications as red circles, or provides a formula to convert Km values
to RGB colors. This is clearly not very well thought out and just at the
"idea" stage. (Cytoscape provides some functionality like that, e.g.
mapping of gene expression values to graph node colors).

(\*) in phyloXML:

`   `<property datatype="xsd:decimal" ref="Km" applies_to="node" unit="mM">  
`   0.1`  
`   `</property>

Chris

NeXML
-----

From: Rutger Vos <rutgeraldo@gmail.com>  
Date: October 22, 2010 5:34:38 AM EDT

Hi Chris and Hilmar,

I agree with Chris that the main issue is how to visualize annotations,
and whether a "visual language" could be devised/agreed upon to deal
with at least a subset of those annotations. In the context of this
conversation we've been having about a controlled vocabulary of
biological events on trees, you can imagine that some of these events
would have fairly obvious and intuitive icons (e.g. maybe an extinction
could be visualized as a little cross (as ToLWeb does)) or colour
mappings.

Rutger

Hilmar's Comments
-----------------

I was assuming at first that phylogenetic data meant the character
matrix (or alignment) data underlying trees, but interestingly both
Chris and Rutger interpreted this to mean data with which to decorate a
tree or an alignment, and then I wasn't actually sure anymore myself
what the intended meaning was. Whoever gave rise to that, any thoughts?
