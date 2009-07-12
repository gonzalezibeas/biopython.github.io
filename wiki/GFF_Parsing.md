---
title: GFF Parsing
permalink: wiki/GFF_Parsing
layout: wiki
---

GFF Parsing
===========

*Note:* GFF parsing is not yet integrated into Biopython. This
documentation is work towards making it ready for inclusion. You can
retrieve the current version of the GFF parser from:
<http://github.com/chapmanb/bcbb/tree/master/gff>. Comments are very
welcome.

Generic Feature Format (GFF) is a biological sequence file format for
representing features and annotations on sequences. It is a tab
delimited format, making it accessible to biologists and editable in
text editors and spreadsheet programs. It is also well defined and can
be parsed via automated programs. GFF files are available from many of
the large sequencing and annotation centers. The
[specification](http://www.sequenceontology.org/gff3.shtml) provides
full details on the format and its uses.

Biopython provides a full featured GFF parser which will handle several
versions of GFF: GFF3, GFF2, and GTF. It supports writing GFF3, the
latest version.

GFF parsing differs from parsing other file formats like GenBank or PDB
in that it is not record oriented. In a GenBank file, sequences are
broken into discrete parts which can be parsed as a whole. In contrast,
GFF is a line oriented format with support for nesting features. GFF is
also commonly used to store only biological features, and not the
primary sequence.

These differences have some consequences in how you will deal with GFF:

-   Files are first examined to determine available annotations and
    define items of interest.
-   Sequences will often be parsed separately, from an associated
    FASTA file.
-   Parsing needs to consider available memory, which can be quickly
    used up on files with many annotations. This problem can be solved
    via two methods:
    -   Limiting parsing to features of interest.
    -   Iterating over portions of the file.

The documentation below provides a practical guide to examining, parsing
and writing GFF files in Python.

Examining your GFF file
-----------------------

GFF Parsing
-----------

### Basic GFF parsing

### Providing initial sequence records

### Limiting parsed lines

### Iterating over portions of a file

Writing GFF3
------------