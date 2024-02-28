# Documentacao-CSS

````
/* GLOBAL */

/* Define variáveis globais para cores, tamanhos de fonte e transições */
:root {
  --bg-body: hsl(0, 0%, 8%);
  --bg-body2: hsl(0, 0%, 14%);
  --accent: hsl(153, 71%, 59%);
  --text1: hsl(0, 0%, 100%);
  --text2: hsl(0, 0%, 85%);
  --invalid: hsl(7, 100%, 68%);
  --fs-18: 1.125rem;
  /* ... outras variáveis de tamanho de fonte */
  --transition: 250ms ease-in-out;
}

/* Define estilos básicos para o documento HTML */
html,
body {
  overflow-x: hidden;
}

html {
  box-sizing: border-box;
  font-size: 100%;
}

/* Define o box model padrão e a fonte para todos os elementos */
*,
*::before,
*::after {
  box-sizing: inherit;
}

body,
input,
textarea,
button {
  font-family: 'Space Grotesk', sans-serif;
}

body {
  margin: 0;
  background-color: var(--bg-body);
  color: var(--text1);
  font-size: var(--fs-18);
  line-height: 1.56;
  padding-bottom: 25rem; /* Margem inferior para evitar que o conteúdo seja ocultado pelo rodapé fixo */
}

/* Estilos para fundos menos escuros */
.bg-less-dark {
  background-color: var(--bg-body2);
}

/* Estilos para cabeçalhos, parágrafos e links */
h1,
h2,
h3,
p {
  margin-block-start: 0;
}

h1,
h2,
h3 {
  line-height: 1;
}

/* Define estilos para títulos de diferentes tamanhos */
.header-xl {
  /* Tamanho de fonte responsivo com clamp() */
  font-size: 2.5rem;
  font-size: clamp(2.5rem, 0.7rem + 7.68vw, 5.5rem);
  letter-spacing: -0.028em;
  line-height: 1.1;
}

/* Define estilos para parágrafos */
p {
  /* Tamanho de fonte responsivo com clamp() */
  font-size: 1rem;
  font-size: clamp(1rem, 0.79rem + 0.89vw, 1.125rem);
  line-height: 1.5;
  color: var(--text2);
}

/* Define estilos para links e botões */
a {
  transition: color var(--transition);
}

/* Define estilo para o foco visível em elementos focáveis */
a:focus-visible,
input:focus-visible,
textarea:focus-visible {
  outline: 2px dashed var(--accent);
  outline-offset: 2px;
}

/* Define estilo para inputs e textareas inválidos */
input:invalid,
textarea:invalid {
  outline-color: var(--invalid);
}

/* Define estilo para links com sublinhado */
a.underline,
button {
  /* Estilo de botão com efeito de sublinhado animado */
  display: inline-block;
  padding-bottom: 0.625rem;
  font-size: 1rem;
  line-height: 1.625;
  letter-spacing: 0.143em;
  font-weight: 700;
  text-transform: uppercase;
  color: var(--text1);
  text-decoration: none;
  background-image: linear-gradient(
    to right,
    var(--accent) 75%,
    var(--accent) 75%
  );
  background-position: 0 2.1em;
  background-repeat: repeat-x;
  background-size: 8px 2px;
}

/* Estilo de hover para links */
a:hover {
  color: var(--accent);
}

/* Define estilos para imagens e SVGs */
img,
svg {
  display: block;
}

/* Define estilo para ocultar visualmente, mas manter acessível para leitores de tela */
.visually-hidden {
  position: absolute;
  left: -10000px;
  top: auto;
  width: 1px;
  height: 1px;
  overflow: hidden;
}

/* Define estilo para wrapper principal */
.wrapper {
  /* Define largura máxima responsiva com base em variável de container */
  width: calc(100% - 2rem);
  max-width: var(--container);
  margin-inline: auto;
}

/* ACESSIBILIDADE */

/* Certifique-se de fornecer alternativas de texto para imagens */
img,
svg {
  /* O atributo 'alt' é fundamental para usuários de leitores de tela */
  alt: "";
}

/* Mantenha uma boa estrutura de cabeçalho para facilitar a navegação */
h1, h2, h3 {
  /* Use cabeçalhos em ordem lógica */
}

/* Atribua rótulos apropriados para controles de formulário */
label {
  /* Use o atributo 'for' correspondente ao ID do controle */
}

/* Utilize atributos 'aria-' para identificar regiões e controles importantes */
.header {
  /* Use 'role="banner"' para identificar o cabeçalho do site */
}

````
