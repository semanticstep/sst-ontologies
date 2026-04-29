# SST Ontologies

Higher-level ontologies for industrial product data that integrate modelling concepts from international standards into a unified, single-level data model. This bridges major incompatibilities between these standards.

## Integrated Standards

| Standard | Description |
|----------|-------------|
| **ISO 15926 series** | Life-cycle Integration (LCI) for process plants, including oil and gas production facilities |
| **ISO 10303 series** | STEP — STandard for the Exchange of Product model data |
| **IEC 61360-4** | IEC Common Data Dictionary (CDD) for electric/electronic components |
| **ISO/IEC 81346** | Standard Series on Reference Designation System (RDS) |
| **ASD S3000L** | Logistic Support Analysis (LSA) |
| **ISO/IEC 80000** | Quantities and Units |

## Ontologies

The following ontology files are embedded in this module:

| Ontology | File | Description |
|----------|------|-------------|
| `color` | `ontologies/color/color.ttl` | Color ontology |
| `countrycodes` | `ontologies/countrycodes/countrycodes.ttl` | Country code ontology |
| `currencycodes` | `ontologies/currencycodes/currencycodes.ttl` | Currency code ontology |
| `eed` | `ontologies/eed/eed.ttl` | Electric/electronic data ontology |
| `lci` | `ontologies/lci/lci.ttl` | Life-cycle integration ontology |
| `owl` | `ontologies/owl/owl.ttl` | OWL ontology definitions |
| `qau` | `ontologies/qau/qau.ttl` | Quantities and units ontology |
| `rdf` | `ontologies/rdf/22-rdf-syntax-ns.ttl` | RDF ontology definitions |
| `rdfs` | `ontologies/rdfs/rdf-schema.ttl` | RDFS ontology definitions |
| `rep` | `ontologies/rep/rep.ttl` | Representation ontology |
| `sh` | `ontologies/sh/shacl.ttl` | SHACL ontology definitions |
| `skos` | `ontologies/skos/skos.ttl` | SKOS ontology definitions |
| `ssmeta` | `ontologies/ssmeta/ssmeta.ttl` | SST meta ontology |
| `sso` | `ontologies/sso/sso.ttl` | Semantic STEP ontology |
| `xsd` | `ontologies/xsd/xsd.ttl` | XML Schema datatype definitions |

## Usage

This is a Go module that embeds all ontology files via `embed.FS`:

```go
import "github.com/semanticstep/sst-ontologies"

// Access embedded ontology files
content, err := ontologies.FS.ReadFile("ontologies/sso/sso.ttl")
```

## Requirements

- Go 1.22 or later