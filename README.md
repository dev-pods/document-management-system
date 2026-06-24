# Document Management System com GitHub Copilot

_Domine o Agent Mode e o Coding Agent do GitHub Copilot construindo um sistema
completo de gestão de documentos._

## Bem-vindo

- **Para quem é:** equipes de desenvolvimento que querem dominar fluxos de
  trabalho avançados com agentes do GitHub Copilot.
- **O que você vai aprender:** planejar com Plan Mode, delegar tarefas a agentes,
  usar diferentes modos de agente, aproveitar agentes da comunidade e acionar o
  Coding Agent para análise, refatoração e automação.
- **O que você vai construir:** um sistema de gestão de documentos — o Document
  Management System (DMS) — com upload, listagem e download de documentos, com
  backend Node.js + Express e frontend React + Vite.
- **Pré-requisitos:**
  - Conta GitHub com acesso ao GitHub Copilot e ao Copilot Coding Agent
  - Familiaridade com VS Code
  - Noções de JavaScript e APIs REST
- **Duração:** aproximadamente 4 horas.

## Como funciona este exercício

Este é um exercício autoguiado no formato GitHub Skills. Ao criar o repositório a
partir do template, a **Mona** abre uma **issue de
acompanhamento** e publica o primeiro passo lá. Você desenvolve em branches de
trabalho e, a cada `commit` e `push`, um fluxo de automação valida seu progresso
e publica o próximo passo como um novo comentário na issue. Os Passos 1 a 4
acontecem na branch `feature/dms` (criada no setup), integrada à `main` por Pull
Request ao final do Passo 4. A refatoração (Passo 5) e a automação (Passo 6) usam
branches dedicadas (`refactor/solid` e `chore/ci`), criadas a partir da `main`
atualizada, e também são integradas por Pull Request — praticando o fluxo real de
trabalho.

### Como iniciar

1. Crie um repositório a partir deste template.

   [![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?style=for-the-badge&logo=github&logoColor=white)](https://github.com/new?template_owner=dev-pods&template_name=document-management-system&owner=%40me&name=document-management-system&description=Exerc%C3%ADcio:+GitHub+Copilot+(Agent+Mode+%2B+Coding+Agent)&visibility=public)
   
2. Aguarde cerca de 20 segundos e atualize a aba **Issues** do repositório: a
   issue do exercício será criada com o setup e o Passo 1.
3. Abra o projeto em um GitHub Codespace (ambiente já configurado com Node.js e as extensões do GitHub Copilot).

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

## Agenda (4 horas)

| Passo | Tema                              | Modo do Copilot           | Tempo |
| ----- | --------------------------------- | ------------------------- | ----- |
| -    | Setup do ambiente                 | -                         | 15min |
| 1    | Planejamento                      | Plan Mode                 | 30min |
| 2    | Backend                           | Agent Mode                | 45min |
| 3    | Frontend                          | Agent Mode                | 30min |
| -    | Ponto de discussão                | -                         | 15min |
| 4    | Agentes da comunidade e customizados | Agent Mode             | 30min |
| 5    | Análise e refatoração             | Coding Agent              | 35min |
| 6    | Automação (CI e testes)           | Coding Agent              | 30min |
| Fim  | Encerramento e módulo avançado    | Agent Mode                | 10min |

## Objetivos de aprendizagem

**Agent Mode**

- Planejar tarefas com o agente de planejamento.
- Delegar tarefas para agentes.
- Utilizar diferentes modos de agente.
- Utilizar agentes disponíveis na comunidade.

**Coding Agent**

- Executar análises profundas de código.
- Refatorar trechos inteiros com contexto ampliado.
- Recomendar padrões arquiteturais.
- Automatizar tarefas de desenvolvimento com raciocínio avançado.

---

&copy; 2026 GitHub &bull; [Código de Conduta](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [Licença MIT](https://gh.io/mit)
