# JavascriptNinja
🐱‍👤JavascriptNinja - Our JavascriptVerse discoverys. from [StudyVerse](https://github.com/VictorPereiira/StudyVerse)


### ⚓ Summary

---

[Javascript Cheat Sheet | OverAPI.com](https://overapi.com/javascript)

[Use Maps more and Objects less](https://www.builder.io/blog/maps)

![Untitled](https://user-images.githubusercontent.com/64560823/219747879-36cc40cf-8fe6-4745-9ac3-dfc8829f5e9c.png)
![Untitled (1)](https://user-images.githubusercontent.com/64560823/219747909-e75ac74a-4b8e-4622-9a17-cd85d925e122.png)
![Untitled (2)](https://user-images.githubusercontent.com/64560823/219747933-0a84cc42-80ac-4b3f-b6c8-871dc21c33d3.png)


```jsx
Destructuring Assigment 

// #Basic variable assignment
	const list = [orage, apple],
				[firstElement, secondElement] = list

	// is equivalent to:
		const list = [orage, apple],
					firstElement = list[0],
					secondElement = list[1]

// #Assignment separate from declaration
	let a, b;
	[a, b] = [1, 2] // a=1 and b=2

// #Default values
	let a, b

	[a=5, b=7] = [1] // ignore a=5 ( a = 1 and b = 7 )

// #Swapping variables
	let a = 1, b = 3
	[a, b] = [b, a]

	const arr = [1,2,3]
	[arr[2], arr[1]] = [arr[1], arr[2]]

// #Array returned from a function
	function f() {
	  return [1, 2, 3]
	}

	let a, b;
	[a, b, c] = f() // a = 1, b = 2 and c = 3

	// Ignoring some returned values
	[a, , c] = f() // a = 1 and c = 3 
	[,,] = f() // ignore all returned values

// #Rest pattern unpack array
const [a, ...b] = [1, 2, 3] // a = 1 and b = [2, 3]
	

```

- Object destructuring
    - [ ]  Searching
    
- Math
    1. `Math.cbrt(x)` → Retorna a raiz cúbica de um número (\root{3}{x}).
    2. `Math.ceil(x)` → Retorna o menor inteiro que é maior ou igual a um número.
    3. `Math.floor(x)` → Retorna o maior inteiro que é menor ou igual a um número.
    4. `Math.max([x[,y[,…]]])` **→** Retorna o maior dentre os parâmetros recebidos.
    5. `Math.min([x[,y[,…]]])` **→** Retorna o menor dentre os parâmetros recebidos.
    6. `Math.pow(x,y)` **→** Retorna a base `x` elevada à potência `y` do expoente, ou seja, x^y.
    7. `Math.random()`**→** Retorna um número pseudo-aleatório entre 0 e 1.
    8. `Math.round(x)` **→** Retorna o valor arredondado de `x`, para o valor inteiro mais próximo.
    9. `Math.sign(x)` **→** Retorna o sinal de `x`, indicando se é positivo, negativo ou zero.****
    10. `Math.trunc(x)`**→** Retorna a parte inteira de `x`, removendo quaisquer dígitos fracionários.
    11. `Math.sqrt(x)`**→** Retorna a raiz quadrada positiva de um número (\sqrt x).
    
- Number
    1. **`[Number.MAX_VALUE](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE)` →** O maior número representável positivo.
    2. **`[Number.MIN_VALUE](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/MIN_VALUE)`** → O número mínimo representável positivo - isto é, o número positivo mais próximo de zero (sem ser zero na verdade).
    3. [https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString)
    4. [https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat)

- Highlights
    1. [Basics]
    2. [Variables]
    3. [Data strucuture and Types]
    4. [Converting strings to numbers]
    5. [Condicional Statements]
    6. [Loops and iteration]
    7. Functions
    
- Others
    1. [Destructuring]
    2. [Math and Number]

> Basics
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

- JavaScript is case-sensitive ******and ****Unicode

- Instructions are called statements
    
    → semicolons not necessay, but best pratice
    
    → ECMAScript automatic insertion semicolons
    
    → Some characters are considered whitespace
    
- Comments basics and [Hashbang comment](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#hashbang_comments)

> Variables
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

1. Declarations - keywords , object literal ( Destructuring Assigment ) and undeclared global
2. Identifiers and assign
3. Scope - local and global 
4. Evaluating variables - undefined, NaN and null

- Examples
    
    ```jsx
    // With keywords
    var planet = 'Saturn';
    let moon = 82;
    const inhabited = false;
    
    // With undeclared global
    x = 42
    ```
    
    ```jsx
    // Const + att
    const MY_OBJECT = {'key': 'value'};
    MY_OBJECT.key = 'otherValue';
    
    const MY_ARRAY = ['HTML','CSS'];
    MY_ARRAY.push('JAVASCRIPT');
    console.log(MY_ARRAY); //logs ['HTML','CSS','JAVASCRIPT'];
    ```
    

- Errors
    1. same name variable
    

> Data strucuture and Types
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

- String → Sequence of text wrapped in quotes.
- Number → Represents numbers.
- Boolean → True or False. ( 0 or 1 )
- Undefined → Value is not defined.
- Symbol → Instace are unique and immutable

> Converting strings to numbers
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

- parseInt()
- parseFloat()

```jsx
parseInt('101', 2) // 5
```

```jsx
'1.1' + '1.1' // '1.11.1'
(+'1.1') + (+'1.1') // 2.2
// Note: the parentheses are added for clarity, not required.
```

> Condicional Statements
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

### Representation

- if else if
- if and else
- switch

### Falsy values

- `false`
- `undefined`
- `null`
- `0`
- `NaN`
- the empty string (`""`)

All other values—including all objects—evaluate to `true` when passed to a conditional statement.

```jsx
// if and else
if (condition) {
	statement_1
} else {
	statement_2
}
```

```jsx
// if else if
if (condition_1) {
statement_1
} else if (condition_2) {
statement_2
} else {
	statement_3	
}
```

```jsx
// switch 
switch (expression) {
	case label_1:
		statements_1
		[break;]
	case label_2:
		statements_2
		[break;]
		…
	default:
		statements_def
		[break;]
}
```

> Loops and iteration
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

1. while 
    1. do while
    
2. for 
    1. for in ( objet )
    2. for of ( array )
    
3. labeled [  SEARCH  ]
    1. break
    2. continue

> Functions
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

- Basic definning
- Anonymous function
- Arrow function
- Functions parametres
- [Predefined functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions#predefined_functions)

- Scope
- Recursion

```jsx
// Recursion

var x = 0;
while (x < 10) { // "x < 10" is the loop condition
   // do stuff
   x++;
}

function loop(x) {
  if (x >= 10) // "x >= 10" is the exit condition (equivalent to "!(x < 10)")
    return;
  // do stuff
  loop(x + 1); // the recursive call
}
loop(0);
```

```jsx
// Basic definning 
function function_name(parameters) {
	return value
}
```

```jsx
// Anonymous functions
var fucntion_name = function (parameters) {
	return value
}
```

```jsx
// Arrow function
function Person() {
  this.age = 0;

  setInterval(() => {
    this.age++; // |this| properly refers to the person object
  }, 1000);
}

var p = new Person();
```

```jsx
// Recursion

var x = 0;
while (x < 10) { // "x < 10" is the loop condition
   // do stuff
   x++;
}

function loop(x) {
  if (x >= 10) // "x >= 10" is the exit condition (equivalent to "!(x < 10)")
    return;
  // do stuff
  loop(x + 1); // the recursive call
}
loop(0);
```

```jsx
// Recursion

var x = 0;
while (x < 10) { // "x < 10" is the loop condition
   // do stuff
   x++;
}

function loop(x) {
  if (x >= 10) // "x >= 10" is the exit condition (equivalent to "!(x < 10)")
    return;
  // do stuff
  loop(x + 1); // the recursive call
}
loop(0);
```

> Destructuring
> 

- Array Destructuring

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

```jsx
Destructuring Assigment 

// #Basic variable assignment
	const list = [orage, apple],
				[firstElement, secondElement] = list

	// is equivalent to:
		const list = [orage, apple],
					firstElement = list[0],
					secondElement = list[1]

// #Assignment separate from declaration
	let a, b;
	[a, b] = [1, 2] // a=1 and b=2

// #Default values
	let a, b

	[a=5, b=7] = [1] // ignore a=5 ( a = 1 and b = 7 )

// #Swapping variables
	let a = 1, b = 3
	[a, b] = [b, a]

	const arr = [1,2,3]
	[arr[2], arr[1]] = [arr[1], arr[2]]

// #Array returned from a function
	function f() {
	  return [1, 2, 3]
	}

	let a, b;
	[a, b, c] = f() // a = 1, b = 2 and c = 3

	// Ignoring some returned values
	[a, , c] = f() // a = 1 and c = 3 
	[,,] = f() // ignore all returned values

// #Rest pattern unpack array
const [a, ...b] = [1, 2, 3] // a = 1 and b = [2, 3]
	

```

- Object destructuring

> Math and Number
> 

[⚓](https://www.notion.so/Javascript-b90c8703c8e14e1bb87449da6ac80a9e)

<aside>
🔸 *This is a object*

</aside>

- Math
    1. `Math.cbrt(x)` → Retorna a raiz cúbica de um número (\root{3}{x}).
    2. `Math.ceil(x)` → Retorna o menor inteiro que é maior ou igual a um número.
    3. `Math.floor(x)` → Retorna o maior inteiro que é menor ou igual a um número.
    4. `Math.max([x[,y[,…]]])` **→** Retorna o maior dentre os parâmetros recebidos.
    5. `Math.min([x[,y[,…]]])` **→** Retorna o menor dentre os parâmetros recebidos.
    6. `Math.pow(x,y)` **→** Retorna a base `x` elevada à potência `y` do expoente, ou seja, x^y.
    7. `Math.random()`**→** Retorna um número pseudo-aleatório entre 0 e 1.
    8. `Math.round(x)` **→** Retorna o valor arredondado de `x`, para o valor inteiro mais próximo.
    9. `Math.sign(x)` **→** Retorna o sinal de `x`, indicando se é positivo, negativo ou zero.****
    10. `Math.trunc(x)`**→** Retorna a parte inteira de `x`, removendo quaisquer dígitos fracionários.
    11. `Math.sqrt(x)`**→** Retorna a raiz quadrada positiva de um número (\sqrt x).
    
- Number
    1. **`[Number.MAX_VALUE](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/MAX_VALUE)` →** O maior número representável positivo.
    2. **`[Number.MIN_VALUE](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/MIN_VALUE)`** → O número mínimo representável positivo - isto é, o número positivo mais próximo de zero (sem ser zero na verdade).
    3. [https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString)
    4. [https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat)
    
- [ ]  search - Unpacking values from a regular expression match
