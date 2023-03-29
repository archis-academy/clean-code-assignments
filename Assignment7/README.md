# clean-code-assignments

7.Use comments to explain complex code or your thought process:

```
// Bad

function processData(data) {

  // process the data

}

// Good

function processData(data) {

  // Convert data to JSON object and parse it

  const jsonData = JSON.parse(data);

  // Loop through each item in the JSON object and process it

  for (let item of jsonData) {

    // Process each item

  }

}
```

Question : JavaScript Program to Add Digits of a Number

```
Example:

Input : 123
Output :6
```
