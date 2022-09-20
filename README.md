# Lógica de Programação e Algorítimos com JavaScript

Resolução dos exercícios do livro [Lógica de Programação e Algorítimos com JavaScript](https://www.novatec.com.br/livros/logica-programacao-algoritmos-com-javascript-2ed/) de Edécio Fernando Iepsen (novatec).

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
