# Ontology

<details>

<summary>TODO Fix this</summary>

Adds a property (= “a turbine HAS a blade” or “ a sensor MEASURES physical quantity) to the classes from the taxonomy. It is a way of showing the properties of a subject and how they are related. Metadata ontologies capture how data sets are connected.

Has a syntax eøgø belog to An ontology is an explicit specification of a conceptualization. https://doi.org/10.1006/knac.1993.1008

Conceptualisation: abstract model (of a domain, with relevant concepts and relations) Explicit: the meaning of all concepts is defined

The conceptualization should be shared among the cognitive agents. In computer science context, the specification has to be formal i.e. machine readable.

Therefore for the purpose of knowledge representation in the context of metadata: An ontology is a formal explicit description of concepts in a domain of discourse (classes (sometimes called concepts)), properties of each concept describing various features and attributes of the concept (slots (sometimes called roles or properties)), and restrictions on slots (facets (sometimes called role restrictions)). https://protege.stanford.edu/publications/ontology\_development/ontology101.pdf

It’s possible to view ontology as a directed graph with classes (concepts) as nodes, and the properties (roles) as edges. In such a view, a taxonomy is a specific case of the abovementioned graph, with edges only of the type : “IS-A” (subClassOF)

Types of Ontologies: Based on Level of generality: Top Level Ontology, Domain Ontology, Task Ontology, Application Ontology Based on Level of Semantic Expressivity: Controlled Vocabulary (Terms), Glossary (Data Dictionary), Formal “IS-A” (Formal Taxonomy), Description Logics, First Order Logics

Example: OWL Ontology Language is based on Description Logics, OWL Ontology consists of : Classes, Properties (Roles), Individuals (Instances of classes) OWL OntologyAssumptions: open world (absence of information is NOT valued as False), and No unique names (ex. WIndTurbineA can be same as WIndTurbineB, unless expressed explicitly)

</details>

