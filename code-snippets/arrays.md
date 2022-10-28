<div align="center">
<h1>Arrays</h1>
</div>

 <ol>

<li>

**What will be the output?**

```JS
let array = [1, 2, 3, 4, 5, 6];
let [a, b, , ...rest] = array;

console.log(a)
console.log(b)
console.log(c)
console.log(rest)
let c;
```

- A: `1, 2, 3, [ 4, 5, 6 ]`
- B: `1, 2, c is not defined`
- C: `1, 2, NaN, undefined`
- D: `1, 2, c is not defined, [4, 5, 6]`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

---

<li>

**What will be the output?**

```JS
let array1 = [1, 2, 3, 4, 5, 6];
let array2 = array1
array2.push(7, 8, 9, 10)
console.log(array1)
console.log(array2.sort())

```

- A: `[ 1, 2, 3, 4, 5, 6 ], [ 1, 10, 2, 3, 4, 5, 6, 7, 7, 8, 8, 9, 9 ]`
- B: `[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 7, 8, 9, 10 ], [ 1, 10, 2, 3, 4, 5, 6, 7, 7, 8, 8, 9, 9 ]`
- C: `[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 7, 8, 9, 10 ], [ 1, 2, 3, 4, 5, 6, 7, 7, 8, 8, 9, 9, 10 ]`
- D: `[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 7, 8, 9, 10 ], [ 1, 2, 3, 4, 5, 6 ]`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

---

 <li>

**What will be the output?**

```JS
let array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
function checkNum(num) {
    return num >= 4;
}

let newArray1 = [array.map((item) => {
    return item
})].filter(checkNum)

let newArray2 = array.filter(checkNum).map((item) => {
    return item
})

console.log(newArray1)
console.log(newArray2)

```

- A: `[ [] ], [ [ 4, 5, 6, 7, 8, 9, 10 ] ]`
- B: `NaN, []`
- C: `[], [ 4, 5, 6, 7, 8, 9, 10 ]`
- D: `[ [] ], [ 5, 6, 7, 8, 9, 10 ]`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
</li>

---

<li>

**Guess the output**

```JS
 let array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
function checkNum(num) {
    return num > 4;
}
let newArray = [array.filter(checkNum).map((item, index) => {
    return item - array[index]
}).reduce((acc, curr) => {
    return acc + curr
})]

console.log(newArray)
```

- A: `[ 24 ]`
- B: `24`
- C: `NaN`
- D: `Undefined`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

---

<li>

**Guess the following output?**

```JS
const doSomething = (a, b) => {
    return [a + b, a - b, a * b, a / b]
}
let [...rest] = doSomething(4, 2)

console.log(rest * rest)
```

- A: `[ 36, 4, 64, 4 ]`
- B: `18`
- C: `NaN`
- D: `rest is not defined`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
</li>

---

<li>

**Guess the following output?**

```JS
const doSomething = (a, b) => {
    return [a + b, a - b, a * b, a / b]
}
let someVariable = 5;
let [...rest] = doSomething(4, 2)

someVariable = rest.reduce((acc, total) => {
  return 0 + total;
});

console.log(someVariable)
```

- A: `960`
- B: `192`
- C: `NaN`
- D: `2`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: D

</p>
</details>
</li>

---

<li>

**Guess the following output?**

```JS
const doSomething = (a, b) => {
    return [a + b, a - b, a * b, a / b]
}
let someVariable = 5;
let [...rest] = doSomething(4, 2)

someVariable = rest.reduce((acc = 1, total) => {
  return acc + total;
});

console.log(someVariable)
```

- A: `19`
- B: `192`
- C: `NaN`
- D: `18`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

---

<li>

**Guess the following output?**

```JS
const nums = [1, 2, 3, 4, 5, 6];

const res = nums.forEach((item) => {
  return item * item;
});

console.log(res);
```

- A: `null`
- B: `[ 1, 4, 9, 16, 25, 36 ]`
- C: `[1, 2, 3, 4, 5, 6]`
- D: `Undefined`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: D

</p>
</details>
</li>

---

<li>

**Guess the following output?**

```JS
let array = [1, 2, 3];
let array2 = array;
let array3 = [...array];

console.log(array.concat(4));
console.log(array2.concat(5));
console.log(array3.concat(6, 7));
```

- A: `[ 1, 2, 3, 4 ], [ 1, 2, 3, 5 ], [ 1, 2, 3, 6, 7 ]`
- B: `[ 1, 2, 3, 4, 5 ], [ 1, 2, 3, 4, 5 ], [ 1, 2, 3, 6, 7 ]`
- C: `[ 1, 2, 3 ], [ 1, 2, 3, 4, 5 ], [ 1, 2, 3, 6, 7 ]`
- D: `[ 1, 2, 3, 4 ], [ 1, 2, 3, 5 ], [ 1, 2, 3, 6, 7 ]`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>
</li>

---

<li>

**Guess the following output?**

```JS
const clothes = ['jacket', 't-shirt'];
clothes.length = 0;

console.log(clothes[0]);
```

- A: `jacket`
- B: `undefined`
- C: `error`
- D: `not defined`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>
</ol>
