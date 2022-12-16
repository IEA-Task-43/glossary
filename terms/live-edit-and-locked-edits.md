# Metadata

> “Data that provides information about other data” \[[wikipedia](https://en.wikipedia.org/wiki/Metadata)]

Metadata is defined as data about data. It gives context to the data it describes. Although this is a complete definition of what metadata is, it is not specific enough for most people. So, it can be useful to refine the idea of metadata to more specific subsets: [schemas][schema.md], [vocabularies][vocabulary.md], and ontologies[ontology.md].

Structured (and often standardised) information associated with a resource, that provides information about the resource itself.

Metadata provides [context](context.md) and [pragmatics](pragmatics.md) (which may be general or domain-specific) for its resource.

{% hint style="success" %}
**Purpose**

Metadata allows you to:

* Make resources [findable](fair-principles.md), by providing a high-level overview which can be inserted into a search index
* Make resources [reusable](fair-principles.md), by providing information about how they were generated in the first place.
{% endhint %}

## Types of Metadata

{% tabs %}
{% tab title="Administrative" %}
Administrative metadata is information about the creators or suppliers of the data, or terms under which it is available, such as:

* Author
* Date create
* Organisation
* License
{% endtab %}

{% tab title="Descriptive" %}
Descriptive metadata contains information related to the data content such as:

* Topic
* External conditions
* Content
* Quality
* Assumptions made
* Provenance
{% endtab %}

{% tab title="Structural" %}
Structural metadata contains information about the data storage or transmission format, such as:

* Size
* File type
* Data structure (eg properties, and or reference to a [schema](schema.md))
{% endtab %}
{% endtabs %}

## Useful syntaxes for metadata

We think the following syntaxes will be most useful for definition (but this is by no means an exhaustive list):

* [OWL (Web Ontology Language)](https://www.w3.org/TR/owl-semantics/syntax.html)
* [JSON (Javascript Object Notation)](https://www.json.org/json-en.html)
* [OpenGraph](https://ogp.me)
