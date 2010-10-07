---
title: Multiple Whole Genome Syntenic Analyses Visualization: identifying patterns of conservation and divergence across multiple whole genomes
---

Use case from [Eric](Eric "wikilink").

Motivation  

-   Many genomes coming online. Need interactive methods and tools to
    compare and visualize multiple whole genomes in order to identify
    patterns of conservation and divergence in the structure and
    evolution of multiple genomes. GBrowse\_syn (no my understanding),
    does not scale well to whole genomes.
    -   [Mauve](http://asap.ahabs.wisc.edu/mauve/index.php) scales well
        to multiple whole genome comparisons

Key Challenges  

-   Visualization: the visualization system must be able to identify:
    -   syntenic regions
    -   duplicated regions (segmental or whole genome)
    -   inverted regions
    -   translocations (chromosome fusion and fission events;
        translocation of chromosome segments)
    -   [Mauve](http://asap.ahabs.wisc.edu/mauve/index.php) is capable
        of displaying syntenic regions along with degree
        of conservation. Can also identify inverted regions, and
        relatively easily be hacked to identify translocations.
-   Possible visualization views
    -   Syntenic dotplots.
    -   Parallel line coordinates
    -   Circle View
    -   [Mauve](http://asap.ahabs.wisc.edu/mauve/index.php) can only
        display parallel line coordinates.
-   Useful system with working examples
    -   [SyMap](http://symapdb.org): Demonstrates all viewpoints

Preconditions for Use:  

-   Pairwise putative homologous gene sets between all query species
    -   These data would likely be housed in the GMOD installation and
        not submitted by the user

User Steps  

-   User selects:
    -   genomes or genomic regions to visualize
        -   organisms of interest
        -   gene of interest by name
        -   gene of interest by sequence
    -   type of visualization

Results  

-   Interactions by user with visualizations
    -   scaling (zoom in/out)
    -   change view types

References (optional)  

-   [SyMap](http://symapdb.org): [Soderlund C. et al. SyMAP: a system
    for discovering and viewing syntenic regions of FPC maps.
    Genome Res.
    2006;16:1159-1168.](http://bioinformatics.oxfordjournals.org/cgi/ijlink?linkType=ABST&journalCode=genome&resid=16/9/1159)

[Category:Use Cases](Category:Use_Cases "wikilink")
