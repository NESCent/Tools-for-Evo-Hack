---
title: Front end for Chado Natural Diversity
---

(started by [Vladimir](User:Vg34 "wikilink"))

**The idea**: A front-end application for managing data persisted in a
Chado NatDiv schema.

Motivation
----------

Many scientists who collect data that could be persisted in Chado NatDiv
use ad hoc solutions for maintaining these data, such as combination of
spreadsheets and files/directories with a certain naming convention.
Existence of the Chado NatDiv schema alone does not help many of these
scientists, due to (1) fairly specialized expertise needed to install an
RDB and a Chado NatDiv schema in it and (2) lack of a user-friendly
front end to Chado NatDiv.

Preconditions for use
---------------------

The user starts a new project that collects natural diversity data or
already has a data collection maintained in a "legacy" ad hoc system.

User steps
----------

(or, **Desired Features**)

-   Set up a new database to keep track of data for a new natural
    diversity project and customize it (with suitable controlled
    vocabularies, etc.) for the specific needs of this project.
-   Enter, maintain, and browse the data.
-   Import data in bulk from an existing collection, if available in a
    reasonable format.
-   Pull subsets of the data out in formats suitable for
    analysis software.

Concrete examples
-----------------

### Association Mapping in Populus

This is from a NESCent working group on Emerging Model Systems. (Polulus
is apparently the plural of Poplar, the tree.)
--[Vladimir](User:Vg34 "wikilink")

1.  I have genotyped several hundred trees for several thousand SNPs. I
    established four clonally replicated field trials for the same
    genotypes located in a north to south cline. Multiple clones of each
    genotype are included in each field trial. Each clone has been
    measured for three different phenotypic traits, wood chemistry, leaf
    shape, and height.
2.  I would like to be able to record information about each genotype,
    including pedigree information (if known), the geographic location
    the genotype was collected, and information about why the genotype
    was collected.
3.  I would like to see the SNP markers as a track, compared to the
    reference genome. I would like to see either SNPs for a specific
    individual, or else see a pile up of SNPs for all individuals.
4.  I would like to be able to enter GPS location for the field sites,
    and also for individual trees. Would be great to be able to view
    this like google maps.
5.  It will be very important to be able to record environmental data
    over time for each site. This might include data collected by
    automated measuring devices in real time.
6.  I would like to see phenotypic measurements for each individual
    clone displayed as either raw data (e.g. quantitative measurement
    for wood chemistry, or an image for leaf shape), or as mean/standard
    deviation for a genotype (or family or some other grouping…perhaps
    allow user to specify what genotypes).
7.  I would like to be able to make comparisons and analysis including…
    what is the phenotypic mean for individuals with a specific SNP,
    what is the phenotypic mean for all individuals on each site, what
    is the frequency of SNPs at a given locus for specific
    individuals (e.g. comparing trees at the phenotypic extremes), which
    genotypes had the best performance at an individual site or
    across sites.
8.  Would like to be able to analyze genotype/phenotype associations,
    effect of Genotype x Environment, population structure.

### Population Genetics features requested by EMS

This is a more abstracted list of features requested by the Emerging
Model Systems working group at NESCent. Some of these go beyond the
scope of the "NatDiv front end" usecase per se, but could be useful for
context. --[Vladimir](User:Vg34 "wikilink")

-   **Samples:** ability to track of large numbers of samples
    -   individual sample number
    -   phenotypic scores (morphological, developmental, genetic, etc)
    -   field location (GPS location or field site for
        natural populations)
    -   environmental conditions (additional descriptive field data)
    -   genetic cross (cross, generation, etc)
-   **Genetic Maps:** ability to view genome sequences (physical map)
    and linkage map (genetic map).
-   **Genetic Markers:** Markers for population genetics vary from SNPs
    anchored to a reference genome, to isozymes or other markers that
    may not even be genetically mapped. Need to be able to record basic
    information about what a given marker represents, and would be
    desirable to be able to summarize core statistics about a given
    marker for a given population.
-   **Geographic Maps:** Be able to view location of sample collections
    and field sites, like with google maps. Perhaps ability to overlay
    environmental information would be desirable? UC Berkeley’s Museum
    of Vertebrate Zoology has been creating a GIS-based system in which
    to search and map museum specimens in a geographic context.
-   **Comparative analyses:** ability to compare new genome (or
    genome sequences) to other annotated sequences already
    publicly available.
-   **QTL mapping:** ability to keep track of genotypes and phenotypes
    (from crossing experiments), which can then be imported into common
    QTL mapping software.
-   **Association studies:** ability to keep track of genotypes and
    phenotypes (from natural populations), which can then be important
    into standard statistical packages.

Notes: The Mimulus database serves as a good starting point for our
Population Genomics needs.

### Genetic connectivity between coastal marine communities

This sketches the needs of Shane Lavery from University of Auckland in
New Zealand, who was a NESCent short-term visitor in Spring 2010.
--[Vladimir](User:Vg34 "wikilink")

-   This is a study of genetic connectivity between New Zealand coastal
    marine communities. It involves analysis of data from previously
    published studies, which traditionally considered only
    single-species genetic connectivity. The existing data is
    constituted of allele/loci frequencies associated with various
    populations, as well as accompanying data about various
    characteristics of the populations and experimental conditions.
    Newer studies also often make available the mtDNA sequences of
    individuals that were sampled to measure the frequencies. There are
    about 40-50 published studies of this kind that are available.
-   What's needed is suitable organization, techniques, and tools for
    collating and managing this existing data in order to facilitate
    their exploration and analysis in his study. In particular, it would
    be useful to support visualization of geographic locations of
    sampling sites on a map across species.

Key Challenges
--------------

(from the point of view of making work on this usecase *feasible at this
hackathon*)

-   Have 2-3 real datasets at hand to use for evaluation and testing
    during development.
-   Identify an existing Chado front end that could naturally be
    extended to support the NatDiv module or identify a suitable front
    end technology for implementing the NatDiv front end from scratch.
-   Availability of a server machine to install development instances.
-   Someone with a better (than the initiator of this usecase)
    understanding of the biological and informatics aspects of this
    usecase to take charge. These can be two different people, though.

Possibly-relevant software
--------------------------

-   [Tripal](http://gmod.org/wiki/Tripal) - a Chado front end
    implemented in [Drupal](http://drupal.org/), a popular framework for
    implementing web-based content management.
-   [XORT](http://gmod.org/wiki/Xort) - a GMOD tool for interchange of
    data between relational schemas (in particular, Chado), via an
    XML representation.

