# Apresentações GLP Laboratórios — site estático

Pasta pronta para publicar no GitHub Pages. Nenhuma dependência externa: fontes, fotos,
logos e certificados ficam na pasta `assets/`, compartilhada por todas as páginas (cada
imagem existe uma vez só, mesmo quando aparece em vários decks e nas versões PT e EN).

## Conteúdo

| Arquivo | O que é |
|---|---|
| `index.html` | Índice com um card por apresentação (botões PT/EN e download de PDF) |
| `mineracao.html` / `mineracao-en.html` | Mineração / Mining — 17 slides |
| `institucional.html` / `institucional-en.html` | Institucional / Corporate — 16 slides |
| `laboratorios-parceiros.html` / `…-en.html` | Laboratórios Parceiros / Partner Laboratories — 12 slides |
| `alimentos.html` / `alimentos-en.html` | Alimentos / Food — 10 slides |
| `oleo-gas.html` / `oleo-gas-en.html` | Óleo & Gás / Oil & Gas — 17 slides |
| `integracao.html` / `integracao-en.html` | Integração / Onboarding — 9 slides (uso interno) |
| `*.pdf` | O PDF de cada apresentação, com o mesmo nome da página |
| `assets/` | Imagens e fontes usadas pelas páginas — **precisa ir junto** |
| `.nojekyll` | Impede o GitHub de processar os arquivos com Jekyll |
| `robots.txt` | Pede aos buscadores para não indexar |

## Como publicar

1. Crie um repositório no GitHub (pode ser público — o conteúdo não é secreto,
   mas nenhuma página é indexável).
2. Suba **o conteúdo desta pasta na raiz do repositório**, não a pasta em si.
   O `index.html` precisa ficar na raiz, com a pasta `assets/` ao lado.
3. No repositório: **Settings → Pages → Source: Deploy from a branch**,
   branch `main`, pasta `/ (root)`. Salve.
4. Em um ou dois minutos o site sai em
   `https://SEU-USUARIO.github.io/NOME-DO-REPO/`.

O arquivo `.nojekyll` precisa ir junto. Sem ele o GitHub roda o Jekyll,
que pode ignorar arquivos.

## Domínio próprio (opcional)

Para publicar em `apresentacoes.glplab.com.br`:

1. Crie um arquivo `CNAME` na raiz do repositório com uma única linha:
   `apresentacoes.glplab.com.br`
2. No DNS do domínio, crie um registro CNAME apontando
   `apresentacoes` para `SEU-USUARIO.github.io`.
3. Em Settings → Pages, preencha o campo Custom domain e marque
   **Enforce HTTPS**.

## Sobre a não indexação

Todas as páginas trazem `<meta name="robots" content="noindex,nofollow">`,
que é o mecanismo que efetivamente funciona.

O `robots.txt` só é lido pelos buscadores quando está na **raiz do domínio**.
Num endereço do tipo `usuario.github.io/repo/`, a raiz é `usuario.github.io/`,
que pertence a outro repositório — então ali o `robots.txt` desta pasta é
ignorado e a meta tag é o que segura. Com domínio próprio, os dois passam a valer.

## Como usar as apresentações

- `←` `→` ou clique nas laterais — navegar
- `O` — visão geral com miniaturas
- `F` — tela cheia
- `#7` no fim do endereço abre direto no slide 7
- Botão **← Índice** na barra inferior volta para a página inicial

## Atualizar

Estes arquivos são uma cópia do momento em que foram gerados: para atualizar, gere de novo
e suba por cima. Os nomes das imagens em `assets/` mudam quando a imagem muda, então vale
apagar a pasta `assets/` antiga do repositório antes de subir a nova, para não acumular
arquivos que ninguém usa mais.
