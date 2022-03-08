# Schema Language

A method of expressing the contents of a [schema](schema.md) that is a combination of [syntax](the-gitbook-editor.md) (usually a unique syntax for a given schema language) with some [semantics](collections.md) particular to writing schema.

{% hint style="success" %}
Task 43 has been evaluating different Schema Languages based on their features and the needs of the community. The [comparisons table is here](https://docs.google.com/spreadsheets/d/1\_iskx2hJ8TOEOygPN\_9ecfQNFHSlgKmNomQr5xXsxJY/edit?usp=sharing) - a fuller report with better descriptions of the features and why they're relevant is pending.
{% endhint %}

Examples of Schema Languages include:

* JSONSchema
* XMLSchema (XSD)
* RDFSchema (RDFS)
* AvroSchema,
* English\*,
* German\*,
* and many others…

{% hint style="warning" %}
\*A Schema Language _could_ simply be a plain language like English or German - although a linguistic solution struggles to meet FAIR Principles, being difficult to search and hard for machines to parse unambiguously.
{% endhint %}

### Some examples of schema in different languages

{% tabs %}
{% tab title="JSONSchema" %}
Let's take data in JSON format:&#x20;

```
{
  "productId": 1,
  "productName": "A green door",
  "price": 12.50,
  "tags": [ "home", "green" ]
} 
```

While generally straightforward, the example leaves some open questions. Here are just a few of them: What is productId? Is productName required? Can the price be zero (0)? Are all of the tags string values?

JSON Schema is a Schema language that is a proposed IETF standard for how to answer such questions for data. A schema for the example above can be:

```
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "$id": "https://example.com/product.schema.json",
  "title": "Product",
  "description": "A product from Acme's catalog",
  "type": "object",
  "properties": {
    "productId": {
      "description": "The unique identifier for a product",
      "type": "integer"
    },
    "productName": { "description": "Name of the product", "type": "string" },
    "price": {
      "description": "The price of the product",
      "type": "number",
      "exclusiveMinimum": 0
    },
    "tags": {
      "description": "Tags for the product",
      "type": "array",
      "items": { "type": "string" },
      "minItems": 1,
      "uniqueItems": true
    }
  },
  "required": ["productId", "productName", "price"]
}
```

&#x20;
{% endtab %}

{% tab title="XMLSchema" %}
The purpose of an XML Schema is to define the legal (valid) building blocks of an XML document: the elements and attributes that can appear in a document the number of (and order of) child elements data types for elements and attributes default and fixed values for elements and attributes

```
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="note"> 
        <xs:complexType>
            <xs:sequence>
                <xs:element name="to" type="xs:string"/>
                <xs:element name="from" type="xs:string"/>
                <xs:element name="heading" type="xs:string"/>
                <xs:element name="body" type="xs:string"/>
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>
```

Wikipedia has a [more complex example of a schema written in XSD](https://en.wikipedia.org/wiki/MPEG-7).
{% endtab %}

{% tab title="Plain English" %}
A schema written in plain English, translated from the JSONSchema example.

> I need you to tell me the product name, which must be text, and a unique identifying integer for that product. I also need to know the price of the product, which can't be less than or equal to zero. You may also tell me some key words associated with the project to aid in its description.

{% hint style="danger" %}
This seems a bit facetious, because we'd never actually write schema like this... But it's important to illustrate that we actually \*can\* - and frequently, this is how schemas start: as a discussion about what data you need.&#x20;
{% endhint %}
{% endtab %}
{% endtabs %}





