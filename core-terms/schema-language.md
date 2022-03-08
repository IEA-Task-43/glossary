# Schema Language

A method of expressing the contents of a [schema](schema.md) that is a combination of [syntax](the-gitbook-editor.md) (usually a unique syntax for a given schema language) with some [semantics](collections.md) particular to writing schema.



Examples of Schema Languages include:

* JSONSchema
* XMLSchema (XSD)
* AvroSchema,
* English\*,
* German\*,
* and many others…

\*A Schema Language could even include plain language like English or German - although such languages can be less precise and would not meet FAIR principles

An example of a schema written in an XMLSchema schema language. https://en.wikipedia.org/wiki/MPEG-7

RDF Schema (RDFS):

XML Schema An XML Schema describes the structure of an XML document. The XML Schema language is also referred to as XML Schema Definition (XSD) The purpose of an XML Schema is to define the legal (valid) building blocks of an XML document: the elements and attributes that can appear in a document the number of (and order of) child elements data types for elements and attributes default and fixed values for elements and attributes

\<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

\<xs:element name="note"> [xs:complexType](xs:complexType) [xs:sequence](xs:sequence) \<xs:element name="to" type="xs:string"/> \<xs:element name="from" type="xs:string"/> \<xs:element name="heading" type="xs:string"/> \<xs:element name="body" type="xs:string"/> \</xs:sequence> \</xs:complexType> \</xs:element>

\</xs:schema>

JSON Schema (JSON Schema is based on the concepts from XML Schema (XSD), but is JSON-based): Let's take data in JSON format: { "productId": 1, "productName": "A green door", "price": 12.50, "tags": \[ "home", "green" ] } While generally straightforward, the example leaves some open questions. Here are just a few of them: What is productId? Is productName required? Can the price be zero (0)? Are all of the tags string values? When you’re talking about a data format, you want to have metadata about what keys mean, including the valid inputs for those keys. JSON Schema is a proposed IETF standard how to answer those questions for data. A schema for the example above can be: { "$schema": "https://json-schema.org/draft/2020-12/schema", "$id": "https://example.com/product.schema.json", "title": "Product", "description": "A product from Acme's catalog", "type": "object", "properties": { "productId": { "description": "The unique identifier for a product", "type": "integer" }, "productName": { "description": "Name of the product", "type": "string" }, "price": { "description": "The price of the product", "type": "number", "exclusiveMinimum": 0 }, "tags": { "description": "Tags for the product", "type": "array", "items": { "type": "string" }, "minItems": 1, "uniqueItems": true } }, "required": \[ "productId", "productName", "price" ] } For comparison of different schema languages see the Table from Sub-challenge A

th
