# Materiais comerciais GLP Laboratórios — site estático

Pasta pronta para publicar no GitHub Pages. Nenhuma dependência externa: fontes, fotos,
logos e certificados ficam na pasta `assets/`, compartilhada por todas as páginas (cada
imagem existe uma vez só, mesmo quando aparece em vários decks e nas versões PT e EN).

## Conteúdo

| Arquivo | O que é |
|---|---|
| `index.html` | Página inicial: apresentações e materiais de apoio, um card por item (botões PT/EN e download de PDF) |
| `mineracao.html` / `mineracao-en.html` | Mineração / Mining — 17 slides |
| `institucional.html` / `institucional-en.html` | Institucional / Corporate — 16 slides |
| `laboratorios-parceiros.html` / `…-en.html` | Laboratórios Parceiros / Partner Laboratories — 12 slides |
| `alimentos.html` / `alimentos-en.html` | Alimentos / Food — 10 slides |
| `oleo-gas.html` / `oleo-gas-en.html` | Óleo & Gás / Oil & Gas — 17 slides |
| `integracao.html` / `integracao-en.html` | Integração / Onboarding — 9 slides (uso interno) |
| `*.pdf` | O PDF de cada apresentação, com o mesmo nome da página |
| `materiais/` | One-pages (`onepage-<tema>-pt.pdf` / `-en.pdf`: mineracao, oleo-gas, alimentos, agua, laboratorios-parceiros, wipe-test) e o artigo do Wipe Test (`artigo-wipe-test-pt.pdf` / `-en.pdf`) |
| `assets/` | Imagens e fontes usadas pelas páginas — **precisa ir junto** |
| `.nojekyll` | Impede o GitHub de processar os arquivos com Jekyll |
| `robots.txt` | Pede aos buscadores para não indexar |

## Materiais de apoio (one-pages e artigo)

Os PDFs ficam em `materiais/` e aparecem na seção **Materiais de apoio** do `index.html`,
cada um em português e inglês. As miniaturas dos cards são `assets/th-*.webp`.
Para trocar um one-page, substitua o PDF em `materiais/` mantendo o mesmo nome — o card
continua funcionando. Contato padrão nos materiais: `vendas@glplab.com.br`,
`propostas@glplab.com.br` e WhatsApp +55 19 98455-9001.

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

### Modo apresentação (todas as apresentações, PT e EN)

- `P` ou botão **Modo apresentador** — abre uma segunda janela com slide atual, próximo
  slide, notas, relógio e cronômetro. As duas janelas andam juntas.
  Nos decks em inglês a janela do apresentador, os botões e as notas ficam em inglês
  (**Presenter mode**).
- Projetor/TV: arraste a janela dos slides para a segunda tela e aperte `F` nela.
  Teams/Meet: compartilhe só a **janela** dos slides.
- `L` — apontador laser (na janela do apresentador, passe o mouse sobre o slide atual)
- `B` ou `.` — tela preta · `T` — pausa o cronômetro (janela do apresentador)
- Passadores comuns funcionam (PageDown/PageUp; `F5` entra em tela cheia)
- As notas ficam em `window.__notes`, perto do fim de cada arquivo, uma lista de tópicos por
  slide (a ordem segue a dos slides). Para mudar uma nota, edite o texto dentro dessa lista.
  O idioma da janela do apresentador segue o atributo `lang` da página (`pt-BR` ou `en`).
- Atenção: as notas fazem parte do arquivo publicado, então quem abre o código da página
  consegue lê-las.

## Atualizar

Estes arquivos são uma cópia do momento em que foram gerados: para atualizar, gere de novo
e suba por cima. Os nomes das imagens em `assets/` mudam quando a imagem muda, então vale
apagar a pasta `assets/` antiga do repositório antes de subir a nova, para não acumular
arquivos que ninguém usa mais.
