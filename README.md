# T3A1 Workbook
## Q1: Provide an overview and description of a standard source control process for a large project
*Source control is the management and tracking of changes to code. Large projects often have numerous individuals contributing and writing code simultaneously. In order to prevent bugs, conflicts, and overwriting other's code, source control is relied on to ensure the development process is smooth with little wasted time backtracking. Below, the standard source control process Git Feature Branch Workflow will be discussed in detail.*

### <strong>Git Feature Branch Workflow Overview</strong>

1. The code on the `main` branch should always be deployable.
2. All new features should be their own branch with a descriptive name.
3. Code should be committed and pushed to these branches consistently throughout development.
4. Pull requests should happen often and definitely before a branch is merged with the `main`.
5. Merges only happen after a pull request is extensively reviewed.
6. Code is deployed immediately after review.


### <strong>Git Feature Branch Workflow Description</strong>
The Feature Branch Workflow is based on the idea that any new feature should be developed on a separate dedicated branch away from the `main` branch. The perk of this workflow is that it allows developers to work on new features without the possibility of breaking existing features on the `main` branch. This ensures that the `main` branch remains consistently functional throughout the development process. 

The feature branch workflow also facilitates extensive use of pull requests, allowing for collaboration and the ability for other developers to sign off before the feature branch is merged into the `main` branch. Pull requests allow the developers to have an open discussion about the code before any major merges or changes. The facilitation of open discussion about feature branches before each branch is implemented greatly reduces the chance that merged code contains bugs or conflicts with with the `main` branch, but also ensures that the feature is complete and functions appropriately. This workflow has a few advantages over others.  The main advantage is that it is incredibly simple. This makes it ideal for small teams and web applications where only a single version is in production. 

Despite the numerous benefits, the Git Feature Branch Workflow has its downsides. This strategy doesn't always support continuous integration due to often having long-lived feature branches that are not merged until the feature is completed. Since the feature branches are often extensive, merges in the feature branch workflow often run a much higher risk of conflict with the `main` branch. This often leads to a great deal of time dedicated to ensuring that the feature branch is merged without breaking the `main` branch.  This workflow also does not support having multiple versions of the product at a time due to everything stemming from the single `main` branch. 

<br>

![image](/docs/featurebranchworkflow.png)
<sup>Creator: David Tjomsland</sup>
<br>

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
*MERN stack is a web development framework that consists of the stack MongoDB, Express.js, React.js, and Node.js.  React is used to create the front-end, Express is used as the server-side framework which runs inside a Node server, and MongoDB is used to store any data. This stack allows for rapid development due to the extensive utilization of a single language: JavaScript. The general high level structure and components of a MERN stack application will be discussed below.*

<br>

![image](/docs/MERNstack.png)
<sup>Creator: David Tjomsland</sup>

<br>

### <strong>Front-end:</strong>

<strong>React.js:</strong>

React.js is a JavaScript library created by Meta that allows for the development of complex user interfaces. The primary feature of React.js is the ability to create code that is reusable, which saves large amounts of time in the development process. The key to this feature is that React.js is component based, allowing for components to be reused throughout the application. Another key feature of React.js is that it utilizes a virtual DOM, which is a representation of the original DOM. Changes made only modify the Virtual DOM, which saves resources and time due to eliminating the need to send a request to the server every time the user interacts with the interface. React.js utilizes JavaScript XML (JSX), which is neither HTML or XML, but a syntax extension to JavaScript. JSX assists in describing what the UI should look like and writing the aforemantioned components. 

React's role in MERN stack is provide a user friendly UI that can collect user data and input which can be sent server-side for processing.

<br>

### <strong>Server-side (Back-end):</strong>

<strong>Node.js:</strong>

Node.js is an open source server environment that utilizes JavaScript. 

<strong>Express.js:</strong>




### <strong>Database: </strong>

<strong>MongoDB:</strong>
MongoDB is a NoSQL database which stores each record as a document. These documents consist of key-value pairs that are similar to JSON objects. MongoDB utilizes JavaScript which keeps the language used uniform across the entire stack. The primary unit of a MongoDB are the individual documents which are identifiable through the use of a primary key. MongoDB makes use of the Mongo shell which allows users to execute CRUD operations through the use of JavaScript.  

MongoDB's role in MERN stack is to store the JSON documents that are created by the React.js front end and processed by the Express.js server. 




  



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