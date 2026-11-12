# TypeScript

TypeScript is strongly and statically typed. No type mismatches by compile-time checking and Type inference.

## Typing function
```
function process({ name, age }): { name: string, age: number }): number {
  console.log('Processed ${name}, ${age} y/o.')
  return age
}
let ageProcessed: number
ageProcessed = process({ name: 'Bob', age: 40 })
```

## Typing callback function
```
const processFunction = (fn: (name: string) => string) ==> {
  fn('Bob')
}

const function((name) ==> {
  console.log('Process ${name}')
  return string
)

let status: string
status = processFunction(function)
```

## Typing arrow function
```
const processLong: (a: number, b: number) => number = (a, b) => {
  return a + b;
};

const processShort = (amount: number, add: number): number => {
  return amount + add;
};

type ProcessInput = (amount: number, add: number) => number;
const execute = (fn: processInput) => fn(100, 20);
execute(processLong);  // 120
execute(processShort); // 120
```

## Function inference
```
const cardTypes = ['Mastercard', 'Visa', 'American']
cardTypes.forEach(function (type) {
  console.log(type.toUpperCase())
})
```

## Objects
```
let client = {
  name: 'Bob',
  credit: 10000
}
function createClient(name: string, credit: number){
  return { name, credit}
}
const bob = createClient('Bob', 10000)
```

## Intersection Type 
```
```

## Type Indexing
```
type PersonProperties = {
  isActive: bolean,
  address: {
    country: string,
    city: string
  }
}

const addressPerson: PersonProperties['address']{
  country: 'Earth',
  city: 'Madrid'
}
```

## Type from value
```
```

## Arrays
```
```

--
• Union Types (A | B): Permiten que una variable acepte varios tipos posibles.

• Generics (<T>): Crean componentes y funciones reutilizables que mantienen el tipado dinámico.

• Type Narrowing / Type Guards: Refinan un tipo amplio a uno específico mediante validaciones como typeof o instanceof.

• Utility Types: Herramientas nativas para transformar tipos existentes (Partial, Pick, Omit, Record).

• Conditional Types (T extends U ? X : Y): Evalúan condiciones lógicas a nivel de tipos para devolver uno u otro.

• Mapped Types: Iteran sobre las claves de un tipo existente para crear uno nuevo con propiedades modificadas.

• Inferencia de Tipos (infer): Extrae y captura tipos dinámicamente dentro de un Conditional Type.

