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

- A: `a and d`
- B: `a,b and d`
- C: `a,b,c and d`
- D: `a,d and c`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>

</li>
</ol>

