# JavaScript Math

In Ruby, solving for the square root of a number involves using the `.sqrt` class method on the `Math` class.

While JavaScript supports a lot of the same mathematical operations as Ruby, there is one big difference. `Math` in JavaScript is actually a single built-in object that you can perform operations on. This `Math` object does have plenty of convenience functions that allow you to do math simply and easily. Think of these functions as the equivalent of instance methods in Ruby. You can read more about math in JavaScript [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

Please feel free to use the console in the Chrome or Firefox Developer Tools to play around with these convenience methods.

## Objectives

+ Explain how numbers work in JS
+ Round numbers to the nearest whole number
+ Perform a series of math problems on numbers following order of operations

## Rounding

If you'd like to round to the nearest whole number, use the `.round()` method built out for you by JavaScript's Math class.

```javascript
// Returns the value 20
Math.round(20.49);

// Returns the value 21
Math.round(20.5);

// Returns the value -20
Math.round(-20.5);

// Returns the value -21
Math.round(-20.51);
```

## Floor

If you'd like to round to a whole number less than or equal to a number, use `Math.floor()`.

```javascript
// Returns 45
Math.floor(  45.95 );

// Returns -46
Math.floor( -45.95 );
```

## Absolute Value

The `Math.abs()` function returns the absolute value of a number.

```javascript
// Returns the value 1
Math.abs('-1');

// Returns the value 1.67
Math.abs('1.67');

// Returns the value 2.5
Math.abs(-2.5);
```

## Square Root

To take the square root of a number, pass the number to the Math class' `sqrt()` method.

```javascript
// Returns the value 3
Math.sqrt(9); // 3

// Returns the value 1.414213562373095
Math.sqrt(2);

// Returns the value 1
Math.sqrt(1);

// Returns the value 0
Math.sqrt(0);
```

## Order of Operations

Just like in Ruby, parentheses indicate precedence. For instance, the equation to convert Fahrenheit to Celsius is to first subtract thirty-two then multiply by five-ninths. To prioritize this subtraction before the multiplication happens, we wrap it in parentheses.

```js
temp_in_fahrenheit = 104
var celsius = (temp_in_fahrenheit - 32) * 5/9;
var rounded = Math.round(celsius);
rounded + "°C";

// Returns the value "40°C"
```

If we forgot to wrap the subtraction in parentheses, the code would multiply thirty-two by five-ninths then subtract this product from the value for Fahrenheit, leading to a return value of "86°C" instead (for reference, 86°C is 187°F).

## Adding Strings and Numbers

Something to be aware of as a Rubyist learning JavaScript is that JavaScript will concatenate numbers. In Ruby, when you add the strings "1", "2", and "3", you get the return string "123". However, if you were to add the strings "1" and "2" plus the number 3, you would get a type error:

Ruby:
```ruby
# Ruby

"1" + "2" + "3"
# => "123"

"1" + "2" + 3
# => TypeError: no implicit conversion of Fixnum into String
```

Unlike Ruby, JavaScript will convert this final number into a string and tack that string onto the end.

Javascript:
```javascript
// JavaScript

"1" + "2" + "3"
// => "123"

"1" + "2" + 3
// => "123"
```

Here are some more examples of JavaScript adding strings with one number:

```javascript
"1" + "5"
// => "15"

"1" + 5
// => "15"

5 + "1"
// => "51"
```

Notice that if a number, or numbers, preceed the string, JavaScript will perform the math on the numbers before adding the result of the math to the String at the end:

```javascript
5 + 5 + "5"
// => "105"
```

However, if a string starts off the statement, JavaScript will treat the following numbers as strings and not perform math on them:

```javascript
"5" + 5 + 5
// => "555"
```

For more info, see the [docs for the addition operator](http://es5.github.io/#x11.6.1).


## Resources

* [MDN - Math](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)
* [Addition operator](http://es5.github.io/#x11.6.1)
* [Arithmetic Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/intro-to-math.js' title='JavaScript Math'>JavaScript Math</a> on Learn.co and start learning to code for free.</p>

<p class='util--hide'>View <a href='https://learn.co/lessons/intro-to-math.js'>Math in JS</a> on Learn.co and start learning to code for free.</p>
