# Lógica de Programação e Algorítimos com JavaScript

Resolução dos exercícios do livro [Lógica de Programação e Algorítimos com JavaScript (2º edição)](https://www.novatec.com.br/livros/logica-programacao-algoritmos-com-javascript-2ed/) de Edécio Fernando Iepsen (editora Novatec).

> Todos os exercícios desse repositório foram resolvidos com a ajuda da ferramenta [prompt-sync](https://www.npmjs.com/package/prompt-sync), para podermos rodar `prompts` de JavaScript no terminal, com NodeJS. Mais informações no [prompt-sync-template](https://github.com/petry078/prompt-sync-template).

## Capítulo 1

**a) Elaborar um programa que leia um número. Calcule e informe seus vizinhos, ou seja o número anterior e posterior.**

```javascript
let numero = Number(prompt("Número:"))
let menor = numero - 1
let maior = numero + 1

alert(`Vizinhos: ${menor} e ${maior}`)
```
**b) Elaborar um programa para uma pizzaria, o qual leia o valor total de uma conta e quantos clientes vão pagá-la. Calcule e informe o valor a ser pago por cliente.**

```javascript
let conta = Number(prompt("Qual valor da conta?"))
let clientes = Number(prompt("Quantos clientes vão pagar?"))
let resposta = conta / clientes

alert(`Valor por pessoa: R$ ${resposta},00`)
```

**c) Elaborar um programa para uma loja, o qual leia o preço de um produto e informe as opções de pagamento da loja. Calcule e informe o valor para pagamento à vista com 10% de desconto e o valor em 3x.**

```javascript
let preco = Number(prompt("Qual valor do produto?"))
let desconto = Math.round(preco * 0.10)
let precoComDesconto = Math.round(preco - desconto)
let precoParcelado = Math.round(preco / 3)

alert(`Preço à vista: R$${precoComDesconto}, ou em 3x de R$${precoParcelado}, sem júros`)
```

**d) Elaborar um programa que leia 2 notas de um aluno em uma disciplina. Calcule e informe a média das notas.**

```javascript
let n1 = Number(prompt("N1: "))
let n2 = Number(prompt("N2: "))
let media = (n1 + n2) / 2

alert(`Média: ${media}`)
```
## Capítulo 2

**a) Elaborar um programa para um cinema, que leia o título e a duração de um filme em minutos. Exiba o título do filme e converta a duração para horas e minutos.**

```javascript
let filmTitle = prompt("Film title: ")
let filmLenght = Number(prompt("Lenght in minutes: "))

let filmHours = Math.floor(filmLenght / 60)
let filmMinutes = 130 % 60

alert(`${filmTitle}\n${filmHours} hours and ${filmMinutes} minutes.`)
```

**b) Elaborar um programa para uma revenda de veículos. O programa deve ler modelo e preço do veículo. Apresentar como resposta o valor da entrada (50%) e o saldo em 12x.**

```javascript
let carModel = prompt("Car model: ")
let carPrice = Number(prompt("Car price: "))

let carPrice1 = carPrice / 2
let carPrice2 = carPrice1 / 12

alert(`${carModel}\n First pay: R$ ${carPrice1.toFixed(2)} + 12x R$ ${carPrice2.toFixed(2)}`)
```

**c) Elaborar um programa para um restaurante que leia o prceo por kg e o consumo (em gramas) de um cliente. Exiba o valor a ser pago**

```javascript
let priceKg = Number(prompt("Price by kilogram: "))
let priceGr = Number(prompt("Customer consumption (in grams): "))

let priceToPay = (priceKg / 1000) * priceGr

alert(priceToPay)
```

**d) Uma farmácia está com uma promoção. Na compra de duas unidades de um mesmo medicamento, o cliente recebe como desconto os centavos do valor total. Elaborar um programa que leia a descrição e o preço de um medicamento. Informe o valor do produto na promoção.**

```javascript
let price = Number(prompt("Price: "))
let price2 = Math.floor(price) * 2
alert(`Buy 2 pay only $ ${price2}`)
```
**e) Elaborar um programa para uma lan house de um aeroporto. O programa deve ler o valor de cada 15 minutos de uso de um computador e o tempo de uso por um cliente em minutos. Informe o valor a ser pago pelo cliente, sabendo que as frações extras de 15 minutos devem ser cobradas de forma integral.**

```javascript
let price15 = Number(prompt("Price for 15 min:"))
let timeUsed = Number(prompt("Minutes used:"))
let total = (timeUsed / 15) * price15
alert(`Bill: $ ${total}`)
```

**f) Um supermercado está com uma promoção. Para aumentar suas vendas no setor de higiene, cada etiqueta de produto deve exibir uma mensagem anunciando 50% de desconto (para um item) na compra de três unidades do produto. Elaborar um programa que leia descrição e preço de um produto. Apresente as mensagens indicando a promoção.**

```javascript
let price = Number(prompt("Price:"))
let discount = price / 2
let total = discount + price + price
alert(total)
```
## Capítulo 3

**a) Elaborar um programa para uma empresa que leia o salário e o tempo que um funcionário trabalha na empresa. Sabendo que a cada 4 anos (quadreiênio) o funcionário recebe um acréscimo de 1% no salário, calcule e informe o número de quadriênios a que o funcionário tem direito a o salário final.**

```javascript
const prompt = require("prompt-sync")();
let salary = Number(prompt("Salary: "))
let time = Number(prompt("Time of service (years): "))
let years4 = Math.floor(time / 4)
let bonus = salary * years4 / 100
console.log(`Quadrenniums: ${years4}`)
console.log(`Final salary: ${(salary+bonus).toFixed(2)}`)
```

**b) Elaborar um programa para uma veterinária, que leia o peso de uma ração em kg e o quanto um gato consome por dia da ração, em gramas. Informe quantos dias irá durar a racão e quanto sobra da ração (em gramas).**

```javascript
const prompt = require("prompt-sync")();
let weightInKg = Number(prompt("Weight (kg): "))
let catEatsByDay = Number(prompt("Cat eats by day (grams): "))
let weightInGrams = weightInKg * 1000
let itWillLast = Math.floor(weightInGrams / catEatsByDay)
let leftover = weightInGrams % catEatsByDay
console.log(`This cat will eat for ${itWillLast} days and will be ${leftover} grams of leftover`)
```

## Capítulo 4

**a) Elabore um programa que leia um número. Informe se ele é par ou ímpar. Faça com if..else tradicional e, após, tente criar a condição com o operador ternário.**

```javascript
const prompt = require("prompt-sync")()
let num1 = prompt("Número: ")

 if (num1 % 2 === 0) {
     console.log(`Par ${num1}`) //template string
 } else { 
     console.log("Ímpar")
 }

//Ternary
 num1 % 2 === 0 ? console.log(`Par ${num1}`) : console.log("Ímpar")
```

**b) Elabore um programa que leia a velocidade permitida em uma estrada e a velocidade de um condutor (carro). Se a velocidade for inferior ou igual à permitida, exiba "Sem multa". Se a velocidade for de até 20% maior que a permitida, exiba "Multa leve". Se a velocidade for superior a 20% da velocidade permitida, exiba "Multa grave".**

```javascript
let speedLimit = Number(prompt("Speed limit (km/h): "))
let carSpeed = Number(prompt("Car speed (km/h): "))
if (carSpeed <= speedLimit){
    console.log("No fine ;D")
} else if (carSpeed <= speedLimit + (speedLimit * 0,20)) {
    console.log("Lesser fine")
} else {
    console.log("Greater fine")
}
```

**c) Elaborar um programa para simular um parquímetro, o qual leia o valor de moedas depositado em um terminal de estacionamento rotativo. O programa deve informar o tempo de permanência do veículo no local e o troco (se existir). Se o valor for inferior ao tempo mínimo, exiba a mensagem: "Valor insuficiente".**

```javascript
Resolução
```

**d) Elaborar um programa que leia três lados e verifique se eles podem ou não formar um triângulo. Para formar um triângulo, um dos lados não pode ser maior que a soma dos outros dois. Caso possam formar um triângulo, exiba também qual o tipo do triângulo: Equilátero (3 lados iguais), Isóceles (2 lados iguais) e Escaleno (3 lados diferentes).**

```javascript
const prompt = require("prompt-sync")();

console.log("* Equilateral = 3 equal sides;")
console.log("* Isosceles = 2 equal sides and 1 different;")
console.log("* Scalene = 3 different sides.")

let sideAB = prompt("Centimeters for A-B:  ")
let sideBC = prompt("Centimeters for B-C:  ")
let sideCA = prompt("Centimeters for C-A:  ")

if (sideAB == sideBC && sideBC == sideCA) {
    console.log("Equilateral")
} else if (
    sideBC == sideCA && sideAB != sideBC ||
    sideAB == sideCA && sideBC != sideCA ||
    sideAB == sideBC && sideCA != sideAB 
    ){
        console.log("Isosceles")
    } else if (
        sideAB != sideBC && sideCA != sideAB ||
        sideBC != sideCA && sideAB != sideBC ||
        sideCA != sideAB && sideAB != sideCA
    ){
        console.log("Scalene")
    }
```
> [Veja os desenhos feitos durante a abstração deste problema aqui.](https://github.com/petry078/exercicios-javascript/blob/main/img/README.md)

## Capítulo 5

**a) Elabore um programa que leia o nome de uma fruta e um número. O programa deve repetir a exibição do nome da fruta, de acordo com o número informado. Utilize `*` para separar os nomes.**

```javascript
const prompt = require("prompt-sync")()
let fruit = prompt("Fruit: ")
let num1 = prompt("Number: ")
let counter = 0

do {
    counter++
    console.log(`${fruit} *`)
} while (counter < num1)
```

**b) Digamos que o número de chinchilas de uma fazenda triplica a cada ano, após o primeiro ano. Elabore um programa que leia o número inicial de chinchilas e anos e informe ano a ano o número médio previsto de chinchilas na fazenda. O número inicial de chinchilas deve ser maior ou igual a 2 (um casal).**

```javascript
const prompt = require("prompt-sync")()
let initialNumberOfRodents = prompt("Initial number of Chinchilas: ")
let years = prompt("How many years of chinchila production? ")
let counter = 0

do {
    counter++
    console.log(`After year ${counter}: ${initialNumberOfRodents * 3}`)
    initialNumberOfRodents = initialNumberOfRodents * 3
} while (counter < years)
```

**c) Elabore um programa que leia um número e verifique se ele é ou não perfeito. Um número dito perfeito é aquele que é igual à soma dos seus divisores inteiros (exceto o próprio número). O programa deve exibir os divisores do número e a soma deles.**

```javascript
```
