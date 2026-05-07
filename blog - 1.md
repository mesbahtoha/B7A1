## Blog Topic 1:
# Why "unknown" is the Safer Choice Over "any" in Typescript

## Introduction

In Typescript, handling unpredictable data is common. Developers often use `any`, but it creates serious risks. A safer alternative is `unknown`, which forces better type checking and improves reliability.

---

Why `any` is a Type Safety Hole

The `any` type disables Typescript's type checking completely.

```ts 
let value: any = "Mesbah";
value = 10;
value.toUpperCase(); // No error, but runtime crash
```

Here, Typescript allows everything, even incorrect operations. This is why `any` is called a type safety hole.

---

## Why `unknown` is Safer

`unknown` keeps flexibility but forces validation before use.

```ts
let value: unknown = "Mesbah";

if (typeof value === "string") {
  console.log(value.toUpperCase());
}
```

You must check the type first, which prevents runtime errors.

---

## Type Narrowing

Type narrowing means refining a variable’s type using checks.

```ts
function checkType(value: unknown) {
  if (typeof value === "string") {
    return "String";
  } else if (typeof value === "number") {
    return "Number";
  }
}
```

This ensures safe and predictable behavior.

---

## Conclusion

- `any` removes all safety
- `unknown` enforces checking
- Type narrowing ensures correctness

Using `unknown` leads to more reliable and maintainable code.
