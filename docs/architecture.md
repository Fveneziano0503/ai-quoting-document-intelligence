# Architecture

Current: local HTML → deterministic parser → manual costing → review gate → CSV. No server, authentication, persistent database, API key, or network request is used. Document text is rendered as text, not executable HTML.

Planned: uploaded documents → document text extraction → LLM structured output with source references → field validation → human correction → costing system. An eventual upload service needs access controls, file limits, reliable source storage, and auditable versions. Drawing interpretation must preserve units, tolerances, revision, and source evidence rather than guessing.

The current parser accepts one labeled field per line and does not claim free-form understanding. Duplicate labels are ambiguous. Required-field presence is not proof of technical completeness. CSV output escapes quotes and prefixes leading formula characters.
