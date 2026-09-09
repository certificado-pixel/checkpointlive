# AEPRO × Monopolize — Plano interno

Site estático (1 arquivo, sem build) com o plano de ativação da live "Monopolize White Label" — uso interno da equipe. Não é indexado por buscadores (`<meta name="robots" content="noindex, nofollow">`), mas fica publicamente acessível a quem tiver o link — não é um ambiente com senha.

## Subir no GitHub

Dentro da pasta com o `index.html`:

```bash
git init
git add index.html logo.png favicon.png README.md
git commit -m "Plano interno: live Monopolize White Label"
git branch -M main
git remote add origin <URL_DO_SEU_REPO_VAZIO>
git push -u origin main
```

## Publicar na Vercel

1. Acesse vercel.com → **Add New… → Project**.
2. Importe o repositório que você acabou de subir.
3. Não precisa configurar nada (é HTML puro, sem framework) — clique em **Deploy**.
4. A Vercel te dá uma URL pública (algo como `plano-monopolize.vercel.app`); dá pra trocar depois por um domínio próprio em **Settings → Domains**.

## O que ainda falta / detalhes

- As marcações de checklist e os campos editáveis (metas, números) salvam no **localStorage do navegador** de quem acessa — não sincronizam entre computadores nem entre pessoas da equipe. Se quiserem que todo mundo veja o mesmo estado compartilhado, precisa de um backend simples (planilha, banco, ou similar).
- O link "← voltar para a página de inscrição" no topo aponta para `https://paulotomas.vercel.app/` (o site público da live). Se o domínio da landing mudar, atualize esse link no `index.html`.
- Datas e números do plano estão fixos no HTML — edite direto o arquivo se algo mudar (data da live, metas, etc).
