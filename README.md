# PARTHENOS Discovery Labs

Various scripts and results for exploring and curating the data of the [PARTHENOS Project](http://www.parthenos-project.eu/).


[PARTHENOS Discovery](https://parthenos.acdh.oeaw.ac.at/) is an application that gives access to the metadata records contributed by the partners of the PARTHENOS project, research infrastructures and initiatives in the broad domain of humanities and cultural heritage.
These records are being regularly harvested   converted into a common semantic model, the PARTHENOS Entities Model and ingested into a triple store. PARTHENOS Discovery allows to navigate, explore and search this data.

Due to the heterogeneity and idiosyncracies of the contributed datasets as well as due to the complex mapping process, the aggregated dataset exhibits a number of issues regarding the data quality. Major issues are 

* *Missing data* – There are often large lacunae in the aggregated data space. This can be due to
erroneous or incomplete mapping, but mostly it is already the source metadata that does not make
certain characteristics of a resource explicit.
* *Missing Labels* – Entities that don't feature a human-readable representationWhile
* *Literals referring to entities* – Ideally a reference to an entity should be done with an unambiguous
identifier, a URI. However, oftentimes, due to limitations of the source metadata schema and/or the
metadata authoring tools, simple literals are used to denote entities like persons or institutions.
This approach is inherently prone to spelling variations and ambiguous references. PEM offers
a well-defined way to model these entities, however the problems in the source data counteract
this potential. A major challenge in the mapping effort was to generate PEM entities out of this
underspecified references, especially to generate a sensible, stable URI denoting given entity.
Due to the principal uncertainty when trying to disambiguate a literal reference to an entity, a policy
has been adopted, that if the same literal is encountered in the context of one provider it is considered
the same identical entity. However when identical literals come from different sources, the
probability that they don’t refer to the same entity is deemed higher, therefore in such case two distinct
entities are created, even though with identical label or appellation. The merging of identical
entities is left for a separate curation step.
* *Variability of descriptors* - related to the previous problem, values in fields oftentimes come in
various spellings or language variants, leading to generation of separate entities.
* *Same information in many graphs* – Presumably due to modelling error in the mapping process
certain triples are repeated many times. E.g. the type of a collection consisting of many individual
datasets may be indicated repeatedly in the context of every dataset. Albeit this is technically not
incorrect, it clutters the data space with duplicate information leading to confusion of the user and
potential problems (unexpected expansion of the result) in complex queries. Top 100 most often
reoccurring triples appear in the dataset over 3 mio. times.