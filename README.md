# geontology

> An open-access ontology and web frontend for Structural Geology and translations

## Context

Translation of key terms in Structural Geology and tectonics is a key issue. To solve this, we propose the development of an ontology of key concepts in the fields, linked by a set of possible relations created by scholars working within relevant disciplines.

After populating an OWL triplestore, we develop a simple platform where users can view and explore the ontology, and can submit corrections or additions via an intuitive interface. Changes enter a queue to be reviewed by adminstrators, and are displayed within the platform after approval.

## Triplestore vs relational database

Previous related research has employed relational databases for storing content. We instead opt for the use of an RDF triplestore because triplestores are:

* well-designed for the (semantic) web
* less vulnerable to SQL injection attacks
* easier to ingest existing resources, because the subject-predicate-object structure is simpler than a relational database with many tables
* easier to share and open-source data as plain XML
* implementation-agnostic: the ontology content, which will be made available for free, will conform to well-adopted standard, and can thus be processed with a number of tools and not rely on a particular database software
* easy to extend with new relations

## Method

1. Convene workshop in which participants can improve on existing geology-related ontologies such as [GSO](https://github.com/Loop3D/GKM).
2. Populate [XML format ontology](https://www.w3.org/TR/2012/REC-owl2-quick-reference-20121211/) with pre-existing resources
3. Develop web platform that allows exploring data and creating new nodes/links (with superusers able to confirm additions)

## Tech stack

* aiohttp backend
* [RDFLib](https://en.wikipedia.org/wiki/RDFLib) and [OWL-RL](https://github.com/RDFLib/OWL-RL) for managing the ontology
* Vue.js frontend
