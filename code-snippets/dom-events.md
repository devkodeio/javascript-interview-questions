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

---

<li>
  
**What will be the output ?**

```HTML
<p onclick="console.log('One')">
  <div onclick="console.log('Two')">
    <h1 onclick="console.log('Three')">
      Click Me
    </h1>
  </div>
</p>
```

- A: `One`
- B: `Three`
- C: `One Two Three`
- D: `Three Two`
- E: `Three Two one`

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
  
**What will be the output ?**

```HTML
<div onclick="console.log('One')">
  <div onclick="event.stopPropagation();console.log('Two');">
    <div onclick="console.log('Three')">
      Click Me
    </div>
  </div>
</div>
```

- A: `One`
- B: `Three`
- C: `One Two Three`
- D: `Three Two`
- E: `Three Two one`

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
  
**What will be the output ?**

```HTML
<div onclick="console.log('One')">
  <div onclick="return false;console.log('Two');">
    <div onclick="console.log('Three')">
      Click Me
    </div>
  </div>
</div>
```

- A: `One`
- B: `Three`
- C: `One Two Three`
- D: `Three Two`
- E: `Three Two one`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: None of the above

</p>
</details>

</li>

---

<li>
  
**What will be the output ?**

```HTML
<div>
  <div class="number-box">1</div>
  <div class="number-box">2</div>
  <div class="number-box">3</div>
  <div class="number-box">4</div>
</div>
  <script>
  const arr = document.querySelectorAll('.number-box');
  console.log(arr);
</script>
```

- A: `array of length 4`
- B: `undefined`
- C: `NodeList of length 4`
- D: `empty array`
- E: `empty NodeList`

<br/>

<details>
<summary><b>Answer</b></summary>
<p>

#### Option: C

</p>
</details>

</li>
</ol>
