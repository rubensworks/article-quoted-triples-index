## Related Work
{:#related-work}

Given the recent introduction of RDF-star and the concept of quoted triples,
scientific literature on making use of it is limited.
First, [several use cases](cite:cites kasenchak2021use, solidsignedrdfstar) have been explored using quoted triples.
Furthermore, a declarative language called [*RML-star*](cite:cites rmlstar) has been introduced that allows
heterogeneous datasources such as CSV and JSON to be mapped into RDF datasets containing quoted triples.
This language is an extension of the [RML language](cite:cites rml),
and has been implemented in [Morph-KGCstar](cite:cites morphkgcstar).
Similarly, [RSP-QL*](cite:cites rspqlstar) was introduced as an extension to the
[RSP-QL model](cite:cites rspql) for RDF Stream Processing to support quoted triples.
Finally, [two approaches](cite:cites transformingrdfstarpropgraphs) are identified to transform RDF datasets
containing quoted triples into a [property graphs model](cite:cites propertygraphs).

RDF-star is seeing wide adoption among SPARQL implementations,
for which a full list of implementations that adhere to the RDF-star community group specification can be found in
[](cite:cites rdfstarimplementations).
Unfortunately, none of these approaches clearly document their storage and indexing approach,
which motivates the need for this article on comparing various indexing techniques.
