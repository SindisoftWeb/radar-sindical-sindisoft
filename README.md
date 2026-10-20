# Radar Sindical — Sindisoft

Portal editorial da Sindisoft construído com Astro e preparado para publicação estática pelo Cloudflare Pages.

## Configuração no Cloudflare Pages

- Framework preset: **Astro**
- Build command: **npm run build**
- Build output directory: **dist**
- Root directory: **(em branco)**
- Production branch: **main**

## Desenvolvimento

Instale Node.js 20.3+ e execute:

- `npm install`
- `npm run dev`
- `npm run build`

## Como publicar artigos novos pelo GitHub ou ChatGPT

Crie um arquivo Markdown em `src/pages/artigos/nome-do-artigo.md`:

```md
---
layout: ../../layouts/ArticleLayout.astro
title: "Título do artigo"
description: "Resumo curto e informativo"
category: "Gestão sindical"
date: "2026-10-20"
readingTime: "4 min"
---

Texto do artigo em Markdown.
```

O Astro gera automaticamente a página do novo artigo; a página inicial também o incluirá na lista pesquisável. Após cada commit na branch `main`, o Cloudflare Pages compila e publica a nova versão.

## Diretrizes editoriais

- Os três artigos iniciais são guias práticos originais, não notícias factuais recentes.
- Notícias devem ter fonte confiável e data; não publicar notícias inventadas ou informações não verificadas.
- Temas jurídicos, trabalhistas e financeiros exigem conferência das fontes oficiais e revisão técnica quando necessário.
- Não armazenar credenciais, chaves, listas de contatos privados nem dados pessoais sensíveis no repositório público.
- Substituir o símbolo gráfico temporário pela identidade oficial da Sindisoft quando houver arquivo de marca autorizado.
- O formulário de newsletter não foi ativado; só deve ser implementado com ferramenta de coleta e consentimento apropriados.
