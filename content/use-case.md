## Use Case
{:#use-case}

As example use case to illustrate different indexing approaches,
we introduce a fictional dataset containing statements from different people
on the color of violets in [](#usecase-dataset).

<figure id="usecase-dataset" class="listing">
````/data/usecase-dataset.ttl````
<figcaption markdown="block">
Turtle snippets containing statements by Alice and Bob on the color of violets.
</figcaption>
</figure>

To find out what color each person says violets have,
we can execute the SPARQL query from [](#usecase-query).
This query contains a variable in the subject position,
and a variable inside the quoted triple pattern of the object position.
For brevity in the remainder of this article, we refer to the variables inside quoted triple patterns as _quoted variables_.

<figure id="usecase-query" class="listing">
````/data/usecase-query.txt````
<figcaption markdown="block">
SPARQL query to find what color each person says violets have.
</figcaption>
</figure>

More advanced datasets may also contain _nested_ quoted triples,
in which any term inside a quoted triple could be another quoted triple.
There is no upper limit of the nesting depth that can occur.
