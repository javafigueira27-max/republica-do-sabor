# República do Sabor — versão preparada para Vercel

Esta pasta foi preparada para deploy na Vercel usando Express/Node.js.

## Deploy
1. Crie um repositório no GitHub e envie todo o conteúdo desta pasta.
2. Na Vercel: Add New → Project → importe o repositório.
3. Não defina Build Command personalizado. O projeto já possui `vercel.json`.
4. Deploy.

## Endereços esperados
- Site: `/`
- Cardápio: `/cardapio.html`
- Galeria: `/galeria.html`
- Sobre: `/sobre.html`
- Contactos: `/contactos.html`
- Admin: `/admin`

## Importante sobre os dados
A aplicação original grava `data/*.json` e uploads em `public/images/`. Esse armazenamento local é adequado para desenvolvimento/local, mas não deve ser considerado persistente em execução serverless. O site pode abrir e as APIs podem responder, porém alterações feitas no painel podem não sobreviver a novas instâncias/deploys.

Para produção com administração persistente, a próxima etapa deve migrar os dados/uploads para armazenamento persistente (por exemplo, Vercel Blob/Drive ou uma base de dados externa).

## Node.js
O projeto está configurado para Node 24.x, evitando a descontinuação do Node 20 na Vercel em outubro de 2026.
