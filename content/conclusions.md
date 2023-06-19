## Conclusions
{:#conclusions}

In this article, we discussed four approaches for the in-memory indexing of quoted triples,
ranging from very naive to highly optimized for quoted triple pattern access.

Our results show that the indexed quoted dictionary approach is orders of magnitude faster than other indexing approaches.
In the most extreme case, this approach is over 4.000 to 11.000 times faster than other indexing approaches
for a dataset size of 1 million with quoted triples at depth 5.
For smaller dataset sizes, lower quoted triple depths, and other types of queries, the difference becomes smaller.
This significant speedup at query time comes with the expected cost of increased storage size and ingestion time,
which is approximately two-fold for a large dataset.

As such, for use cases where quoted triple pattern queries occur at any depth,
and the storage size and ingestion time costs are acceptable,
the indexed quoted dictionary approach is highly beneficial for achieving good query performance.
Furthermore, given the fact that this approach stores quoted triple terms separate from all other terms inside the dictionary,
there is no significant overhead of using such a dictionary by default in triplestores,
even if the properties of datasets that are to be ingested are unknown beforehand.

In future work, there is a need to evaluate the performance of different indexing approaches over real-world data,
as we only evaluated performance over a custom generated dataset, which [does not capture the properties of the real-world](cite:cites duan2011apples).
Furthermore, we wish to evaluate the performance of these indexes within full SPARQL queries
by plugging them into [SPARQL query engines](cite:cites comunica).

In conclusion, the outcomes of this work show that the addition of the concept of quoted triples into the RDF and SPARQL recommendations
necessitates changes in triplestores in terms of indexing and dictionary encoding,
but that approaches such as the indexed quoted dictionary are able to provide very good performance,
while not requiring overly complicated additions implementation-wise.
