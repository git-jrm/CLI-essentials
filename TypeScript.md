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

## Type alias
```
type IdType = '${string}-${string}-${string}-${string}-${string}'
type PayMethods = 'debit' | 'credit' | 'cash' | 'account' // --> Union Types

type ClientInput = {
  name: string
  credit: number
}

type ClientProperties = {
  readonly id?: IdType
  isActive?: boolean
  payMethod?: PayMethods
}

type Client = ClientInput & ClientProperties // --> Intersection Types

let client: Client = {
  name: 'Bob',
  credit: 10000
}

function createClient(client: ClientInput): Client {
  const { name, credit} = client
  return {
    id: crypto.randomUUID(),
    name,
    credit,
    isActive: true
  }
}

const bob = ObjectcreateClient({ name: 'Bob', credit: 10000 })
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
  country: 'USA',
  city: 'NY'
}
```

## Type from value
```
```

## Arrays
```
```

--

• Generics (<T>): Crean componentes y funciones reutilizables que mantienen el tipado dinámico.

• Type Narrowing / Type Guards: Refinan un tipo amplio a uno específico mediante validaciones como typeof o instanceof.

• Utility Types: Herramientas nativas para transformar tipos existentes (Partial, Pick, Omit, Record).

• Conditional Types (T extends U ? X : Y): Evalúan condiciones lógicas a nivel de tipos para devolver uno u otro.

• Mapped Types: Iteran sobre las claves de un tipo existente para crear uno nuevo con propiedades modificadas.


