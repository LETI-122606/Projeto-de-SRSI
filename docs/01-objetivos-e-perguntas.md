# Objetivos e perguntas de investigação

## Objetivo

Analisar estudos científicos sobre ataques de *prompt injection* em aplicações baseadas em LLMs, com especial atenção à fuga de dados e ao uso indevido de ferramentas. O trabalho procura identificar as principais formas de ataque, perceber como funcionam as defesas e comparar os resultados dos testes apresentados pelos investigadores.

## Pergunta geral

**GRQ —** What are the main prompt injection threats affecting data confidentiality and access control in LLM-based applications, and how effective are the proposed mitigation mechanisms?

## Perguntas de investigação

**RQ1 —** What are the main prompt injection attack vectors and their potential consequences for data confidentiality and access control?

Foca-se nos ataques, na origem do conteúdo malicioso e nas consequências para a confidencialidade e para as ações que o agente pode executar.

**RQ2 —** What detection and mitigation techniques have been proposed to address these security threats?

Identifica as técnicas propostas para detetar, prevenir ou limitar os efeitos dos ataques.

**RQ3 —** How do existing mitigation techniques compare in terms of effectiveness, limitations and evaluation methodologies?

Compara os testes, as métricas, os resultados e as limitações das defesas. A comparação tem em conta que os estudos utilizam modelos, tarefas e cenários diferentes.

**RQ4 —** How has scientific research on these security threats evolved over the selected review period?

Descreve a distribuição temporal e os tipos de contributo dos nove estudos analisados. Esta amostra não é usada para afirmar tendências de toda a literatura.

## Estrutura PIPOC

| Elemento | Aplicação no projeto |
|---|---|
| Population | Aplicações, agentes e serviços que usam LLMs. |
| Intervention | Ataques de *prompt injection* e técnicas de prevenção, deteção ou mitigação. |
| Comparison | Comparação de defesas e de configurações com e sem proteção. |
| Outcome | Efeitos na confidencialidade, nas ações autorizadas e nos resultados e custos das defesas. |
| Context | Aplicações que consultam documentos, processam dados externos ou utilizam ferramentas e APIs. |

As perguntas e a estrutura PIPOC seguem o enquadramento descrito no relatório do projeto.
