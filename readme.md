# React

### React.js é um framework do JavaScript desenvolvida por engenheiros do Facebook.

### Motivos que fazem as pessoas usarem/estudarem react:

- React é ***rápido**.* As aplicações em react podem lidar com atualizações complexas e mesmo assim continuar sendo rápido e responsivo.
- React é ***modular.*** Em vez de usar arquivos gigantescos, você pode criar arquivos pequenos e reutilizá-los.
- React é ***escalável.*** Programas grandes que estão em constante mudança de dados é onde o react melhor performa.
- React é ***“popular”.*** Uma dos maiores motivos do pessoal procurar o react é pela sua fama no mercado de trabalho, e não estão errados kk.

# Introdução ao JSX 🤘🏽

## Hello world! :)

Olhe este código:

```jsx
const h1 = <h1>Hello world</h1>;
```

Parece JavaScript, por começar com `const` e terminar com `;`. Caso tente executar em um arquivo HTML, não irá funcionar. 

Entretanto, no código temos `<h1> Hello world </h1>`, que é igual a sintaxe HTML. Essa parte não funcionaria se você tentasse executá-la em um arquivo JavaScript.

Porém, esta *“mistura”* é chamado de **JSX** 

## O que é JSX?

JSX é uma extensão para o JavaScript. Ele foi escrito para ser usado com o React. O código JSX se assemelha muito com HTML.

Como o JSX é uma extensão para o JavaScript, significa que **JSX não é JavaScript válido**, ou seja, os navegadores da Web não irá conseguir ler.

Se um arquivo JavaScript tiver código JSX, esse arquivo terá que ser compilado. Isso significa que antes que o arquivo chegue ao navegador web, um compilador JSX traduzirá em JavaScript vanilla.

## Elementos JSX

Os elementos JSX são tratados como expressões em JavaScript.

Um elemento JSX pode ser salvo em uma varíavel, passado para uma função, armazenada em objeto ou array...

Exemplo de um elemento JSX sendo salvo em uma varíavel:

```jsx
const navBar = <nav>I am a nav bar</nav>;
```

Exemplo de vários elementos JSX sendo salvo em um objeto:

```jsx
const myTeam = {
	center: <li>Benzo Walli</li>,
	powerForward: <li>Raha Loa</li>,
	smallForward: <li>Tayshaun Dasmoto</li>,
	shootingGuard: <li>Colmar Cumberbatch</li>,
	pointGuard: <li>Femi Billon</li>
};
```

## Atributos em JSX

Um atributo JSX é escrito usando a mesma sintaxe de HTML: um nome, e sua atribuição há um valor entre aspas.

Exemplo:

```jsx
my-atribute-name="my-attribute-value"
```

Exemplo na prática:

```jsx
<a href='http://www.example.com'>Welcome to the Web</a>;

const title = <h1 id='title'>Introduction to React.js: Parte 1</h1>;
```

Exemplo de muitos atributos a apenas um elemento JSX, assim como em HTML:

```jsx
const panda = <img src='images/panda.jpg' alt='panda' width='500px' height='500px' />;
```

## JS aninhado

Você consegue aninhar elementos JSX dentro de outros elementos JSX, assim como em HTML.

Exemplo de JSX aninhado:

```jsx
<a href='https://www.example.com"><h1>Click me!</h1></a>
```

Para não parecer algo tão fora do comum, podemos usar as quebras de linhas para deixar no estilo mais HTML 😎.

```jsx
<a href='https://www.example.com">
	<h1>
		Click me!
	</h1>
</a>
```

Caso você opte pelo estilo html, você deve escrever o código entre parênteses.

```jsx
(
	<a href='https://www.example.com">
		<h1>
			Click me!
		</h1>
	</a>
)
```

Da mesma forma que o elemento JSX não aninhado pode ser salvas em variáveis, funções e etc. Elementos aninhados também podem!

```jsx
const theExample = (
   <a href="https://www.example.com">
     <h1>
       Click me!
     </h1>
   </a>
 );
```

## Elementos externos JSX

**Uma expressão JSX deve ter um elemento externo.**

Este código é inválido:

```jsx
const paragraphs = (
	<p>I am a paragraph.</p>
	<p>I, too, am a paragraph.</p>
);
```

Este código é valido:

```jsx
const paragraphs = (
	<div id='i-am-the-elemento-externo'>
		<p>I am a paragraph.</p>
		<p>I, too, am a paragraph.</p>
	</div>
);
```

*Em outras palavras, o elemento JSX deve conter apenas um elemento EXTERNO (um elemento pai que envolve todos os outros elementos filhos).*

## Renderizando JSX

Renderizar uma expressão em JSX é fazê-la aparecer na tela.

```jsx
ReactDOM.render(<h1>Hello world</h1>, document.getElementById('app'));
```

## ReactDOM.render()

**ReactDOM** é uma biblioteca JavaScript. Nela contém vários métodos do React, todos eles lidam com o **DOM.**

**ReactDOM.render()** é a maneira mais comum de renderizar um JSX.

O primeiro parâmetro do método render é um JSX, no caso o: `<h1>Hello world</h1>`, já o segundo será o elemento onde irá aparece o JSX (no caso, o texto Hello world), que foi selecionado acessando o DOM e selecionando o elemento pela id: `document.getElementById('app')`, 

## Passando uma váriavel ao ReactDOM.render()

O primeiro parâmetro deve ser **avaliado** como uma expressão JSX, não necessáriamente uma expressão JSX literal. Isso significa que podemos usar uma variável, desde que ela seja uma expressão JSX.

Exemplo:

```jsx
const toDoList = (
	<ol>
		<li>Learn React</li>
		<li>Become a developer</li>
	</ol>
);

ReactDOM.render(
	toDoList,
	document.getElementById('app')
);
```

# JSX Avançado 😎