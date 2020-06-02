@snap[north]
## An Introduction to Functions
#### From Code Immersives
@snapend

@snap[south]
![](https://www.codeimmersives.com/wp-content/uploads/2019/09/cropped-CodeImmersives_Logo_RGB_NYC_BW-3.png)
@snapend

---
@snap[north]
![](https://3.bp.blogspot.com/-42oCVxzA_qI/T1GmphVyvxI/AAAAAAAAQJw/pS1nJXrbXXc/s400/Assembly_Line.jpg)
@snapend

@snap[midpoint]
## Functions
@snapend

@snap[south span-100 text-08]
Every part of your code should have one job! That makes it easy to separate your code, so you can:

@ul
* Run the same code whenever you need to without repeating yourself.
* Easily see what a bit of code is supposed to do.
* Figure out why it's not, in fact, doing that.
@ulend
@snap[south-east]
![](./assets/img/CodeImmersives.jpg)
@snapend
---

## What does a function look like?

##### Something like this:
@snap[code-noblend]
```javascript
function incrementX() {
  x = x + 1;
}
```
@snapend
---

### What are all those parts, though?

@snap[code-noblend]
```javascript
function incrementX() {
  x = x + 1;
}
```
@snapend

@snap[text-08]
@ul
* `function` declares the function - like `let` for variables.
* `incrementX` is the name of the function.
* Everything in the curly braces is the code that runs when the function is "called".
@ulend
@snapend
---

### Let's see it in action!

@snap[code-noblend]
```javascript
let x = 3;

function incrementX() {
  x = x + 1;
}
```
@snapend

POP QUIZ HOTSHOT: What is `x` now?

@ul
* TRICK QUESTION. The keyword `function` defines the function, but doesn't in any way run its code.
* Like how declaring the variable and giving it a value doesn't actually EVALUATE its value.
@ulend

---

### We "call" a function by saying its name _with parentheses_.

@snap[code-noblend]
```javascript
let x = 3;

function incrementX() {
  x = x + 1;
}

incrementX();
```
@snapend

What is `x` *now*?

---

### Calling it multiple times?

@snap[code-noblend]
```javascript
let x = 3;

function incrementX() {
  x = x + 1;
}

incrementX();
incrementX();
incrementX();
```
@snapend

What is `x` after all those function calls?

---

## Scope

#### What happens in functions stays in functions.

@ul
* Inside a function, you can look at the code "outside".
* But to code outside, the code *inside* is an impenetrable black box.
@ulend

---

### So code in `incrementX` can see `x`.
It's looking outside.

@snap[code-noblend]
```javascript
let x = 3;

function incrementX() {
  x = x + 1;
}

incrementX();
incrementX();
incrementX();
```
@snapend

---

### But code outside can't see anything in.

@snap[code-noblend]
```javascript
let x = 3;

function incrementX() {
  x = x + 1;
  let y = 3;
}

incrementX();

y = y + 1;
```
@snapend

**ERROR!**

---

## Global Variables

For a short time, we'll solve this problem by declaring any variables we want to change *globally*--that is, *outside* the function.

Variables *inside* will be for internal use only.

Our next tool, parameters, will be a much cleaner solution!

---
@snap[north span-100]
## Our new weapon:

@snapend
We now have functions!
@snap[span-80 south]
![](https://camo.githubusercontent.com/2d8b6d9f60ed366cf5e9dc3ea23378a2c6a7548e/68747470733a2f2f7468756d62732e6766796361742e636f6d2f466169746866756c4c617766756c4b7573696d616e73652d6d61782d316d622e676966)
@snapend
