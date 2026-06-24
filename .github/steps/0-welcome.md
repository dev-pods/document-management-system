# Setup do ambiente

Bem-vindo ao workshop. Neste passo você prepara o ambiente para os próximos
módulos.

## O que você vai fazer

1. Garantir que o repositório foi criado a partir do template.
2. Abrir o projeto em um GitHub Codespace.
3. Validar que o GitHub Copilot está ativo.

## Passo a passo

1. No seu repositório, clique em **Code > Codespaces > Create codespace on main** ou clique no atalho abaixo.

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

2. Aguarde o ambiente subir. As extensões `GitHub.copilot` e
   `GitHub.copilot-chat` já vêm configuradas.
3. Abra o chat do Copilot e confirme que ele responde.
4. Instale as dependências do seed:

   ```bash
   cd backend && npm install
   cd ../frontend && npm install
   ```

5. Rode o teste de fumaça do backend:

   ```bash
   cd backend && npm test
   ```

6. Crie a branch de trabalho do exercício e publique-a. Você vai desenvolver os
   Passos 1 a 4 nela e integrá-la à `main` por Pull Request ao final do Passo 4:

   ```bash
   git checkout -b feature/dms
   git push -u origin feature/dms
   ```

## Conclusão do passo

O setup não exige validação automática. Com o ambiente pronto, os testes do seed
passando e a branch `feature/dms` publicada, siga para o **Passo 1: Planejamento**,
publicado logo abaixo nesta issue.
