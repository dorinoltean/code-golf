#  Javascript code golf tips

## for vs while

```js
while(cond)
for(;cond;)
// uses same amount of characters.
```

## Evaluation of logical operators
When you use logical operators js will return the last evaluated expression.

```js
a=1,b=2,c=3
console.log(a&&b&&c) 
// expected output: 3
// evaluates all three expressions and returns the result of the last one

a=1,b=0,c=3
console.log(a&&b&&c)
// expected output: 0
// because second expresion is Falsy it stops evaluating the last expression and returns the second one
```
