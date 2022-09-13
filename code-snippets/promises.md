<div align="center">
<h1>Promises</h1>
</div>

<ol>
<li>

**Promise is introduced in which version of JavaScript?**

- A: `ES5`
- B: `ES6`
- C: `ES8`
- D: `ES8`

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

**When do we say that a promise is 'settled'?**

- A: `If it is fulfilled`
- B: `If it is rejected`
- C: `If it is pending`
- D: `If it is either fulfilled or rejected`

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
const validateUsernamePassword = (username, password) => {
	return new Promise((resolve, reject) => {
		if (username == "ABC" && password == "123") {
			resolve("SUCCESS!");
		} else {
			reject("FAILURE!");
		}
	});
};

validateUsernamePassword("ABC", "123")
	.then((msg) => {
		console.log(msg);
	})
	.catch((err) => {
		console.log(err);
	});
```

- A: `SUCCESS!`
- B: `FAILURE!`

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

**What will be the output?**

```JS
let setTimeoutResolveReject = new Promise((resolve, reject) => {
	setTimeout(() => {
		resolve("YES");
	}, 3000);
	setTimeout(() => {
		reject("NO")
	}, 2000);
});

setTimeoutResolveReject
.then((msg) => {
	console.log(msg);
})
.catch((err) => {
	console.log(err);
})
```

- A: `YES`
- B: `NO`
- C: `NO\nYES`
- D: `YES\nNO`

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

**While execution, the random value of `randomWaitTime` generated was `3800`. What will be the output?**

```JS
let examplePromise = new Promise((resolve, reject) => {
	let timeout = 3000;
	let randomWaitTime = Math.floor(Math.random() * 5000) + 1;
	console.log(randomWaitTime);
	if (randomWaitTime <= timeout) {
		setTimeout(() => {
			resolve();
		}, randomWaitTime);
	} else {
		setTimeout(() => {
			reject();
		}, randomWaitTime);
	}
});

examplePromise
	.then(() => {
		console.log("RESOLVED!");
	})
	.catch(() => {
		console.log("REJECTED!");
	});
```

- A: `RESOLVED!`
- B: `REJECTED!`

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

**Which of the following isn’t a method of Javascript Promise?**

- A: `Promise.then()`
- B: `Promise.all()`
- C: `Promise.error()`
- D: `Promise.catch()`

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

**Which of the following isn’t a state of Javascript Promise?**

- A: `fulfilled`
- B: `awaited`
- C: `pending`
- D: `rejected`

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

**What is the output?**

```JS
new Promise((resolve, reject) => {
  console.log(4)
  resolve(5)
  console.log(6)
}).then(() => console.log(7))
.catch(() => console.log(8))
.then(() => console.log(9))
.catch(() => console.log(10))
.then(() => console.log(11))
.then(console.log)
.finally(() => console.log(12))
```

- A: `4 6 7 9 11 12`
- B: `4 6 7 9 11 undefined 12`
- C: `4 6 8 12`

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

**What's the output of the following Promise Operation?**

```JS
const promise_1 = Promise.resolve('First');
const promise_2 = Promise.resolve('Second');
const promise_3 = Promise.reject('Third');
const promise_4 = Promise.resolve('Fourth');

const runPromises = async () => {
	const res1  = await Promise.all([promise_1, promise_2])
	const res2  = await Promise.all([promise_3, promise_4])
	return [res1, res2];
}

runPromises()
	.then(res => console.log(res))
	.catch(err => console.log(err))
```

- A: `[['First', 'Second'], ['Third']]`
- B: `[['First', 'Second'], ['Third', 'Fourth']]`
- C: `[['First', 'Second']]`
- D: `'Third'`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: D

> `Promise.all[...promises]` method wait for an array of promises to resolve. Promise.all() will reject immediately upon any of the input promises being rejected. In our case, During runPromises() function invocation, promise_3 gets rejected with the value 'Third'. The value gets logged to the console, via error handling Promise Instance Method `catch()`. As a result, 'Third' gets printed.

</p>
</details>
</li>

---

<li>

**What's the output of the following Promise operation?**

```JS
var p = new Promise((resolve, reject) => {
  reject(Error('The Fails!'))
})
p.catch(error => console.log(error.message))
p.catch(error => console.log(error.message))
```

- A: `print error message once`
- B: `print error message twice`
- C: `Unhandled Promise Rejection warning`
- D: `process exits`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

> The promise `p` gets rejected due to `reject` callback in Promise Constructor and the error message gets attached to the `.catch()` method. In this case, `.catch()` works like the DOM `.addEventListener('event', callback`) method. Both catch method will be called separately with the same arguments. Hence, the error message gets printed twice.

</p>
</details>
</li>

---

<li>

**What's the order of output of the following Promise operation?**

```JS
console.log('initial');
setTimeout(function() {
   console.log('setTimeout');
}, 0);
var promise = new Promise(function(resolve, reject) {
   resolve();
});
promise.then(function(resolve) {
   console.log('1st Promise');
})
.then(function(resolve) {
   console.log('2nd Promise');
});
console.log('final');
```

- A: `initial \n 1st Promise \n 2nd Promise \n setTimeout \n final`
- B: `initial \n final \n 1st Promise \n 2nd Promise \n setTimeout`
- C: `initial \n setTimeout \n 1st Promise \n 2nd Promise \n final`
- D: `initial \n final \n 1st Promise \n setTimeout \n 2nd Promise`

<br/>
<details>
<summary><b>Answer</b></summary>
<p>

#### Option: B

</li>

</ol>
