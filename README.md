# JavaScript Interview Questions (Code Snippets)

## Type coersion
### 1. What will be the output?
```javascript
console.log('9' + 5)
console.log('9' - 5)
```
<details>
<summary>Answer</summary>

```javascript
'95'
4
```
</details>

### 2. What will be the output?
```javascript
true + true === 2
```
<details>
<summary>Answer</summary>

```javascript
true
```
</details>

### 3. What will be the output?
```javascript
console.log(2 + 2 + '2')
console.log('2' + 2 + 2)
```
<details>
<summary>Answer</summary>

```javascript
'42'
'222'
```
</details>

### 4. What will be the output?
```javascript
console.log(1 + 2 * 3)
console.log(1 + '2' * '3')
```
<details>
<summary>Answer</summary>

```javascript
7
7
```
</details>

### 5. What will be the output?
```javascript
console.log(1 < 2 < 3)
console.log(3 > 2 > 1)
```
<details>
<summary>Answer</summary>

```javascript
true
false
```
</details>

### 6. What will be the output?
```javascript
console.log(5 + -"2" - false + "10")
```
<details>
<summary>Answer</summary>

```javascript
310
```
</details>

### 7. What will be the output?
```javascript
console.log(('b' + 'a' + + 'a' + 'a').toLowerCase())
```
<details>
<summary>Answer</summary>

```javascript
'banana'
```
</details>

## Primitive vs Reference types
### 8. What will be the output?
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
new value another value new value
```
</details>

### 9. What will be the output?
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
{x: 5, y: 2}
{x: 5, y: 2}
```
</details>

### 10. What will be the output?
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
true
{a: 1, b: 2}
```
</details>

## let/var/const

### 11. What will be the output?
```javascript
function func() {
    let a = 'red';

    if (true) {
        let a = 'blue';
        console.log(a);
    }
    console.log(a);
}

func();
```
<details>
<summary>Answer</summary>

```javascript
blue red
```
</details>

### 12. What will be the output?
```javascript
const age;
let name;
var name;

console.log(age);
console.log(name);
```
<details>
<summary>Answer</summary>

```javascript
const age; // SyntaxError: Missing initializer in const declaration
let name; 
var name; // SyntaxError: Identifier 'name' has already been declared
```
</details>

### 13. What will be the output?
```javascript
var x = 10;
if(true){
    let x = 20;
}
console.log(x);
```
<details>
<summary>Answer</summary>

```javascript
10
```
</details>

## Hoisting
### 14. What will be the output?
```javascript
function foo() {
    bar();
    return;

    function bar() {
        console.log('bar');
    }
}

foo();
```
<details>
<summary>Answer</summary>

```javascript
'bar'
```
</details>

### 15. What will be the output?
```javascript
var foo = "bar";
function greet(){
    console.log(foo);
    var foo = "foo";
}

greet();
```
<details>
<summary>Answer</summary>

```javascript
undefined
```
</details>

### 16. What will be the output?
```javascript
function foo() {
    a = 100;
    var b = 200;
}

foo();
console.log(a);    
console.log(b);     
```
<details>
<summary>Answer</summary>

```javascript
100
'Error: b is not defined'
```
</details>
