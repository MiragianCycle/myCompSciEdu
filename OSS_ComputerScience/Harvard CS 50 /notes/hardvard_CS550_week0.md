# CS50 Computer Science

## WEEK 0 

**David Malan** 

### What is Computer Science?

**INPUT -> PROGRAM -> OUTPUT**

- We use Decimal (Base10) to represent numbers, and thus data 
- Computers use two digits (Binary) to represent all data 
- Binary uses 0s and 1s 
- These are called bits (BInary digITS)
- Computers use electricity to charge, which in turn can represent the two binary states of digits 
- The Os and 1s can be thought of as On and Off
- Electrical charge can represent 1, and the missing charge can represent 0 
- Two bits can count 1 number 
- Three bits can go up to 8 numbers i.e 2(3). *Please note that while mathematically there are 8 possibilities here, the computer begins counting with 0(zero), which leads to **7** permutations*
- Transistors in chips represent the state of being On and Off, 1 or 0 
- Consider the decimal system 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 
    - A number such as 123 
    - 3 here is the unit 10(0) to 10 to power 0
    - 2 here is the 10s 10(1) which is 10 to power 1 
    - 1 here is 100s or 10(2) which is 10 to power 2 
    - In the above case, we are using the Base10(Decimal) to represent the idea of 123 
    - Base10 because the 0-9 in the decimal system is 10 digits; Base2 because 0-1 in binary is two numbers 
    - Computers have only Base2(Binary) to represent the same number of 123. How would it do that? We learnt that represent 123 in Base10 requires us to think of powers of 10 - i.e. 10(0), 10(1) and so. 
    - In the same vein as above, the number of 123 can be represented with Base2 using powers of 2 i.e. 2(0), 2(1), 2(2)


*Table1* **A COMPARISON BETWEEN BINARY AND DECIMAL** 

|  2(2)    |  2(1)  | 2(0)  |   | 10(2)  | 10(1)  | 10(0)  |
| -------- | ------ | ----- |   | -----  | -----  | ----   |
|   4      |   2    |   1   |   |  1     |  2     | 3      |


- What does 110010 represent in the decimal system? 50 
- How does a computer represent letters of an alphabet? 
    - We can assign alphabets to number. Capital 'A' is 65 which in turn becomes 010000001
    - Thus 65 in any computational context is the same i.e 65 
    - This is the ASCII standard 
    - ASCII does allow for punctuation, lower case letter, etc., 
    - 72, 73, & 33 represent *Hi!* 
    - Refer ASCIIchart.com 
    - *Hi!* therefore can be represented as binary in the following way **010010000 01001001 00100001**
    - Computers today 8 bits. Which means for the message *Hi!* uses 24 bits
    - We classify each 8 bits as a **byte** 
    - Therefore, how many symbols or characters can be represented with 8 bits? The answer is **256** because each bit has two possible states (0 or 1), which with 8 bits means 2(8), the answer for which is 256 (i.e. it is 2x2x2x2x2x2x2x2)
    - **255** in the above example would be the *highest* number in the above example as, again, the computer begins counting from 0 
- Why is ASCII and the US Keyboard Layout not enough? *Because the US keyboard doesn't represent accents and other important characters that are part of other languages?*
- Why is 256 total possibilities not enough? *Because ASCII can't represent some languages that have more than 256 permutations.* 
- In addition, emojis exist, which also require representation in binary form 
- **Unicode** tries to be a universal system that bridges binary representation to the ability to represent all languages, not just US-English 
- How does represent colours, and eventually images? 
- For colours, the same logic of assigning numbers to letters applies here to colours; we represent colours with numbers such as RGB, HEX, etc., 
- **RGB**, the colour system that we defined in the early part of the 18th century after Newton's prism, uses numbers to represent colour 
- Look at these numbers we saw earlier: **72 73 33** was *Hi!* earlier, but in the context of RGB, the 72 73 33 represent *some amount of red, some amount of green, and some amount of blue*
- Now if you cast our minds to the earlier part of the lecture where we said that there were 256 possible permutations (with 255 being the highest possible permutation), we can state that each of the digits representing the RGB colours can have 255 possibilities. Thus **R** can have numbers of *0-255 representing the different shades of red*, **G** can have *0-255 possibilities of green,* and **B** can have *0-255 shades of blue* 
- Thus from these humble bits, we extrapolate images to dots > pixels > and grids, and resolutions 
- In this same vein, how might we represent video data using Bits? 
- The above 72 73 33 is a yellow emoji of the tears of joy
- Thus when we receive an emoji, it is the computer receiving a random decimal number - in this case, 128,514 - which it converts to binary. This is the case for all data, as all data is mapped to a binary data 
- David Malan: "when it's being displayed on the screen, is the result of the computer interpreting-- the 128,514 value is knowing oh, that's the emoji with the face of tears of joy. But when it comes to displaying the information on your screen, now your computer is going to be using different patterns of bits to control the colors of the dots on the screen."
- The displaying of ths information on screen using a different pattern of bits to control colors of the dots is called **Pixels**
- Zoom heavily into low resolution of images and chances are you will see these pixels, in what is called *pixelation*
- The resolution of an image is just how many pixels or dots there are horizontally and vertically. 
- Therefore it can be said that each dot is using *24 bits or 3 bytes* 
- e photographs you and I take and the images you and I download from the internet are typically measured not even in bytes, per se, but in kilobytes, for thousands of bytes, or megabytes for millions of bytes, or if it's a video file, it might get even bigger, billions, or gigabytes. But that's all that is happening underneath the hood. We're just representing information in this way.
- Now let's turn to videos. How might videos be represented using the logic that we discussed for numbers, text and images? 
- A video is a series of images being rendered a n times per second 
- Music could be represented where frequencies are represented via numbers while another number would represent the duration of that note (or frequency)
- File extensions are basically represent a whole bunch of humans agreeing how to store patterns of zeros and ones in a file so that when those zeros and ones are loaded into a computer for display or for interpretation, it knows what those patterns represent. Images are represented slightly differently, sound and video are represented slightly differently, but it's all zeros and ones at the end of the day
- By agreeing to the patterns of 1s and 0s and how they represent different types of data, we can use this to input something into the computer so that we can have an output 
- Now that we have established the basis upon which computers represent different kinds of data that we input in order to get an output, we have to now consider what happens in the process between Input and Output
- This is the black box into which computer problems solving happens 
- *Algorithms* are essentially step by step instructions and they've been used by humans for many applications prior to the introduction of computers 
- Examples of algorithms include cooking instructions, but these algorithms that we use outside the context of computers have room for ambiguity while the algorithms we ask computers to perform can have **no room for ambiguity** 
- Precision is important in computer science 
- The onus therefore is on humans to increase precision and decrease ambiguity
- This can be demonstrated using the contacts on our phones 
- If we consider the traditional equivalent of a contact app -i.e. the yellow pages - how might we find the number of someone named David? 
- One answer is to go page at a time - while this is correct, it isn't efficient 
- This tension between correctness of an algorithm and its efficiency are constant in solving computational problems - some algorithms are slower and less efficient than others, even if they are, for all intents and purposes, correct 
- Another approach to the scouring the yellow pages is to go two pages at a time, but this solution will result in another problem: the probability of skipping your name while going n pages/turn. 
- This above example is what computer science is referred to as a *bug*
- Another way to solve the above yellow page problem is to divide up the full stack of data - if we are looking for a David, for instance, we can go to the middle of the yellow pages, at which point we know that the answer **WON'T** be after M; therefore we can ignore all entries after M
- Now we have only 50% of the problem to look at in order to solve the problem 
- The same logic through which we removed 50% of the starting dataset is used here for the remaining 50%. 
- With remaining data set, we again go to the middle point at which point we ask, again, where the letter D would be in relation to the middle of this new dataset. 
- The 50% of this new dataset that *doesn't* include D can once again be discarded 
- This process can be continued until you arrive at a dataset that is narrowed down to where D is 
- We did this by discarding all irrelevant data 
- This way is way more efficient 
- This third algorithms is also correct AND efficient 
- This can be represented via the graph below: 

![image-20210523163217543](image-20210523163217543.png)
*Diagram 1: Problem solving, efficiency* A

- The graph above shows each of the methods and their respective times to solve the problem. 
- Method 1 and 2, represented by the red and yellow, lines show that as the dataset increases in size, as does the time taken
- Specifically method 1 has a **one-to-one** relationship with the number of pages; as the number of pages increase, as does time. The implication is that this algorithm won't scale well as datasets increase 
- Method 2 has a similar relationship though it is technically more efficient. But every time a page is added to the dataset, it will add one more step, and thus time 

![image-20210523164459141](image-20210523164459141.png)

- Now consider Method 3. In here, the time taken to solve the problem doesn't rise as the size of the problem increases
- We can consider the lines representing the three methods mathematically. 
    - The red line representing the first method is represented by the letter *n*, since this has a one to one relationship with the dataset (or the number of pages in this case) then the time taken will be in direct relation to the number of pages 
    - The yellow line representing the second method (whereby we jump two pages at a time) shows that time can be divided in half i.e. if *n* represented the number of pages, then n/2 entails that we will finish the problem in half the time compared to method 1 
    - Finally the green line  as a logarithm with a base of 2. And this just means that this graph, the green line describes how much time it takes to solve a problem when on each pass, on each step, you are dividing the problem, in this case, by half. The other two algorithms are taking one or two bites out of the problem. The third algorithm was taking half of the whole problem at a time. And that's what made it all the more powerful. 
- Programming is the act of translating these algorithms into code, or pseudocode 
- Pseudocode is in a language you understand. It is precise and has no space for ambiguity 
- Let's consider the pseudocode that you would write to solve a problem such as the one above 
  
    > Step 1 Pick up phone book 
    > Step 2 Go to middle of book 
    > Step 3 If person = David
    > Step 4 Then which half of the book does it fall into 
    > Step 5 Look in the appropriate half of the book until 
    > Step 6 Person = David 
- The above pseudocode can be repeated as the scale of the book (i.e. dataset)
- Now consider the sequence of the pseudo code again 
    > **Pick up** phone book 
    > **Open to** middle of the phone book 
    > **Look at** page 
    > **if Person** is on page 
        > **Call** Person 
    > **Else If** person is earlier in the book 
        > **Open** to middle of left half of the book 
        > Repeat **Look at**
    > **Else if** person is later in book 
        > **Open to** middle of right half of the book 
        > Repeat **Look at** 
   > Else 
       > **Quit** 

- The text in bold above (verbs) are an essential concept in programming called **FUNCTIONS**
- While the text that is bold (but not verbs) such as **IF** and **ELSE IF** are *conditions 
- The text following the condition is called **BOOLEAN EXPRESSIONS** 
- Boolean expression is a question that has to be answered either a yes or a no (or 1 or 0)
- Finally the line to **REPEAT** is an instruction to repeat the earlier instruction until the computation objective has been reached; this serves to reduce code length and promotes economy of coding 
- This lesson will focus on touching on these concepts using *SCRATCH* Programming language 
- We will go from a graphical programming language to a more text, traditional programming **C** 
- Scratch will allow us to learn these concepts to scratch
- Using Scratch, we can graphically represent the fundamental idea of computer science which is **INPUT** >> **ALGORITHM**  >> **OUTPUT** 
- In our example on Scratch we asked the Cat to Say hello, and ask for the name. 
- Once that name is *INPUT* then the cat uses that input to send a personalized greeting to the user 
- This idea shows a fundamental use of function - i.e. the output of function (in this case, asking for the user's name) can become input to another function (which is sending a personalized greeting) 
- In the above case, there are two functions: *ASKING* for user name, and *SENDING PERSONALIZED GREETING* where the output of one function is the input of another function 
- Graphically this would be *HELLO* & *ANSWER* [both inputs] **JOIN** [the algorithm]   *HELLO*, *<ANSWER>* [both outputs, but *ANSWER* is in brackets because it was a variable user input of the first function]
- Nesting functions is essentially taking inputs and generating outputs 
- Scratch also has graphical elements to represent loops - in our example, we made the cat meow three times by using the **repeat** condition i.e. meow 10 times. Even graphically, the use of the loop reduced the number of blocks we had to employ, which means that it results in economical code 
- In revisiting the second iteration of the above example where we had the cat meow three times, and then reduced the lines of code by using a loop until a certain condition is met. 
- We can further economize the code above by considering another fundamental idea in programming, which is **ABSTRACTION**[^1]: 
           > *Its main goal is to handle complexity by hiding unnecessary details from the user. That enables the user to implement more complex logic on top of the provided abstraction without understanding or even thinking about all the hidden complexity.*

- Abstraction has the advantage of allowing us to reuse code because the implementation has already been done, and doesn't concern the program we are trying to write. 


#### ASSIGNMENT 

It???s time to choose your own adventure! Your assignment, quite simply, is to implement in Scratch any project of your choice, be it an interactive story, game, animation, or anything else, subject only to the following requirements:

     + Your project must have at least two sprites, at least one of which must resemble something other than a cat.
     + Your project must have at least three scripts total (i.e., not necessarily three per sprite).
     + Your project must use at least one condition.
     + Your project must use at least one loop.
     + Your project must use at least one variable.
     + Your project must use at least one sound.
     + Your project should be more complex than most of those demonstrated in lecture (many of which, though instructive, were quite short) but it can be less complex than Ivy???s Hardest Game. As such, your project should probably use a few dozen puzzle pieces overall.



**QUOTE FROM DAVID MALAN**
> *So an algorithm, step by step instructions, a function is the computer's implementation of an algorithm.*

[^1]:  https://stackify.com/oop-concept-abstraction/ 
