<div align="center">
  <h1>DOM Events</h1>
</div>

<ol>
<li>

**What will be the output ?**

```HTML
<button onclick="console.log('One')" onclick="console.log('Two')">
  Click Me
</button>
```

- A: `One`
- B: `Two`
- C: `One Two`
- D: `Two One`

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

```HTML
<button id="button" onclick="console.log('One')">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.onclick = function() {
    console.log('Two');
  }
</script>
```

- A: `One`
- B: `Two`
- C: `One Two`
- D: `Two One`

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

```HTML
<button id="button" onclick="console.log('One')">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.addEventListener('click', function() {
    console.log('Two');
  });
</script>
```

- A: `One`
- B: `Two`
- C: `One Two`
- D: `Two One`

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

```HTML
<button id="button" onclick="console.log('One')">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.addEventListener('click', function() {
    console.log('Two');
  });

  button.onclick = function() {
    console.log('Three');
  }
</script>
```

- A: `One Two`
- B: `Two Three`
- C: `Three Two`
- D: `One Two Three`

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

```HTML
<button id="button">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.addEventListener('click', function() {
    console.log('One');
  });

  button.onclick = function() {
    console.log('Two');
  }
</script>
```

- A: `One`
- B: `Two`
- C: `One Two`
- D: `Two One`

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

```HTML
<button id="button">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.addEventListener('click', function() {
    console.log('One');
  });
  
  button.onclick = function() {
    console.log('Two');
  }
  
  button.setAttribute('onclick', "console.log('Three')");
</script>
```

- A: `One Two Three`
- B: `One Two`
- C: `One Three`
- D: `Three Two One`

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

```HTML
<button id="button" onclick="console.log('One')">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.addEventListener('click', function() {
    console.log('Two');
  });
  
  button.addEventListener('click', function() {
    console.log('Three');
  }, false);
</script>
```

- A: `One Two`
- B: `One Three`
- C: `One Two Three`
- D: `Three One Two`

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

```HTML
<button id="button" onclick="console.log('One')">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  function clickHandler() {
  	console.log('Two');
  }
  
  button.addEventListener('click', clickHandler);
  
  button.addEventListener('click', clickHandler, false);
</script>
```

- A: `One Two`
- B: `One Three`
- C: `One Two Three`
- D: `Three One Two`

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

```HTML
<button id="button" style="display: none;">
  Click Me
</button>

<script>
  const button = document.getElementById('button');
  
  button.onclick = function() {
    console.log('One');
  }
  
  button.addEventListener('click', function() {
    console.log('Two');
  });
  
  setTimeout(function(){
    button.click();
  }, 1000);
</script>
```

- A: `One Two`
- B: `One Three`
- C: `One Two Three`
- D: `Three One Two`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: A

</p>
</details>

</li>
</ol>
