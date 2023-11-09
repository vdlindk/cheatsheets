# Typescript tips

## Rename object properties through function parameters

```typescript
const myObject = {
  label: "firstName",
  val: "Koen",
};

function transform({
  label: param,
  val: value,
}: {
  label: string;
  val: string;
}) {
  return { param, value };
}

console.log(transform(myObject));
// [LOG]: {
//   "param": "firstName",
//   "value": "Koen"
// }
```
