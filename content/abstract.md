## Abstract
<!-- Context      -->
The upcoming RDF 1.2 recommendation is scheduled will introduce the concept of _quoted triples_,
which allows statements to be made about other statements.
<!-- Need         -->
Since quoted triples enable new forms of data access in SPARQL 1.2, in the form of _quoted triple patterns_,
there is a need for new indexing strategies that can efficiently handle these data access patterns.
<!-- Task         -->
As such, we explore and evaluate different in-memory indexing approaches for quoted triples.
<!-- Object       -->
In this paper, we investigate four indexing approaches,
and evaluate their performance over an artificial dataset with artificial triple pattern queries.
<!-- Findings     -->
Our findings show that the so-called *indexed quoted triples dictionary* vastly outperforms other approaches
in terms of query execution time at the cost of increased storage size and ingestion time.
<!-- Conclusion   -->
Our work shows that indexing quoted triples in a dictionary separate from non-quoted RDF terms achieves good performance,
and can be implemented using well-known indexing techniques into existing systems.
<!-- Perspectives -->
Therefore, we illustrate that the addition of quoted triples into the RDF stack can be achieved in a performant manner.
