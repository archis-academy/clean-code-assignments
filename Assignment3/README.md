# clean-code-assignments

3.Avoid global variables: Use local variables whenever possible, and avoid polluting the global namespace with unnecessary variables. For example:

```
// Bad

let user = {

  name: "John",

  age: 30

};

function updateUser() {

  user.age++;

}

// Good

function updateUser(user) {

  user.age++;

}

let user = {

  name: "John",

  age: 30

};

updateUser(user);

```

Question : Write a JavaScript program to display the reading status (i.e. display book name, author name and reading status) of the following books.

```
const library = [
   {
       author: 'Bill Gates',
       title: 'The Road Ahead',
       readingStatus: true
   },
   {
       author: 'Steve Jobs',
       title: 'Walter Isaacson',
       readingStatus: true
   },
   {
       author: 'Suzanne Collins',
       title:  'Mockingjay: The Final Book of The Hunger Games',
       readingStatus: false
   }];

```
