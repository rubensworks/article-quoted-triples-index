## Introduction
{:#introduction}

[RDF](cite:cites spec:rdf) and [Labeled Property Graphs (LPGs)](cite:cites propertygraphs) have been around in recent years
as two major but diverging approaches for modeling [Knowledge Graphs](cite:cites knowledgegraphs).
One of the main reasons for divergence, is the fact that LPGs allow datasets to contain statements about other statements, while RDF does not.
This concept enables attaching metadata to statements, such as certainties or temporal validity.
For example, it allows one to express _"Alice says that Violets are Blue."_,
where the statement statement about Violets being Blue is *quoted* inside a statement from Alice.

In an effort to align these incompatibilities between RDF and LPGs,
the [RDF\*](cite:cites rdfstar) approach was introduced,
which proposes an extension of the RDF data model and SPARQL query language with support for the concept of *quoted triples*.
This approach was picked up by a [W3C community group](https://w3c.github.io/rdf-star/),
and standardized in the [RDF-star and SPARQL-star community group report](cite:cites spec:rdfstar).
This work is now being carried forward by the [W3C RDF-star working group](https://www.w3.org/groups/wg/rdf-star/)
for standardization into the RDF 1.2 and SPARQL 1.2 recommendations.

Given the [wide range of practical real-world applications](cite:cites kasenchak2021use, solidsignedrdfstar) for quoted triples,
[many open-source and commercial RDF and SPARQL systems have already implemented parts of this approach](cite:cites rdfstarimplementations).
Notable are systems such as BlazeGraph, GraphDB, and Stardog,
which offer the storage of quoted triples in their triplestore, and enable queryable access using SPARQL.
Even though some approaches offer reports of their systems passing RDF-star specification tests,
and provide high-level documentation explaining the concepts of quoted triples for end-users,
none of them offer detailed descriptions of their indexing approach,
or query performance evaluations over them.
As such, there is an open knowledge gap on the research question
*"How to index quoted triples, and what is the impact on ingestion, storage, and query performance?"*.

To fill this gap, we explore four different indexing approaches,
implement them in a single system for fair comparison,
and evaluate them in terms of ingestion time, storage size, and query performance.
We focus on in-memory indexing, but approaches are generalizable to mixed disk/memory approaches such as [HDT](cite:cites hdt).
Like [many RDF indexing approaches](cite:cites rdf3x,hexastore),
we focus on providing indexed access for triple pattern queries,
as these form the basis for answering full SPARQL queries.
