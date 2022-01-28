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

**What will be the output ?**

```JS
function animal(){
  console.log("Cat");
}

var otherAnimal;

animal();
otherAnimal();

otherAnimal = function() {
  console.log("Dog");
}
```

- A: `Cat Dog`
- B: `Cat undefined`
- C: `Cat TypeError: otherAnimal is not a function`
  
---

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
  
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
 <li>

**What are the logged values of a and b ?**

```JS
var a = 10;
console.log("line number 2", a);

function fn() {
  console.log("line number 4", a);
  var a = 20;
  a++;
  console.log("line number 7", a);
  if (a) {
    var a = 30;
    a++;
    console.log("line number 11", a);
  }
  console.log("line number 13", a);
}
fn();
console.log("line number 2", a);
```

- A:
```HTML
line number 2 10
line number 4 10
line number 7 21
line number 7 31
line number 13 31
line number 2 31
```
- B:
```HTML

line number 2 10
line number 4 undefined
line number 7 21
line number 11 31
line number 13 31
line number 2 10
```
- C:
```HTML
line number 2 10
line number 4 10
line number 7 21
line number 11 31
line number 13 31
line number 2 10
```

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>

</li>
</li>  

---

<li>

**What will be the output?**

```JS
function foo() {
  let a = b = 0;
  a++;
  return a;
}

foo();
console.log(typeof a);
console.log(typeof b);
```

- A: `number \n number`
- B: `undefined \n number`
- C: `undefined \n undefined`
- D: `number \n undefined`

<br/>
<details>
<summary><b>Answer</b></summary>

<p>

#### Option: B

</p>

</details>
</li>
</ol>
