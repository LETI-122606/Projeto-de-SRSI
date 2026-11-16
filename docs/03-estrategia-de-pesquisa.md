# Estratégia de pesquisa

## Bases de dados

A pesquisa principal foi realizada nas seguintes bases científicas:

- IEEE Xplore
- ACM Digital Library
- Scopus

Os resultados exportados foram reunidos e geridos no Parsifal. A sintaxe foi adaptada às opções de pesquisa de cada base de dados.

## Grupos de termos

Os termos de cada grupo foram ligados por OR. Nas combinações principais, os grupos foram ligados por AND.

**G1 — Tecnologia**

"large language model" OR "large language models" OR "LLM" OR "LLM-based application" OR "generative AI"

**G2 — Ameaça**

"prompt injection" OR "indirect prompt injection" OR "instruction injection"

**G3 — Impactos e defesas**

"data leakage" OR "data exfiltration" OR "access control" OR "mitigation" OR "defense" OR "defence" OR "detection"

**G4 — Revisões**

Pesquisa inicial: "systematic literature" OR "systematic review" OR "literature review"

Pesquisa alargada: os termos anteriores foram complementados com "survey" OR "systematic mapping" OR "scoping review" OR "systematization of knowledge".

## Combinações testadas na IEEE Xplore

| Código | Combinação | Resultados | Finalidade |
|---|---|---:|---|
| V1 | G1 AND G2 | 347 | Pesquisa principal mais abrangente. |
| V2 | G1 AND G2 AND G3 | 265 | Pesquisa principal mais específica. |
| S3 | G1 AND G2 AND G4 inicial | 8 | Identificação de revisões anteriores. |
| S4 | G1 AND G2 AND G4 alargado | 23 | Alargamento da pesquisa de revisões. |

A V2 devolveu menos 82 resultados do que a V1, uma diferença de cerca de 23,6%. A V1 foi utilizada como base da pesquisa principal. As pesquisas S3 e S4 serviram para localizar revisões anteriores e apoiar o enquadramento do tema.

## Limites dos registos disponíveis

Os valores da tabela são os resultados dos testes realizados na IEEE Xplore. O relatório não apresenta as contagens equivalentes da ACM Digital Library e da Scopus, nem a data exata de execução das pesquisas. Também não contém o histórico integral das consultas adaptadas a cada base de dados. Por isso, esses elementos não são reconstruídos nem estimados neste repositório.
