# Orquestrador Dinâmico para LLMs 🧠⚙️

Um *System Prompt* universal projetado para transformar assistentes de IA (Google Antigravity, OpenAI Codex/ChatGPT, Anthropic Claude) em parceiros de desenvolvimento adaptáveis. 

Em vez de tratar todos os prompts da mesma forma, este orquestrador ajusta a profundidade, a verbosidade e a abordagem da IA de acordo com a complexidade da tarefa, evitando interrupções em códigos longos e economizando tempo em tarefas simples.

## 🚀 Como usar

Copie o conteúdo do arquivo `prompt-orquestrador.md` e cole na área de **Instruções de Sistema** (System Prompt) da sua plataforma favorita:

- **Google AI Studio / Antigravity:** Cole no campo "System Instructions".
- **ChatGPT (OpenAI):** Cole em "Custom Instructions" ou envie como a primeira mensagem de um projeto.
- **Claude (Anthropic):** Use na configuração de "Project Instructions" ou na API via parâmetro `system`.

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
