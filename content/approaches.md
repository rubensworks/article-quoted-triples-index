## Indexing Approaches
{:#approaches}

In this section, we introduce four approaches for indexing quoted triples,
with increasing levels of complexity.
These approaches build upon the well-established method of storing triples in different orders
and using dictionary encoding as explained in [](#background).
Our approaches only rely on changes within the dictionary mechanism,
while the triple index itself remain unchanged.

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
