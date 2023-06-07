## Abstract
<!-- Context      -->
The upcoming RDF 1.2 recommendation will introduce the concept of _quoted triples_,
which allows statements to be made about other statements.
<!-- Need         -->
Since quoted triples enable new forms of data access, in the form of _quoted triple patterns_,
there is a need for new indexing strategies that can efficiently handle these data access patterns.
<!-- Task         -->
As such, we explore and evaluate different in-memory indexing approaches for quoted triples.
<!-- Object       -->
In this paper, we investigate three indexing approaches,
and evaluate their performance over an artificial dataset with artificial triple pattern queries.
<!-- Findings     -->
Our findings show that our two indexing approaches vastly outperform the baseline
in terms in storage size, ingestion time, and query throughput.
<!-- Conclusion   -->
Our work shows that storing quoted triples separately from non-quoted triples achieves good performance,
and can be implemented using well-known indexing techniques into existing systems.
<!-- Perspectives -->
Therefore, we shown that the addition of quoted triples into the RDF stack can be achieved in a performant manner.
