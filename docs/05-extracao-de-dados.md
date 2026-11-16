# Processo de extração de dados

## Ferramenta e conjunto de dados

O Parsifal foi utilizado para reunir as referências e registar os dados dos estudos selecionados. Para cada um dos nove estudos analisados em profundidade foi preenchido um formulário com **12 campos de extração**, além do título do artigo.

A exportação foi convertida para CSV e guardada de forma comprimida em:

**data/parsifal/data-extraction.csv.gz**

As instruções para descomprimir e abrir o ficheiro estão em [data/README.md](../data/README.md).

## Dicionário de dados

| N.º | Campo | Conteúdo registado |
|---:|---|---|
| — | article | Título do artigo. |
| 1 | Tipo de contributo do estudo | Ataque, defesa, benchmark, avaliação ou outro tipo de contributo. |
| 2 | RQ1 — Vetor e superfície de ataque | Origem e forma de introdução do conteúdo malicioso. |
| 3 | RQ1 — Objetivo e consequências do ataque | Resultado que o atacante procura e consequências observadas. |
| 4 | RQ1 — Impacto na confidencialidade e controlo de acesso | Relação do ataque com dados sensíveis, permissões e ações não autorizadas. |
| 5 | RQ2 — Mecanismo de deteção ou mitigação | Técnica defensiva proposta ou avaliada. |
| 6 | RQ2 — Funcionamento e camada de aplicação da defesa | Como funciona a defesa e em que parte da aplicação atua. |
| 7 | RQ3 — Dataset, benchmark e cenário experimental | Conjunto de testes, tarefas e ambiente experimental. |
| 8 | RQ3 — Modelos e configuração experimental | Modelos e configurações usados nas experiências. |
| 9 | RQ3 — Métricas e resultados quantitativos | Métricas reportadas e resultados numéricos. |
| 10 | RQ3 — Comparadores, custos e limitações | Comparações realizadas, custos e limitações identificadas. |
| 11 | RQ4 — Tipo de publicação | Tipo de publicação científica. |
| 12 | Evidência — Secção ou página do artigo | Localização da informação usada na extração. |

## Utilização dos dados

Os campos foram usados para organizar a síntese dos vetores de ataque, das consequências, das defesas, das configurações experimentais e das limitações. A síntese comparativa está em [06-resultados-e-limitacoes.md](06-resultados-e-limitacoes.md).

Os resultados quantitativos devem ser lidos no contexto do artigo de origem. Métricas como ASR e ASV não são equivalentes e não devem ser agregadas numa média comum sem uma base metodológica que o permita.
