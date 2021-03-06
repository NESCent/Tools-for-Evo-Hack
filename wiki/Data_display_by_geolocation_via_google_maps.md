---
title: Data display by geolocation via google maps
---

use case by [seth](seth "wikilink")

Motivation  

With the addition of the geolocation tables to the ND natural Diversity
Module it is envisaged that researchers from a variety of fields (no pun
intended) will want to display data in reference to the location in
which a survey / experiment was carried out.

Key Challenges  

1.  Requirements
    -   what kind of data can it display? can everything be reduced to:
        1.  coloured pushpins (i.e. Anopheles gambiae found here = green
            dot, arabiensis here = yellow dot, stephensi = blue dot)
        2.  or a two-colour scale (% of major v minor allele found in
            these location)
    -   how scalable is the data? and is it desirable to take steps to
        limit \# of sites displayed for the sake of speed?

<!-- -->

1.  Implementation
    -   it is presumed the system would use the Google Maps API, or
        something similar in order to display the data - does this have
        the flexibility we would need?
    -   If we decide to pursue this we could have a server set up to
        feed simple json classes from the natdiv database.
        -   would this be flexible enough to allow further development
            after the hackathon?
        -   is an alternative to json preferable?

Preconditions for Use:  

-   geolocations to be stored in ND geolocation tables
-   values to be plotted taken from either:
    -   phenotype module
    -   genotype module
    -   stock prop
-   and directly related to
    -   stock

User Steps  

-   e.g. show frequencies of 2La / 2L+ inversions for all samples
    in cameroon.
-   e.g. show locations for all samplings in project X
-   + others (please add your own)

Results  

-   map with pins for binary values / heatmaps for real no.s

[Category:Use Cases](Category:Use_Cases "wikilink")
