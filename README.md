# Orquestrador Dinâmico para LLMs 🧠⚙️

Um *System Prompt* e **Skill Nativa** universal projetada para transformar assistentes de IA (Google Antigravity, Anthropic Claude Code, OpenAI Codex/ChatGPT) em parceiros de desenvolvimento adaptáveis. 

Em vez de tratar todos os prompts da mesma forma, este orquestrador ajusta a profundidade, a verbosidade e a abordagem da IA de acordo com a complexidade da tarefa, evitando interrupções em códigos longos e economizando tempo em tarefas simples.

## 🚀 Como instalar como Skill Nativa (Antigravity, Claude Code, Codex)

Esta skill possui suporte nativo à infraestrutura global de habilidades (*Global Skills*) utilizando o arquivo `SKILL.md`. Siga os passos abaixo de acordo com seu ambiente:

### Para Google Antigravity / Superpowers
1. Clone este repositório para o seu diretório de skills local:
   ```bash
   git clone https://github.com/OrlanRocha/orquestrador-dinamico.git ~/.gemini/skills/orquestrador-dinamico
   ```
2. O agente carregará o `SKILL.md` automaticamente durante conversas quando você precisar de adaptação dinâmica.

### Para Claude Code
1. Clone o repositório na sua pasta de skills do Claude:
   ```bash
   git clone https://github.com/OrlanRocha/orquestrador-dinamico.git ~/.claude/skills/orquestrador-dinamico
   ```

### Para Codex / Outros CLI
1. Clone o repositório na pasta de agentes global:
   ```bash
   git clone https://github.com/OrlanRocha/orquestrador-dinamico.git ~/.agents/skills/orquestrador-dinamico
   ```

---

## 📝 Como usar como System Prompt Clássico (ChatGPT, Web UIs)

Caso não use ferramentas de CLI com suporte a skills, copie o conteúdo do arquivo `prompt-orquestrador.md` e cole na área de **Instruções de Sistema**:

- **Google AI Studio:** Cole no campo "System Instructions".
- **ChatGPT (OpenAI):** Cole em "Custom Instructions" ou envie como a primeira mensagem de um projeto.
- **Claude (Web):** Use na configuração de "Project Instructions".

---

## ⚙️ Modos Automáticos

A IA alternará silenciosamente entre os seguintes modos conforme a necessidade:

1. **⚡ Modo Rápido:** Para pedidos bem definidos, localizados e de baixo impacto. Entrega direta com verificação proporcional.
2. **🏗️ Modo Arquiteto:** Para decisões estruturais e dependências. Recomenda uma solução justificada e implementa quando solicitado.
3. **🐛 Modo Debug:** Reproduz problemas, testa hipóteses e corrige causas sustentadas por evidências, verificando o resultado.

## 🕹️ Gatilhos Manuais
Você pode forçar a IA a entrar em um modo específico colocando uma destas tags no início da sua mensagem:
- `[Modo Rápido]`
- `[Modo Arquiteto]`
- `[Modo Debug]`

As tags selecionam a abordagem e o estilo de comunicação, preservando evidências, verificações e limites de autorização.

## 📦 Continuidade em tarefas grandes

Com ferramentas de arquivos, a skill organiza etapas internas e continua até concluir o objetivo ou encontrar um bloqueio real, sem exigir “continuar” por causa do tamanho do código.

Em ambientes somente de texto, entrega unidades completas e utilizáveis. Se o trabalho não couber em uma resposta, informa o que foi entregue e o que falta antes de solicitar a próxima interação. Entregas por etapa também podem ser escolhidas pelo usuário.

O `SKILL.md` é a referência para a skill; `prompt-orquestrador.md` é a versão autocontida para instruções textuais. Nenhuma versão concede permissões adicionais ou garante capacidades que o ambiente não oferece.
