# Ada College JavaScript Coding Style

## Naming

### Variable names
- Variables should use camelCase naming, and start with a lower-case letter.
- Boolean variables should sound like a question.

```js
// no:
var Name = 'Alex';
var user_age = 16;
var userTired = true;

// yes:
var name = 'Alex';
var userAge = 16;
var isUserTired = true;
```

### Function names
- Functions should follow the same convention as variables.
- If possible, a function name should contain a verb: what does the function _do_?
- If possible, a function name should contain a noun: what does the function _concern_?

```js
// no:
function user() {
  return { name: 'sally' };
}

function add(a, b) {
  return a + b;
}

// yes:
function createUser() {
  return { name: 'sally' };
}

function addNumbers(a, b) {
  return a + b;
}
```

### Class names
- Classes should use CamelCase and start with an upper-case letter.
- Class names should be nouns.

## Functions
- Write code by breaking a problem down into several small functions/methods
- 10 lines is a long method. Aim for 5.

```js
// no
function updateGame() {
  if (downPressed) {
    playerPosition.y += 10;
  } else if (upPressed) {
    playerPosition.y -= 10;
  }

  for (var i = 0; i < bullets.length; i++) {
    bullets[i].y += 20;
  }

  for (var i = 0; i < bullets.length; i++) {
    if (playerPosition.y === bullets[i].y) {
      alert('you lose!');
    }
  }
}

// yes
function updateGame() {
  movePlayer();
  moveBullets();
  checkBulletsHitPlayer();
}

function movePlayer() {
  if (downPressed) {
    playerPosition += 10;
  } else if (upPressed) {
    playerPosition -= 10;
  }
}

function moveBullets() {
  for (var i = 0; i < bullets.length; i++) {
    moveBullet(bullets[i]);
  }
}

function moveBullet(bullet) {
  bullet.y += 20;
}

function checkBulletsHitPlayer() {
  for (var i = 0; i < bullets.length; i++) {
    checkBulletHitPlayer(bullets[i]);
  }
}

function checkBulletHitPlayer(bullet) {
  if (hitTest(bullet, playerPosition)) {
    alert('you lose!');
  }
}

function hitTest(objA, objB) {
  return objA.y === objB.y;
}
```

## Whitespace
### Indentation & newlines
- Indent with two spaces
- Add a newline after each `{`
- Each `{` should be on the same line as its statement
- Each `}` should be on its own line, or be followed by an `else`
- Indent / detent after each `{` / `}`
- Indent / dedent after each `[` / `]` when writing arrays over multiple lines
- Do not use `if`/`for` etc. without `{ }`

```js
// no:
if (something) {
doThing();
}

if (something) {doThing()}

if (something) doThing();

if (something)
  doThing();

if (something)
{
  doThing();
}

if (something) {
  doThing();
}
else {
  doOtherThing();
}

if (something) {
  doThing();
    doOtherThing();
}

// yes:
if (something) {
  doThing();
}

if (something) {
  doThing();
} else {
  doOtherThing();
}

if (something) {
  doThing();
  doOtherThing();
}
```

### Spaces
- include spaces around binary operators
- include spaces after commas
- no space after the function name when calling a function
- include a space after keywords like `if` and `for`
- include a space before `{`

```js
// no:
a+b
addNumbers (a,b);
if(something){
}

// yes:
a + b
addNumbers(a, b);
if (something) {
}
```
