## Blog Topic 3:
# How Generics Make TypeScript Powerful and Reusable

## Introduction

Generics are one of the most powerful features in TypeScript. They allow developers to write reusable and type-safe code that works with multiple data types.

---

## What Are Generics?

Generics allow functions and classes to work with any type while keeping strict type checking.

```ts
function identity<T>(value: T): T {
  return value;
}
```

This function works for any type but still preserves type safety.

---

## Reusable Functions

Without generics:

```ts
function getString(value: string): string {
  return value;
}
```

With generics:

```ts
function getValue<T>(value: T): T {
  return value;
}
```

Now one function works for all types.

---

## Real Example

```ts
function getProperty<T, K extends keyof T>(obj: T, key: K): T[K] {
  return obj[key];
}

const user = { name: "Mesbah", age: 22 };

getProperty(user, "name");
```

This ensures:

- Key must exist
- Correct return type

---

## Benefits

- Code reusability
- Strong type safety
- Less duplication
- Better scalability

---

## Conclusion

Generics allow developers to write flexible yet safe code. They are essential for building large-scale and maintainable TypeScript applications.
