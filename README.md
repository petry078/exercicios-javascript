# Resolução dos exercícios do livro Lógica de Programação e Algorítimos com JavaScript

## Capítulo 1

**a) Elaborar um programa que leia um número. Calcule e informe seus vizinhos, ou seja o número anterior e posterior.**

```javascript
let numero = Number(prompt("Número:"))
let menor = numero - 1
let maior = numero + 1

alert(`Vizinhos: ${menor} e ${maior}`)
```
