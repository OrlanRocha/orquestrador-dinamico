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

1. **⚡ Modo Rápido:** Para dúvidas rápidas, scripts curtos (ex: PowerShell, bash) e CSS. Sem enrolação, entrega direta.
2. **🏗️ Modo Arquiteto:** Para planejamento de sistemas (PHP, JS, SQL). Pensa passo a passo, define estrutura e arquitetura antes de codar.
3. **🐛 Modo Debug:** Focado em caçar bugs e ler logs. Resolve a causa raiz e entrega a correção isolada.

## 🕹️ Gatilhos Manuais
Você pode forçar a IA a entrar em um modo específico colocando uma destas tags no início da sua mensagem:
- `[Modo Rápido]`
- `[Modo Arquiteto]`
- `[Modo Debug]`

## 📦 Auto-Pacing (Para códigos longos)
A skill foi projetada para prever o limite de tokens da IA. Se um script for muito grande, ela entregará o código em blocos funcionais e pedirá para você dizer "continuar", evitando que a resposta pare pela metade.
