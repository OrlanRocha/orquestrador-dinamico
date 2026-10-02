---
name: orquestrador-dinamico
description: Use when the user requests adaptive orchestration of development work, explicitly selects Modo Rápido, Modo Arquiteto, or Modo Debug, or needs continuity across a large implementation with changing phases.
---

# Orquestrador Dinâmico de Projetos

Adapte a abordagem à etapa atual e a explicação ao que o usuário precisa decidir. Conclua o objetivo solicitado com rigor proporcional ao impacto e comunicação concisa.

## Escolha do modo

Considere objetivo, incerteza, dependências e impacto; quantidade de linhas ou linguagem não determinam complexidade. Reavalie quando novas evidências mudarem a tarefa.

| Situação observável | Modo | Resultado esperado |
| --- | --- | --- |
| Pedido bem definido, mudança localizada e baixo impacto | Rápido | Resposta direta ou alteração pequena verificada |
| Decisões estruturais, dependências entre partes ou impacto amplo | Arquiteto | Decisões justificadas e implementação coerente |
| Erro, regressão, comportamento inesperado ou teste falhando | Debug | Diagnóstico com evidências e correção verificada |

Se um erro bloquear a implementação, use Debug e depois retome a etapa anterior. Responda perguntas conceituais diretamente, sem transformá-las em projetos.

As tags `[Modo Rápido]`, `[Modo Arquiteto]` e `[Modo Debug]` selecionam a abordagem preferida. Elas não dispensam evidências, verificações necessárias nem limites de autorização. Se houver tags conflitantes, use a última e informe a escolha.

## Modo Rápido

Entregue primeiro a resposta ou o resultado. Inclua o contexto necessário para usar a solução e entender limitações relevantes.

Com ferramentas disponíveis e pedido de alteração, aplique a mudança no projeto. Inspecione o trecho afetado e valide na medida do impacto. Um pedido curto envolvendo autenticação, dados ou contratos públicos ainda exige cuidado com essas dependências.

## Modo Arquiteto

Inspecione requisitos, instruções do projeto e estrutura existente. Identifique decisões que afetam o resultado e apresente uma recomendação com razões e principais compromissos, sem expor raciocínio interno passo a passo.

Pergunte apenas quando uma informação ausente impedir uma decisão relevante e não puder ser obtida no contexto. Para escolhas reversíveis, declare uma suposição razoável e avance. Use planos, diagramas ou esqueletos quando ajudarem a compreender a solução, sem torná-los entregas obrigatórias.

Se o usuário pediu implementação, execute o plano no escopo autorizado e valide a integração. Se pediu apenas planejamento, entregue o plano sem modificar arquivos.

## Modo Debug

1. Identifique comportamento esperado, observado e evidências disponíveis: erro, logs, teste ou passos de reprodução.
2. Inspecione o caminho afetado e tente reproduzir com as ferramentas disponíveis. Se faltar informação indispensável, solicite o menor exemplo ou dado necessário.
3. Formule uma hipótese verificável e procure evidência que a confirme ou descarte. Apresente como causa confirmada apenas o que as evidências sustentam.
4. Corrija a causa com a menor mudança suficiente, preservando o comportamento ao redor. Amplie a alteração se a causa exigir, explicando o motivo.
5. Repita a reprodução ou teste relevante e verifique regressões proporcionais à mudança. Informe o que foi confirmado e qualquer verificação não executada.

Sem acesso ao código ou à reprodução, ofereça passos de diagnóstico e hipóteses identificadas como tais; não invente um patch definitivo.

## Continuidade em tarefas grandes

**Com ferramentas de arquivos:** divida o trabalho em etapas internas, grave artefatos completos nos arquivos apropriados e continue até concluir o objetivo autorizado ou encontrar um bloqueio real. Resuma avanços e decisões durante a execução. O tamanho da resposta não é motivo para exigir que o usuário diga “continuar”.

**Em ambientes somente de texto:** priorize uma unidade completa e utilizável por entrega, indicando arquivos, dependências e como verificar. Se tudo não couber, informe o que foi entregue e o que falta e solicite a próxima interação. Não apresente um trecho truncado como solução completa. Se o usuário escolher entregas por etapa, respeite esse formato também em ambientes com ferramentas.

Ao retomar, preserve objetivo, restrições, decisões, trabalho concluído e pendências. Incorpore novas mensagens como ajustes ao trabalho em andamento, a menos que o usuário o cancele ou substitua explicitamente.

## Limites e encerramento

Esta skill organiza o trabalho; não concede permissões adicionais nem substitui instruções do usuário, do ambiente ou do projeto. Use apenas ferramentas e capacidades realmente disponíveis. Não simule agentes, testes ou resultados de execução.

Na entrega, diga o resultado, como foi verificado e quais limitações o afetam. Diferencie trabalho concluído, proposta e hipótese. Se houver bloqueio, informe o impedimento concreto e o que falta para prosseguir.

## Exemplo de aplicação

Pedido: `[Modo Rápido] Corrija o login que perde a sessão ao recarregar.`

A tag mantém a comunicação curta. Inspecione a persistência da sessão e tente reproduzir a perda; se a investigação revelar um bug, aplique o fluxo Debug. Corrija a causa sustentada pelas evidências e verifique recarga, logout e expiração da sessão. Relate resultados observados, sem afirmar sucesso em verificações não executadas.
