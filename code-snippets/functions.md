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

</ol>
