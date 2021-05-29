### Pseudocode for the passenger counter app 



**Stage 1**

- *Initalize count to 0* (zero)

- *Listen for clicks on the increment button* 

- *increment the count variable when the button is clicked* 

- *change the count-el in the HTML to reflect the new count* 


>  One way to achieve that increment is to include the onclick event listener increment() into the HTML as follows: 

  

```html
<html>
    <head>
        <link rel="stylesheet" href="index.css">
    </head>
    <body>
        <h1>People entered:</h1>
        <h2 id="count-el">0</h2>
        <button id="increment-btn" onclick="increment()">INCREMENT</button>
        <script src="index.js"></script>
    </body>
</html>
```



> This event listener *increment()* is  a **function** that needs to initialized in the javascript file as follows: 

```javascript

function increment() {
    console.log("The button was clicked")
}


```



> Essentially the above HTML is saying that every time the button is clicked , I want you to run the function **increment()**, and **increment ()** itself is at this point only displaying a message in the console log confirmng that the button was indeed clicked. 

Functions are important because they allow us to use **less code** to achieve the same result. One way to think of functions is to view them as **commands** that we ask Javascript to remember and run when we ask it to.  In the case discussed, Per talked about a hypothetical countdown from 5. If we were to do this *wihtout* functions, our code would look like this:

``` javascript
  console.log(4)

  console.log(3)

  console.log(2)

  console.log(1)
```

  A better approach is to declare this function in Javascript and call upon it whenever needed, thereby recycling parts which in turn leads to more economical code. In the above example, we would **refactor** the code to a function called **countdown**() as follows:

```javascript
function countdown() {

	console.log(5)

	console.log(4)

	console.log(3)

    console.log(2)

    console.log(1)

}
```

Note the above we are merely *declaring* the function. In order to run it, we must call upon it or invoke the **countdown**() function. 

```javascript
// Create a function (you decide the name) that logs out the number 42 to the console
// Call/invoke the function

function myLogger() {
    console.log(42)
}

myLogger() 
```



```javascript
let lap1 = 34
let lap2 = 33
let lap3 = 36

// Create a function that logs out the sum of all the lap times

function totalLog() {
   let totalTime = lap1 + lap2 + lap3
    console.log(totalTime)
}

totalLog()


```

The above was my code. Note, the variable totalLog can only be referenced within this function because it is not *a global variable*; instead it is being used only by this function when invoked. 

The same problem above can be refactored as follows as well: 

```javascript
let lap1 = 34
let lap2 = 33
let lap3 = 36

// Create a function that logs out the sum of all the lap times
function logLapTime() {
    // let totalTime = lap1 + lap2 + lap3
    console.log(lap1 + lap2  + lap3)
}

logLapTime()
```

The next problem is a lap counter for a race. My solution:



```javascript
let lapsCompleted = 0

// Create a function that increments the lapsCompleted variable with one
// Run it three times

function lapCounter() {
    lapsCompleted = lapsCompleted + 1
}

lapCounter()
lapCounter()
lapCounter()
console.log(lapsCompleted)
```

