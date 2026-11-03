# Gaia-X Trust Framework Ontology & SHACL Shapes

Este repositorio aloja la ontología canónica **OWL/RDF**, las restricciones **SHACL (Shapes Constraint Language)** y los contextos **JSON-LD** del **Gaia-X Trust Framework**, preparados para la integración con la metodología **A&AD (Accounting & Audit by Design)**.

---

## 📁 Contenido del Repositorio

1. **[`gaia-x-trustframework.owl.ttl`](gaia-x-trustframework.owl.ttl):**
   * Definición formal de las clases ontológicas de Gaia-X (`gx:LegalPerson`, `gx:LegalParticipant`, `gx:ServiceOffering`, `gx:DataResource`, `gx:ComplianceCredential`).
   * Propiedades de identidad y trazabilidad (`gx:vatID`, `gx:leiCode`, `gx:registrationNumber`, `gx:policy`).
   * Namespace oficial: `https://w3id.org/gaia-x/development#`.

2. **[`gaia-x-trustframework.shacl.ttl`](gaia-x-trustframework.shacl.ttl):**
   * Shapes de validación determinista que verifican la conformidad de participantes y ofertas de datos antes de su publicación en catálogos federados.

3. **[`gaia-x-context.jsonld`](gaia-x-context.jsonld):**
   * Contexto normativo JSON-LD para serializar y deserializar credenciales verificables (VCs) y auto-descripciones (*Self-Descriptions*).

---

## 🔗 Integración con el Stack A&AD

* **Mapeo con FIBO & Sunder:** La clase `gx:LegalPerson` se enlaza directamente con `fibo:StockCorporation` definida en el esquema maestro [`sunder_zachman_dfrnt_instances_v4.schema.json`](https://github.com/AI2Accountans/AAxD).
* **Validación Shift-Left:** Los shapes SHACL de este repositorio son ejecutables en tiempo de ingesta mediante validadores Python (`pyshacl`), motores Prolog o en la base de datos de grafos **TerminusDB / DFRNT**.
* **Repositorio Matriz:** [AI2Accountans/AAxD](https://github.com/AI2Accountans/AAxD).

