# Passo 4: Agentes da comunidade e customizados

Neste passo você aprende a personalizar o comportamento do GitHub Copilot com
três níveis de customização e a aproveitar agentes da comunidade.

## Contextualização: os três níveis de customização

Muita gente conhece apenas os prompt files. Existem três mecanismos
complementares, e vale entender quando usar cada um.

| Recurso             | Onde fica                          | O que é                                                        | Quando usar                                                  |
| ------------------- | ---------------------------------- | -------------------------------------------------------------- | ------------------------------------------------------------ |
| Custom instructions | `.github/copilot-instructions.md`  | Regras aplicadas automaticamente a todo prompt                 | Convenções do projeto (stack, arquitetura, upload local)     |
| Custom agent        | `.github/agents/*.agent.md`        | Persona persistente com ferramentas restritas, modelo e handoffs | Papéis: planner (só leitura), reviewer, TDD                  |
| Prompt file         | `.github/prompts/*.prompt.md`      | Tarefa única invocada manualmente via `/comando`               | Scaffolding, gerar testes, preparar PR                       |

### Atualização de nomenclatura (importante)

O que antes era chamado de **custom chat modes** (`*.chatmode.md`) passou a se
chamar **custom agents**, com a extensão `*.agent.md`, na pasta `.github/agents`.
O formato `*.chatmode.md` é legado. Neste workshop usamos `*.agent.md`.

### Handoffs

Um diferencial dos custom agents são os **handoffs**: botões que transicionam de
um agente para outro com um prompt pré-preenchido. Isso permite fluxos guiados
como **Planner -> Implementação -> Reviewer**, exatamente o fluxo deste
treinamento. Os handoffs são declarados no frontmatter do arquivo do agente.

## O que você vai fazer

1. Explore os custom agents já incluídos em `.github/agents`:
   - `planner.agent.md`
   - `code-reviewer.agent.md`
   - `tdd.agent.md`
2. Abra o seletor de agentes no chat com `/agents` e o de prompts com `/prompts`.
3. Crie pelo menos um prompt file próprio em `.github/prompts` para uma tarefa
   recorrente do seu fluxo.
4. Explore o repositório da comunidade [awesome-copilot](https://github.com/github/awesome-copilot)
   e adapte um agente ou prompt útil para o projeto.

## Conclusão do passo

Faça commit das suas customizações e push na branch `feature/dms`:

```bash
git add .github/agents .github/prompts
git commit -m "feat: agentes customizados e prompt files"
git push
```

A automação valida a presença de um custom agent e de um prompt file e libera o
Passo 5.

Com isso encerramos o trabalho em Agent Mode. **Abra um Pull Request da branch
`feature/dms` para a `main` e faça o merge** para integrar os Passos 1 a 4. Os
próximos passos partem da `main` já atualizada.
