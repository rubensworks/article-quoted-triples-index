## Indexing Approaches
{:#approaches}

In this section, we introduce four approaches for indexing quoted triples,
with increasing levels of complexity.
These approaches build upon the well-established method of storing triples in different orders
and using dictionary encoding as explained in [](#background).
Our approaches only rely on changes within the dictionary mechanism,
while the triple index itself remain unchanged.

### Singular Dictionary

A straightforward way to achieve dictionary encoding of quoted triples,
is to include quoted triples directly inside the dictionary of all other RDF terms.
As such, quoted triples are handled in exactly the same manner as other RDF term types.
For dictionaries that map strings to integers, this requires a mechanism to convert quoted triples into strings.
[](#figure-dict-singular) shows an example of such dictionary contents based on our use case data.

<figure id="figure-dict-singular">
<img src="img/dict-singular.svg" alt="[Singular Dictionary]" style="width: 50%">
<figcaption markdown="block">
Plain terms and quoted triples are stored inside the same dictionary.
</figcaption>
</figure>

Executing triple pattern queries is identical to the baseline approach as explain in [](#background),
except for triple patterns containing quoted variables, such as the query `?person :says <<Violets haveColor ?color>>`.
As this approach has no direct way of matching the `?color` variable to quoted triples,
we are required to convert quoted triple patterns containing variables to variables,
and perform a post-processing step to only emit those triples that match the quoted triple pattern.
The pseudo-code of this algorithm is shown in [](#algorithm-query-dict-singular).

<figure id="algorithm-query-dict-singular" class="algorithm">
````/algorithms/query-dict-singular.txt````
<figcaption markdown="block">
Pseudocode of the algorithm for executing triple pattern queries using a singular dictionary.
</figcaption>
</figure>

The main advantage of this approach lies in its simplicity of implementation.
However, there are two main disadvantages:

1. Storage overhead: Quoted triples with shared terms lead to a storage overhead, such as the duplicate storage of `:Violets` and `:haveColor` in [](#figure-dict-singular).
2. Lack of quoted triple pattern index: When executing triple pattern queries with quoted variables, there is no indexed access to matching quoted triples, which can lead to query performance issues.

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
