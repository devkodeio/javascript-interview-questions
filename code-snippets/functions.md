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

**What is the output ?**

```JS
const animal = {
  animal_name: "cat",
  action: function () {
    console.log(`${this.animal_name} is doing action`);
  }
};

setTimeout(animal.action, 1000);

```

- A: `cat is doing action`
- B: `undefined is doing action`
- C: `null is doing action`
- D: `error`

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

**What is the output ?**

```JS
const animal = {
  animal_name: "cat",
  action: function () {
    console.log(`${this.animal_name} is doing action`);
  }
};

setTimeout(function () {
  animal.action();
}, 1000);

```

- A: `cat is doing action`
- B: `undefined is doing action`
- C: `null is doing action`
- D: `error`

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

**What is the output ?**

```JS
const animal = {
  animal_name: "cat",
  action: function () {
    console.log(`${this.animal_name} is doing action`);
  }
};

let func = animal.action.bind(animal);
setTimeout(func, 1000);

```

- A: `null is doing action`
- B: `undefined is doing action`
- C: `cat is doing action`
- D: `error`

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

**What is the output ?**

```JS
function getFunc() {
  let value = "Hey !";

  let func = new Function("console.log(value)");

  return func;
}

getFunc()();

```

- A: `Hey !`
- B: `error: value is not defined`
- C: `null`

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

**What is the output ?**

```JS
function getFunc() {
  let value = "Hello Friends !";
  let func = () => {
    alert(value);
  };
  return func;
}

getFunc()();

```

- A: `Hey !`
- B: `error: value is not defined`
- C: `Hello Friends !`
- D: `null`

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
function getAge() {
  'use strict';
  age = 21;
  console.log(age);
}

getAge();
```

- A: `21`
- B: `undefined`
- C: `ReferenceError`
- D: `TypeError`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

With "use strict", you can make sure that you don't accidentally declare global variables. We never declared the variable age, and since we use "use strict", it will throw a reference error. If we didn't use "use strict", it would have worked, since the property age would have gotten added to the global object.

</p>
</details>

</li>

---

<li>

**What will be the output ?**

```JS
const obj = { 1: 'a', 2: 'b', 3: 'c' };
const set = new Set([1, 2, 3, 4, 5]);

obj.hasOwnProperty('1');
obj.hasOwnProperty(1);
set.has('1');
set.has(1);
```

- A: `false true false true`
- B: `false true true true`
- C: `true true false true`
- D: `true true true true`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

All object keys (excluding Symbols) are strings under the hood, even if you don't type it yourself as a string. This is why `obj.hasOwnProperty('1')` also returns true.

It doesn't work that way for a set. There is no '1' in our set: `set.has('1')` returns `false`. It has the numeric type 1, set.has(1) returns true.

</p>
</details>

</li>

---

</ol>
