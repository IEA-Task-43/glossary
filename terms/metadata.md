# Metadata

Data that provides information about other data \[[wikipedia](https://en.wikipedia.org/wiki/Metadata)].

Metadata is structured (and often standardised) information associated with a (data) resource, that provides information about the resource itself.

Metadata provides [context](context.md) and [pragmatics](pragmatics.md) (which may be general or domain-specific) for its resource.

{% hint style="success" %}
**Purpose**

Metadata allows you to:

* Make resources [findable](fair-principles.md), by providing a high-level overview which can be inserted into a search index
* Make resources [reusable](fair-principles.md), by providing information about how they were generated in the first place.
{% endhint %}

## Types of Metadata

The [How To Fair](https://howtofair.dk/how-to-fair/metadata/) project describes three different types of metadata, Administrative, Description and Structural.

{% tabs %}
{% tab title="Administrative" %}
Administrative metadata is relevant for managing data, for example:

* Project
* Resource owner
* Collaborators
* Funder
* Organisation
* License

These can usually be assigned before you collect or create the data resource itself.
{% endtab %}

{% tab title="Descriptive (citation)" %}
Descriptive (_citation_) metadata allows people to discover and identify the resource:

* Author
* Title
* Abstract
* Keywords
* Topic
* Persistent identifier
* Related resources

These are usually assigned at the point of publication.

{% hint style="info" %}
**Tip**

To facilitate data discovery, descriptive metadata can be made far more powerful than merely a citation.

For example, "find data containing rainfall in Africa last year" requires that a search index or graph is populated with temporal and locational values extracted from the data or its structural metadata.

In such cases "structural" metadata might also be thought of as "descriptive", and the lines blur between them. Extra search fields might include, for example:

* Datetimes or ranges
* Geolocations
* External conditions
* Other content-derived fields
* Data type
{% endhint %}
{% endtab %}

{% tab title="Structural (provenance)" %}
{% hint style="warning" %}
The [definition of structural metadata from the How To Fair project](https://howtofair.dk/how-to-fair/metadata/) incorporates two aspects, we've differentiated them into "provenance" and "form" for clarity.
{% endhint %}

Structural (provenance) metadata are data about how a resource came about, for example:

* Collection method
* Sampling procedure
* Assumptions made
* Researcher notes

These metadata have to be gathered by the researchers according to best practice in their research community. They should be added continuously throughout data generation and processing.

{% hint style="info" %}
**Tip**

The semantics used in defining the data and its structural metadata should provide meaning and context to the data in a formal and machine-readable way. However, where richer meaning or context is difficult or impossible to formally capture, this structural metadata should be used to convey such information.
{% endhint %}
{% endtab %}

{% tab title="Structural (form)" %}
{% hint style="warning" %}
The [definition of structural metadata from the How To Fair project](https://howtofair.dk/how-to-fair/metadata/) incorporates two aspects, we've differentiated them into "provenance" and "form" for clarity.
{% endhint %}

Structural (form) metadata are data about how a resource is internally structured, including for example:

* Data size
* Storage details (eg file types, encodings and/or database details)
* Content and format (data structure)
  * Specified directly, by listing Categories, Variables, Column Names, Types, Relations etc, or
  * Specified indirectly, by referencing an external [schema](schema.md) or [ontology](ontology.md).

Content and format will usually be defined by researchers or engineers planning the project, while storage details will usually be defined by the data engineering team tasked with maintaining infrastructure.

All such metadata should (ideally) be established _a priori_ to data generation (see ["de-risking a project](schema.md#example-uses-for-schema)"), but may evolve during the lifetime of a data resource.
{% endtab %}
{% endtabs %}



## Useful syntaxes for metadata

We think the following syntaxes will be most useful for definition (but this is by no means an exhaustive list):

* [OWL (Web Ontology Language)](https://www.w3.org/TR/owl-semantics/syntax.html)
* [JSON (Javascript Object Notation)](https://www.json.org/json-en.html)
* [OpenGraph](https://ogp.me)
