# JavaScript Interview Questions (Code Snippets)

## Type coersion
### 1. What will be the output?
```javascript
console.log(1 < 2 < 3)
console.log(3 > 2 > 1)
```
<details>
<summary>Answer</summary>

```javascript
console.log(1 < 2 < 3) // true
console.log(3 > 2 > 1) // false
```
</details>

### 2. What will be the output?
```javascript
console.log(2 + 2 + '2')
console.log('2' + 2 + 2)
```
<details>
<summary>Answer</summary>

```javascript
console.log(2 + 2 + '2') // '42'
console.log('2' + 2 + 2) // '222'
```
</details>

### 3. What will be the output?
```javascript
console.log(('b' + 'a' + + 'a' + 'a').toLowerCase())
```
<details>
<summary>Answer</summary>

```javascript
console.log(('b' + 'a' + + 'a' + 'a').toLowerCase()) // 'banana'
```
</details>

## Primitive vs Reference types
### 4. What will be the output?
```javascript
let obj1 = { key: 'value'};
let obj2 = obj1;
let obj3 = obj2;

obj1.key = 'new value';
obj2 = { key: 'another value' };

console.log(obj1.key, obj2.key, obj3.key);
```
<details>
<summary>Answer</summary>

```javascript
let obj1 = { key: 'value'};
let obj2 = obj1;
let obj3 = obj2;

obj1.key = 'new value';
obj2 = { key: 'another value' };

console.log(obj1.key, obj2.key, obj3.key); // new value another value new value
```
</details>

### 5. What will be the output?
```javascript
let a = {
    x: 1,
    y: 2,
};

let b = a;
a.x = 5;

console.log(a);
console.log(b);
```
<details>
<summary>Answer</summary>

```javascript
let a = {
    x: 1,
    y: 2,
};

let b = a;
a.x = 5;

console.log(a); // {x: 5, y: 2}
console.log(b); // {x: 5, y: 2}
```
</details>

### 6. What will be the output?
```javascript
let a = {a: 1, b:2}
let b = a

a = true

console.log(a)
console.log(b)
```
<details>
<summary>Answer</summary>

```javascript
let a = {a: 1, b:2}
let b = a

a = true

console.log(a) // true
console.log(b) // {a: 1, b: 2}
```
</details>

## let/var/const
## Closures
## Asynchronicity
