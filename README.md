# T3A1 Workbook
## Q1: Provide an overview and description of a standard source control process for a large project

<br>

## Q2: What are the most important aspects of quality software?

<br>

## Q3: Outline a standard high level structure for a MERN stack application and explain the components

<br>

## Q4: A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?

<br>

## Q5: With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges

<br>

## Q6: With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature

<br>

## Q7: Explain control flow, using an example from the JavaScript programming language

<br>

## Q8: Explain type coercion, using examples from the JavaScript programming language
Type coercion is the automatic conversion of a value from one datatype to another. Type coercion is also known as implicit conversion, meaning it is done by code behind the scenes rather than manually. 

In JavaScript, type coercion includes conversions such as string to number, number to string, and boolean to number, to name a few. Type coercion is common when operators are used on different data types.   For instance, when a string and a number are added or an equality operator (==) is used on two different dataypes. In these cases, one of the datatypes will be automatically converted to allow the operation to complete successfully. 

*Below are examples of type coercion using examples from JavaScript.*

<strong>Example 1:String to Number Conversion</strong> 

When math operators such as subtraction (-), division (/), multiplication (*), or modulus (%) are used, all values involved that are not number are converted to the number datatype. This occurs because these operations can only be applied to the number datatype. 

```
const number = 10;
const stringNumber = "9";

let dif = number - stringNumber;

console.log(dif)
```

In the example above, JavaScript will coerce `stringNumber` into a number datatype, then perform the operation. The value of dif will be the difference between `10` and `9` which is `1`.
<br>

<strong>Example 2: Number to String Conversion</strong> 

When the math operator such addition (+) is used between a string and a number, the number will be converted to a string and JavaScript will concatenate the two strings together. 

```
const number = 10;
const stringNumber = "9";

let sum = number + stringNumber;

console.log(sum)
```

In the example above, JavaScript will coerce `number` into the string datatype resulting in `10` being added to `stringNumber`.  Because of coercion, the result of `number + stringNumber` results in the string `"109"`

<strong>Example 3: Boolean to Number</strong> 






## Q9: Explain data types, using examples from the JavaScript programming language

<br>

## Q10: Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language

<br>

## Q11: Explain how objects can be manipulated in JavaScript, using examples from the JavaScript programming language

<br>

## Q12: Explain how JSON can be manipulated in JavaScript, using examples from the JavaScript programming language

<br>

## Q13: For the code snippet provided below, write comments for each line of code to explain its functionality. In your comments you must demonstrates your ability to recognise and identify functions, ranges and classes

```
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it was made in ' + this.model;
  }
}

let makes = ["Ford", "Holden", "Toyota"]
let models = Array.from(new Array(40), (x,i) => i + 1980)

function randomIntFromInterval(min,max) { // min and max included
    return Math.floor(Math.random()*(max-min+1)+min);
}

for (model of models) {

  make = makes[randomIntFromInterval(0,makes.length-1)]
  model = models[randomIntFromInterval(0,makes.length-1)]

  mycar = new Model(make, model);
  console.log(mycar.show())
}
```