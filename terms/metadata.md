# Metadata

Data that provides information about other data \[[wikipedia](https://en.wikipedia.org/wiki/Metadata)].

Metadata is structured (and often standardised) information associated with a (data) resource, that provides information about the resource itself.

Metadata provides [context](context.md) and [pragmatics](pragmatics.md) (which may be general or domain-specific) for its resource.

{% hint style="success" %}
**Purpose**

Metadata allows you to:

* Make resources [findable](fair-principles.md), by providing a high-level overview which can be inserted into a search index
* Make resources [reusable](fair-principles.md), by providing information about how they were generated in the first place.

Thinking about types of metadata allows you to:

* Decide **who** should be produce metadata and **when** that should happen


{% endhint %}

## Types of Metadata

A 'type' of metadata is a broad-brush classification of what a metadata element is for and (correspondingly) who might create it and when. The [How To Fair](https://howtofair.dk/how-to-fair/metadata/) project describes three different types of metadata, Administrative, Description and Structural. Wikipedia [defines many more](https://en.wikipedia.org/wiki/Metadata)!

How To Fair's Structural metadata description incorporates two aspects, we've differentiated them into "provenance" and "form" to help highlight the different roles and times.&#x20;

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
Structural (provenance) metadata describes how a resource came about, for example:

* Collection method
* Sampling procedure
* Assumptions made
* Researcher notes

These metadata have to be gathered by the researchers according to best practice in their research community. They should be added continuously throughout data generation and processing.

{% hint style="info" %}
**Tip**

The [semantics](semantics.md) used in defining the data and its structural metadata should provide meaning and context to the data in a formal and machine-readable way. However, where richer meaning or context is difficult or impossible to formally capture, this structural metadata should be used to convey such information.
{% endhint %}
{% endtab %}

{% tab title="Structural (form)" %}
Structural (form) metadata describes how a resource is internally structured, for example:

* Data size
* Storage details (eg file types, encodings and/or database details)
* Content and format (data structure)
  * Specified directly, by listing Categories, Variables, Column Names, Types, Relations etc, or
  * Specified indirectly, by referencing an external [schema](schema.md) or [ontology](ontology.md).

Structural (form) metadata arises from the decisions taken by the data engineering team, who should architect their infrastructure in close collaboration with researchers to anticipate size, content and format.

These details should (ideally) be established _a priori_ to data generation (see ["de-risking a project](schema.md#example-uses-for-schema)"), but may evolve throughout the lifetime of a resource.
{% endtab %}
{% endtabs %}

## The Dublin Core Metadata Initiative

The [Dublin Core Metadata Initiative](https://www.dublincore.org/resources/metadata-basics/) is an organisation dedicated to metadata. They give a [set of fifteen widely used metadata elements](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/). If publishing a data resource on the web, these elements serve as a guide for metadata should be included in order to best facilitate information discovery.

<details>

<summary>See the Dublin Core elements</summary>

See the [DCMI elements page](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/) for full descriptions.

* Contributor
* Coverage
* Creator
* Date
* Description
* Format
* Identifier
* Language
* Publisher
* Relation
* Rights
* Source
* Subject
* Title
* Type

</details>

Whilst metadata need not be limited to this (particularly in cases where rich [descriptive metadata](metadata.md#types-of-metadata) can be used to query for datasets, as opposed to search based methods), adhering to the Dublin Core should ensure a good search ranking and help you conform to the [FAIR principles](fair-principles.md).

{% hint style="success" %}
**Purpose**

The Dublin Core allows you to:

* Quickly define a set of metadata to make a published data resource findable
{% endhint %}

{% hint style="info" %}
**Tip**

As discussed in [Structural (form) metadata](metadata.md#types-of-metadata), a [schema](schema.md) can be an important element of your metadata, for describing the content of the data resource.

It is also possible to use schema in a different way - not to describe the resource itself, but to describe the associated metadata!

This allows you to check that the provided metadata is correct. The Dublin Core Metadata Initiative [publish schema](https://www.dublincore.org/schemas/) for just this purpose.
{% endhint %}

## Useful syntaxes for metadata

We think the following syntaxes will be most useful for definition (but this is by no means an exhaustive list):

* [OWL (Web Ontology Language)](https://www.w3.org/TR/owl-semantics/syntax.html)
* [JSON (Javascript Object Notation)](https://www.json.org/json-en.html)
* [OpenGraph](https://ogp.me)
