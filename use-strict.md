### What is `"use strict"`?

This is a typical interview question. Find below one of the ways to answer the question:

The strict mode allows you to place a function or program in a strong operating context. It also makes debugging easier

It can be used in two ways:

- as a string on the first line of your code. this puts your entire code in a strong operating context

`"use strict"`

- another way to use is within functions where you want it applied. this is usually relevant when working in a legacy javascript context

```
function newCode() {
   "use strict"
   // code within function operates in a strong operating context
}
```

> The creators proposed the use of strings to allow older browsers to recognize it without throwing an error; older browsers will see as it a mere string and move on to execute other codes, while newer browsers will recognize it and use it to operate in a strong operating context

### What does it do?

1. In strict mode, a variable cannot be assigned a value without first being declared.

        "use strict";

        name = 'Dami'; // will throw an error!

2. It prevents the use of reserved JS keywords as variable names

        "use strict";

        var let = 1; // will throw an error!
        var eval = 1; // will throw an error!
        eval("var a = 1"); // the expression inside the eval is ignored if in strict mode which is safe, unlike when in non-strict mode where the variable a leaks out.

3. It does not allow deletion of variables, functions and function arguments. E.g

        "use strict";

        var name = 'Dami';
        delete name; // not allowed!

        function moo() {  };
        delete moo; // not allowed!

        function foo(bar) {
            delete bar; // not allowed!
        } 
