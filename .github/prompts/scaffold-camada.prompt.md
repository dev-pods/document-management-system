---
description: Cria uma camada completa do backend (route, controller, service, repository) para um recurso.
name: scaffold-camada
argument-hint: nome do recurso (ex. documents)
agent: agent
---

# Scaffold de camada do backend

Crie a estrutura completa de uma camada para o recurso `${input:recurso:nome do recurso}` seguindo a Clean Architecture simples do projeto.

Gere os arquivos em `backend/src`:

1. `routes/${input:recurso}.routes.js` - define os endpoints e delega ao controller.
2. `controllers/${input:recurso}.controller.js` - trata entrada/saída HTTP e validação básica.
3. `services/${input:recurso}.service.js` - concentra as regras de negócio.
4. `repositories/${input:recurso}.repository.js` - cuida da persistência.

Requisitos:

- Respeite o fluxo `routes -> controllers -> services -> repositories`.
- Uploads gravados no filesystem local via multer com diskStorage.
- Metadados em memória nesta fase.
- Trate erros nos limites do sistema.
