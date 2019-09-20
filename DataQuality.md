# Data quality

Following are the main classes of curation issues in Parthenos Discovery (or in any aggreagtion and mapping effor really):

* **Missing data** – There are often large lacunae in the aggregated data space. This can be due to erroneous or incomplete mapping, but mostly it is already the source metadata that does not make certain characteristics of a resource explicit.

* **Missing Labels** – Many entities don't feature a human-readable denoting string

* **Literals referring to entities** – The PEM, being rooted in [CIDOC CRM](http://www.cidoc-crm.org/), promotes virtually each piece of information to an entity. E.g. a title is not just a string property of some resource, but an entity in its own right, with a separate URI identifier and with a relation ( [*crm:P131_is_identified_by*]() ) to the resource it identifies. However in the source data (mostly XML-based metadata records), most "secondary" entities used to describe a resource, like e.g. organisations or persons are referenced only by a literal, a human readable string. This approach is inherently prone to spelling variations and ambiguous references. A major challenge in the mapping effort was to generate PEM entities out of this underspecified references, especially to generate a sensible, stable URI denoting given entity. However given that this generation could only be grounded in the available  unreliable string information, it inherits the problematic characteristics of the source information.
Nevertheless moving away from literals to URI-referenced entities is a necessary precondition for any further disambiguation and normalisation efforts.

* **Same information in many graphs** – Presumably due to modelling error in the mapping process certain triples are repeated many times. E.g. the type of a collection consisting of many individual datasets may be indicated repeatedly in the context of every dataset. Albeit this is technically not incorrect, it clutters the data space with duplicate information leading to confusion of the user and potential problems (unexpected expansion of the result) in complex queries.
