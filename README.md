# The Art of writing clean code

<img src='https://res.cloudinary.com/practicaldev/image/fetch/s--DVv9dGmZ--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kt2oyitm2dj73brrj8my.jpg' alt="Laptop with javascript code" />

## What is clean code all about 

  <p>
  When it comes to writing software, one of the most important aspects is writing clean, maintainable code. 
    Clean code refers to code that is easy to understand, modify, extend and also maintain. Writing clean code is a skill that is crucial for every developer to master. A clean code should be very easy to read even from another developer even if the code has been written years ago. 
  </p>
  
  <p>
    <i>"Any fool can write code that a computer can understand. Good programmers write code that humans can understand."</i>  - Martin fowler
  </p>
  
  <p> Now that we have learn what clean code does, lets look at the benefit of clean code, lets take a look at unclean code. </p>
  
  ## Unclean code
   <p> As You may know unclean code is the vice-versa of clean code. writing unclean code is not a crime and you will not be arrested for that, but the problem is that you may not recognise the code years to come and it will be very hard to maintain. lets look at common causes of unclean code. </p>
  
  ## Common causes of unclean code 
  <ul>
    <li> Too much work pressure </li>
    <li> When the existing codebase is already complex and unclean </li>
    <li> Short delivery time  </li>
    <li> Not following the team pattern or the company pattern </li>
    
  </ul>
  
  ## Benefit of clean code
  
  <ol>
  <li> Clean and understandable </li>
  <li> Flexible and easy to maintain </li>
  <li> Maintaining consistency accross all codebase </li>
  <li> Easy to extend and also to intergrate to other applications </li>
  
  </ol>
  
   <p> There are many benefits of clean code, but i have just mention a few </p>
  
  <p> All though there is now particular rule or standard of writing clean code, but these standard are mostly used by developers world wide, and although many developers have their own way of writing clean code, but here are few tips,
    <p> <i> <bold> " When writing code, write code for beginners even an beginner in programming will understand " </bold> </i>   <span>  -- Ezeobi Kingsley Sunny </span>  
    </p>
    Okay now that we have a good understanding of clean code and unclean code, lets look at the tips for writing clean code, I will be using javaScript as the programming language, please Note that this applies to all programming language.
  </p>
  
  ## Tips for writing clean code
  
  ### Keep it simple: 
  <p>Use the simplest solution that will work and avoid unnecessary complexity. This will make your code easier to understand and maintain. </p>
  
 ```javascript
function getLastLetter (letter) {
  const letters = letter.split("");
  let lastLetter = '';
  letters.forEach((letter, i) => {
    if(i === letters.length - 1) {
      lastLetter = letter
    }
  })
  lastLetter = letters[letters.length - 1];
  return lastLetter;
  }
 
 ```
    
    
    
```javascript
function getLastLetter (letter) {
  const letters = letter.split("");
  const lastLetter = letters[letters.length - 1];
  return lastLetter;
 }
 ```
  
  As you can see the second implementation is cleaner and more readable than the first implementation  

  #### Use descriptive variable and function names: 
  Use clear, descriptive names that accurately describe the purpose of the variable or function. This will make your code more readable and easier to understand. The concept is 
  <ul>
    <li> Use Nouns for naming  variables </li>
    <li> Use Plural for naming arrays </li>
    <li> Use an action word for naming functions </li>
  </ul>
  
  for example for naming variables use
```javascript
const l  = "kdfkjdf"; // wrong
const letters = "kdfkjdf"; // correct
```
  
  for example for naming functions use an action 
```javascript
const getLastL  = () => {...}; // wrong
const getLastLetter = () => {...}; // correct
```
  
  for example for naming arrays use plurals
```javascript
const numberList  = [2,4,5]; // wrong
const numbers =  [2,4,5]; // correct
```
 
   for example for naming booleans
```javascript
const loading  = true // wrong
const isLoading = true; // correct
// or you can use
const entered = true; // wrong
const hasEntered = true;  // correct
```  
  
  #### Organize your code: 
    Organize your code: Break your code up into small, manageable functions, and organize your code in a logical manner. This will make it easier for others to understand and work with your code.
    
  #### Follow a consistent style: 
  Use a consistent style and naming conventions throughout your codebase. This will make it easier for others to understand your code and for you to come back to your own code and understand it. if you are working with a team use the team recommended naming conventions and rule.
  
  #### Comment your code:
   Use Long comment ( multi-line comment) for very long functions, class or method and this will make it easier for the person reading it to understand thatn using short comment every where, sometimes try to avoid using short comment if neccessary
  
  lets go back to oour complicated function
  
```javascript
function getLastLetter(letter) {
  // letters
  const letters = letter.split("");

  // initial Last letter
  let lastLetter = "";

  // looping through the letters
  letters.forEach((letter, i) => {
    if (i === letters.length - 1) {
        lastLetter = letter;
    }
  });

  // assigned the last letter
  lastLetter = letters[letters.length - 1];

  // returns the last letter
  return lastLetter;
}
```
```javascript

 / **
 * A function that loops through all the letters and gets the last letter
 * @param {string} letter - The word, may be a Noun, verb e.t.c
 * @returns {string} - The last letter
 */
function getLastLetter(letter) {
  const letters = letter.split("");
  let lastLetter = "";
  letters.forEach((letter, i) => {
      if (i === letters.length - 1) {
          lastLetter = letter;
      }
  });
  lastLetter = letters[letters.length - 1];
  return lastLetter;
}
```
  
 As you can see the multi-line comment says it all without me reading the code and it is neater than the single line comment which is somehow scattered and  allows me to check through the code. Note: for generating multi-line comment like this in javaScript read <a href='https://jsdoc.app/about-getting-started.html'> JSDoc </a>
 
 
 #### Deleting commented code: 
  commented code can cause a lot of distraction and could not be updated for a very long time since nobody will want to delete to code that another person commented, instead of commenting a code, simply delete it as it will not be useful
  
  
Writing clean code can be very slow and stressfull, but trust, once you mastered writing clean code, you will be able to maintain your project and will be loved by also your team members 
Although this are a few tips to writing clean code. check out this resources and books to know more about clean code

https://martinfowler.com/books/refactoring.html --- Refactoring -- By Martin fowler
<p>
https://www.oreilly.com/library/view/clean-code-a/9780136083238/ -- Clean Code: A Handbook of Agile Software Craftsmanship -- By Robert C. Martin.
<p>

-- By Ezeobi Kingsley Sunny


   
   




  
  
  
