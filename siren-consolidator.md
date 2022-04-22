---
permalink: /siren-consolidator/
---
# Siren Consolidator
This plugin provides an Elasticsearch ingest processor which merges documents into a central index from one or more satellite indices.

​The merging consolidates satellite documents into one unique central document by matching on keys such as driving license number, email, phone number, or any other values known to uniquely identify an entity.

Chosen values from different satellite indices can be merged into lists of values in the central document.

For more information, see the [documentation](https://download.support.siren.io/plugins/siren-consolidator/siren-consolidator.pdf).


| Elasticsearch Version | Siren Consolidator Plugin |
| --- | --- |
| 7.11.2 | [7.11.2-1.0.0](https://download.support.siren.io/plugins/siren-consolidator/siren-consolidator-7.11.2-1.0.0.zip) |
