
# JavaScript

## Apresentação e histórico

JavaScript foi inicialmente desenvolvido em 1995 pela Netscape com intensão de tornar as páginas web, que antes eram completamente estáticas, em páginas dinâmicas, através da introdução de uma linguagem de programação para o browser da empresa, o Netscape Navigator 2.0. Inicialmente na versão beta a linguagem chamava-se LiveScript, porém ao ser lançada, o nome "JavaScript" foi finalmente adotado. 

## Características da Linguagem
JavaScript é uma linguagem de programação com multiplos paradígmas. É possível escrever código JavaScript funcional, ou imperativo(mudando estado), ou até orientado a objetos(JavaScript possui sua própria implementação de classes).

Como citado anteriormente, o propósito de JavaScript inicialmente ser uma linguagem de programação embutida em um browser para tornar páginas da web estáticas em páginas dinâmicas. Ainda hoje, a linguagem continua comprindo seu proósito inicial, porém há outras tecnologias que permitem utilizar JavaScript com outros propósitos, como por exemplo a criação de aplicativos, games e até servidores com Node.js. 

O sitema de tipagem em Javascript é dinâmico e fraco. Os tipos das variáveis são atribuídos com relação ao valor, e é possível transofrmar uma variável que era string em um int por exemplo. Objetos são baseados em um protótipo, `Object.prototype`.
```javascript
let a = "variavel string"
console.log(typeof a) // 'string'
a = 0
console.log(typeof a) // 'number'
a = []
console.log(typeof a) // 'object'
a = {}
console.log(typeof a) // 'object'
```

O ambiente de execução é imediato, já que JavaScript é uma linguagem interpretada. Porém engines costumam utilizar compiladores JIT(just in time) para optimizar a performace da linguagem, traduzindo JavaScript direto para código de máquina.

Há diversas implementações de JavaScript, sendo a mais utilizada a engine V8, desenvolvida pela Google e utilizada em seu browser Chrome, além de em Electron e Node.js. Vale citar a SpiderMonkey, desenvolvida pela Mozilla Fundation e utilizada no seu browser Firefox. 

## Capacidades da Linguagem
### Metaprogramação
JavaScript na sua mais nova versão(ECMAScript 6) é capaz de realizar metaprogramação. Com o método `eval`, é possível executar uma string como código em tempo de execução:
```javascript
const a = ['b', 'c', 'a']
eval('a.sort()')
console.log(a) // ['a', 'b', 'c']
```
Também é possível fazer reflexão, definir novas propriedades ou até utilizar proxies. Objetos de JavaScript são extremamente maleáveis.
### Gerenciamento de Ciclo de Vida
O ciclo de vida de JavaScript começa com a compilação da V8, depois a alocação de memória. Quando não há mais referências a uma variável, o coletor de lixo se encarrega de limpar a memória. Caso a variável seja utilizada somente dentro de um certo escopo, a keyword `let` deve ser utilizada. Caso declarada como `var`, ou sem usar nenhuma keyword, será criada no escopo global ou de função, e pode não ser descartada ao sair do bloco imediato.
```javascript
if(true){
    var a = "a";
    b = "b";
    let c = "c";
}
console.log(a, b) // a b
console.log(c) // Uncaught ReferenceError: c is not defined
```

### Segurança 
JavaScript em sua história foi vítima de muitos bugs de segurança, geralmente relacionados a implementações dos browsers. Porém, por os browsers manterem a execução do script em uma sandbox, desenvolvedores não podem por exemplo criar arquivos no computador do usuário, ou acessar partes da memória que não são suas próprias variáveis. Desenvolvedores utilizam bibliotecas contidas em pacotes como o NPM, e as vezes, o desenvolvedor de tais bibliotecas é atacado, comprometendo a segurança da biblioteca e de todos os apps que a utilizaram. 

### Performance
JavaScript é uma linguagem de alto nível, então sua performance é, dependendo da aplicação, cerca de 2 a 10 vezes pior do que um código compilado em C.


### Confiabilidade
JavaScript não possui boa confiabilidade já que a tipagem é bem fraca. É possível chamar uma função de multiplicação com uma string por exemplo, o que gera `NaN`(not a number). Uma função que precise de um parâmetro seja uma array, podemos passar um int, o que gera um erro de runtime caso não checamos o tipo do parâmetro dentro da própria função. Isto é um problema que linguagens como TypeScript tentam resolver adicionando tipos a JavaScript.

### Concorrência e Threading 
JavaScript utiliza eventos para se valer da concorrência e threading. As famosas `Promise` e os identificadores `async` e `await` permitem criar funções que não interrompem o fluxo do programa, e chamam uma outra função, "callback", quando finalizam a sua execução.

## Produtividade do Desenvolvedor
### Frameworks e Contâiners
Há inúmeros frameworks que trabalham com JavaScript. Alguns dos mais famosos são React, Angular e Vue. Também há frameworks mais antigos como o jQuery.

### Ferramentas Disponíveis
Ferramentas disponíveis incluem pacotes de bibliotecas como NPM, uma REPL na maioria dos navegadores(chamado de "Console" no Chrome e Firefox) que permite executar código JavaScript linha a linha, além de diversas ferramentas de debugging que permitem, por exemplo, criar breakpoints dentro de funções para avaliar o valor de variáveis na memória e melhor identificar bugs.

### Sintaxe, Semântica e Operações Predefinidas
JavaScript possuí uma sintaxe inspirada em Java, que é simples de ler e escrever. Como linguagens de programação como C++ ou Java, JavaScript utiliza os símbolos {} para definir escopo. Identação não é obrigatória, porém recomendada. Diferentemente de C++ e Java, JavaScript não força o desenvolvedor a terminar linhas como o símbolo ;, seu uso é opcional, porém recomendado. Estruturas como estas tornam o código JavaScript extremamente fácil de organizar, o que o deixa mais legível.

## Ecossistema
JavaScript completou 26 anos em 2021. Como é a linguagem utilizada pela grande maioria de páginas web para criar interatividade, a comunidade JavaScript é extremamente matura, contando com diversos fóruns, vídeos, tutoriais, palestras e eventos. 

Há um pouco de fragmentação por causa dos frameworks. Todos são JavaScript, e possuem escrita JavaScript, porém introduzem tantas funcionalidades que é difícil traduzir um código escrito para React para um código escrito em Vue, o que fragmenta um pouco a comunidade. 

---

## Informações Adicionais


## Referências 

1. https://www.freecodecamp.org/news/var-let-and-const-whats-the-difference/
Var, Let, and Const – What's the Difference?
2. https://www.freecodecamp.org/news/javascript-under-the-hood-v8/
How JavaScript Works: Under the Hood of the V8 Engine
3. https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Asynchronous/Promises
Graceful asynchronous programming with Promises
4. https://trio.dev/blog/javascript-framework
JavaScript Frameworks: What Are They and How Do They Work?