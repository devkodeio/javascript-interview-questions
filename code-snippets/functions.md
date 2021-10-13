<div align="center">
  <h1>Functions</h1>
</div>

<ol>

<li>

**What will be the Output??**

```JS
function setName() {
   this.name = 'devkode';
}
setName();
console.log(this.name);
```

- A: `‘devkode’`
- B: `undefined`
- C: `An Error will be thrown`
- D: `null`

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

**What will be the output ?**

```JS
function fun(num1) {
    var num2 = 6;
    function TDK() {
        var num3 = 10;
        console.log(num1 * num2 * num3)
    }
    return TDK;
}
var TeamDevKode = fun(5)
TeamDevKode ()
```

- A: `undefined`
- B: `0`
- C: `300`
- D: `infinity`

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

**What will be the output ?**

```js
x = 1;
function func() {
  this.x = 2;
  return x;
}
let a = new func();
console.log(a.x);
```

- A: `1`
- B: `2`
- C: `undefined`

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

**What will be the output ?**

```js
let arr = Array.from(Array(10).keys());
function func(a) {
  console.log(arguments.length);
}
func(arr);
func(...arr);
```

- A: `10 10`
- B: `10 1`
- C: `1 10`
- D: `1 1`

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

**What will be the output ?**

```js
function func(a, b) {
  arguments[1] = 2;
  console.log(b);
}
func(1);
```

- A: `2`
- B: `undefined`
- C: `1`
- D: `null`

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

**What will be the output ?**

```js
var x = 3;
var obj = {
  x: 2,
  foo: {
    x: 1,
    bar: function () {
      return this.x;
    },
  },
};
var func = obj.foo.bar;
console.log(func());
console.log(obj.foo.bar());
```

- A: `3 1`
- B: `undefined 1`
- C: `1 1`
- D: `2 1`

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

**What will be the output ?**

```js
var foo = function foo() {
  console.log(foo === foo);
};
foo();
```

- A: `false`
- B: `true`
- C: `error`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>

</li>

---
