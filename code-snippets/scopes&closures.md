<div align="center">
  <h1>Scopes & Closures</h1>
</div>

<ol>
<li>

**Which variables end up being part of `func's` closure ?**

```JS
var c = 10;

function foo(a){
    let b = 8;
    const d = 10;
    return function bar(){
        return a + d + c;
    }
}

const func = foo(7);
```

-   A: `a and d`
-   B: `a,b and d`
-   C: `a,b,c and d`
-   D: `a,d and c`

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
const fn = () => {
  a = 2;
  console.log(a);
}

fn();


```

-   A: `undefined`
-   B: `2`
-   C: `Uncaught ReferenceError: a is not defined`

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
for (var i = 0; i < 4; i++) {
  setTimeout(() => console.log(i), 0)
}

```

-   A: `0 1 2 3`
-   B: `4 4 4 4`

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

```JavaScript
for(let i = 0; i < 5; i++){
    setTimeout(() => console.log(i), 1);
}
```

-   A: `0 0 0 0 0`
-   B: `1 2 3 4 5`
-   C: `5 5 5 5 5`
-   D: `0 1 2 3 4`

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

**What will be the output?**

```JavaScript
let count = 0;
(function immediate() {
  if (count === 0) {
    let count = 1;
    console.log(count);
  }
  console.log(count);
})();
```

-   A: `0 0`
-   B: `1 1`
-   C: `1 0`
-   D: `0 1`

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

**what would be the typeof a and typeof b**

````function foo() {
  let a = b = 0;
  a++;
  return a;
}
foo();
console.log(typeof a)
console.log(typeof b)
````
  
-   A: `Number Number`
-   B: `Number undefined`
-   C: `undefined Number`
-   D: `not define not define`

<br/>
  
  <details>
<summary><b>Answer</b></summary>

<p>

#### Option: C

</p>

</details>

</li>
</ol>
