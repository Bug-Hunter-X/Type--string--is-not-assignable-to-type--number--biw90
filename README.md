# Type 'string' is not assignable to type 'number'

This is a common error in TypeScript. It occurs when you try to pass a string to a function that expects a number.

## Bug

```typescript
function add(a: number, b: number): number {
  return a + b;
}

const result = add(1, '2');
```

This code will produce the error: `Type 'string' is not assignable to type 'number'.`

## Solution

The solution is to make sure that you are passing numbers to the function.  You can do this by converting the string to a number using `parseInt()` or `parseFloat()`.

```typescript
function add(a: number, b: number): number {
  return a + b;
}

const result = add(1, parseInt('2', 10));
```