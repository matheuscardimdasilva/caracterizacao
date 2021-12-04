
# Python

## Apresentação e histórico

Python apareceu inicialmente em 1991. Criado por Guido van Rossum, a linguagem foi inicialmente desenvolvida para suceder a linguagem de programação ABC. 

## Características da Linguagem
Python é uma linguagem de programação com multiplos paradígmas. É possível escrever código Python funcional, ou imperativo(procedural), orientado a objetos(Python possui sua própria implementação de classes).

O sitema de tipagem em Python é dinâmico e forte. 
```python
a = "a"
b = 1
c = a + b # TypeError: can only concatenate str (not "int") to str
```

O ambiente de execução é imediato, já que Python é uma linguagem interpretada. Porém diferentes implementações de Python podem usar compiladores JIT(just in time) para optimizar a performace da linguagem, ou compilar Python para bytecode.

Há diversas implementações de Python, sendo a referência CPython, que compila para bytecode da PVM(Python Virtual Machine). Outras implementações como PyPy possuem um JIT(just in time) compiler.

## Capacidades da Linguagem
### Metaprogramação
Python possui ferramentas para realizar metaprogramação, como metaclasses, metaobjetos e funções como `eval`, que possibilita executar uma string como código em tempo de execução. Também é possível fazer reflexão, e até acessar nomes específicos no escopo global com `globals()['Foo']`, ou nomes dentro de uma classe com o atributo `__dict__`
### Gerenciamento de Ciclo de Vida
O ciclo de vida do Python começa com a compilação em bytecode, depois a alocação de memória. Quando não há mais referências a uma variável, o coletor de lixo se encarrega de limpar a memória. 


### Segurança 
Exploits que geram falhas de segurança na linguagem são corrigidos nas novas versões(Python 3+), porém o suporte para as versões antigas(Python 2 por exemplo) foi descontinuado.  

### Performance
Python é uma linguagem de alto nível, então sua performance é pior do que um código compilado em C. Por ser uma linguagem geralmente interpretada, os custos sobem ainda mais.


### Confiabilidade
Por ter tipagem forte, Python possui uma confibiabilidade razoável, porém, por ser dinâmica, é fácil gerar erros no runtime que não são visíveis em tempo de compilação.

### Concorrência e Threading 
Python usa bibliotecas para permitir a cricação de multiplos threads concorrentes. Um exemplo é a biblioteca `threading`

## Produtividade do Desenvolvedor
### Frameworks e Contâiners
Há inúmeros frameworks que trabalham com Python, dependendo do que o desenvolvedor deseja criar. Alguns dos mais famosos são Django, Flask e Web2Py.

### Ferramentas Disponíveis
Ferramentas disponíveis incluem pacotes de bibliotecas como PIP, uma REPL (pode ser aberta com o comando `python`) que permite executar código Python linha a linha, além de diversas ferramentas de debugging que permitem, por exemplo, criar breakpoints dentro de funções para avaliar o valor de variáveis na memória e melhor identificar bugs.

### Sintaxe, Semântica e Operações Predefinidas
A sintaxe de Python tem um foco em ser simples de ler e escrever. Identação é obrigatória, já que esta é utilizada para definir bloco, o que força o desenvolvedor a manter o seu código bem identado, tornando o código mais legível. Diferentemente de C++ e Java, Python não utiliza o símbolo `;` no final de linhas. 

## Ecossistema
Python completou 30 anos em 2021. Python é uma das linguagens mais populares, e também vem crescendo bastante, sendo adotada para diversos propósitos desde o desenvolvimento de servers, até microcontroladores. A comunidade Python é extremamente matura, contando com diversos fóruns, vídeos, tutoriais, palestras e eventos. 

## Referências 

1. https://medium.com/fintechexplained/advanced-python-metaprogramming-980da1be0c7d
Advanced Python: Metaprogramming
2. https://betterprogramming.pub/the-life-cycle-of-python-instance-objects-4a719fb4e925
The Life Cycle of Python Instance Objects
3. https://www.northeastern.edu/graduate/blog/most-popular-programming-languages/
The 10 Most Popular Programming Languages to Learn in 2021