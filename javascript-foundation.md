hey guy's i am sharing javaScript-foundation deep into dive (50% learning journey share)
====================================================================================================

(1) .History Of javaSCript
(2) .What is javascript
(3) .Why we need of javascript

================================================================
first we understand History of javascript then we know what and why
-> in 1990 there are one web browser availble in the markete that (NetScap) the founder of Netscap mark Anderson
netscap web browser which is used to dominate the world in 90's with the market share of around 90%.

->this is where the history of javascript start from 
in that time how much website are present was statics website 
this is the problem beacause the static website can not perform a dynamic tast in the sence of dyanamic that is can not able to 
perform a operation like calculator and some mathematical operation and some logical operation 

how to works stactic website in that time -( [Server] ------ > [Browser] ) multiple html files are kept on the server , any users
open the browser(Netscap) search the content on the serach bar like a google search then what heppend (Server) respond with html
file , server kept html then resopone an html , the html files can not able to perform a logical and  methamtical task because html are plane a text and images that it 

Now, 
->netscap in 1995 so, the founder of Netscap obserb the problem to Decide to Develop Programming language for his Netscap
mark anderson hire a software Engineer to develop a Programming language for NetScap That person is ---- 'Brendan Eich'
are developing programming language start, he develop the whole new Language in just 10 freaking days 
the language is called (Mocha) then it is changed into (LiveScript) then finaly changed (JavaScript). Brendan Eich is the Creator of javascrip

Law : - in 2007 Jeff Atwood give a law "Any Application that can be Written in javascript" it Atwood's Law
now 2026 Why we need Javascript is true - in the java script create webapplication , mobileApplication, DesktopApplication, Gaming Application even Ai Application , the jeff Atwood statement are true in this time javascript capture almost 96% of market


Now Back to Story Again -> 
when was running the javascript in NetScap Billgates has a InternetExplorer Browser in this browser not any programming language 
then Billgate apply the reverse enginnering to extract using javascript to become a (JSCript) it was runnig on the enternet Explorar , the the NetScap founder was franstating mark Andersong go to the ECMA -(Europian computer manufacture Assocaition)
reveel the probles billgats use the reverse engineering to extract my javascript language to build new Jscript for Owen browser
please to set Standarication , all query are listen carefully by ECMA then provide the Standarition of the javascript , in this time we all knows ECMA SCript is nothing it is a Standaritation of javascrip then Adaopt all browser javascript

---- now , Entry the Chrome in the market in (2008) the market is reflect 90 degree suddanly, chrome is deminant to capture the whole market why , because in the chrome browser inbuilt a V8 Enging that Engine are Very fast as compare to NetScape
now come to the Firefox in the firefox javascript engine --- Spidermonkey it is less fast as compare to javascript V8 Engine
that is the resone chrome is more popular Browser.


now , Everything is all right but after 1 Years (2009) one software engineer to take a javascript V8 Engin and put the engine into different software that is born a (Node.JS) and same javascript runnig on the server side out from the browser as a act of node.js that person is 'Ryan Dohl' 

IT all the Intresting History .
============================================================

Hey, Dude Programming is start in javascript
================================================================
let's understand let,const varibles 
======================
using let variable -> a let varible is a dynamic in the sence change the original value assign into new value again and again.

examole:(1) (Let Variable)
let x = 20
console.log(x) - > output is (20)
now, x = 50 // again assign 
consolo.log(x) -> now the original value is changed output is (50)
now, x = 70 // again assign -> output (70)
rule remember let variable can changed. any where 

example:(2) (Const Variable)
const x = 20
cosnole.log(x) // ouput is 20 perfect
but,
we are assigning again 
x = 30
console.log(x) // Error (Can not Assign to Const Variable)
ruel remember : Const variable can not change (Only for primitive datatype) , (for non-primitive you can change)

What will Happend in memory :-
in javascript there are two type of memory (Stack Area) (Heap Area)

visualize the memory in case of (Let Variable)

==============
| Stack Area |   All primitive value store in stack area link (let x = 20) take address @764388 like this if you assign again to the x then change the value only address will be same , same as the const case but not Assign Again
==============

=============
| Heap Area  |  isko hum aage dekhenge 
=============

// const and let variable concept is end here................


@ Primitive DataType in javascript Start here..........
theory : 
primitive data type is just a standard name behind the scene variable memory address

/ ***now perform a Practicle to understand primitive data types ***/
``` javascript
let x = 10 // (javascript v8 engine see 10 is a number then it will consider as a -> number datatype)
let age = 20 // (same it is number datatype)
let name = 'KumarDev' // (now, javascript v8 engine see 'KumarDev' , v8 engine it will consider as String datatype)
let isTrue = false // (javascript v8 engine it will consider as boolean type )
let piValue = 3.1415 // (javascript v8 engine it will consider as number)
let x ''  // (It is empty string , javascript v8 engin it will conside as string)
let x   // (javascript consider as undefined)
```

if you want check the which type of value and variables --> (typeOf(variabl-name)) it is return the type

(x , age, name, isTrue,   ) it is just a variable address in memory of  javascript
---------------------------
note. "Javascript does not allocate memory by itself"
- Memory Allocated by the operating System , and javascript use the allocated memory and manage it .
- The Reality is more deeper (Etna dimag me rakhana)

===================================================================================== End ....
@ (Dialog Box in javascript )
=================================
there are three type :
1.Alert()
2.Confirm()
3.Prompt()
therse are browser Dialoge Function it is used to intract the user to take some inputs and display some messages

alert()--- it is used to display the message 
``` javascript
const displayMessage = alert('Welcome to the profile page') // like this
```
Confirrm() --- it is used for desition yes/no and return the boolean value
```javascript
const isConfirm = confirm('Are you sure to terminate your programs') // user click (yes) - true / (no) false
if (isConfirm){
console.log('Program is terminated successfully')
}
```
prompt() --- it is used to take some input from user 
``` javascript
const userName = prompt('Enter your user name')
const userPassword = prompt('Enter a password')
console.log(userName , userPassword)
```
note:. iska use isse bhi jada hai isme condition bhi laga skte hai isko kahi bhi use kar skte hai
avi ke liye etna hi jaise jaise hum aage jaenge iska use aapko dekhne ko milega .

======================================= End............

------------------------------------------------
@ Template Literals | String Methods and Property
---------------------------------------------------
template literas : it is modern way of javascript to write an string is called templete literals 
- insert the variable and expression directly into the string
- it is used to make a dynamic and readable that's it
- template literals use by backtik (``)
- systex ${} -> in the curly blackets we insert variable and expression
- ${} enven you can many thing pass into the bracket
--------------${}---------------
           - Variables
           - math calculation
           - function call
           - boolean Expression
           - object Property
           - Ternary operator
  ------------------------------------

better understanding with example : (Different different way )

```javascript
const firstName = 'kumar'
cosnt lastName = 'Dev'
const age = 25
cosnole.log(`my first name is : ${firstName} `)
console.log(`my last name is : ${lastName}`)
console.log(`and , i am ${age} years old`)
```
...........................
output = 
my first name is kumar
my last name is Dev
and, i am 25 years old
............................

// second Example:

```javascript
const firstName = 'kumar'
cosnt lastName = 'Dev'
const age = 25
const userMessage = `firstname : ${firstName} lastname : ${lastName}and , i am ${age} years old`
console.log(userMessage)
```
........................................................
Output = 
firstname : Kumar lastname : Dev and, i am 25 years old.
.........................................................

// Third Example 

``` javascript
const x = 10
const y = 20
console.log(`The sum of a+b = ${x+y}`)
```
......................
output = 
the sum of a+b = 30
......................

// Old method in javascript (String)
```javascript
const name = 'Kuamr'
const age = 25
const address = 'Bihar'
cosnt myDetails = 'My name is : ' + name + ' and, i am ' + age + ' years old. and i am belong to ' + address
console.log(myDetails)
```
...................................................................
output = 
my name is : Kumar and, i am 25 years old and i an belong to bihar
....................................................................

note. (Remembar)
now you can see the difference which one is best to use modern ya old method you can pick any one code is same and output is same but writing a code in old method time consuming and not readable  

now you can explore the string Method 
-toUppercase()
-toLowercase()
-trim()
-trimEnd()
-trimStart()
-include()
-slice()
-splite()
-lenght // it is propert not a method
-replace()

---------------------------------------------------- End 







