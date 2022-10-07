<div align="center">
<h1>Objects</h1>
</div>

 <ol>

<li>

**let a=3;**
**let b = new Number(3);**
**let c=3;**

**console.log(a == b);**
**console.log(a === b);**
**console.log(b === c);**

- A: `true false true`
- B: `false false true`
- C: `true false false`
- D: `false true true`

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

**What will be the output of the following code?**

```JS
const telegramGroup = {
   name: 'TeamDevkode'
}
const { name: TDK } = telegramGroup;

console.log(TDK);
```

- A: `null`
- B: `Error will be thrown`
- C: `TeamDevkode`
- D: `undefined`

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

**What will be the output?**

```JS
let myName = 'Sunny';
let groupName = myName;

myName = 'DevKode';
console.log(groupName);


const obj1 = {
    id:1,
    name:"Sunny",
}

const obj2 = obj1;
obj2.name = 'DevKode';
console.log(obj1);
```

- A: `Sunny , { id: 1, name: 'Sunny' }`
- B: `DevKode,{ id: 1, name: 'Sunny' }`
- C: `DevKode,{ id: 1, name: 'DevKode' }`
- D: `Sunny,{ id: 1, name: 'DevKode' }`

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

```JS
 function greet(person) {
  if (person == { name: 'Narendra Modi' }) {
    return 'hey Narendra Modi'
  } else {
    return 'hey Donald Trump'
  }
}

console.log(greet({ name: 'Narendra Modi' }))
```

- A: `hey Narendra Modi`
- B: `hey Donald Trump`

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
const sample = ["xyz", "abc", "test", "ryan", "apple"];
delete sample[3];
console.log(sample.length);
```

- A: `4`
- B: `5`
- C: `Error updating the constant variable.`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</p>
</details>
</li>

</ol>

---

<li>

**What will be the output?**

```JS
const fruits_obj = { 0 : "apple" , 1 : "mango" ,  2:"banana"};
const fruits_arr = ["apple","mango", "banana"];

console.log(typeof fruits_obj);
console.log(typeof fruits_arr);
console.log(fruits_obj == fruits_arr);
``` 

- A: `Object , Array , False`
- B: `Object , Array , True`
- C: `Object , Object , False`
- D: `Object , Object , True`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>
</li>

</ol>
