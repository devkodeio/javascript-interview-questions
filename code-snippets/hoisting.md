<div align="center">
  <h1>Hoisting</h1>
</div>

<ol>
<li>

**What will be the output ?**

```JS
console.log(typeof foo);

function foo() {
  return "bar";
}
var foo = "bar";

```

- A: `undefined`
- B: `string`
- C: `function`

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

```JS
function foo() {
  return "bar";
}
var foo;

console.log(typeof foo);
```

- A: `undefined`
- B: `string`
- C: `function`

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

```JS
if (true) {
  function foo() {
    console.log(1);
  }
} else {
  function foo() {
    console.log(2);
  }
}

foo();
```

- A: `1`
- B: `2`

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
function foo() {
  bar();

  return;

  function bar() {
    console.log("bar");
  }
}

foo();
```

- A: `undefined`
- B: `bar`
- C: `Uncaught ReferenceError: bar is not defined`

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

```JS
function foo(x) {
  x();

  function x() {
    console.log("foo");
  }
}

foo(function() {
  console.log("bar")
});
```

- A: `foo`
- B: `bar`
- C: `Uncaught ReferenceError: x is not defined`

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
foo();

function foo() {
  console.log(1);
}

var foo = function() {
  console.log(2);
};

function foo() {
  console.log(3);
}

foo();
```

- A: `3 3`
- B: `3 2`
- C: `1 2`
- D: `1 3`

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

**What are the logged values of a and b ?**

```JS
b = function a(){};
var a = b = 6;
a = function b(){};
function b() {};
function a() {};
console.log(a,b);
```

- A: `ƒ b(){} 6`
- B: `ƒ a(){} 6`
- C: `ƒ b(){} ƒ a(){}`
- D: `ƒ a(){} ƒ b(){}`
- E: `6 ƒ a(){}`
- F: `6 ƒ b(){}`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>

</li>  
</ol>
