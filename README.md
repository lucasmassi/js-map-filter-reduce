# Manipulando arrays em Javascript
Funções que realmente ajudam na hora de manipular arrays de diversos tipos e tamanhos.

# Map()
```
// Array com números
const numbers = [33, 20, 40, 60];

// Array com objetos
const myObjects = [
  {
    name: 'Lucas Massi',
  },
  {
    name: 'Joel Ribeiro',
  }
];

// Map sendo utilizado para multiplicação, ele sempre irá retornar um novo array
let newArrayNumbers = numbers.map(number => number * 2);
console.log(newArrayNumbers); // => [66, 40, 80, 120]

// Map sendo utilizado para deixar todos nomes do array maíusculo
let newArrayObjects = myObjects.map(object => object.name.toUpperCase());
console.log(newArrayObjects) // => ['LUCAS MASSI', 'JOEL RIBEIRO']

```

# Filter()
```
// Array com números
const numbers = [33, 20, 40, 60];

// Array com objetos
const myObjects = [
  {
    name: 'Lucas Massi',
  },
  {
    name: 'Joel Ribeiro',
  }
];

// Filtramos os valores menores que 40, ou seja, apenas os maiores vão para o novo array
let newArrayNumbers = numbers.filter(number => number > 2);
console.log(newArrayNumbers); // => [33, 20]

// Filtramos o array MyObjects pelo nome
let newArrayObjects = myObjects.filter(object => object.name === 'Lucas Massi');
console.log(newArrayObjects) // => [ { name: 'gandalf' } ]
```

# Reduce()
```
// Array com números
const numbers = [33, 20, 40, 60];

// Array com objetos
const users = [
  {
    name: 'Lucas Massi',
    brtd: 20
  },
  {
    name: 'Joel Ribeiro',
    brtd: 25
  }
];

// Breve explicação:
// prevValue = valor anterior, ou seja,o valor que está sendo acumulado, pode dar o nome que quiser
//             desde que seja o primeiro parametro, e você use o mesmo nome dentro da função
// numero = o elemento do array
// 0 = valor inicial da contagem, no nosso caso zero
let totalCount = numbers.reduce( (prevValue, number) => prevValue + number, 0 )
console.log(totalCount) // => 153

// prevValue = valor anterior, ou seja,o valor que está sendo acumulado, pode dar o nome que quiser
//             desde que seja o primeiro parametro, e você use o mesmo nome dentro da função
// objeto = um elemento do array
// 10 = valor inicial da contagem, no nosso caso 10
let countYears = users.reduce( (prevValue, user) => prevValue + user.brtd, 10)
console.log(countYears) // => 45
