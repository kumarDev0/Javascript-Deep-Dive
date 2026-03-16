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





