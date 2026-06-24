# Passo 6: Automação com o Coding Agent

No último passo obrigatório você vai automatizar o projeto delegando a criação da
pipeline e dos testes ao Copilot Coding Agent.

## Objetivo

Criar uma pipeline de CI no GitHub Actions que instala dependências, builda e
roda os testes, além de ampliar a cobertura de testes do backend.

## O que você vai fazer

1. Abra uma issue descrevendo a pipeline desejada e atribua ao Copilot Coding
   Agent (cloud), disponível no seu ambiente.
2. Alternativamente, use o Agent Mode local para criar o workflow.
3. Garanta que a pipeline cobre: install, build e test.

## Prompt sugerido para a issue

```
Crie um workflow de CI em .github/workflows/ci.yml que, em push e pull_request:
instala as dependências do backend e do frontend, builda o frontend e roda os
testes do backend com npm test. Adicione também testes para os endpoints de
upload, listagem e download.
```

## Critério de conclusão

A automação valida que existe um arquivo `.github/workflows/ci.yml`.

Sincronize sua `main` local com o remoto e crie uma branch dedicada para a
automação:

```bash
git checkout main
git pull origin main
git checkout -b chore/ci
git add .github/workflows/ci.yml backend/test
git commit -m "ci: pipeline de install, build e test"
git push -u origin chore/ci
```

Quando a automação encontrar a pipeline na branch, o passo de encerramento é
liberado. Para concluir o projeto, **abra um último Pull Request da `chore/ci`
para a `main` e faça o merge**.
