# TypeScript

## Intersection Type 
´´´
´´´

## Type Indexing
´´´
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
´´´

## Type from value
´´´

´´´

## Arrays
´´´

´´´

--
• Union Types (A | B): Permiten que una variable acepte varios tipos posibles.

• Generics (<T>): Crean componentes y funciones reutilizables que mantienen el tipado dinámico.

• Type Narrowing / Type Guards: Refinan un tipo amplio a uno específico mediante validaciones como typeof o instanceof.

• Utility Types: Herramientas nativas para transformar tipos existentes (Partial, Pick, Omit, Record).

• Conditional Types (T extends U ? X : Y): Evalúan condiciones lógicas a nivel de tipos para devolver uno u otro.

• Mapped Types: Iteran sobre las claves de un tipo existente para crear uno nuevo con propiedades modificadas.

• Inferencia de Tipos (infer): Extrae y captura tipos dinámicamente dentro de un Conditional Type.

