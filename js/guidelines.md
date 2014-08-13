# ZEIT ONLINE JS Coding Guidelines

## Notation
All functions and variables should be named in CamelCase (eg. "doCounting").   
A function name should include an action and a noun (eg. "countNumber"), if the return value is in boolean the action should be "has" (eg. "hasNumber").

## Indentation
We use soft tabs (4 spaces) for indentation.

## Whitespace
General use:
- no trailing whitespace
- no whitespace in empty lines

Use maximal whitespacing ([jQuery Style][1]), this means:
- use one whitespace behind: comma ```( , )```, colon ```( : )```, opening round brackets ```( ( )``` and before closing brackets ```( ) )```
- use one whitespace before and behind equals sign ```( = )``` and mathematical operators ```( +, *, -, / )``` and comparisons ```( ==, ===, !=, !==, &&, ||, >, < )```

```js
if ( bla == foo ) {
  foo( "bar", "baz", { zoo: 1 } );
}
```
## Whitespace Exceptions
There are some exceptions to the whitespacing policy:

```js
// Function with a callback, object, or array as the sole argument:
// No space on either side of the argument
foo({
    a: "alpha",
    b: "beta"
});
 
// Function with a callback, object, or array as the first argument:
// No space before the first argument
foo(function() {
    // Do stuff
}, options );
 
// Function with a callback, object, or array as the last argument:
// No space after the last argument
foo( data, function() {
    // Do stuff
});

// Usage of jQuery object
$( '<div class="myclass"></div>' );
```
## Format
- use curly brackets to form blocks of code

```js
// wrong!
if ( true ) foo( "help!" );

// correct!
if ( true ) {
    foo( "911" );
} 
```

- whenever possible, define all variables of a function at one place (always use var)

```js
var title = "My title",
    subtitle = "My subtitle",
    story = "My story";
```

- global variabels should always be referenzed by using the window object (eg. window.myGlobalVar) 
- strings should be defined with double quotes

```js
var title = "My title";
```
- usage of strings within the jquery object should be encapsulated with single quotes

```js
$( '<div class="myclass"></div>' );
```
## Comparisons
For comparisons use:

String: typeof object === "string"
Number: typeof object === "number"
Boolean: typeof object === "boolean"
Object: typeof object === "object"
Plain Object: jQuery.isPlainObject(object)
Function: jQuery.isFunction(object)
Array: jQuery.isArray(object)
Element: object.nodeType
null: object === null
null or undefined: object == null
Global Variables: typeof variable ==="undefined"
Local Variables: variable === undefined
Properties: object.prop === undefined

## Documentation
Use [JsDoc Style][2] to describe functions.

```js
/**
 * writes a book.
 * @param {string} title - The title of the book.
 * @param {string} author - The author of the book.
 */
function writeBook( title, author ) {
}
```
##Hinting
JS Hint should be used with the following settings:

```
'-W015': true, //don't show indentation warnings  
browser: true, // set browser environment  
curly: true, // require curly braces around control structure  
eqeqeq: true, // prohibits the use of == and != in favor of === and !==  
forin: true, // requires all for in loops to filter object's items  
indent: 4, // tabsize should be 4 spaces  
jquery: true, // set query globals  
latedef: true, // never use vars before they are defined  
loopfunc: true, // no warnings about functions in loops  
trailing: true, // makes it an error to leave a trailing whitespace  
undef: true, // just use defined var, If your variable is defined in another file, you can use /*global ... */ directive to tell JSHint about it   
```

[1]: http://contribute.jquery.org/style-guide/js/#spacing "jQuery Style Guide"
[2]: http://usejsdoc.org/ "JsDoc"
[3]: http://www.jshint.com/ "JsHint"






