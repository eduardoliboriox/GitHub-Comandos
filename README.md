---

# 📘 Comandos Git Essenciais

Lista prática dos comandos mais úteis para trabalhar com Git e GitHub no dia a dia.

---

## 🔹 Inicialização e Status

```bash
git init
git status
```

---

## 🔹 Adicionar e Committar

```bash
git add .
git add arquivo.ext
git commit -m "msg"
git commit --amend        # Edita o último commit
git log                   # Mostra histórico de commits
```

---

## 🔹 Branches

```bash
git branch                # Lista branches
git branch -M main        # Renomeia branch atual para main
git branch nova-branch    # Cria nova branch
git checkout nova-branch  # Troca para outra branch
git checkout -b nova      # Cria e já troca
git merge nome-da-branch  # Faz merge
```

---

## 🔹 Remotes

```bash
git remote -v
git remote add origin https://github.com/usuario/repositorio.git
git remote add publico https://github.com/usuario/repositorio-publico.git
git remote set-url origin https://github.com/usuario/novo-repo.git
git remote remove origin
git remote rm origin
```

---

## 🔹 Push e Pull

```bash
git push -u origin main
git push origin main
git push --force origin main
git pull                      # Atualizar seu projeto local com as mudanças que estão no GitHub      
git pull origin main
```

---

## 🔹 Reset / Undo

```bash
git reset --soft HEAD~1       # Reverte commit mantendo alterações
git reset --hard HEAD~1       # Reverte commit apagando alterações
git restore arquivo.ext       # Restaura arquivo modificado
git checkout -- arquivo.ext   # Forma antiga do restore
```

---

## 🔹 Clonar e Duplicar Repositórios

```bash
git clone https://github.com/user/repo.git
git clone --bare repo.git     # Para duplicar repositórios
```

---

## 🔹 Limpar Histórico (útil para repos públicos)

```bash
rm -rf .git                   # Remove o histórico
git init                      # Inicia novo repositório do zero
```

---

## 🔹 Sequências 
```bash
git remote -v
git remote set-url origin https://github.com/usuario/novo-repo.git
git push -u origin main
```

```bash
git fetch origin
git reset --hard origin/main
```

# 📘 DICIONÁRIO COMPLETO DE CSS — GUIA DE ESTUDO

Este documento reúne **conceitos, seletores, propriedades e padrões de CSS**, indo do básico ao avançado, incluindo práticas modernas usadas em projetos reais (layout, responsividade, mobile-first, UX e manutenção).

---

## 📌 O QUE É CSS

CSS (Cascading Style Sheets) é a linguagem usada para **estilizar documentos HTML**, controlando cores, tamanhos, espaçamentos, layout, animações e responsividade.

Estrutura básica:

```css
seletor {
  propriedade: valor;
}
```

---

## 🎯 SELETORES CSS

### Básicos

| Seletor | Nome      | Exemplo    | Descrição           |
| ------- | --------- | ---------- | ------------------- |
| `*`     | Universal | `* {}`     | Todos os elementos  |
| `tag`   | Elemento  | `p {}`     | Todas as tags `<p>` |
| `.`     | Classe    | `.box {}`  | `class="box"`       |
| `#`     | ID        | `#menu {}` | `id="menu"`         |

### Combinadores

```css
div p {}        /* descendente */
div > p {}      /* filho direto */
h1, h2 {}       /* múltiplos */
.box.active {}  /* múltiplas classes */
```

### Avançados

```css
[class*="col-"] {}   /* contém texto */
input[type="date"] {}
```

---

## 🧠 VARIÁVEIS CSS

### `:root`

Define variáveis globais.

```css
:root {
  --primary-color: #0d6efd;
}
```

### `var()`

Usa a variável.

```css
color: var(--primary-color);
```

---

## 📦 BOX MODEL

Ordem:

```
margin → border → padding → content
```

### `margin`

Espaço externo.

```css
margin: 10px;
margin-bottom: 20px;
```

### `padding`

Espaço interno.

```css
padding: 12px;
```

### `border`

```css
border: 1px solid #ccc;
border-radius: 12px;
```

### `box-sizing`

```css
box-sizing: border-box;
```

---

## 📐 TAMANHOS E UNIDADES

| Unidade | Significado      |
| ------- | ---------------- |
| `px`    | pixel            |
| `%`     | porcentagem      |
| `vw`    | largura da tela  |
| `vh`    | altura da tela   |
| `em`    | relativo ao pai  |
| `rem`   | relativo ao root |

```css
width: 100%;
max-width: 1200px;
min-height: 100vh;
```

---

## 🧭 POSICIONAMENTO

### `position`

| Valor      | Função          |
| ---------- | --------------- |
| `static`   | padrão          |
| `relative` | relativo a si   |
| `absolute` | relativo ao pai |
| `fixed`    | fixo na tela    |
| `sticky`   | gruda ao rolar  |

```css
position: fixed;
bottom: 0;
```

### `inset`

```css
inset: 0;
```

### `z-index`

```css
z-index: 1050;
```

---

## 📐 FLEXBOX

```css
display: flex;
```

### Propriedades principais

```css
flex-direction: row | column;
justify-content: center;
align-items: center;
flex-wrap: wrap;
gap: 10px;
```

### `flex`

```css
flex: 1;
flex: 0 0 50%;
```

---

## 🧩 GRID

```css
display: grid;
grid-template-columns: repeat(2, 1fr);
gap: 16px;
```

### `aspect-ratio`

```css
aspect-ratio: 1 / 1;
```

---

## 🎨 CORES E FUNDO

```css
color: #000;
background-color: #f8f9fa;
background-image: url(img.png);
background-size: cover;
background-position: center;
```

---

## 🖼️ IMAGENS

```css
object-fit: cover;
object-fit: contain;
```

---

## ✍️ TEXTO

```css
font-family: 'Open Sans', sans-serif;
font-size: 16px;
font-weight: 600;
text-align: center;
line-height: 1.5;
letter-spacing: 1px;
text-transform: uppercase;
white-space: nowrap;
```

---

## 🖱️ INTERAÇÃO

### Estados

```css
:hover {}
:active {}
:focus {}
:focus-visible {}
```

### Cursor

```css
cursor: pointer;
```

---

## 🎞️ ANIMAÇÕES E TRANSIÇÕES

### `transition`

```css
transition: all 0.3s ease;
```

### `transform`

```css
transform: scale(1.05);
transform: translateY(-2px);
```

---

## ✂️ OVERFLOW E SCROLL

```css
overflow: hidden;
overflow-x: auto;
```

### Scroll customizado

```css
::-webkit-scrollbar { width: 6px; }
```

---

## 📱 RESPONSIVIDADE

### Media Query

```css
@media (max-width: 768px) {}
@media (min-width: 769px) {}
@media (orientation: landscape) {}
```

---

## 🖨️ IMPRESSÃO

```css
@media print {
  header { display: none; }
}
```

---

## 🧪 PRIORIDADE E BLINDAGEM

### `!important`

```css
color: red !important;
```

---

## 🧠 FUNÇÕES ÚTEIS

```css
width: calc(100% - 40px);
font-size: clamp(14px, 2vw, 18px);
```

---

## 🧠 PROPRIEDADES AVANÇADAS

```css
pointer-events: none;
user-select: none;
will-change: transform;
@supports (display: grid) {}
```

---

## ✅ BOAS PRÁTICAS

* Use **classes**, evite IDs
* Centralize cores em variáveis
* Mobile-first quando possível
* Evite `!important`
* Organize por seções
* Comente o CSS

---

## 📚 OBJETIVO DO REPOSITÓRIO

Este arquivo serve como **guia pessoal de estudo**, referência rápida e base para evolução em CSS moderno.

**“Dicionário Completo de CSS — Guia de Estudo”**

### O que esse guia tem:

* Seletores (`.`, `#`, combinadores, avançados)
* Variáveis CSS (`:root`, `var`)
* Box Model completo
* Flexbox e Grid (com exemplos reais)
* Cores, fundo, imagens
* Tipografia e texto
* Interação (`hover`, `active`, `focus`)
* Transições e transformações
* Scroll customizado
* Responsividade (media queries)
* Impressão (`@media print`)
* Funções modernas (`calc`, `clamp`)
* Propriedades avançadas
* Boas práticas profissionais

### Como usar no repositório

Sugestão de estrutura:

```
css-dicionario/
├── README.md   ← (esse conteúdo)
├── exemplos/
│   ├── flexbox.css
│   ├── grid.css
│   └── media-queries.css
└── playground/
```

