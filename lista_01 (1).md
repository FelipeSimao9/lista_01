# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

``a) Imprime os números pares de 1 a 10.``

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10.

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

``A) let carro = new Carro("Toyota");``

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

``A) 18``

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

``A) ![Uma imagem](assets/ex04_1.PNG)``

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

``A) ![Uma imagem](assets/ex05_1.PNG)``

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

``A) "Olá, meu nome é João. Olá, meu nome é Maria."``

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!
```javascript
//criando a classe animal e atribuindo dois atributos nome e idade
class Animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    //definindo o metodo descrever 
    descrever() {
        console.log(`O animal ${this.nome} tem ${this.idade} anos.`);
    }
}

// criar objetos dentro da classe "Animal"
const cachorro = new Animal("cachorro", 5);
const gato = new Animal("gato", 3);

// usando o metodo "Descrever" para os objetos da classe animal gato e cachorro
cachorro.descrever();
gato.descrever();

```
______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

```javascript

// cria a classe animal
class Animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`O animal ${this.nome} tem ${this.idade} anos.`);
    }
}

// cria a classe gato que ehrda da classe animal
class Gato extends Animal {
    constructor(nome, idade, cor) {
        super(nome, idade);
        this.cor = cor;
    }

    miar() {
        console.log("Miauuu!");
    }
}

// cria os objetos gato e cachorro da classe animal
const cachorro = new Animal("cachorro", 5);
const gato = new Gato("gato", 3, "preto");

// chama o metodo descrever para os animais e o miado do gato
cachorro.descrever();
gato.descrever();
gato.miar();

```

______

**9)** Vamos criar um programa em JavaScript para somar notas!
```javascript
//cria a classe somadorDeNotas
class SomadorDeNotas {
    constructor() {
        this.total = 0;
    }

    adicionarNota(nota) {
        this.total += nota;
    }

    verTotal() {
        console.log(`O total das notas é: ${this.total}`);
    }
}

// cria o objeto somador para somar as notas
const somador = new SomadorDeNotas();

// adiciona notas aleatorias
somador.adicionarNota(8);
somador.adicionarNota(7.5);
somador.adicionarNota(9);

// chama o metodo somador para ever o total das notas
somador.verTotal();
```

______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:
```javascript
// cria aclasse funcionario
class Funcionario {
    // construtor para atribuir os atributos nome idade e salariobase
    constructor(nome, idade, salarioBase) {
        this.nome = nome;
        this.idade = idade;
        this.salarioBase = salarioBase;
    }

    // metodo para calcular o salario
    calcularSalario() {
        return this.salarioBase; 
    }
}

// cria a classe professor que herda da classe funcionario as funcoes nome idade e salariobase
class Professor extends Funcionario {
    // construtor que herda o nome a idade e o salariobase da classe funcionario e que adiciona duas novas: disciplina e horas aula
    constructor(nome, idade, salarioBase, disciplina, horasAula) {
        super(nome, idade, salarioBase); 
        this.disciplina = disciplina;
        this.horasAula = horasAula;
    }

    // metodo para calcular o salario do professor
    calcularSalario() {
        return this.salarioBase * this.horasAula; //multiplica o salario base pelas horas de aula
    }
}

// cria o objeto professor com dados inventados
const professor1 = new Professor("João", 35, 3000, "Matemática", 20); // salario base: 3000, 20 horas de aula
const professor2 = new Professor("Maria", 40, 3500, "Português", 18); // salario base: 3500, 18 horas de aula

//chamando o método calcularSalario() para cada objeto e mostrando o salario calculado no console
console.log(`${professor1.nome}: Salário total = R$${professor1.calcularSalario()}`);
console.log(`${professor2.nome}: Salário total = R$${professor2.calcularSalario()}`);

```
