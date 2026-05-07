# `any` vs `unknown` in TypeScript

## Introduction

In TypeScript, sometimes we do not know what type of data we will get.  
For that, we can use `any` or `unknown`.

But they are not the same.

- `any` removes type safety
- `unknown` keeps code safer

---

## Why `any` is Dangerous

`any` allows everything.  
TypeScript will not check for mistakes.

```ts
let data: any = "Hello";

data.toUpperCase();
data.notRealMethod(); // No TypeScript error
```

This can create bugs in real projects.  
That is why `any` is called a **type safety hole**.

---

## Why `unknown` is Safer

`unknown` also accepts any value, but TypeScript forces us to check the type first.

```ts
let data: unknown = "Hello";

data.toUpperCase(); // Error
```

---

## Type Narrowing

Before using an `unknown` value, we check its type.  
This is called **type narrowing**.

```ts
let data: unknown = "Hello";

if (typeof data === "string") {
  console.log(data.toUpperCase());
}
```

Now TypeScript knows `data` is a string inside the `if` block.

---

## Conclusion

- `any` is unsafe
- `unknown` is safer
- Type narrowing helps prevent errors

So, in most cases, `unknown` is better than `any`.
