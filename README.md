
# Aula Completa: HTML + CSS na Fazendinha CSS (obrigado, Bryan!)

## Início da Aula: O que vamos aprender?
**Objetivo**: Fazer uma página HTML e estilizar totalmente usando CSS.

**Conteúdos esperados**:
- Estrutura básica HTML
- Elementos principais (`div`, `img`, `p`, `h1`, `span`)
- Atributos (`id`, `class`, `alt`, `href`)
- CSS externo, interno e inline
- Seletores CSS
- Box model
- Propriedades visuais (`color`, `background`, `border`, `padding`, `margin`, etc.)
- Positioning
- Flexbox e Grid (básico)
- Animações e transições
- Responsividade
- Pseudo-elementos e pseudo-classes

Vamos aprender **tudo isso** criando a fazendinha!

---

## Estrutura HTML básica

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Fazendinha CSS</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Bem-vindo à Fazendinha CSS 🐄🌻</h1>
  <div class="sky"></div>
  <div class="field"></div>
  <div class="cow"></div>
</body>
</html>
```

**Conceitos**:
- Estrutura HTML básica
- Tag `<link>` para CSS externo
- Divisão com `<div>`
- Título com `<h1>`

---

## Primeiros estilos CSS: Céu e Campo

```css
body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
  text-align: center;
}

.sky {
  width: 100%;
  height: 50vh;
  background: linear-gradient(to bottom, #87ceeb, #add8e6);
}

.field {
  width: 100%;
  height: 50vh;
  background-color: #7cfc00;
}
```

**Conceitos**:
- `margin`, `padding`, `font-family`
- `width`, `height`, `background`, `linear-gradient`
- Unidades relativas (`vh`, `%`)

---

## A Vaca Aparece!

```html
<div class="cow"></div>
```

```css
.cow {
  width: 100px;
  height: 60px;
  background-color: white;
  border: 2px solid black;
  border-radius: 20px;
  position: absolute;
  bottom: 10vh;
  left: 10vw;
}
```

**Conceitos**:
- `border`, `border-radius`
- `position: absolute`

---

## Imagens e Texto

```html
<div class="cow">
  <img src="https://placekitten.com/100/60" alt="Vaquinha">
  <p>Mimosa 🐮</p>
</div>
```

```css
.cow img {
  width: 100%;
  height: auto;
  border-radius: 20px;
}

.cow p {
  margin: 5px 0 0;
  font-weight: bold;
}
```

**Conceitos**:
- Uso de `<img>`, `alt`
- Texto com `<p>`, propriedades de fonte

---

## Manchinhas com Pseudo-elementos

```css
.cow::before, .cow::after {
  content: '';
  width: 20px;
  height: 20px;
  background: black;
  border-radius: 50%;
  position: absolute;
}

.cow::before {
  top: 10px;
  left: 10px;
}

.cow::after {
  top: 30px;
  left: 60px;
}
```

**Conceitos**:
- Pseudo-elementos `::before`, `::after`

---

## Movimento e Animação

```css
@keyframes moveCow {
  0% { left: 10vw; }
  50% { left: 70vw; }
  100% { left: 10vw; }
}

.cow {
  animation: moveCow 8s infinite linear;
}
```

**Conceitos**:
- `@keyframes`
- `animation`

---

## Adicionando um Sol

```html
<div class="sun"></div>
```

```css
.sun {
  width: 80px;
  height: 80px;
  background: yellow;
  border-radius: 50%;
  position: absolute;
  top: 20px;
  right: 20px;
  box-shadow: 0 0 20px yellow;
  animation: spinSun 10s linear infinite;
}

@keyframes spinSun {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

**Conceitos**:
- `box-shadow`
- `transform: rotate`

---

## Responsividade (Media Queries)

```css
@media (max-width: 600px) {
  .cow {
    width: 70px;
    height: 40px;
  }

  .sun {
    width: 50px;
    height: 50px;
  }
}
```

**Conceitos**:
- `@media` queries para responsividade

---

## Resumo Geral

- Estrutura básica do HTML
- Divs e Containers
- Seletores e Estilização no CSS
- Box Model e Posicionamento
- Animações e Transições
- Responsividade
- Pseudo-elementos

---


# 💻 Desafios de CSS – Pair Programming

Neste documento, você encontrará **cinco desafios de CSS** que devem ser resolvidos em duplas (pair programming). Cada desafio contém:

- ✅ Objetivo
- 🧱 Código HTML base
- 🎯 Imagem da solução esperada

---

## 🔷 Desafio 1: Layout Responsivo

### ✅ Objetivo:
Transformar um layout de **3 colunas em desktop** para **2 colunas no tablet** e **1 coluna no mobile**, usando CSS Grid e media queries.

### 🧱 HTML Base
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Layout Responsivo</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Minha Página Responsiva</h1>
    <p>Veja como o layout se adapta ao tamanho da tela.</p>
  </header>

  <main class="grid-container">
    <section class="col">
      <h2>Notícias</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse sit amet.</p>
    </section>
    <section class="col">
      <h2>Eventos</h2>
      <ul>
        <li>Workshop de CSS</li>
        <li>Webinar de Acessibilidade</li>
        <li>Hackathon Universitário</li>
      </ul>
    </section>
    <section class="col">
      <h2>Contato</h2>
      <form>
        <input type="text" placeholder="Seu nome"><br><br>
        <input type="email" placeholder="Seu e-mail"><br><br>
        <button type="submit">Enviar</button>
      </form>
    </section>
  </main>
</body>
</html>
```

### 🎯 Solução esperada


---

## 🔷 Desafio 2: Modal com Flexbox

### ✅ Objetivo:
Criar um **modal centralizado na tela** com `display: flex`.

### 🧱 HTML Base
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Modal com Flexbox</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Portal de Cursos Online</h1>
    <p>Aprenda novas habilidades com especialistas do mercado.</p>
  </header>

  <main>
    <section>
      <h2>Cursos em destaque</h2>
      <ul>
        <li><strong>Desenvolvimento Web</strong> – HTML, CSS, JS e mais</li>
        <li><strong>UX Design</strong> – Experiência do usuário na prática</li>
        <li><strong>Data Science</strong> – Python e análise de dados</li>
      </ul>
    </section>

    <section>
      <h2>Depoimentos</h2>
      <blockquote>
        “Excelente plataforma. Os professores são incríveis!” — Ana Souza
      </blockquote>
    </section>
  </main>

  <!-- Modal sobreposto -->
  <div class="overlay">
    <div class="modal">
      <h2>Confirmação de Inscrição</h2>
      <p>Você tem certeza que deseja se inscrever neste curso?</p>
      <div class="modal-actions">
        <button>Sim, inscrever</button>
        <button>Cancelar</button>
      </div>
    </div>
  </div>
</body>
</html>
```

### 🎯 Solução esperada


---

## 🔷 Desafio 3: Formulário com Estilização Coesa

### ✅ Objetivo:
Aplicar estilos para tornar um formulário mais legível e visualmente agradável, com campos alinhados e botão destacado.

### 🧱 HTML Base
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Formulário de Cadastro</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Cadastre-se</h1>
  <form class="formulario">
    <label for="nome">Nome completo</label>
    <input type="text" id="nome" placeholder="Digite seu nome completo">

    <label for="email">E-mail</label>
    <input type="email" id="email" placeholder="exemplo@email.com">

    <label for="senha">Senha</label>
    <input type="password" id="senha" placeholder="Crie uma senha segura">

    <label>
      <input type="checkbox"> Aceito os termos de uso
    </label>

    <button type="submit">Registrar</button>
  </form>
</body>
</html>
```

### 🎯 Solução esperada


---

## 🔷 Desafio 4: Card com Imagem e Texto Sobreposto

### ✅ Objetivo:
Criar um **card com imagem de fundo** e **texto centralizado sobreposto**.

### 🧱 HTML Base
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Card com Imagem</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Galeria de Destinos</h1>
  <div class="card">
    <img src="https://placehold.co/400x200" alt="Imagem de uma praia ensolarada">
    <div class="card-text">Praia do Sol</div>
  </div>
  <p>Explore nossos pacotes de viagem e viva experiências incríveis!</p>
</body>
</html>
```

### 🎯 Solução esperada


---

## 🔷 Desafio 5: Galeria de Imagens com Grid Responsivo

### ✅ Objetivo:
Organizar uma galeria de imagens com display: grid, ajustando o número de colunas conforme a largura da tela (sem media queries explícitas).

### 🧱 HTML Base
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Galeria de Imagens</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Galeria de Viagens</h1>
  <div class="galeria">
    <img src="https://placehold.co/200x150" alt="Imagem 1">
    <img src="https://placehold.co/200x150" alt="Imagem 2">
    <img src="https://placehold.co/200x150" alt="Imagem 3">
    <img src="https://placehold.co/200x150" alt="Imagem 4">
    <img src="https://placehold.co/200x150" alt="Imagem 5">
    <img src="https://placehold.co/200x150" alt="Imagem 6">
  </div>
</body>
</html>
```

### 🎯 Solução esperada

---

# BÔNUS: Canvas + P5.js

O seguinte código carrega um elemento \<canvas\> em sua página. O canvas é um container de pixels, e você pode manipular esses pixels da forma como desejar. Por exemplo, você pode carregar uma imagem .jpg ou .png sobre ele, e usar seu mouse para pintar sobre essa imagem com a cor que quiser. Para carregar o canvas de forma fácil, utilizamos a biblioteca P5.js, que abstrai o javascript para funções lógicas de manipulação de pixels e imagens. Veja o exemplo e execute em seu editor.

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Anotações com P5.js</title>
  <script src="https://cdn.jsdelivr.net/npm/p5@1.11.7/lib/p5.js"></script>
</head>
<body>
  <h2>Carregue uma imagem e use o pincel vermelho para anotar</h2>
  <button id="imgBtn" type="button">Carregar imagem</button>
  <script>
    let img;
    let brushSize = 10;

    function setup() {
      let canvas = createCanvas(800, 600);
      canvas.parent(document.body);
      background(255);
      noFill();
      stroke(255, 0, 0); // cor do pincel vermelho
      strokeWeight(brushSize);

      let btn = document.getElementById('imgBtn');
      btn.addEventListener('click', handleImageUpload);
    }

    function draw() {
      // pintura com o mouse
      if (mouseIsPressed && img) {
        line(pmouseX, pmouseY, mouseX, mouseY);
      }
    }

    function handleImageUpload(event) {
      img = loadImage("https://placehold.co/800x600", function(){
        image(img, 0, 0, width, height);
      });
    }
  </script>
</body>
</html>
```

Boa programação! 🚀


**Fim da Aula!**
