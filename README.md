# 🌲 Wiki — Vale das Araucárias

Wiki do mod **Vale das Araucárias**, que traz a cultura e a biodiversidade do Sul do Brasil para Stardew Valley.

Aqui você encontra informações sobre peixes, plantações, árvores, receitas, personagens e outras novidades do projeto.

## 🌐 Acesse a wiki
[Visite nossa wiki](https://gabriellig-maker.github.io/Vale-das-Arauc-rias-wiki/)

## 📚 Sobre o projeto
Desenvolvido na disciplina **Oficina de Integração 2**, com o núcleo temático **Tecnologia, Poder e Trabalho**.

## 🛠️ Tecnologias
HTML e CSS.

🚧 Projeto em desenvolvimento, com novos conteúdos e atualizações.


## Arquivos

Todos os arquivos ficam na raiz do repositório.

| Arquivo | Para que serve |
|---|---|
| `index.html` | Página principal |
| `peixes.html`, `lavouras.html`, `arvores.html`, `receitas.html` | Listas por assunto |
| `cultivo.html`, `calendario.html`, `conjuntos.html`, `locais.html`, `aldeoes.html` | Guias e páginas temáticas |
| `jundia.html`, `araucaria.html`, `mandioca.html`… | Um artigo por peixe, árvore, lavoura e item processado |
| `sobre.html`, `instalacao.html`, `atualizacoes.html` | Informações do projeto |
| `indice.html`, `busca.html` | Índice alfabético, categorias e pesquisa |
| `gab.html` | Página reservada do aldeão planejado |
| `modelo-artigo.html` | Modelo para criar artigos novos (não aparece nos buscadores) |
| `404.html` | Página de erro usada pelo GitHub Pages |
| `estilo.css` | Todo o visual do site |
| `*.png` | Sprites reais do mod (copiados ou recortados do ZIP 1.8.1) |
| `*.svg` | Logotipos (`logo.svg`, `logo-principal.svg`), céu noturno (`fundo-noite.svg`), moldura de madeira (`moldura.svg`), favicon, ícones e imagens provisórias |
| `.nojekyll` | Arquivo vazio que desliga o processamento Jekyll do GitHub Pages (opcional) 



## Configurar a pesquisa

A wiki não tem busca própria (isso exigiria servidor ou JavaScript). A página `busca.html` envia a pesquisa ao Google,
restrita ao endereço do site. Ela vem configurada para `belfortkafag.github.io/ValeDasAraucariasWiki`.
Se o seu endereço for outro, abra `busca.html` e troque só o `value` desta linha:

```html
<input type="hidden" name="as_sitesearch" value="belfortkafag.github.io/ValeDasAraucariasWiki">
```

A pesquisa só encontra páginas que o Google já indexou; páginas novas podem levar alguns dias.
O índice A–Z (`indice.html`) funciona sempre, sem depender de buscador.

## Editar textos

1. No GitHub, abra o arquivo `.html` e clique no lápis (*Edit this file*).
2. Altere só o texto entre as tags. Exemplo: em `<p>Texto aqui.</p>`, mude apenas `Texto aqui.`
3. Clique em *Commit changes*.

Tabelas: cada linha é um `<tr>` e cada célula é um `<td>` (ou `<th>` no cabeçalho). Para criar uma linha nova,
copie uma linha inteira (`<tr> … </tr>`) e troque o conteúdo.

## Trocar imagens

Os sprites que já existem no mod estão no site: peixes (`jundia.png`), lavouras (`mandioca.png`,
`sementes-de-cevada.png`, `mandioca-estagio-1.png`, `mandioca-maduro.png`), árvores (`araucaria-verao.png`,
`araucaria-estagio-4.png`) e itens (`butia.png`, `farinha-de-milho.png`).

Onde ainda não existe sprite, a página usa uma imagem provisória em SVG com um comentário logo acima:

```html
<!-- IMAGEM: Bisque de Cavaco | substituir por bisque-de-cavaco.png -->
<img src="imagem-alimento.svg" alt="Bisque de Cavaco" width="32" height="32">
```

Para trocar:

1. Envie o arquivo (por exemplo, `bisque-de-cavaco.png`) para a **raiz** do repositório.
2. Mude só o `src`: `src="bisque-de-cavaco.png"`.
3. Se for pixel art, acrescente `class="pixel"` para manter os pixels nítidos.

Use tamanhos múltiplos do original: um sprite de 16×16 fica bom em 32×32 ou 48×48; um de 16×32, em 32×64.

Imagens provisórias disponíveis: `imagem-padrao.svg`, `imagem-peixe.svg`, `imagem-arvore.svg`, `imagem-planta.svg`,
`imagem-personagem.svg`, `imagem-alimento.svg`, `imagem-item.svg` e `imagem-local.svg`
(todas aparecem no fim de `modelo-artigo.html`).

## Criar uma página nova

1. Copie `modelo-artigo.html` e salve com um nome curto, sem acentos e sem espaços (ex.: `pirao-de-peixe.html`).
2. No arquivo novo, troque o `<title>`, a `<meta name="description">`, o `href` da aba **Artigo** e o `<h1>`.
3. Apague a linha `<meta name="robots" content="noindex">`.
4. Preencha a caixa de informações (`infobox`), o sumário e as seções. Apague a seção de imagens provisórias do fim.
5. Coloque um link para a página nova em uma lista (ex.: `receitas.html`) e no `indice.html` (na letra e na categoria).

O menu lateral está repetido em todas as páginas. Para mudar o menu, use *localizar e substituir em todos os arquivos*
de um editor de código, como o editor web do GitHub (aperte `.` na página do repositório) ou o VS Code.

## Fonte dos títulos

Os títulos usam a fonte Open Sans, carregada do Google Fonts pela primeira linha do `estilo.css`.
Sem internet (por exemplo, abrindo os arquivos no computador), o navegador usa uma fonte sem serifa parecida.

## Links

- Para outra página: `<a href="jundia.html">Jundiá</a>`
- Para uma seção: `<a href="peixes.html#covo">Peixes de covo</a>` (o destino precisa ter `id="covo"`)
- Para conteúdo ainda não publicado, sem link quebrado (fica em vermelho, como na MediaWiki):
  `<span class="link-novo" title="Página ainda não publicada">IFSC Chapecó</span>`

## Componentes visuais (classes do `estilo.css`)

| Classe | Uso |
|---|---|
| `infobox` | Caixa de informações com moldura de madeira, à direita do artigo |
| `moldura` | Aplica a moldura de madeira (`moldura.svg`) a qualquer bloco |
| `banner-principal`, `menu-principal`, `caixa`, `selos` | Banner, menu de assuntos, caixas e selos da página principal |
| `toc` | Sumário recolhível (`<details>`) |
| `tabela`, `tabela-larga`, `tabela-rolagem` | Tabelas no estilo wiki; a rolagem evita estourar a tela no celular |
| `galeria` | Imagens com legenda (estágios, estações) |
| `navbox` | Caixa de navegação no fim dos artigos |
| `categorias` | Barra de categorias no fim dos artigos |
| `aviso aviso-info` / `aviso-planejado` / `aviso-implementado` / `aviso-removido` | Avisos |
| `status status-implementado` / `status-planejado` / `status-nao-confirmado` / `status-removido` | Etiquetas de situação |
| `descricao-jogo` | Citação do texto exibido no jogo |
| `pixel` | Mantém sprites nítidos quando ampliados |
| `icone`, `estacao` | Ícones de 16 px (estações, qualidade, ouro, energia, saúde) |

## De onde vêm os dados

- **Mod:** `content.json`, `data/arvores.json`, `data/arvores_regionais/*.json`, `data/lavouras/*.json`,
  `i18n/default.json`, `LISTA.txt`, READMEs e documentos de `docs/` da versão 1.8.1.
- **Jogo base:** local, horário, estação, clima e dificuldade dos peixes, e ingredientes, efeitos e receitas dos pratos
  do jogo, que o mod preserva. Conferidos na Stardew Valley Wiki em inglês (outubro de 2026).
- **Valores calculados:** preços por qualidade e por profissão, energia e saúde e o calendário de colheitas usam as
  fórmulas do jogo sobre os números do mod.

## Conteúdo planejado e não confirmado

Não existem nos arquivos da versão 1.8.1 e aparecem marcados como **Planejado** na wiki:
aldeões novos (Gab), IFSC Chapecó no lugar da Biblioteca, Tozzo no lugar do JojaMart e o Centro Comunitário
regionalizado. As receitas antigas (polenta, churrasco gaúcho e outras 13) aparecem como **Retiradas**,
porque saíram do mod na versão 1.6.0.

Quando o mod ganhar uma versão nova, atualize os artigos afetados e a página `atualizacoes.html`.
