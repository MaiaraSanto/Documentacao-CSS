# Documentaçãoo-CSS


Documentação do código CSS do Projeto Final do Módulo HTML e CSS da StackX, para facilitar a compreensão dos elementos utilizados na aplicação, 
bem como e as futuras manutenções que serão executadas.


```bash

/* GLOBAL */

/* Variáveis globais para cores, tamanhos de fonte e transições */
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


/* Estilos básicos para o documento HTML */
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


/* Estilos para títulos de diferentes tamanhos */
.header-xl {
  /* Tamanho de fonte responsivo com clamp() */
  font-size: 2.5rem;
  font-size: clamp(2.5rem, 0.7rem + 7.68vw, 5.5rem);
  letter-spacing: -0.028em;
  line-height: 1.1;
}

/* Determina estilos para parágrafos */
p {
  /* Tamanho de fonte responsivo com clamp() */
  font-size: 1rem;
  font-size: clamp(1rem, 0.79rem + 0.89vw, 1.125rem);
  line-height: 1.5;
  color: var(--text2);
}


/* Conceito de estilos para links e botões */
a {
  transition: color var(--transition);
}


/* Estilo para o foco visível em elementos focáveis */
a:focus-visible,
input:focus-visible,
textarea:focus-visible {
  outline: 2px dashed var(--accent);
  outline-offset: 2px;
}


/* Estilo para inputs e textareas inválidos */
input:invalid,
textarea:invalid {
  outline-color: var(--invalid);
}


/* Estilo para links com sublinhado */
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


/* Delimita estilos para imagens e SVGs */
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


/* Estilo para wrapper principal */
.wrapper {
  /* Define largura máxima responsiva com base em variável de container */
  width: calc(100% - 2rem);
  max-width: var(--container);
  margin-inline: auto;
}



Contraste de Cores:

A `acessibilidade` visual é essencial para garantir que todas as pessoas possam ler e entender o conteúdo da página. O código utiliza variáveis CSS para definir cores como fundo, texto e destaque. Essas variáveis são cruciais para manter um bom contraste entre o texto e o plano de fundo, o que facilita a leitura para pessoas com diferentes necessidades visuais.
Foco Visível:

Quando um usuário navega por uma página usando apenas o teclado, é fundamental que o foco seja claramente visível. O código define um estilo para o foco visível em elementos como links (<a>) e controles de entrada (<input>, <textarea>), utilizando uma borda pontilhada de cor específica. Isso garante que usuários que dependem da navegação por teclado possam identificar facilmente onde estão na página.
Imagens e SVGs:

Imagens e gráficos vetoriais escaláveis (SVGs) são elementos importantes em uma página da web, mas é crucial garantir que sejam acessíveis a todos os usuários. No código fornecido, há estilos aplicados a esses elementos para garantir que sejam exibidos corretamente e interpretados de maneira adequada por pessoas com deficiência visual ou que utilizam leitores de tela.
Navegação e Layout Responsivo:

A navegação e o layout responsivo são aspectos cruciais da `acessibilidade` web. O código demonstra um layout responsivo, adaptando-se de forma fluida a diferentes tamanhos de tela e dispositivos, incluindo dispositivos móveis. Isso é importante para garantir que todos os usuários possam acessar e interagir com o conteúdo de maneira eficaz, independentemente do dispositivo que estão utilizando.
Rótulos de Formulário:

Embora não estejam presentes no código CSS fornecido, é importante notar que rótulos de formulário adequados devem ser fornecidos no HTML para garantir uma experiência de formulário acessível. Isso envolve associar corretamente os rótulos aos controles de entrada, o que facilita a compreensão do propósito de cada campo de formulário por usuários de leitores de tela.
Desempenho:
Utilização de Variáveis CSS:

O código faz um uso eficaz de variáveis CSS (--nome-da-variável), o que contribui para uma folha de estilo mais organizada, `perfomática` e fácil de manter. As variáveis permitem que valores comuns, como cores e tamanhos de fonte, sejam definidos uma vez e reutilizados em todo o código, facilitando a consistência e a manutenção.
Layout Responsivo e Flexível:

O uso de unidades flexíveis, como rem, vw, em e clamp, ajuda a criar layouts responsivos que se adaptam de uma `perfomance` eficaz a diferentes tamanhos de tela e dispositivos. Isso é fundamental para garantir uma experiência de usuário consistente e agradável, independentemente do dispositivo utilizado para acessar a página.
Minimização de Estilos e Aninhamento:

O código  está bem estruturado e evita aninhamentos excessivos de seletores CSS, o que pode contribuir para um código mais limpo e eficiente. No entanto, é sempre importante revisar e otimizar os seletores CSS para garantir que o estilo seja aplicado de maneira eficiente e sem impacto negativo no desempenho da página.
Utilização de Media Queries:

As media queries são utilizadas para aplicar estilos específicos com base no tamanho da tela e nas características do dispositivo do usuário. Isso garante que o layout e os estilos sejam ajustados de forma adequada para proporcionar uma experiência de usuário otimizada em diferentes dispositivos e resoluções de tela.
Transições e Animações Suaves:

O código faz uso de transições CSS (transition) para criar animações suaves, proporcionando uma experiência de usuário mais agradável e interativa. Essas transições são aplicadas de maneira cuidadosa para garantir que não afetem negativamente o desempenho da página, contribuindo para uma experiência de usuário mais fluida e envolvente.
Em resumo, o código demonstra um compromisso com a acessibilidade e o desempenho, implementando práticas recomendadas para garantir uma experiência de usuário inclusiva e eficiente. 


```
