# Syntax

A set of rules that defines the combinations of symbols that are considered to be correctly structured statements or expressions in a language or data format. Syntax therefore refers to the form of the data or code, and is contrasted with [semantics](collections.md) – the meaning.

## Examples

We can express semantically identical data (in this case metadata for a webpage header) using different syntaxes.

{% tabs %}
{% tab title="HTML" %}
In HTML (HyperText Markup Language) with opengraph attributes:

```html
<head>
    <meta property="og:type" content="article">
    <meta name="description" content="Science to build on">
</head>
```
{% endtab %}

{% tab title="JSON" %}
In JSON (JavaScript Object Notation):

```json
{
  "type": "article",
  "description": "Science to build on",
}
```
{% endtab %}
{% endtabs %}

## Useful syntaxes for metadata

We think the following syntaxes will be useful for definition of [metadata](live-edit-and-locked-edits.md) (but this is by no means an exhaustive list:

* [OWL (Web Ontology Language)](https://www.w3.org/TR/owl-semantics/syntax.html)
* [JSON (Javascript Object Notation)](https://www.json.org/json-en.html)
* [OpenGraph](https://ogp.me)
