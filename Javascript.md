# technical_interview
### 1. Explain Hoisting in javascript.
**Answer:**
Hoisting is the default behaviour of javascript where all the variable and function declarations are moved on top.
```bash
hoistedVariable = 3;
console.log(hoistedVariable); // outputs 3 even when the variable is declared after it is initialized	
var hoistedVariable
```

###2. What is the difference between == and === in JavaScript?
**Answer:**In JavaScript, == is the loose equality operator, which compares two values for equality after performing type coercion if necessary. This means it converts the operands to the same type before comparing.

=== is the strict equality operator, which compares both the values and their types, without performing type conversion.
