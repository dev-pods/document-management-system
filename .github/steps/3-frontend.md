# Passo 3: Frontend com Agent Mode

Com o backend pronto, construa a interface do DMS em React + Vite usando o
Agent Mode.

## Objetivo

Criar a interface que permite enviar, listar e baixar documentos, consumindo a
API do backend via `fetch`.

## O que você vai fazer

1. No modo **Agent**, crie os componentes em `frontend/src/components`:
   - `UploadComponent`
   - `DocumentList`
   - `DownloadButton`
2. Crie o cliente de API em `frontend/src/services` que consome o backend pelo
   prefixo `/api` (proxy já configurado no Vite).
3. Monte a página principal reutilizando os componentes.

## Prompt sugerido

```
Crie os componentes UploadComponent, DocumentList e DownloadButton em
frontend/src/components e um cliente de API em frontend/src/services que
consome o backend via fetch usando o prefixo /api. Atualize App.jsx para
montar a interface de upload, listagem e download. Use componentes funcionais
com hooks e evite duplicação.
```

## Validação manual

Rode os dois servidores em terminais separados:

```bash
cd backend && npm run dev
cd frontend && npm run dev
```

Abra o frontend, envie um arquivo e confirme que ele aparece na lista e pode
ser baixado.

## Conclusão do passo

Faça commit dos componentes e do serviço e push na branch `feature/dms`:

```bash
git add frontend/src
git commit -m "feat: interface de upload, listagem e download"
git push
```

A automação valida os componentes e libera o Passo 4.

---

## Ponto de discussão (15 min)

Antes de seguir, pare para a dinâmica em grupo. Compartilhem prompts que
funcionaram melhor, decisões de arquitetura e diferenças entre as soluções
geradas pelos agentes. Esta troca alinha o grupo antes dos módulos avançados.
