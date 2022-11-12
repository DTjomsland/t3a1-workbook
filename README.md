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

React.js is a JavaScript library created by Meta that allows for the development of complex user interfaces. The primary feature of React.js is the ability to create code that is reusable, which saves large amounts of time in the development process. The key to this feature is that React.js is component based, allowing for components to be reused throughout the application. Another key feature of React.js is that it utilizes a virtual DOM, which is a representation of the original DOM. Changes made only modify the Virtual DOM, which saves resources and time due to eliminating the need to send a request to the server every time the user interacts with the interface. React.js utilizes JavaScript XML (JSX), which is neither HTML or XML, but a syntax extension to JavaScript. JSX assists in describing what the UI should look like and writing the aforementioned components. 

The role of React.js in MERN stack is provide a user friendly UI that can collect user data and input which can be sent server-side for processing.

<br>

### <strong>Server-side (Back-end):</strong>

<strong>Node.js:</strong>

Node.js is an open source server environment that utilizes JavaScript. Node.js is capable of asynchronous I/O which allows other processing to continue before the entire transmission has finished. 

A typical Node.js file request would look like the following:

- Task is sent to the file system
- Server is ready to handle the next request
- When the file system opens and reads the file, then the server sends the content back to the front-end.

This varies significantly from other environments in terms fo efficiency.  Typically, the server is not ready to handle the next request until the entire transmission has finished, meaning the request would need to be handled and the content returned to the front-end before the next task could begin. This greatly reduces the wait time and efficiently uses memory.

The role of Node.js in MERN stack is to provide a server-side environment that can execute JavaScript, in this case, Express.js.

<strong>Express.js:</strong>

Express.js is an unopinionated server-side JavaScript framework that runs inside a Node.js environment. It provides powerful models for URL routing and handling HTTP requests and responses. The Express.js framework is for the most part minimalist, but there are numerous compatible middleware packages created by other developers that can address most problems a developer may face.  

The role of Express.js in MERN stack is to process requests (XHRs/GETs/POSTs) from the React.js front-end and perform CRUD operations on the MongoDB database.

<br>

### <strong>Database: </strong>

<strong>MongoDB:</strong>
MongoDB is a NoSQL database which stores each record as a document. These documents consist of key-value pairs that are similar to JSON objects. MongoDB utilizes JavaScript which keeps the language used uniform across the entire stack. The primary unit of a MongoDB are the individual documents which are identifiable through the use of a primary key. MongoDB makes use of the Mongo shell which allows users to execute CRUD operations through the use of JavaScript.  

MongoDB's role in MERN stack is to store the JSON documents that are created by the React.js front end and processed by the Express.js server. 


<br>


## Q4: A team is about to engage in a project, developing a website for a small business. What knowledge and skills would they need in order to develop the project?
*When developing a website for a small business, a team must have extensive knowledge and deploy a fairly large amount of soft and technical skills to both streamline the development process and provide a quality product. The required soft and technical skills will be discussed in detail below.* 

<br>

### Soft Skills and Knowledge:

- <strong>Time Management:</strong> Procuring and maintaining a schedule for the development process is key to providing a quality product and ensuring that it is shipped on time. Productivity apps such as Trello are excellent tools to assist with keeping a development team on task and on time. 

- <strong>Client Management:</strong> Maintaining transparency and an excellent relationship with a client ensures that the product is shipped as desired. From staying in contact to keeping the client in the loop about changes and updates, having client management skills is paramount for a smooth development process.

- <strong>Project Management:</strong> Knowing where to start and how to maintain the course for a project is essential to ensuring both the client and developers stay happy. 

- <strong>Interpersonal Skills:</strong> Designing a quality website is often a team effort involving people from various professions.  The ability to provide clear explanations about the vision of the project is incredibly important in order to keep everyone on the same page. 

- <strong>Critical Thinking:</strong> The entire process of creating a website puts critical thinking skills to the test. Every decision, even the smallest, must be well thought out and every consequence for a decision must be considered. 

<br>

### Technical Skills and Knowledge:

- <strong>HTML:</strong> HyperText Markup Language is the foundation for most websites. It is typically the first skill learned and requires in depth knowledge to use appropriately and effectively. HTML provides the structure of a website.

- <strong>CSS:</strong> Cascading Style Sheets defines the visual appearance of HTML. Developers must have extensive knowledge of CSS in order to create a website that is visually appealing and user-friendly.

- <strong>JavaScript:</strong> Interactive components of the front-end of website are handled by JavaScript. Developers must know JavaScript in order to make a modern web application.  JavaScript knowledge also streamlines the development process because it can be used in both the frontend and the backend.

- <strong>Sever-side Languages:</strong> No website is complete without a rock solid backend.  This requires knowledge of common server-side programming languages such as JavaScript, PHP, Python, and Ruby.

- <strong>Database Management Systems:</strong> Knowledge of database management systems is key to providing a website that is both effective and secure. Examples of common database management systems include PostgreSQL and MongoDB.

- <strong>Version Control:</strong> Knowledge and experience with common modern practices of version control is a must in order to ensure that the development process is smooth and consistent. Git is the most widely used version control system.

- <strong>User Experience and User Interface:</strong> UX/UI is paramount in creating a great product in the modern world. Knowledge of UX/UI is key to the development of a product that users enjoy and will return to in the future. 

- <strong>Color Theory:</strong> Knowledge of colors is a must when developing a website. Website color palettes must be appealing to the user, but also must take into consideration the target audience and potential for users to have differing needs.  For example, colorblindness and other visual disabilities.

<br>

## Q5: With reference to one of your own projects, discuss what knowledge or skills were required to complete your project, and to overcome challenges
*In reference to my portfolio project, I needed to deploy a large range of skills and knowledge in order to successfully complete my web page. The skills and knowledge that were needed will be discussed in detail below.*

<br>

### Soft Skills and Knowledge

- <strong>Time Management:</strong> Time management skills were a must in order to develop my portfolio website in the allotted amount of time. For this project, I used Trello to keep myself focused, on task, and on time. Each feature was given a Trello card and within each card was a list of tasks that needed to be completed with a due date. As tasks were completed successfully, they would be moved to the *Done* list, and then the development of the feature with the next closest due date would be begin. Trello can only do so much in assisting with time management as it cannot force you to complete the task. That being so, motivation and perseverance were essential in managing my time for this project.

- <strong>Project Management:</strong> Knowing when and where to begin the project as well as ensuring development stayed the course played a major role in the completion and quality of my portfolio website. I deployed project management skills from the start of the project, which included proper planning through the use of Trello, detailed mock-ups on Figma, and hammering out a general theme early (colors, fonts, and design styles). When a task was first able to be completed, I made sure that I did so to prevent any need for backtracking and redoing work. I also implemented a basic Git Feature Branch Workflow that I made sure to stick to in order to keep the project moving forward.

- <strong>Critical Thinking:</strong> Since the material was mostly new to me, I relied heavily on critical thinking skills in order to connect to the dots between the new technologies I learned, as well as thinking ahead about the consequences of my styling choices. Every decision was heavily pondered no matter how insignificant it initially seemed. 

<br>

### Technical Skills and Knowledge:

- <strong>HTML:</strong> The project was completed with very limited knowledge of web based technologies, so I relied heavily on my basic HTML skills and knowledge in order to complete it on time and correctly.  A lot of thought goes into creating a semantically correct web page. Proper usage of the different tags and maintaining appropriate page structure is an important skill to know not just for ease of development, but to ensure the page is accessible to all and easily findable by search engines.

- <strong>CSS:</strong> Knowledge of CSS and SCSS was utilized in the creation of my portfolio project. My web page was very interactive and made extensive use of animations to bring it to life. This required a bit more advanced knowledge of CSS animations and transformations in order to complete.  SCSS knowledge allowed for my style sheet to be as DRY as possible with the use of variables for colors and even the generation of random numbers for my animations. 

- <strong>Version Control:</strong> Git and GitHub were used extensively throughout the development of my portfolio website. My knowledge of these technologies assisted in ensuring that the project stayed organized and kept moving forward.  Utilizing the common version control method of Git Feature Branch Workflow, a working product always remained intact after every merge.  This allowed for me to focus more time on developing and less time on backtracking in order to fix conflicts and bugs.

- <strong>User Experience and User Interface:</strong> Knowledge of UX and UI was required in order to make a web page that was both satisfying to look at and  navigate. Heavy planning and personal testing was utilized in order to give the website the feel that I wanted. Features such as animations and colors were utilized to make the website exciting and interactive without being overwhelming to the user. Colors were heavily relied upon to draw the user in and direct them to where I wanted them to go next. The navigation elements were designed to make navigating the website straight forward and obvious, ensuring the user knew where they were and where they were about to go.

- <strong>Color Theory:</strong> Basic color theory was implemented to create a visually appealing website. Online tools assisted me in sorting out which colors would be used as well as the appropriate colors to pair with each other. A dark theme was implemented to create a website that has elements that pop and excite the user. Consideration was made to those with disabilities as well, providing appropriate levels of contrast throughout the site.

- <strong>Prototyping:</strong> Knowledge of prototyping software ensured that I knew what I was going to create before I began creating it.  Starting a project without extensive mock-ups and prototypes guarantees that time will be wasted backtracking nd changing features. This was avoided through the use of Figma, which was utilized to create mock-ups of every web page as well as the arrangement of elements on the most common screen sizes.

<br>

## Q6: With reference to one of your own projects, evaluate how effective your knowledge and skills were for this project, and suggest changes or improvements for future projects of a similar nature
*In reference to my portfolio project, I needed to deploy a large range of skills and knowledge in order to successfully complete my web page. An evaluation of my use of these skills and knowledge will be conducted in detail below.*

<br>

### Soft Skills and Knowledge


- <strong>Time Management:</strong> Managing my time was an issue during the creation of my portfolio project, but I feel like I managed it quite well considering my lofty goals with technologies that I had just been acquainted with. I utilized Trello relatively well throughout the development process, but did find myself going off-script fairly often.  While working, I found that if I learned a new skill, I would immediately need to apply it to previously completed work instead of continuing to complete the task at hand which took up a lot of time. The ability stick to the plan and timeline of the project is a skill that I need to work on. 

- <strong>Project Management:</strong> Planning and executing the steps for my portfolio website was well organized for the most part. I had a plan and I stuck to it outside of a few instances where I learned a new skill and applied it elsewhere. A notably good example was how well the website was sorted before I wrote a line of code.  All of my colors, margins, sizes, and fonts were planned beforehand. It saved a lot of time not having to rewrite code over and over because of trial and error. I feel as though this was one of my strongest skills deployed for my portfolio project.

- <strong>Critical Thinking:</strong> This is a skill that I felt I used to the best of my ability at the time.  I spent a lot of time connecting dots and understanding how everything interacts.  Just about every feature had a pros and cons list in order to make the best choices. I would definitely have done certain parts differently based on the knowledge I have now, but given the knowledge I had at the time, I feel like i utilized my critical thinking skills effectively and to the fullest extent given the circumstances.

<br>

### Technical Skills and Knowledge

- <strong>HTML:</strong> My HTML knowledge was lacking at the beginning of the project. I was constantly switching between tag types due to confusion and initially overused divs. I was able to fully grasp the use-cases for each tag by the end of the assignment, but I should have spent more time solidifying them before attempting to structure my HTML.  It would have saved quite a bit of time if I had a better understanding from the beginning.

- <strong>CSS:</strong> Styling was the one thing I was very confident about going into the project.  My knowledge of CSS felt solid and I was able to place and style most features without much issue.  If I were to create a similar project, I would definitely spend time gaining more knowledge about SASS and ways in which is expedites the development process. I didn't use too many of it's features for the project.

- <strong>Version Control:</strong> My Git and GitHub Skills and knowledge were not well honed, but were adequate given the size of the project.  I feel I did a good job committing changed frequently throughout the development process.  One area I feel I can improve upon is being diligent about creating new branches for every feature. I was often working on multiple features per branch which was not an issue due to them being relatively small features, but I did have a few issues with breaking my `main` branch and wasting time trying to figure out what feature broke it. 

- <strong>User Experience and User Interface:</strong> My skills in UX/UI were the ones I felt most confident about during the development of the portfolio website. I had used Figma to a large extent before I began the coding process.  The flow and features of the web site were planned early on and fine tuned through many user scenarios. Every placement and style had a reason for why it was there.  One area I was lacking is understanding what the typical breakpoints would be fore devices.  My initial UX design failed to take into account some higher pixel density devices.  Gaining more knowledge about how to handle design for different devices would definitely help improve my skills as a UX designer. 

- <strong>Color Theory:</strong> My skills in color theory were lacking during the creation of the portfolio site.  I feel I some decent raw skills for color choice, but gaining actual knowledge on color theory would've helped me with this project. I relied heavily on color tools such as Coolers to assist me in choosing the color palette.  I think it would be helpful to study color trends and the feelings colors evoke before I develop another website.

- <strong>Prototyping:</strong> My prototyping skills were quite good considering I had just learned how to use Figma.  I spent a great deal of time creating every element on Figma exactly as it should be on the screen. Pixels, color codes, and screen sizes were well planned before a line of code was written.  One area I could use more knowledge on is the advanced prototyping techniques that Figma offers. Constantly having to change colors and styles individually throughout all of my mock-ups was very time consuming, so mastering tools to eliminate that would streamline the development process.

<br>



## Q7: Explain control flow, using an example from the JavaScript programming language

Control flow is the order in which computers execute code. In JavaScript, the computer reads code from top to bottom, line by line, meaning that it starts from the first line and and reads each line in order until it reaches the last line. However, there are structures that can change the control flow.  Structures such as conditionals and loops are used to disrupt the control flow and change the order of execution of the code. Control flow enables our program to make decisions about which code should be executed next.

<br>

*Below are examples from JavaScript of the effect that conditional statements and loops have on the control flow.*

### Example 1: Conditional Statements and Control Flow

Conditional statements are essentially checks to see if a specified condition is true or false. Conditionals direct the control flow by directing the computer to execute different code depending on which condition is met. In short, if the condition is true, the computer will execute Code 1. If the condition is false, the computer will execute Code 2. Conditional statements in JavaScript consist of if...else, switch, and ternary statements.

<br>

<strong>Code Example:</strong> `if...else` statement

```javascript
let dog = true;
if (dog === true) {
    console.log("Who's a good boy!?");
else {
    console.log("Ain't no good boys round here!");
}
```
In the example above, the `if` condition is met, so the the line `console.log("Who's a good boy!?")` will be executed. If the `if` condition was not met, the line `console.log("Ain't no good boys round here!")` would be executed. 

<br>

### Example 2: Loops and Control Flow

Loops allow for repetitive tasks to be executed using less code. Instead of having to write out a line of code for every task, you can utilize a loop to perform the same action to each item which manipulates the control flow to achieve the desired result. Examples of loop types in JavaScript include, but aren't limited to, the for loop, while loop and do...while loop. 

<br>

<strong>Code Example:</strong> `for` loop

```javascript
for (let i = 0; i < 9; i++) {
  console.log(i);
}

// Output:
// 0
// 1
// 2
// 3
// 4
// 5
// 6
// 7
// 8
```

In the example above, the three optional parameters are used to control the execution of the loop. The syntax for this is `for (initialization; condition; finalExpression)`. The variable `i` begins the loop with a value of `0`, and as long it's value is less than `9` the loop is executed.  After each iteration,  the value of `i` is increased by `1` (`i++`).  This alters the control flow by telling the computer to repeat the process 9 times before moving on. 

<br>


## Q8: Explain type coercion, using examples from the JavaScript programming language
Type coercion is the automatic conversion of a value from one datatype to another. Type coercion is also known as implicit conversion, meaning it is done by code behind the scenes rather than manually. 

In JavaScript, type coercion includes conversions such as string to number, number to string, and boolean to number, to name a few. Type coercion is common when operators are used on different data types.   For instance, when a string and a number are added or an equality operator (==) is used on two different data types. In these cases, one of the data types will be automatically converted to allow the operation to complete successfully. 

*Below are examples of type coercion using examples from JavaScript.*

<strong>Example 1: String to Number</strong> 

When math operators such as subtraction (-), division (/), multiplication (*), or modulus (%) are used, all values involved that are not number are converted to the number datatype. This occurs because these operations can only be applied to the number datatype. 

```javascript
const number = 10;
const stringNumber = "9";

let dif = number - stringNumber;

console.log(dif)
```

In the example above, JavaScript will coerce `stringNumber` into a number datatype, then perform the operation. The value of dif will be the difference between `10` and `9` which is `1`.
<br>

<strong>Example 2: Number to String</strong> 

When the math operator such addition (+) is used between a string and a number, the number will be converted to a string and JavaScript will concatenate the two strings together. 

```javascript
const number = 10;
const stringNumber = "9";

let sum = number + stringNumber;

console.log(sum)
```

In the example above, JavaScript will coerce `number` into the string datatype resulting in `10` being added to `stringNumber`.  Because of coercion, the result of `number + stringNumber` results in the string `"109"`

<strong>Example 3: Boolean to Number</strong> 

When a number and a Boolean are added together, the Boolean is converted to a number in order to complete the operation. If the Boolean value is `false`, it will be converted into the number `0`. If the boolean value is `true`, it will be converted into the number `1`. 

```javascript
const number = 10;

let sum = false + 10;

console.log(sum)
```

In the example above, JavaScript will coerce the Boolean value `false` into the number `0`. Because of coercion, the result of `false + 10` is the number `10`.  

<br>

## Q9: Explain data types, using examples from the JavaScript programming language

Data types are a feature of all programming languages, but these types often differ from language to language. A datatype is a classification that specifies the type of value and what type of relational or logical operations can be are allowed to be used on it.  Common data types in most languages include, but are not limited to, integers, booleans, floats, strings, and arrays. 

In JavaScript, there are eight primitive types of data.  These primitive data types include strings, booleans, numbers, BigInt, Symbol, object ,null, and undefined. Of these eight basic data types, seven are primitive and one, Object, is non-primitive.  Object is non-primitive because it can store collections of data while the others can 
only store one single data. *Below are some examples of data types in JavaScript.*

<br>

### Strings
Strings are used to to store text in JavaScript. Basic strings are typically surrounded by single quotes or double quotes, but are surrounded by back ticks when variables or expressions are included in the string. 

<strong>Example:</strong>

```javascript
//single quotes
const myName = 'David';

//double quotes
const yourName = "Frank";

//back ticks
const bestBuds = `${myName} and ${yourName} are best buds!`;
```

<br>

### Numbers
Numbers in JavaScript typically represent integers and floats(decimals/exponents), but can also be infinity+, infinity-, and NaN(not a number).

<strong>Example:</strong>

```javascript
//number
const bestNumber = 12;

//floating number
const worstNumber = 66.6;

//floating number
const confusingNumber = 5e7;

//not a number
const notNumber = "stuff"/5;
console.log(notNumber); //result is NaN
```

<br>

### Booleans
In JavaScript, Booleans represent one of two values: true or false. 

<strong>Example:</strong>


```
const smellyFeet = true;
const washedFeet = false;
```
<br>

### Undefined
In JavaScript, the undefined datatype occurs when a value is not assigned. For instance, if a variable is declared but not given a value or a variable is assigned the value undefined.


<strong>Example:</strong>

```javascript
const myName;
console.log(myName); //result is undefined

const myNameAgain = undefined;
console.log(myNameAgain); //result is undefined
```

<br>

### Null
In JavaScript, null represents an empty value.

<strong>Example:</strong>

```javascript
const mrNoValue = null;
```

<br>

### Symbol

In JavaScript, a Symbol represents an immutable and unique primitive value.

<strong>Example:</strong>

```javascript
//both values contain the same string value, but are different because they are Symbols
const mySymbol1 = Symbol('best workbook ever');
const mySymbol2 = Symbol('best workbook ever');
```

### Object

In JavaScript, an Object represents the only complex data type out of the basic data types because is stores a collection of data rather than one single data. 

<strong>Example:</strong>

```javascript
const numberOneWorkbook = {
  owner: 'David',
  nationality: 'American',
  grade: 84
}
```

## Q10: Explain how arrays can be manipulated in JavaScript, using examples from the JavaScript programming language
Arrays in JavaScript are variables that are used to store different data types and can hold more than one value.
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