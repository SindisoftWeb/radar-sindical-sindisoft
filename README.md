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
image: "/images/artigos/capa-do-artigo.png"
imageAlt: "Descrição objetiva e acessível da imagem"
imageCredit: "Sindisoft / nome da fonte autorizada"
imageSourceUrl: "https://url-original-permitida.exemplo/"
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


## Padrão de imagens dos artigos

Cada artigo pode ter uma **imagem principal** no frontmatter. Essa imagem é exibida automaticamente na capa do artigo, no cartão da biblioteca, no destaque da página inicial e em metadados Open Graph usados por redes sociais.

- **Sindisoft na prática e guias de gestão:** priorize reaproveitar a arte original já publicada no Instagram oficial da Sindisoft ou imagens/telas oficialmente autorizadas do sistema. Preserve arquivo e logotipo oficiais, sem recriação ou adulteração.
- **Notícias sindicais:** procure primeiro uma imagem/fotografia oficial com autorização expressa de reprodução ou licença compatível; verifique licença e condições de crédito. Ser fonte oficial **não implica** licença de reutilização. Registre autor, órgão e URL da imagem. Não copie fotografia de portal de notícias nem use hotlink não autorizado.
- **Sem imagem licenciada:** prefira uma arte editorial própria feita com recursos da marca e o logotipo original do Project (se houver acesso seguro ao arquivo) ou mantenha o fallback tipográfico. **Nunca invente URL de imagem.**
- **Formato e acessibilidade:** dê preferência a PNG/JPG/WebP nítidos e preencha `imageAlt` com descrição significativa. **Nos cards da página inicial**, a imagem ocupa um quadrado completo (`aspect-ratio: 1/1`, `object-fit: cover`), com corte central quando necessário. **Dentro do artigo**, a imagem é exibida integralmente (`object-fit: contain`). Evite posicionar textos essenciais próximos às extremidades das artes destinadas a capas.
- **Hospedagem:** prefira arquivos de imagem sob `public/images/artigos/` no próprio repositório. Referências existentes a `static.metricool.com` são origens da conta oficial e devem ser posteriormente migradas para hospedagem controlada pela Sindisoft para evitar links quebrados; o layout possui fallback visual caso a URL externa falhe.
- **Crédito:** preencha `imageCredit` e, quando disponível, `imageSourceUrl`, especialmente em notícias. Não trate o crédito como substituto de uma autorização de uso.
- **Conferência:** depois da implantação Cloudflare, valide no celular e no desktop o carregamento da imagem, o alt text, ausência de cortes e a prévia do compartilhamento LinkedIn/Facebook.

**Importante:** separar sempre data da notícia original, data da publicação do Radar e os metadados da imagem. Não afirmar que uma imagem é liberada apenas porque aparece em site público.
