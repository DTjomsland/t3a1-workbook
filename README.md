# T3A1 Workbook
## Q1: Provide an overview and description of a standard source control process for a large project
*Source control is the management and tracking of changes to code. Large projects often have numerous individuals contributing and writing code simultaneously. In order to prevent bugs, conflicts, and overwriting other's code, source control is relied on to ensure the development process is smooth with little wasted time backtracking. The standard source control process that will be discussed below is the Git Feature Branch workflow.*

### <strong> Git Feature Branch Overview </strong>
The Feature Branch Workflow is the



<br>

## Q2: What are the most important aspects of quality software?
*When it comes to building quality software, there are numerous important aspects that must be taken into consideration.  From reliability to usability, the quality of each aspect must be meticulously ensured in order to provide the highest quality of software.  The main pillars of quality software consist of the following: usability, reliability, understandability, testability, portability, and efficiency. Below, each of these aspects will be discussed in detail.*

### <strong>Aspects of Quality Software</strong>

<strong>Usability:</strong>

Usability is measured by how easy the software is to use. Software should be user friendly, easily navigated, and relatively simple to learn.  User's skills often vary greatly, so creating intuitive software is key in ensuring all users have a great experience. Users should also be able to to use the core features of software without much help.  This means that key features should be as self-explanatory as possible.

<br>

<strong>Reliability:</strong>

Consistency is key when it comes to software reliability. Software should always behave in a consistent manner regardless of the environment and conditions. The way in which software handles errors is also important when it comes to reliability. It is paramount that errors occur as little as possible and when they do occur, they should be handled gracefully.

<br>

<strong>Understandability:</strong>

Understandability includes the ensuring that the every component and the overall structure of the source code is understandable. The source code should be organized and developed in a consistent manner so that any software engineer can easily understand components and their usage. When software is understandable, it streamlines the development process by reducing back and forth as well as the downtime that occurs when trying to locate and decipher components. If code causes confusion among developers, it is a sign that the code is lacking the necessarily level of understandability. 

<br>


<strong>Testability:</strong>

Software should be easily testable so that bugs and inconsistencies can be found.  Testability includes the ability to test all components and use cases easily and accurately. This should be one of of the primary concerns when planning the structure of software so that it may be easily divided into modules for testing. Testability ensures that software ships and works as intended.

<br>

<strong>Portability:</strong>

Portability ensures that software is not limited to specific environments and contexts. Highly portable software is written once with the ability to be deployed in any environment.  With device and operating system combinations having an incredible amount of variations, it is important to ensure that software works as expected in all cases. 

<br>

<strong>Efficiency:</strong>

Efficient software accomplishes its purpose while using as little amount of resources as possible. Resources include, but aren't limited to: memory, disk space, CPU usage, and external service calls. Minimizing resources is critical in development of software that works smoothly and predictably in all environments since resource availability varies greatly between environments. . 


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

In JavaScript, type coercion includes conversions such as string to number, number to string, and boolean to number, to name a few. Type coercion is common when operators are used on different data types.   For instance, when a string and a number are added or an equality operator (==) is used on two different data types. In these cases, one of the data types will be automatically converted to allow the operation to complete successfully. 

*Below are examples of type coercion using examples from JavaScript.*

<strong>Example 1: String to Number Conversion</strong> 

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

When a number and a Boolean are added together, the Boolean is converted to a number in order to complete the operation. If the Boolean value is `false`, it will be converted into the number `0`. If the boolean value is `true`, it will be converted into the number `1`. 

```
const number = 10;

let sum = false + 10;

console.log(sum)
```

In the example above, JavaScript will coerce the Boolean value `false` into the number `0`. Because of coercion, the result of `false + 10` is the number `10`.  



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