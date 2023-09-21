# Programação funcional com Javascript

```javascript

//Imutabilidade
const pessoa = {nome: 'John', age : 25},
pessoa.email = 'john@gmail.com'
Object.freeze(pessoa)
pessoa.nome = 'Marie' // não é possível alterar o valor das propriedades
delete pessoa.idade // não é possivel deltar uma propriedade
pessoa.email = ''

// Com essa pratica estamos reduzindo o número de side effects presentes na operações por trabalharmos com uma referencia o valor ao invés do
// valor bruto do objeto

```

```javascript
//Recursividade

function calcularFatorial(num) {
  if (num <= 1) {
    return 1;
  }

  return numero * calcularFatorial(num - 1);
}

const numero = 6;

calcularFatorial(6);
```

```javascript
const texto = `random string`;

const func = function (valor) {
  return valor * 10;
};
// funções podem ser utilizados como parâmetros para outras funções

function multiplica(valor) {
  return valor * 10;
}

function multiplicar(x) {
  function somar(x) {
    return x + 10;
  }
}
```

```javascript
/*
Funções puras nao possuem side effects e sempre geram o mesmo output independente do input
as funções descritas abaixo não são puras, pois dependem de lógica fora do seu escopo ou manipulam valores fora do seu próprio escopo ou dos parâmetros sendo passados.
*/
function calcularPotencia(base, exp) {
  return Math.pow(base, exp);
}

let contador = 0;
function soma(a, b) {
  contador++;
  return a + b;
}
```
