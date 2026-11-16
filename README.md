# Projeto de SRSI

## Segurança contra ameaças potenciadas pela inteligência artificial generativa

Trabalho realizado no âmbito da unidade curricular **Segurança em Redes e Sistemas de Informação (SRSI)**, do Mestrado em Engenharia de Telecomunicações e Informática do Iscte.

**Autores:** Pedro Henriques, Eduardo Sousa e André Apostol  
**Ano:** 2026

## Objetivo

O projeto analisa ataques de *prompt injection* em aplicações baseadas em modelos de linguagem de grande dimensão (LLMs), com especial atenção à confidencialidade dos dados, à utilização indevida de ferramentas e ao controlo de acesso. São identificados vetores de ataque e comparadas técnicas de deteção e mitigação descritas na literatura científica.

A pergunta geral e as quatro perguntas de investigação estão em [docs/01-objetivos-e-perguntas.md](docs/01-objetivos-e-perguntas.md).

## Conteúdo do repositório

- **docs/** — documentação do âmbito, protocolo, pesquisas, seleção, extração, análise e trabalho futuro.
- **data/** — dados de extração dos nove estudos analisados, exportados do Parsifal.
- **references/references.md** — referências bibliográficas do relatório.

O ficheiro de extração está em **[data/parsifal/data-extraction.csv](data/parsifal/data-extraction.csv)**. As instruções para o consultar estão em [data/README.md](data/README.md).

## Resultados e transparência metodológica

Foram realizadas pesquisas na IEEE Xplore, ACM Digital Library e Scopus. Os resultados foram reunidos no Parsifal. A exportação bibliográfica utilizada no relatório continha **3.872 registos**, dos quais **485 estavam assinalados como duplicados**, ficando **3.387 registos não duplicados**.

A triagem de títulos e resumos não foi concluída para todos os 3.387 registos. Foram selecionados e analisados em profundidade nove estudos primários, por relevância para as perguntas de investigação. Por isso, este trabalho deve ser entendido como uma análise crítica de nove estudos e **não como uma revisão sistemática exaustiva de toda a literatura**. Os nove estudos não são apresentados como os únicos potencialmente elegíveis.

Os números das pesquisas V1, V2, S3 e S4 disponíveis no relatório são apenas os resultados obtidos na IEEE Xplore. Não foram registadas no relatório as contagens equivalentes por base de dados nem a data exata de execução das pesquisas. Estes elementos não são estimados neste repositório.

As métricas dos artigos também não são diretamente equivalentes. Por esse motivo, os resultados são apresentados no contexto de cada estudo e não é calculada uma média global nem uma classificação geral das defesas.

## Trabalho futuro: componente prática

A componente prática do projeto está prevista para uma fase posterior e **ainda não foi realizada**. A ideia é escolher um ambiente controlado e utilizá-lo para simular cenários de *prompt injection* e testar algumas das defesas identificadas na revisão teórica. Pretende-se verificar se as métricas de sucesso e de desempenho recolhidas nos artigos podem ser reproduzidas nesse ambiente, tendo em conta as diferenças entre modelos, tarefas e configurações.

Na preparação e execução dessa fase, deverão ser respondidas duas perguntas:

- **Porque é que escolhemos o ambiente em que estamos a trabalhar?**
- **De que maneira é que o nosso ambiente poderia ser diferente e melhor?**

A primeira pergunta servirá para justificar a escolha do ambiente e explicar se permite representar os riscos estudados, configurar ferramentas e permissões, simular ataques e recolher métricas de forma controlada. A segunda orientará a análise das limitações do ambiente e a identificação de melhorias possíveis. Nesta fase não é assumido um ambiente específico nem são apresentados resultados experimentais próprios.

A proposta e os pontos a desenvolver estão em [docs/07-trabalho-futuro.md](docs/07-trabalho-futuro.md).

## Estrutura

| Caminho | Conteúdo |
|---|---|
| docs/01-objetivos-e-perguntas.md | Objetivo, GRQ, RQ1–RQ4 e PIPOC |
| docs/02-protocolo-e-criterios.md | Âmbito e critérios de inclusão e exclusão |
| docs/03-estrategia-de-pesquisa.md | Bases de dados, grupos de termos e combinações |
| docs/04-selecao-dos-estudos.md | Registos, duplicados, seleção e limitações |
| docs/05-extracao-de-dados.md | Processo e campos de extração do Parsifal |
| docs/06-resultados-e-limitacoes.md | Síntese dos nove estudos e principais resultados |
| docs/07-trabalho-futuro.md | Preparação da futura componente prática |
| data/parsifal/data-extraction.csv | Exportação dos dados de extração |
| references/references.md | Referências bibliográficas |

## Nota sobre o âmbito

Este repositório documenta a revisão da literatura e os dados extraídos. A implementação experimental própria ainda não foi realizada nesta fase; está prevista como componente prática futura e é enquadrada em [docs/07-trabalho-futuro.md](docs/07-trabalho-futuro.md). As conclusões atuais dizem respeito aos nove estudos analisados e às condições experimentais descritas pelos respetivos autores.
