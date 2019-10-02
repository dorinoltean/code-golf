#  Javascript code golf tips

## for vs while

```js
while(cond)
for(;cond;)
// uses same amount of characters.
```


## Conditional operator instead of if ... else
```js
// Print numbers 1 to 100. If number is even print 'even'
for(i=0;i++<100;)
 if(i%2) console.log(i)
 else console.log("even")

for(i=0;i++<100;)console.log(i%2?i:"even")
```


## Evaluation of logical operators
When you use logical operators js will return the last evaluated expression.

```js

a=1,b=2
console.log(a&&b) 
// expected output: 2
// evaluates first expression to truthy. Goes on to evaluate and write the result of second expression

a=0,b=1
console.log(a&&b)
// expected output: 0
// evaluates first expression to falsy. Writes result of first expression. Second expression is not evaluated

a=1,b=2
console.log(a||b) 
// expected output: 1
// evaluates first expression to truthy. Writes result of first expression. Second expression is not evaluated

a=0,b=1
console.log(a||b)
// expected output: 1
// evaluates first expression to falsy. Goes on to evaluate and write the result of second expression

```
`&& operators are performed before the || operators `


## if(a||b)console.log(c)
Print expression c if a || b

```js
if(a||b)console.log(c)
a||b?console.log(c):0 // in case the result of this evaluation is ignored you can save one character by using conditional operator

```

##  Math.floor

Instead of Math.floor we can use bitwise operators for truncating decimal

```js
x=3.32
console.log(Math.floor(x))
console.log(x|0)
console.log(~~x)
```
// expected output: 3
// bitwise operators are performed in the same order-level as multiplication
// truncating negative numbers using bitwise operators gives different results then Math.floor


