## Indexing Approaches
{:#approaches}

In this section, we introduce four approaches for indexing quoted triples.
The first approach is a naive approach based on traditional RDF indexing,
while the other two approaches are specifically designed for quoted triples.

Say that all approaches have hexastore-like structure in common, and only dict is different.
{:.todo}

### Singular Dictionary

Write me
{:.todo}

<figure id="figure-dict-singular">
<img src="img/dict-singular.svg" alt="[Singular Dictionary]" style="width: 50%">
<figcaption markdown="block">
Plain terms and quoted triples are stored inside the same dictionary.
</figcaption>
</figure>

### Quoted Triples Dictionary

Write me
{:.todo}

<figure id="figure-dict-quoted">
<img src="img/dict-quoted.svg" alt="[Quoted Triples Dictionary]">
<figcaption markdown="block">
Plain terms and quoted triples are stored in separate dictionaries.
</figcaption>
</figure>

### Referential Quoted Triples Dictionary

ALSO IMPLEMENT AND TEST THIS!
{:.todo}

Write me
{:.todo}

<figure id="figure-dict-quoted-referential">
<img src="img/dict-quoted-referential.svg" alt="[Referential Quoted Triples Dictionary]">
<figcaption markdown="block">
Plain terms and quoted triples are stored in separate dictionaries,
where quoted triples are recursively encoded using existing dictionary encodings.
</figcaption>
</figure>

### Indexed Referential Quoted Triples Dictionary

Write me
{:.todo}

<figure id="figure-dict-quoted-referential-indexed">
<img src="img/dict-quoted-referential-indexed.svg" alt="[Indexed Referential Quoted Triples Dictionary]">
<figcaption markdown="block">
Plain terms and quoted triples are stored in separate dictionaries,
where quoted triples are recursively encoded using existing dictionary encodings,
and indexed in a tree structure based on triple components.
</figcaption>
</figure>
