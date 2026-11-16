# Trabalho futuro: preparação da componente prática

## Objetivo

A revisão teórica permitiu identificar vetores de *prompt injection*, consequências para a confidencialidade e o controlo de acesso, mecanismos de defesa e métricas utilizadas para avaliar os resultados. Como continuação do projeto, está prevista uma componente prática para uma fase posterior.

**A componente prática ainda não foi realizada.** Este documento serve apenas para deixar preparada a sua base: não apresenta uma implementação, resultados experimentais ou uma escolha definitiva do ambiente.

O objetivo será selecionar um ambiente controlado, simular cenários de ataque e testar algumas das defesas identificadas na revisão. Pretende-se verificar se as métricas de sucesso e de desempenho recolhidas nos estudos teóricos podem ser reproduzidas nesse ambiente. A comparação terá de considerar que os modelos, as tarefas, as ferramentas e as configurações podem não ser iguais às dos artigos.

## 1. Escolha e justificação do ambiente

A primeira decisão será escolher o ambiente onde decorrerão as experiências. A escolha deverá ser explicada respondendo diretamente à pergunta:

**Porque é que escolhemos o ambiente em que estamos a trabalhar?**

A justificação deverá descrever as características do ambiente e explicar se permite:

- trabalhar com uma aplicação ou agente baseado num LLM;
- introduzir conteúdos externos não confiáveis, incluindo exemplos de *prompt injection* direto ou indireto;
- representar dados que devem permanecer confidenciais;
- configurar ferramentas, permissões e ações que permitam estudar o controlo de acesso;
- observar tentativas de fuga de dados ou de execução de ações não autorizadas;
- recolher registos e métricas e repetir os testes em condições controladas;
- realizar experiências de forma segura, sem afetar serviços ou dados reais.

O ambiente concreto ainda não está definido neste documento. O nome, a arquitetura, os modelos, as ferramentas e as configurações deverão ser acrescentados quando a componente prática começar.

## 2. Simulação e avaliação

Depois de escolhido o ambiente, a componente prática poderá seguir estas etapas:

1. **Definir os cenários:** preparar tarefas legítimas e cenários de ataque inspirados nos estudos analisados, incluindo conteúdos externos maliciosos e tentativas de influenciar as ações do agente.
2. **Estabelecer uma referência:** executar as tarefas sem ataque e registar o comportamento normal do ambiente.
3. **Simular os ataques:** introduzir tentativas de *prompt injection* relacionadas com fuga de informação, acesso a dados e utilização indevida de ferramentas.
4. **Testar as defesas:** selecionar mecanismos identificados na revisão e comparar os resultados com as configurações sem proteção.
5. **Recolher e analisar métricas:** escolher as métricas que o ambiente permite medir e comparar os resultados com os valores reportados nos artigos.

Entre as métricas que poderão ser consideradas estão a taxa de sucesso dos ataques (ASR e variantes), o sucesso das tarefas legítimas, a utilidade sob ataque, os falsos positivos, a latência e os custos. A escolha dependerá dos cenários e dos mecanismos efetivamente implementados. Métricas como ASR, ASR-valid e ASV têm definições diferentes e não deverão ser tratadas como equivalentes nem agregadas sem justificação.

O objetivo será verificar se os resultados e as tendências descritos na literatura podem ser observados no ambiente escolhido. Não se deverá esperar uma reprodução exata dos valores quando os modelos, os dados, as tarefas ou as configurações forem diferentes.

## 3. Limitações do ambiente e possíveis melhorias

Depois dos testes, será importante avaliar as limitações do ambiente e responder à pergunta:

**De que maneira é que o nosso ambiente poderia ser diferente e melhor?**

Esta análise poderá considerar, por exemplo:

- se o ambiente representa de forma suficiente uma aplicação utilizada em contexto real;
- se permite testar diferentes modelos, ferramentas, permissões e tipos de tarefas;
- se os cenários incluem ataques variados e ataques adaptativos;
- se o número de testes é suficiente para interpretar os resultados;
- se as métricas disponíveis permitem avaliar tanto a segurança como a utilidade;
- se existem limitações de tempo, recursos computacionais, custos ou acesso a modelos.

Com base nessa análise, poderão ser propostas melhorias, como aumentar o número de cenários, incluir outros modelos e mecanismos de defesa, testar mais tipos de ataque, aumentar a dimensão da amostra ou comparar o ambiente com outra solução. Estas são possibilidades a avaliar; não são limitações confirmadas, uma vez que o ambiente ainda não foi escolhido.

## 4. Resultado esperado

Espera-se que a componente prática produza uma avaliação experimental documentada e reproduzível. Essa avaliação deverá permitir perceber em que condições os ataques têm sucesso, até que ponto as defesas reduzem esse sucesso e que impacto têm na execução das tarefas legítimas, no tempo de resposta e nos recursos utilizados.

A componente prática deverá complementar a revisão teórica, não substituir os seus resultados. A sua função será testar num ambiente concreto algumas das conclusões e métricas identificadas na literatura.
