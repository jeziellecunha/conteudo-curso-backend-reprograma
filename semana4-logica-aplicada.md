# Lógica aplicada - Arrays, Objetos e Métodos 🚀

**Semana 4 – Resolução de Problemas/Lógica aplicada e JavaScript (sintaxe básica)**

## 

## Sumário

1. [Objetos](https://github.com/reprograma/On12-s4-Logica-3#objetos)

2. [Arrays](https://github.com/reprograma/On12-s4-Logica-3#arrays)

3. [Métodos de iteração](https://github.com/reprograma/On12-s4-Logica-3#métodos-de-iteração)

4. [Extra: Introdução a Programação Orientada a Objeto com JS](https://github.com/reprograma/On12-s4-Logica-3#poo-com-javascript-introdução)

5. [Ferramentas da semana: readline e nodemon](https://github.com/reprograma/On12-s4-Logica-3#readline-e-nodemon)

   

## Objetos

Objeto é um tipo de dado que contém uma coleção de propriedades  organizadas em pares de chave (ou nome) e valor, sendo o valor qualquer  tipo de dado (número, texto, função ou até mesmo outro objeto).

### 

### Inicializando objetos

Para criar um novo Objeto, podemos atribuir a uma variável uma lista  de elementos entre chaves, separados por vírgula e com a notação de `chave : valor`. Também é possível utilizando a palavra reservada `new` ou a partir de uma função.

```
const pessoa = {
  nome: 'Ariel',
  idade: 25,
  profissao: 'desenvolvedora',
};
const pessoa = new Object();

pessoa.nome = 'Ariel';
pessoa.idade = 25;
pessoa.profissao = 'desenvolvedora';
```

### 

### Acessando valores

Notação de ponto

```
const pessoa = {
  nome: 'Ariel',
  idade: 25,
  profissao: 'desenvolvedora',
};

console.log(pessoa.nome); // Ariel
console.log(pessoa.idade); // 25
console.log(pessoa.profissao); // desenvolvedora
```

Notação de colchetes (ou índice)

```
const pessoa = {
  nome: 'Ariel',
  idade: 25,
  profissao: 'desenvolvedora',
};

console.log(pessoa['nome']); // Ariel
console.log(pessoa['idade']); // 25
console.log(pessoa['profissao']); // desenvolvedora
```

Mais exemplos:

Declaração de objetos

```
const objeto = new Object()
objeto.nome = 'cadeira'
objeto.tipo = 'madeira'
objeto.peso = 7

const pokemon = {
  nome: 'Pikachu',
  tipo: 'elétrico',
  altura: 40.6,
}
```

Acessando o valor de uma propriedade do objeto.

```
console.log(pokemon.nome) // Pikachu
const nome = pokemon.nome
const tipo = pokemon.tipo
const altura = pokemon.altura

console.log(nome) // Pikachu
console.log(tipo) // elétrico
console.log(altura) // 40.6
```

Alterando propriedades

```
pokemon.nome = 'Bulbasaur'
```

Adicionando propriedades

```
pokemon.peso = '6,9kg'
```

Deletando propriedades

```
delete = pokemon.peso
```

Atribuição via desestruturação

```
const { nome, tipo, altura } = pokemon

console.log(nome) // Pikachu
console.log(tipo) // elétrico
console.log(altura) // 40.6
```

MDN: [destructuring assignment](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Atribuicao_via_desestruturacao)

### 

### Date

```
const hoje = new Date()

console.log(hoje) // 2020-09-05T10:56:49.693Z

const dia = hoje.getDate()
const mes = hoje.getMonth()
const ano = hoje.getFullYear()

console.log(dia, mes, ano) // 5 8 2020 🤔

const dataFormatada = hoje.toLocaleDateString('pt-BR')
console.log(dataFormatada) // 05/09/2020

const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' }
const dataLonga = hoje.toLocaleDateString('pt-BR', options)
console.log(dataLonga) // sábado, 5 de setembro de 2020
```

MDN: [date](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Date), [toLocaleDateString](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleDateString)

## 

## Arrays

Um array (ou lista) permite armazenar um conjunto de dados e  atribuí-los a uma variável, sendo esta a estrutura de dados mais simples possível.

### 

### Inicializando Arrays

Para criar um novo Array, podemos atribuir a uma variável uma lista  de elementos entre colchetes e separados por vírgula. Também é possível  utilizando a palavra reservada `new` e instanciando os valores que queremos atribuir ou apenas especificando o seu tamanho.

```
const alunasReprograma = ['Andreia', 'Fernanda', 'Mariana', ...];
const alunasReprograma = new Array('Andreia', 'Fernanda', 'Mariana', ...);
```

### 

### Acessando valores

Para acessar o valor de um Array, use a notação de colchetes e  informe a posição que deseja acessar, lembrando que a contagem começa em zero.

```
const alunasReprograma = ['Andreia', 'Fernanda', 'Mariana', ...];

console.log(alunasReprograma[0]) // Andreia
console.log(alunasReprograma[1]) // Fernanda
console.log(alunasReprograma[2]) // Mariana
```

### 

### Métodos de iteração

- `filter` retorna um novo array com os elementos filtrados.
- `find` retorna o primeiro elemento que achar igual ao elemento passado por parâmetro.
- `indexOf` retorna a posição do item passado por parâmetro ou -1 caso não tenha encontrado.
- `length` retorna um número que representa o tamanho do array.
- `map` retorna um novo array sem alterar o array original, criando uma cópia com as alterações que desejamos.
- `pop` remove e retorn o último item do array.
- `push` adiciona um item na última posição do array.
- `shift` remove e retorna o primeiro item do array.
- `slice` copia o array para outra variável.
- `splice` remove o item da posição passada por parâmetro
- `unshift` adiciona um item na primeira posição do array.

#### 

#### for...of

```
for (numero of numeros) {
  const dobro = numero * 2

  console.log(dobro)
}
// 18
// 4
// 10
```

MDN: [for...of](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for...of)

------

#### 

#### map

> O método `map()` invoca a função `callback` passada por argumento para cada elemento do Array e devolve um novo Array como resultado. *Fonte: [MDN map](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/map)*

```
function dobrar(item) {
  return item * 2
}

const numerosDobrados = numeros.map(dobrar)

console.log(numerosDobrados) // [18, 4, 10]
```

Deixando mais conciso:

```
const numerosDobrados = numeros.map(function (item) {
  return item * 2
})

console.log(numerosDobrados) // [18, 4, 10]
```

Refatorando para JS moderno:

```
const numerosDobrados = numeros.map(item => item * 2)

console.log(numerosDobrados) // [18, 4, 10]
```

Obs: o método `map` não alterar o array original. Ele retorna um array novo com o resultado do `map`.

------

#### 

#### find

> O método find executa a função callback uma vez para cada elemento  presente no array até que encontre um onde callback  retorne o valor  true. Se o elemento é encontrado, find retorna imediatamente o valor  deste elemento. Caso contrário, find retorna undefined. *Fonte MDN: [find](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/find)*

```
function procuraCinco(item) {
  return item === 5
}

const achouCinco = numeros.find(procuraCinco)

console.log(achouCinco) // 5
```

------

#### 

#### filter

```
function impar(item) {
  return item % 2 !== 0
}

const numerosImpares = numeros.filter(impar)
```

Deixando mais conciso:

```
const numerosImpares = numeros.filter(function (item) {
  return item % 2 !== 0
})
```

Refatorando para JS moderno:

```
const numerosImpares = numeros.filter(item => item % 2 !== 0)

console.log(numerosImpares) // [9, 5]
```

Obs: o método `filter` não altera o array original. Ele retorna um array novo com o resultado do `filter`.

MDN: [filter](https://github.com/reprograma/On12-s4-Logica-3/blob/master)

------

#### 

#### sort

O método `sort` recebe uma função de callback opcional. Caso a função não seja fornecida, o array segue a ordenação dos caracteres Unicode.

> Se o parâmetro funcaoDeComparacao é fornecido, o array será ordenado  de acordo com o valor de retorno da funcaoDeComparacao. Considerando que a e b são dois elementos sendo comparados, então:
>
> - Se `funcaoDeComparacao(a, b)` for menor que 0, ordena `a` para um índice anterior a `b`, i.e. `a` vem primeiro.
> - Se `funcaoDeComparacao(a, b)` retornar 0, deixa `a` e `b` inalterados em relação um ao outro, mas ordenado em relação a todos os outros elementos.
> - Se `funcaoDeComparacao(a, b)` é maior que 0, ordena `b` para um índice anterior que `a`. `funcaoDeComparacao(a, b)` sempre deve retornar o mesmo valor dado um par específico de elementos `a` e `b` como seus dois parâmetros. Se resultados inconsistentes são retornados, então a ordenação é indefinida.
>
> *Fonte MDN: [sort](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)*

```
let numeros = [ 5, 9, 2]
function funcaoDeComparacao(a, b) {
  
  if (a < b) {
    return -1 // ao retornar valor negativo, a ordem fica [a, b]
  } else if (a > b) {
    return 1 // ao retornar valor positivo, a ordem fica [b, a]
  } else {
    return 0 // ao retornar valor nulo, a ordem permanece [a, b]
  }
}

numeros.sort(funcaoDeComparacao)

console.log(numeros) // [2, 5, 9]
```

Deixando mais conciso:

```
function funcaoDeComparacao(a, b) {
  return a - b
}

numeros.sort(funcaoDeComparacao)

console.log(numeros) // [2, 5, 9]
```

Refatorando para JS moderno:

```
numeros.sort((a, b) => a - b)

console.log(numeros) // [2, 5, 9]
```

**Obs: o método `sort` altera o array original!**

------

#### 

#### reduce

O método `reduce` recebe uma função callback com alguns  parâmetros e essa função é executada a cada elemento presente no array. O resultado é a redução do array a um valor só. Normalmente, utilizamos  os dois primeiros parâmetros: `acumulador` e `itemAtual`.

Por exemplo, podemos executar a soma de todos os valores do array utilizando o método `reduce`:

```
function somarTodos(acumulador, itemAtual) {
  return acumulador + itemAtual
}

const numerosSomados = numeros.reduce(somarTodos)

console.log(numerosSomados) // 16
```

Deixando mais conciso:

```
const numerosSomados = numeros.reduce(function (acumulador, itemAtual) {
  return acumulador + itemAtual
})

console.log(numerosSomados) // 16
```

Refatorando para JS moderno:

```
const numerosSomados = numeros.reduce((acumulador, itemAtual) => acumulador + itemAtual)

console.log(numerosSomados) // 16
```

------

## 

## Readline e Nodemon

- Readline-sync é um pacote maravilhoso para pegar inputs no terminal,  ou seja pegar entradas de dados no sistema. Se você veio de programação  front-end isso equivale a pegar o value do input de um usuário num  formulário.
- Dentro da pasta de seu projetinho instale digitando o comando no terminal: npm install readline-sync
- Nodemon é uma forma de executar o node atualizando automaticamente  sempre que incluirmos e salvarmos novas informações nos arquivos.js
- Dentro da pasta de seu projetinho instale digitando o comando no terminal: npm install nodemon
- Crie o script start no package.json: "scripts": { "start": "nodemon app.js" }
- Execute apenas uma vez: npm run start (após isso ele fica olhando nosso código e atualizando a execução do node)

## 

## Exemplo chefão

Vamos criar um sistema que armazena informações de algumas alunas matrículadas no formato abaixo:

```
nome: string
idade: number
local: string
conteudoFavorito: string
```

Comportamento do sistema:

- deverá ser possível buscar alunas pela localidade
- caso a pessoa usuária escolha não buscar por localidade, deverá mostrar a tabela de alunas ordenada de forma crescente pela idade

Passo 1: npm init -y

Passo 2: npm i --save readline-sync

Passo 3: npm i --save-dev nodemon

Passo 4: crie o script de start

Passo 5: criar .gitignore

Passo 6: criar a database um array de objetos, não esquecer de exportar

Passo 7: criar o arquivo app.js

Passo 8: Rodar projeto npm run start **`E bora codar!`**

