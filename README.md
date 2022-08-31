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
