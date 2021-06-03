# Lógica - Variáveis, Tipos de Dados, Operadores e Condicional 🚀

**Semana 2 – Resolução de Problemas/Lógica aplicada e JavaScript (sintaxe básica)**

- Tipos de dados
- Variáveis
- Operadores
- Estrutura Condicionais

### 1. Apresentação da {profa} Simara

Ex-aluna {reprograma}, desenvolvedora na ThoughtWorks e criadora do Podcast Quero Ser Dev.

### 

### 2. Aprender a aprender programação

- Lógica
- Sintaxe
- Prática
- Como você funciona?
- Foco, dedicação e muita repetição



### 3. O que é JavaScript?

Segundo o livro "Estrutura de dados e algoritmos com javascript", de  Loiane Groner: "Javascript é uma das linguagens de programação mais  populares atualmente, é conhecida como a linguagem da internet porque os navegadores a entendem de modo nativo, sem a instalação de qualquer  plugin."

Praticamente todos os sites e aplicações web usam javascript, até  outras ferramentas que são usadas para web, no fim das contas vão  precisar transformar o código em javascript para que o navegador  entenda.

Além disso, a linguagem javascript evoluiu muito e aparecem até em  aplicativos mobile(com React Native), Softwares de interface gráfica  para Desktop(electron) e até games, robótica e inteligência artificial.  Além disso, tem o backend também utilizando o nodejs.

E tem uma lista imensa de empresas que usam Javascript ou alguma  ferramenta que derivou dela, então o próprio netflix, uber, instagram,  facebook, twitter entre outras. Usam o react que é uma outra ferramenta  baseada em javascript.

Antes da gente encerrar essa parte eu quero fazer um combinado com  você. Se você, é uma pessoa que já teve algum contato com o Javascript,  preste bastante atenção a essas aulas, pois toda vez que você for criar  soluções mais complexas, você vai precisar ter essa base de fundamentos  bem sólida.

| Pontos positivos                                             | Pontos negativos                                             |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `uma ótima linguagem para um primeiro contato com a programação e, por consequência, para se estudar lógica de programação` | Pode conter brechas para a execução de ações maliciosas      |
| `Sintaxe acessível`                                          | Pode ser renderizada de maneiras diferentes pelos dispositivos compatíveis, causando problemas de desempenho. |
| `Grande comunidade ao redor do mundo fazendo a ferramenta evoluir` | Atualizações nem sempre compatíveis com todos os navegadores e sistemas existentes. |

### 

### 4. O que é NodeJS?

É um interpretador Javascript que não depende do navegador. Ele é  formado pelo V8, motor interpretador de Javascript criado pelo Google, e pela libuv, uma biblioteca que deu características de linguagem  back-end para o node.

Node.js revolucionou a forma de programar em Javascript, pois a  linguagem evoluiu de uma forma de dar vida aos elementos no navegador  para uma linguagem capaz de criar software para tratamento de dados no  backend.

### 

### 5. Primeiros passos com Javascript

- Javascript no navegador, interação: console, alert e prompt **Console:** Esta função permite que você faça log no console do navegador moderno. Isso ajuda você a depurar seu código facilmente.

  **alert:** Usar o alerta exibe uma caixa de diálogo com a mensagem fornecida. A  próxima linha de código não será executada até que a caixa de diálogo  seja fechada (clicando no botão OK)

  **Prompt:** O uso do prompt permitirá que você recupere as entradas do usuário. O primeiro parâmetro é o título da caixa de diálogo e o segundo (parâmetro opcional) é o valor padrão da caixa de texto.

- Hello World no terminal do vs code

- 2 formas de rodar um arquivo .js com node (direto no terminal ou run em um arquivo)

### 

### 6. Lógica aplicada

#### 

#### 6.1 Tipos de dados:

JavaScript é uma linguagem dinamicamente tipada.

Isso significa dizer que não é preciso especificar o tipo do dado  quando formos declarar uma variavél. Além disso os tipos de dados são  convertidos automaticamente conforme a necessidade de execução do nosso  script. Mais pra frente você vai perceber isso melhor.

Aprender tipos de dados é um super poder para resolver problemas com estrutura de dados e algoritmos lá no futuro.

Vamos aprender os tipos de dados primitivos em javascript:

##### 

##### String

É uma cadeia de caracteres. A gente identifica o dado do tipo string  quando caracteres formam palavras ou frases entre aspas simples ou  duplas.

Quando queremos escrever textos em javascript é preciso usar uma das  três formas abaixo. Elas não possuem diferenças, só ter atenção pois  você não pode em uma única string começar com uma e terminar com a  outra.

```
Aspas simples ' '
Aspas duplas " "
Template literals ``
```

Podemos também unir strings concatenando ou interpolando.

Os templates literals podemos usar quando queremos interpolar uma string com uma expressão de javascript.

Qual aspas usar? Até onde eu aprendi é uma preferência da pessoa desenvolvedora ou acordo do time. Agora, o JSON só aceita aspas duplas.

```
'Hello'
"World"

//concatenando
console.log('Hello' + ' ' + "World")
// Vai imprimir Hello World

console.log('Hello' + "World")
//Vai imprimir sem espaço HelloWorld

myName = "Simara";
console.log('Hello' + " " + myName)
//Vai imprimir Hello Simara

//interpolando
myName = "Simara";
console.log(`Hello ${myName}`)
//Vai imprimir Hello Simara
```

# 

##### 

##### Number

É o tipo de dado númerico no Javascript e podemos identificar,  geralmente como números inteiros ou decimais, também conhecido como  float.

```
1

1.5 
```

# 

##### 

##### Boolean

É o tipo de dado lógico e tem apenas dois valores.

```
true 
false
```

# 

##### 

##### Null x undefined

Null é um objeto vazio e undefined é o valor pra uma variável não definida, por exemplo.

# 

##### 

##### Objeto, array e function

Um objeto do JavaScript é um mapeamento entre chaves e valores. Chaves são Strings e valores podem ser de qualquer tipo.

```
{ 
    name: "simara",
    age: 32,
    role: "dev",
    isTeacher: true
}
```

Arrays são objetos perfeitos para representação de listas e conjuntos.

```
["aila", "maria", "paula"]
```

Funções são objetos comuns com a capacidade adicional de serem chamados.

```
function soma (a,b) {
    return a + b
}

soma(2,5) // 7
```

#### 

#### Determimando tipos usando o operador typeof

O operador typeof pode te ajudar a encontrar o tipo de sua variavel.

```
typeof 32 //Number
var age = 32 
console.log(typeof age) //Number

typeof "Simara" //string
var myName = "Simara" 
console.log(typeof myName) //String

let lastName
console.log(typeof lastName) //undefined

let myObject = {
    "name" : "Simara",
    "age": 32
}

console.log(typeof myObject) //object

let object = null
console.log(typeof object) //object

function subtrair(){}
console.log(typeof subtrair) //function

let alunas = []
console.log(typeof alunas) //object
```

#### 

#### 6.2 Variáveis:

"Variaveis armazemam dados que podem ser denfinidos, atualizados e recuperados sempre que necessário".

Mas como declarar variaveis no JavaScript?

A gente precisa usar uma palavra reservada do Javascript e um  identificador. Além disso, a gente pode atribuir valores para essas  variaveis.

É mais ou menos assim:

A palavra reservada: var Identificador: myName Atribuindo valor: "Simara"

Declarando uma variavel: var myName Atribuindo valor: myName = Simara Recuperando o dado que está guardado na variavel: myName

Aqui vão algumas dicas pra você ficar muito expert em declarar variaveis com Javascript

- **O que pode?** Podem começar com letra, $ ou _ É possível usar acento, símbolos e números
- **O que não pode?** Não pode começar com número Não pode conter espaço Não podem ser palavras reservadas
- **Qual o ideal?** Ter atenção, pois é case sensitive Use nomes coerentes

Além disso, é também importante saber que a linguagem Javascript  evolui a cada ano. E desde 2015, tem havido uma nova versão lançada a  cada ano que chamamos de ECMAScript. Então não se assuste se você  esbarrar com frenquencia nesse conceito por aí. ECMA é uma organização  que padroniza informações, e o JavaScript foi submetido à ECMA para que  fosse padronizado daí nasceu o ECMAScript, o novo padrão da linguagem.

A mudança mais significativa na linguagem ocorreu em 2015 e é  conhecida com ECMAScript 6 ou ES6, ela surgiu pra linguagem ficar mais  flexivel no uso com o paradigma orientado a objeto. E aqui nas variáveis surgiram as palavras reservadas let e const.

Então agora você pode declarar variaveis das seguintes formas:

```
let language = "Javascript"
const padrão = "ECMAcript"
```

Vem entender melhor quando usar cada uma.

- **Diferenças entre let, const e var:**

1- var são declarações de escopo global ou de escopo de funções, enquanto let e const são de escopo bloqueado.

2- var podem ser atualizadas ou reatribuídas nestes escopos

3- let podem ser atualizadas, mas const não podem ser atualizadas ou reatribuídas

4- Enquanto var e let podem ser declaradas sem inicializar, const precisa ser inicializada durante a declaração

5- var sofrem hoisting de escopo

Ficou por fora quando eu falei de escopo e de hoisting?  Esses conceitos são mais faceis de entender com a mão no código.

Escopo se refere ao local em que podemos acessar a variavel no  algoritmo ou em uma função. E as variaveis podem ser locais ou globais.

Para entender local e global:

```
{
    var age = 32;
}

console.log(age)

//Depois trocar para let

{
    let age = 32;
}

console.log(age)
```

Para entender hoisting:

```
console.log(name)
let name = "Simara"; //vai dar erro

console.log(myLastName)
var myLastName = "Conceição";

var name // por debaixo dos panos é isso que acontece, a declaração sofre hoisting, esse fenomeno de elevação que 
leva a declaração da variavel lá pra cima do escopo. 
name = "Simara";
```

A boa prática é: sempre que possível, evite usar variaveis globais em javaScript, pois elas são prejudiciais para a qualidade do seu cógigo.

#### 

#### 6.3 Operadores:

Precisamos de operadores para realizar qualquer operação em uma  linguagem de programação. O javascript também tem seus operadores  aritméticos, de atribuição, lógicos entre outros.

**Aritméticos:**

| Operador | Descrição                  |
| -------- | -------------------------- |
| `+`      | Adição                     |
| `-`      | Subtração                  |
| `*`      | Multiplicação              |
| `/`      | Divisão                    |
| `%`      | Módulo ou resto da divisão |
| `++`     | Incremento                 |
| `--`     | Decremento                 |



**Atribuição:**

| Operador | Descrição                   |
| -------- | --------------------------- |
| `=`      | Atribuição                  |
| `+=`     | Atribuição de soma          |
| `-=`     | Atribuição de subtração     |
| `*=`     | Atribuição de multiplicação |
| `/=`     | Atribuição de divisão       |
| `%=`     | Atribuição de resto         |



**Comparação:**

| Operador | Descrição                             |
| -------- | ------------------------------------- |
| `==`     | Igual a                               |
| `===`    | Igual a (tanto o valor quanto o tipo) |
| `!=`     | Diferente de                          |
| `>`      | Maior que                             |
| `>=`     | Maior ou igual a                      |
| `<`      | Menor que                             |
| `<=`     | Menor ou igual a                      |



**Lógicos:**

| Operador | Descrição |
| -------- | --------- |
| `&&`     | E         |
| \|\|     | Ou        |
| `!`      | Negação   |



#### 

#### 6.4 Condicional:

São instruções de controle que podemos usar ao construir nossos  códigos. Vamos estudar estudar 2 estruturas condicionais: if...else e  switch.

- Podemos usar **if** se quisermos executar um bloco de código somente se a condição ou verificação lógica for verdadeira.

```
let num = 1
if (num ===1) {
    console.log('num é igual a 1')
}
```

- Podemos usar **if...else** se quisermos executar um  bloco de código somente se a condição ou verificação lógica for  verdadeira. Ou outro bloco de código, somente caso a condição seja  falsa.

```
let number = 0
if (number ===1) {
    console.log('number é igual a 1')
} else {
    console.log(`number não é igual a 1, o valor de number é ${number}`)
}
```

- Além disso para diferentes condições podemos usar vários **if...else** se quisermos executar vários blocos de códigos diferentes.

```
let mes = 'setembro'
if (mes === 'fevereiro') {
    console.log('tem carnaval')
} else if (mes === 'junho'){
    console.log('tem são joão')
} else if (mes === 'dezembro'){
    console.log('tem natal')
} else {
    console.log(`${mes} não é um mês festivo.`)
}
```

- Agora, se a condição que estivermos avaliando for a mesma que a  anterior, porém com valores diferentes, podemos usar a instrução **switch**:

```
let diaDaSemana = 'segunda'
switch (diaDaSemana) {
    case 'domingo':
        console.log('Domingou')
        break
    case 'sábado':
        console.log('Sabadou')
        break
    case 'sexta':
        console.log('Sextou')
        break
    default: 
        `${diaDaSemana} não é um dia festivo.`
}
```

Atenção para as palavras reservadas case, break e default.



#### 

#### 6.5 **Exemplos:**

| Exemplo 01  | Descrição                                                    |
| ----------- | ------------------------------------------------------------ |
| `Variaveis` | Vamos criar variaveis usando let e const, atribuir valores, identificar comportamentos e saídas quando tentarmos recuperar. |

| Exemplo 02                | Descrição                                                    |
| ------------------------- | ------------------------------------------------------------ |
| `Concatenar x interpolar` | Vamos criar variaveis usando let, const, atribuir strings e vamos concatenar e interpolar. |

| Exemplo 03            | Descrição                                                    |
| --------------------- | ------------------------------------------------------------ |
| `Média entre números` | Crie uma variavel e atribua como valor uma operacao de média entre 5 números inteiros e positivos. |

| Exemplo 04     | Descrição                                                    |
| -------------- | ------------------------------------------------------------ |
| `Quero lucrar` | Crie um programa que me diga como lucrar nesta situação: quero  vender uma bicicleta que 60% do seu valor é R$300, por quanto devo  vendê-la para lucrar 25%? |

| Exemplo 05    | Descrição                                                    |
| ------------- | ------------------------------------------------------------ |
| `Quero somar` | Faça um programa que peça dois números e imprima no console a soma desses dois números. |

| Exemplo 06   | Descrição                                                    |
| ------------ | ------------------------------------------------------------ |
| `Desapegada` | Crie um programa que me diga quanto cobrar para vender um notebook  usado: o seu custo foi R$3000, por quanto devo vendê-lo descontando 25%? |

| Exemplo 07             | Descrição                                                    |
| ---------------------- | ------------------------------------------------------------ |
| `conversor de medidas` | Escreva um programa que receba um valor em metros e o exiba no console convertido em milímetros. |

| Exemplo 08                      | Descrição                                                    |
| ------------------------------- | ------------------------------------------------------------ |
| `Semaforo, sinal ou sinaleira?` | Utilizando os conceitos que estudamos, vamos criar um programa que funcionará como um sinal de transito. |

| Exemplo 09 | Descrição                                                    |
| ---------- | ------------------------------------------------------------ |
| `FizzBuzz` | Utilizando os conceitos que estudamos, vamos criar um programa que  irá imprimir 'FizzBuzz'para números divisiveis por 3 e 5, para números  divisíveis por 3 irá impirmir 'Fizz' e para números divisíveis por 5 irá imprimir 'Buzz' e por fim, se não cumprir nenhum dos casos acima  imprime o próprio número. |

| Exemplo 10       | Descrição                                                    |
| ---------------- | ------------------------------------------------------------ |
| `É dia de aula?` | Utilizando os conceitos que estudamos, vamos criar um programa que irá nos informar os dias de aula para a nossa turma. |



------



