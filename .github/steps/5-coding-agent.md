# Passo 5: Análise e refatoração com o Coding Agent

Agora você vai usar o Coding Agent do GitHub Copilot para analisar o projeto em
profundidade e refatorar com contexto ampliado.

## Objetivo

Identificar problemas de arquitetura, code smells e duplicações, e aplicar
melhorias seguindo SOLID, sem quebrar funcionalidades.

## O que você vai fazer

1. Use o agente customizado `code-reviewer` (`.github/agents/code-reviewer.agent.md`)
   para uma análise profunda do codebase.
2. Peça uma lista priorizada de melhorias.
3. Use o handoff **Aplicar refatoração** para transicionar do review para a
   implementação das melhorias.

## Prompt sugerido

```
Faça uma análise profunda do backend e do frontend do DMS. Liste, de forma
priorizada, problemas de arquitetura, code smells, duplicações e riscos de
segurança (por exemplo, path traversal em upload e download). Para cada item,
explique o problema, justifique e proponha a melhoria.
```

## Delegar ao Coding Agent (cloud)

Para tarefas maiores, você pode delegar a refatoração ao Copilot Coding Agent
abrindo uma issue e atribuindo-a ao Copilot. O agente trabalha em segundo plano
e abre um Pull Request com as mudanças.

```
Refatore a camada de serviço do DMS para reduzir duplicação e aplicar o
princípio de responsabilidade única, mantendo todos os testes verdes.
```

## Conclusão do passo

A refatoração acontece em uma **branch dedicada**. Sincronize a `main` (já com o
trabalho do Passo 4) e crie a branch `refactor/solid`:

```bash
git checkout main
git pull origin main
git checkout -b refactor/solid
```

Aplique a refatoração nessa branch (com o Agent Mode local ou trazendo as
mudanças sugeridas pelo Coding Agent) e publique:

```bash
git add .
git commit -m "refactor: aplicar SOLID e remover duplicações"
git push -u origin refactor/solid
```

O push para a branch `refactor/solid` libera o Passo 6. Em seguida, **abra um
Pull Request de `refactor/solid` para a `main` e faça o merge** para integrar a
refatoração.
