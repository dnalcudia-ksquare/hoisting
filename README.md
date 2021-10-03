# Hoisting
## Activity 3: Hoisting
the answers are next to their respective console.log

## Question 1
console.log('bar:',bar) //undefined
bar = 15
var foo = 1
console.log(foo,bar) //1, 15
var bar

## Question 2
var foo = 5
console.log('foo',foo) // 5
var foo;
var bar = 10;
var bar;
console.log('bar:',bar) // 10
var baz = 10
var baz = 12
console.log('baz:',baz) // 12

## Question 3
function foo() {
	function bar() {
  return 5
  }
  return bar()
  
  function bar() {
  return 10
  }
}
console.log(foo()) // 10

## Question 4
function foo() {
	var bar = "Im a bar variable"
  function bar() {
  	return "Im a bar function"
  }
  return bar()
}
console.log(foo()) //Error la función bar no se puede llamar

## Question 5
greeting() //Good evening
var greeting = function() {
console.log('Good morning')
}
greeting() //Good morning
function greeting() {
console.log('Good evening')
}
greeting() //Good morning

## Question 6
var foo = 5
console.log('foo:',foo) //5
var foo = 10
console.log('foo',foo) //10

## Question 7
console.log(foo()); //3
function foo() {
	var bar = function() {
		return 3
	}
  return bar()
  var bar = function() {
  	return 8
  }
}

## Question 8
var x = 'foo';
(function() {
	console.log('x: ' + x) //undefined
  var x = 'bar'
  console.log('x: ' + x) //bar
})()

## Question 9
function foo() {
	console.log('First')
}
foo() //Second
function foo() {
console.log('Second')
}

## Question 10
var foo = 5
function baz() {
	foo = 10
  return
  function foo() {
  
  }
}
baz()
console.log(foo) //5
