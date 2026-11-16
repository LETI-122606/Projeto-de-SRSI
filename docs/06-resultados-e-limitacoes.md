# Síntese dos resultados e limitações

## Tipos de contributo

Os nove estudos analisados cobrem diferentes partes do problema:

- **Demonstrações de ataques:** Greshake et al. (2023) e VORTEXPIA (2026).
- **Formalização e avaliação comparativa:** Liu et al. (2024) e Zhan et al. (2025).
- **Benchmarks e ambientes de teste:** INJECAGENT (2024) e AgentDojo (2024).
- **Mecanismos de defesa:** Spotlighting (2024), Task Shield (2025) e CaMeL (2026).

## Principais resultados quantitativos

| Estudo | Resultado reportado | Como deve ser interpretado |
|---|---|---|
| Liu et al. (2024) | A Combined Attack obteve ASV média de 0,75 com GPT-4. | ASV mede o desempenho na tarefa injetada e não equivale a uma ASR de 75%. |
| INJECAGENT (2024) | ASR-valid de 23,6% no cenário base e 47,0% no cenário reforçado, com GPT-4/ReAct. | Os valores dependem da configuração do agente e da instrução adversarial. |
| AgentDojo (2024) | Na comparação defensiva com GPT-4o, a filtragem de ferramentas reduziu a ASR de 57,69% para 6,84%. | O resultado é específico do benchmark e das tarefas testadas; a utilidade também tem de ser considerada. |
| Spotlighting (2024) | Datamarking reduziu a ASR para 3,10% numa configuração de sumarização com GPT-3.5-Turbo. | O resultado não demonstra, por si só, prevenção de exfiltração por ferramentas. |
| Task Shield (2025) | Com GPT-4o, a ASR passou de 47,69% para 2,07%. | No teste Slack com GPT-4o-mini, a latência mediana passou de 6,17 s para 62,56 s. |
| Zhan et al. (2025) | Os ataques adaptativos ultrapassaram 50% de ASR perante as oito defesas avaliadas. | Avaliação white-box com dois agentes e uma amostra de 100 casos do INJECAGENT. |
| CaMeL (2026) | Num cenário com políticas, os ataques bem-sucedidos passaram de 11 na configuração nativa para zero com CaMeL. | No cenário o3 High, a utilidade passou de 84,5% para 77,3%; o resultado depende das políticas e do modelo de ameaça. |
| VORTEXPIA (2026) | Pontuação média de ataque de 86,12% em duas aplicações experimentais. | A pontuação é atribuída por avaliadores automáticos; não corresponde à percentagem de utilizadores que divulgaram dados reais. |
| Greshake et al. (2023) | Demonstrações de ataques indiretos, incluindo tentativas de divulgação de informação. | O estudo apresenta provas de conceito, não uma ASR global comparável com os benchmarks. |

Os resultados acima reproduzem os valores registados no relatório e no formulário de extração. Devem ser interpretados dentro dos cenários e das métricas de cada artigo.

## Resposta sintética às perguntas de investigação

### RQ1 — Vetores e consequências

Os estudos identificam conteúdos maliciosos inseridos em páginas Web, documentos, mensagens e respostas de ferramentas. As consequências podem incluir alteração das respostas, tentativas de fuga de dados, utilização indevida de ferramentas e pedidos desnecessários de informação pessoal. O impacto depende das capacidades e permissões atribuídas à aplicação.

### RQ2 — Deteção e mitigação

Foram analisadas técnicas que assinalam ou transformam conteúdos externos, detetores de instruções suspeitas, filtros de ferramentas, verificações do alinhamento das ações com a tarefa e arquiteturas que aplicam políticas de segurança fora do LLM. Estas soluções atuam em camadas diferentes e podem ser complementares.

### RQ3 — Eficácia e limitações

Algumas defesas reduzem significativamente a taxa de sucesso dos ataques nos cenários avaliados. Contudo, podem existir custos em utilidade, latência e complexidade. Os ataques adaptativos mostram que uma defesa eficaz contra exemplos conhecidos pode falhar quando o atacante a adapta. Como os estudos usam modelos, tarefas e métricas diferentes, não é possível calcular uma média global nem declarar uma defesa universalmente superior.

### RQ4 — Evolução no período

Na amostra analisada há um estudo de 2023, quatro de 2024, dois de 2025 e dois de 2026. Os contributos passam por demonstrações de ataques, benchmarks, mecanismos de defesa, ataques adaptativos e riscos de privacidade. Esta distribuição descreve apenas os nove estudos selecionados e não representa necessariamente a evolução de toda a área.

## Limitações

1. A triagem de títulos e resumos não foi concluída para todos os 3.387 registos não duplicados.
2. Os nove estudos constituem uma seleção dirigida e podem existir trabalhos relevantes que não foram incluídos.
3. Os estudos usam modelos, tarefas, ambientes e métricas diferentes, o que limita a comparação direta.
4. Algumas avaliações são feitas em ambientes simulados ou com amostras limitadas.
5. A pontuação de pedidos de informação pessoal não demonstra que utilizadores reais tenham divulgado esses dados.
6. Os resultados de uma defesa num benchmark não garantem o mesmo desempenho noutras aplicações.

Por estas razões, as conclusões devem ser entendidas como uma síntese crítica dos nove estudos analisados, e não como uma estimativa da eficácia de todas as defesas disponíveis ou uma revisão exaustiva da literatura.

## Trabalho futuro: preparação da componente prática

A revisão teórica fornece a base para uma componente prática a desenvolver numa fase posterior. Essa componente ainda não foi realizada. O objetivo será selecionar um ambiente controlado, simular cenários de *prompt injection* e avaliar algumas das defesas identificadas, procurando reproduzir as métricas de sucesso e de desempenho recolhidas nos artigos.

A estratégia de avaliação prevista é **benchmarking**: organizar cenários e tarefas, executá-los em condições controladas e comparar os resultados através de métricas. Como possível abordagem para executar os testes, poderá recorrer-se a **black-box testing**, avaliando o comportamento observável do sistema a partir das entradas, respostas e ações produzidas, sem depender do acesso à implementação interna. Assim, black-box testing é uma possível abordagem de teste dentro do benchmarking, não uma alternativa à estratégia de avaliação.

A fase prática deverá responder a duas perguntas:

- **Porque é que escolhemos o ambiente em que estamos a trabalhar?** A resposta deverá justificar se o ambiente permite representar aplicações baseadas em LLMs, introduzir conteúdos não confiáveis, configurar ferramentas e permissões e observar tentativas de fuga de dados ou de ações não autorizadas. Deverá também considerar a segurança, a possibilidade de repetir experiências e a recolha de métricas.
- **De que maneira é que o nosso ambiente poderia ser diferente e melhor?** A resposta deverá identificar limitações do ambiente escolhido e propor melhorias, por exemplo ao nível da variedade de modelos, ferramentas, tarefas, ataques, defesas ou dimensão dos testes.

Estas questões são pontos de trabalho a desenvolver quando o ambiente estiver definido. Não representam resultados nem limitações já confirmadas. A proposta mais detalhada está em [07-trabalho-futuro.md](07-trabalho-futuro.md).
