# Passo 2: Backend com Agent Mode

Agora você vai construir o backend do DMS usando o Agent Mode do GitHub Copilot.
O agente edita arquivos, executa comandos e itera com você.

## Objetivo

Implementar o backend funcional com upload, listagem e download, seguindo a
Clean Architecture simples.

## O que você vai fazer

1. Selecione o modo **Agent** no chat do Copilot.
2. Construa as quatro camadas em `backend/src`:
   - `routes/` define os endpoints e delega aos controllers
   - `controllers/` tratam entrada/saída HTTP e validação básica
   - `services/` concentram as regras de negócio
   - `repositories/` cuidam da persistência
3. Implemente os endpoints:
   - `POST /upload`
   - `GET /documents`
   - `GET /documents/:id/download`

## Dica: use o prompt file de scaffold

Experimente o prompt reutilizável `/scaffold-camada` (definido em
`.github/prompts/scaffold-camada.prompt.md`) para gerar a estrutura da camada de
documentos.

## Prompt sugerido

```
Implemente o backend do DMS no diretório backend/src seguindo a Clean
Architecture simples. Crie as rotas POST /upload, GET /documents e
GET /documents/:id/download. Use multer com diskStorage gravando em
backend/storage e mantenha os metadados em memória. Registre o roteador no
backend/src/app.js.
```

## Restrição importante

Uploads são gravados no filesystem local da aplicação com `multer` e
`diskStorage`. Não utilize provedores externos.

## Conclusão do passo

Garanta que o backend sobe e que os testes passam:

```bash
cd backend && npm test
```

Faça commit das camadas e push na branch `feature/dms`:

```bash
git add backend/src
git commit -m "feat: backend com upload, listagem e download"
git push
```

A automação valida a presença das camadas e libera o Passo 3.
