# Apresentações GLP Laboratórios — site estático

Pasta pronta para publicar no GitHub Pages. Nenhuma dependência externa:
fontes, fotos, logos e certificados estão embutidos em cada arquivo.

## Conteúdo

| Arquivo | O que é |
|---|---|
| `index.html` | Índice com os cards das cinco apresentações |
| `mineracao.html` | Mineração — 17 slides |
| `institucional.html` | Institucional — 16 slides |
| `laboratorios-parceiros.html` | Laboratórios Parceiros — 12 slides |
| `alimentos.html` | Alimentos — 10 slides |
| `integracao.html` | Integração / onboarding — 9 slides (uso interno) |
| `.nojekyll` | Impede o GitHub de processar os arquivos com Jekyll |
| `robots.txt` | Pede aos buscadores para não indexar |

## Como publicar

1. Crie um repositório no GitHub (pode ser público — o conteúdo não é secreto,
   mas nenhuma página é indexável).
2. Suba **o conteúdo desta pasta na raiz do repositório**, não a pasta em si.
   O `index.html` precisa ficar na raiz.
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

As apresentações também estão publicadas como artifacts no Claude, onde são
atualizadas em cima do mesmo link. Estes arquivos são uma cópia do momento em
que foram gerados: para atualizar aqui, é preciso gerar de novo e subir por cima.
