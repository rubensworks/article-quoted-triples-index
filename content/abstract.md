## Abstract
<!-- Context      -->
The upcoming RDF 1.2 recommendation is scheduled to introduce the concept of _quoted triples_,
which allows statements to be made about other statements.
<!-- Need         -->
Since quoted triples enable new forms of data access in SPARQL 1.2, in the form of _quoted triple patterns_,
there is a need for new indexing strategies that can efficiently handle these data access patterns.
<!-- Task         -->
As such, we explore and evaluate different in-memory indexing approaches for quoted triples.
<!-- Object       -->
In this paper, we investigate four indexing approaches,
and evaluate their performance over an artificial dataset with custom triple pattern queries.
<!-- Findings     -->
Our findings show that the so-called *indexed quoted triples dictionary* vastly outperforms other approaches
in terms of query execution time at the cost of increased storage size and ingestion time.
<!-- Conclusion   -->
Our work shows that indexing quoted triples in a dictionary separate from non-quoted RDF terms achieves good performance,
and can be implemented using well-known indexing techniques into existing systems.
<!-- Perspectives -->
Therefore, we illustrate that the addition of quoted triples into the RDF stack can be achieved in a performant manner.

<span id="keywords" rel="schema:about"><span class="title">Keywords</span>
<a href="https://en.wikipedia.org/wiki/Resource_Description_Framework" resource="http://dbpedia.org/resource/Resource_Description_Framework">RDF</a>,
RDF-star,
indexing
</span>

<span class="printonly firstpagefooter">
<span class="firstpagefootertop">&nbsp;</span>
<span class="footnotecopyright">
<span style="font-style:italic">7th Workshop on Storing, Querying and Benchmarking Knowledge Graphs (QuWeDa) at ISWC 2023</span><br />
<img src="img/mail.png" width="12px" /> ruben.taelman@ugent.be (R. Taelman); <img src="img/mail.png" width="12px" /> ruben.verborgh@ugent.be (R. Verborgh)<br />
<img src="img/cc-by.png" width="50px" /><span style="font-size: 0.75em">© 2023 Copyright for this paper by its authors. Use permitted under Creative Commons License Attribution 4.0 International (CC BY 4.0).</span><br />
<img src="img/ceur-ws-logo.png" width="50px" />CEUR Workshop Proceedings (<a href="https://CEUR-WS.org">CEUR-WS.org</a>)<br />
</span>
</span>
