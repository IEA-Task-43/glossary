# Ontology

<details>

<summary>An ontology is an explicit specification of a conceptualization. [<a href="https://doi.org/10.1006/knac.1993.1008">Gruber, 1993</a>]</summary>

Conceptualisation: abstract model (of a domain, with relevant concepts and relations) Explicit: the meaning of all concepts is defined.

In computer science context, the specification has to be **formal** i.e. machine readable.

It’s possible to view ontology as a directed graph with [classes](class.md) (concepts) as nodes, and the [properties](property.md) (roles) as edges. In such a view, a [taxonomy](taxonomy.md) is a specific case of the abovementioned graph, with edges only of the type : “IS-A” (subClassOF)

To add semantic expressevity, in addition to "IS-A" property, it is possible to add other properties to express relationships between classes from the taxonomy. For example: “WindTurbine HAS Blade” or “ Sensor MEASURES PhysicalQuantity.&#x20;

It is a way of showing the properties of a subject and how they are related. Metadata ontologies capture how data sets are connected.&#x20;

Therefore for the purpose of knowledge representation in the context of metadata: An ontology is a formal explicit description of concepts in a domain of discourse (classes (sometimes called concepts)), properties of each concept describing various features and attributes of the concept (slots, sometimes called roles or properties), and restrictions on slots (facets, sometimes called role restrictions). \[See [Ontology 101](https://protege.stanford.edu/publications/ontology\_development/ontology101.pdf)]

#### Types of Ontologies:&#x20;

* Based on Level of generality \[[Guarino,1998](https://csis.pace.edu/\~marchese/CS835/Lec9/guarino98formal.pdf)]:&#x20;
  * Top Level Ontology
  * &#x20;Domain Ontology
  * &#x20;Task Ontology
  * Application Ontology&#x20;

<!---->

* Based on Level of Semantic Expressivity \[[Lassila,2001](http://www.ida.liu.se/ext/epa/ej/etai/2001/018/01018-etaibody.pdf)]
  * Controlled Vocabulary (Terms)
  * Glossary (Data Dictionary)
  * Formal “IS-A” (Formal Taxonomy)
  * Description Logics
  * First Order Logics

Example: OWL Ontology Language is based on Description Logics, OWL Ontology consists of : Classes, Properties (Roles), Individuals (Instances of classes) OWL OntologyAssumptions: open world (absence of information is NOT valued as False), and No unique names (ex. WIndTurbineA can be same as WIndTurbineB, unless expressed explicitly)

</details>
