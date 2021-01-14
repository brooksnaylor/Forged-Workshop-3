# Forged-Workshop-3

### Basic Requirements

#### While Loops (5 points each)

1. **Summation to `n`:** Let's implement the function `sum` that takes a single
   parameter `n`, and computes the sum of all integers up to `n` starting from
   `0`, *e.g.*:

   ```js
   function sum(n) {
     // TODO: your code here
   }
   sum(3); // => 6
   sum(4); // => 10
   sum(5); // => 15
   ```

2. **Factorial of `n`:** The factorial of `n` is the *product* of all the
   integers preceding `n`, starting with `1`, *e.g.*:

   ```js
   function factorial(n) {
     // TODO: your code here
   }
   factorial(3); // => 6
   factorial(4); // => 24
   factorial(5); // => 120
   ```

3. **Repeating a String `n` Times:** Let's write a function called
   `repeatString` that takes two parameters: a string `str`, which is the string
   to be repeated, and `count` -- a number representing how many times the
   string `s` should be repeated, *e.g.*

   ```js
   function repeatString(str, count) {
     // TODO: your code here
   }
   repeatString('dog', 0); // => ''
   repeatString('dog', 1); // => 'dog'
   repeatString('dog', 2); // => 'dogdog'
   repeatString('dog', 3); // => 'dogdogdog'
   ```

   Your task is to implement the `repeatString` function using a `while` loop.

### More Practice (10 points each)

1. Modify your `sum` function from the **Basic Requirements** section to accept
   *two* parameters, `start` and `end`: `sum` should now compute the sum of the
   numbers from `start` to `end`, *e.g.*

   ```js
   function sum(start, end) {
     // TODO: your code here
   }
   sum(2, 7); // => 2 + 3 + 4 + 5 + 6 + 7 => 27
   sum(3, 5); // => 3 + 4 + 5 => 12
   ```

   + What happens if `start` is larger than `end`? Modify `sum` to check for this
     case and, when found, swap the `start` and `end` arguments.


2. Let's pretend for a moment that JavaScript does not have the addition
   operator `+` -- instead, it comes with two functions called `inc` and `dec`
   that perform *increment* and *decrement* respectively:

   ```js
   // ignore the fact that inc makes use of +
   function inc(x) {
     return x + 1;
   }

   function dec(x) {
     return x - 1;
   }
   ```

   Your task is to write a function called `add` that takes two numbers as
   parameters, `x` and `y`, and adds them together. The catch is that you can
   *only* use `inc` and `dec` to accomplish this.

3. Write a function called `isEven` that, given a number `n` as a parameter,
   returns `true` if that number is *even*, and `false` otherwise; however, you
   need to do this **without using the `%` operator.**

4. Write a function called `multiply` that accepts two numbers as parameters,
   and multiplies them together -- but without using the `*` operator; instead,
   you'll need to use repeated addition.

### Advanced (15 points each)

1. **Compute the `n`th Fibonacci Number:** The fibonacci numbers are represented by the
   following sequence:

   ```js
   // fib(n): 1 1 2 3 5 8 13 21
   //         | | | | | |  |  |
   //      n: 0 1 2 3 4 5  6  7
   ```

   That is, `fib(0)` is 1, `fib(1)` is 1, `fib(2)` is 2, `fib(3)` is 3, `fib(4)`
   is 5, etc.

   Notice that each fibonacci number can be computed by adding the **previous
   two** fibonacci numbers, with the exception of the first two: `fib(0)` and
   `fib(1)`. More succinctly,

   + `fib(0)` is `1`
   + `fib(1)` is `1`
   + `fib(n)` is `fib(n - 1) + fib(n - 2)`

    Write a function called `fib` that accepts a number `n` as a parameter and
   computes the `n`th fibonacci number using the above rules.

2. By now you should have worked with the `length` property of strings, *e.g.*
   `"hello".length`. Your task is to write a function called `stringLength` that
   accepts a string as a parameter and computes the length of that string;
   however, as you may have guessed, you are not allowed to use the `length`
   property of the string!

   Instead, you'll need to make use of the string method called `slice`. To
   get an idea of how `slice` works, try the following at a console:

   ```js
   "hello".slice(0);
   "hello".slice(1);
   "".slice(1);
   ```

   For our purposes, we can consider `slice` as taking one argument -- the
   **index** to begin slicing from, and returns a new string starting from that
   index onwards.

   **Indices** are *positions* of characters within strings, and they always
   begin counting from 0, *e.g.*:

   ```js
   // "h e l l o" (spaces added for clarity)
   //  | | | | |
   //  0 1 2 3 4
   ```

   The `"h"` character has index (position) `0` in the string `"hello"`, `"e"`
   has index `1`, `l` has index `2`, etc.

3. The "modulo" operator (`%`) computes the *remainder* after dividing its left
   operand by its right one, *e.g.*

   ```js
   5 % 2; // => 1
   8 % 10; // => 8
   7 % 5; // => 2
   ```

   Write a function called `modulo` that works like the `%` operator, but
   without using it.

4. Write a function called `countChars` that accepts two parameters: a `string`
   and a `character`. This function should return a number representing the
   number of times that the `character` appears in `string`. To access the
   *first* element of a string, you can use the following syntax:

   ```js
   // access the element at index 0
   "hello"[0]; // => "h"
   "dog"[0]; // => "d"
   ```

   **HINT:** You'll also need to make use of the `slice` method as shown above
   in the exercise on computing the length of a string.

5. Implement a function called `indexOf` that accepts two paramters: a `string`
   and a `character`, and returns the *first* index of `character` in the
   `string`. You'll need to make use of the techniques for accessing the *first*
   element of a string and the *rest* of the string (`slice`) as before.

#### Creating Arrays (5 points each)

1. Using the array: `["cat", "fox", "dog", "monkey"]`, what is the index of:

   + "dog"?
   + "monkey"?
   + "cat"?


2. Fix the syntax/style in the following arrays:

  ```js
  [ 1, 3 4 7,9, ]
  "the""quick""brown","fox" "jumped","over" the lazy, "dog",  ]
  [true false,true
  ```

3. Create arrays in the *global scope* of your program consisting of strings that represent:

   + Your favorite TV shows/movies
   + Names of people you know/care about
   + Favorite sports/activities

#### Accessing Array Elements (5 points each)

1. Using the arrays that you created in the last exercise, use the console to access:

    + First elements,
    + Last elements,
    + Other elements!

2. Write a function `first` that takes an array as an argument and returns the
   first element in that array.

3. Write a function `last` that takes an array as an argument and returns the
   *last* element in the array. **Hint:** What is the relationship between the
   *index* of the last element in the array and the *length* of the array?

#### Modifying Arrays (5 points each)

1. Using `push` and `unshift`, make this array contain the
   numbers from zero through seven:

   ```js
   var arr = [2, 3, 4];
   // your code here
   arr; // => [0, 1, 2, 3, 4, 5, 6, 7]
   ```

2. What is *returned* by `push`? Before throwing this into the console, form a
   hypothesis about what you think the return value will be:

   ```js
   var arr = [5, 7, 9];
   arr.push(6); // => ???
   ```

   Were you correct? What is the returned by `push`? Does `unshift` work in the
   same way?

3. We can use the *assignment operator* (`=`) to replace elements in arrays with
   other ones like so:

   ```js
   var animals = ['dog', 'elephant', 'zebra']
   // let's replace 'dog' with 'hippo'
   animals[0] = 'hippo';
   animals; // => ['hippo', 'elephant', 'zebra']
   ```

   Using the same principle, perform the following:

   ```js
   // 1. Change all odd numbers to be those numbers multiplied by two:
   var numbers = [4, 9, 7, 2, 1, 8];
   // TODO: your code here
   numbers; // => [4, 18, 14, 2, 2, 8]

   // 2. Fix the typos by replacing each element with a correctly spelled version
   var places = ['snfranisco', 'oacklannd', 'santacrus']
   // TODO: your code here
   places; // => ['san francisco', 'oakland', 'santa cruz']
   ```

### More Practice (10 points each)

1. Write a function called `nth` that accepts an array and an index as
   parameters, and returns the element at that index.

   ```js
   function nth(array, index) {
     // TODO: your code here
   }
   var animals = ['dog', 'cat', 'gerbil'];
   nth(animals, 2); // => 'gerbil'
   nth(animals, 1) === animals[1]; // => true
   ```

2. Write a function `rest` that returns all the elements in the array *except*
   for the first one. **HINT:** Read about the `slice` method on
   [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
   and/or experiment with `slice` at the console like so:

   ```js
   var numbers = [3, 2, 7, 5];
   numbers.slice(0);
   numbers.slice(1);
   numbers.slice(2);
   numbers.slice(0, 2);
   ```

3. Write a function `butlast` that returns all of the elements in the array
   *except* for the last one (you may want to use `slice` for this one as well).

4. Complete the function `cons` that accepts an element and an array, and
   returns an array with the element added to the *front* of the array:

   ```js
   function cons(x, array) {
     // your code here
   }
   ```

5. Complete the function `conj` that accepts an array and an element, and
   returns an array with the element added to the *end* of the array:

   ```js
   function conj(array, x) {
     // your code here
   }
   ```

6. What benefit(s) might there be to using functions like `cons` or `conj` over
   `unshift` or `push`?

7. Try the following in a console:

   ```js
   var arr = [];
   arr[7] = "Hello."
   arr; // => ???
   ```

   What is the value of `arr` after assigning an element to its seventh index?
   Explain the result in plain English.

### Advanced (15 points each)

1. Without running the below function, use a whiteboard to figure out what it
   should return by repeatedly expanding function invocations:

   ```js
   function mystery(array) {
     if (array.length === 0) {
       return [];
     }
     return conj(mystery(rest(array)), first(array));
   }
   ```

2. Using `first`, `rest`, `conj` and/or `cons`, write functions that accomplish
   the following:

   + `sum` all the elements of an array
   + Given an array, returns a new array with each element *squared*
   + Given an array of numbers, returns a new array of just the *even* numbers

  **HINT:** After figuring out how the `mystery` function works above, use it
   as a reference for how to write this type of function.
   

#### Array Iteration (5 points each)

1. Write a function `sum` that computes the sum of the numbers in an array.

2. Write a function `max` that accepts an array of numbers and returns the
   *largest* number in the array.

3. Try the following at a console:

  ```js
  "the quick brown fox jumped over the lazy dog".split(" ");
  "Hello, world!".split("")
  "1,2,3,4,5,6".split(",")
  ```

  What is returned by `split` (You can read more about it
  [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)),
  and how does it work?

  Use `split` to write a function `longestWord` that takes a string as an
  argument and returns the longest word.

4. Write a function `remove` that accepts an *array* and an *element*, and
   returns an array with all ocurrences of *element* removed.

   ```js
   function remove(array, element) {
     // your code here
   }
   remove([1, 3, 6, 2, 3], 3); // => [1, 6, 2]
   ```

5. Write a function `evens` that accepts an array as an argument, and returns
   an array consisting of all of the *even* numbers in that array.

### More Practice (10 points each)

1. Write a function called `average` that takes an array of numbers as a
   parameter and returns the *average* of those numbers.

2. Write a function called `min` that finds the *smallest* number in an array of
   numbers.

3. Write a function `shortestWord` that works like `longestWord`, but returns
   the *shortest* word instead.

4. Write a function `countChar` that takes two arguments: any string, and a
   *character* (string of one letter), and returns the number of times that the
   character occurs in the string.

5. Write a function `evenLengthWords` that takes an array of *strings* as an
   argument, and returns an array of just the words that have an even length.

### Advanced (15 points each)

1. Read about the `join` method on
   [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
   and use it to implement a function that accepts a string as an argument and
   returns that string *reversed*.

2. Write a function `keep` that "keeps" certain elements in an array. The
   function will need to take *two* arguments, an array, and something else --
   the second argument will be what is used to determine which elements to keep.

   You should be able to use this function to write `evens`, `evenLengthWords`,
   a hypothetical `odds` function, or `oddLengthWords` *without changing the
   `keep` function*.