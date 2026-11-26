# apps

Menu "Apps do dia a dia": um botão para cada app (abre em nova aba).

Publicação: GitHub Pages → https://paineis-gerenciais.github.io/apps/

A capa que leva a este menu fica em https://paineis-gerenciais.github.io/geral/ (repositório `geral`).

## Arquivos

- `index.html` — o menu (HTML + CSS, sem JavaScript). Os botões e o símbolo são feitos em código, não em imagem.
- `favicon.svg` — ícone da aba do navegador.
- `marca/` — a marca deste menu: símbolo, assinaturas, ícones, cores e folha da marca.
- `assets/` — criar se for usar imagem de fundo (`fundo.webp`). O prompt está em `ARTE.md`, no repositório `geral`.

## Adicionar ou tirar um app

Cada botão é um `<li>` em `index.html`.

- **Adicionar:** copie um `<li>` existente e troque quatro coisas: o endereço (`href`), a descrição lida por leitores de tela (`aria-label`), a linha de cima (`class="linha"`) e o nome (`class="nome"`).
- **Ícone:** é o desenho dentro de `<svg>`. Dá para repetir um ícone existente ou pedir um novo.
- **Tirar:** apague o `<li>` do app.
- **Em breve:** projeto ainda não publicado entra como um bloco `<div class="botao verde breve">`, sem endereço, com o selo "Em breve". Não tem clique. Esses botões ficam depois dos publicados.
- **Publicou um "Em breve":** apague o `<li>` dele e crie um botão normal, copiando um dos publicados e aproveitando o mesmo ícone.

Os endereços são relativos (`../carteira/`): funcionam enquanto o app estiver publicado na mesma conta. Para um app em outro endereço, use o endereço completo.

Este menu é público. Só entra aqui o app que pode ser encontrado por qualquer pessoa com o link.

## Colocar a imagem de fundo (opcional)

Sem imagem, o fundo é marfim liso.

1. Gere a imagem com o prompt do `ARTE.md` (repositório `geral`) e salve em `assets/fundo.webp` (1920 px de largura).
2. No alto do `index.html`, troque `--fundo: none;` por `--fundo: url("assets/fundo.webp");`.
