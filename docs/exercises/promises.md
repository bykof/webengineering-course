# Promises Exercises

## 1 Intro

```javascript
const wait = (callback) => {
  setTimeout(callback, 2000);
};
```

1. Call the function `wait` with a callback that calls an `alert('Hello World')`.
2. `Promisify` the function `wait`.

## 2 Async/Await

```javascript
const divide = (a, b) => {};

divide(8, 2).then((result) => {
  if (result !== 4) {
    alert("Wrong!");
  } else {
    alert("Correct");
  }
});

divide(8, 0)
  .then((result) => {
    alert("Wrong!");
  })
  .catch((error) => {
    alert("Correct!");
  });
```

1. Solve divide function
2. Make divide function async
3. Resolve the divide calls with await

## 3 Chaining

```js
class Response {
  constructor() {
    this.data = "[1, 2, 3]";
  }

  async json() {
    return JSON.parse(this.data);
  }

  async text() {
    return this.data;
  }
}

const fetch = () => {
  return new Promise((resolve, reject) => {
    return resolve(new Response());
  });
};

```

1. Resolve fetch with .then

2. Resolve the .json() function of Response by using Promise chaining

3. Rewrite everything with async/await
