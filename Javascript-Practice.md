Java script Practice Topics here :
```
- Function in javascript (various types )
- scope in java script
- block and Lexical Scope and theire memory location
- Hoisting variable
- nested function
- retuen in a function
- higher order function
- call back function
- deep nesting in function
- closure in a function
- closure with callback function
- Event loop with lots of problem
- SetTimeout and SetInterval in javascript
- microtask and macrotask in javascript
- Asynchronous javascript and Synchronous

```
-----------------------------------------------
```
Blend coding practice , futture me aur bhi jada code push karunga yaha par
```

```javascript

// setTimeout and SetInterval


// console.log("Start");

// setTimeout(function () {
//     console.log("Middle");
// }, 0);

// console.log("End");



// * 💻 Coding Task (MUST DO)

// 👉 Task:

// Ek function banao:

// "Loading..." print kare turant

// 2 second baad "Data Loaded" print kare

// 👉 Condition:

// Sirf setTimeout use karna hai

//----------------------------------------



// 💻 Coding Task 2 (Thoda twist)

// 👉 Task:

// Ek program likho:

// Har 1 second me "Running..." print ho

// 5 second baad ye band ho jaye

// 👉 Hint:

// setInterval use hoga

// usko stop bhi karna padega


// * Solution 


// const intervalId = setInterval(function () {
//     console.log("Running...");
// }, 1000);

// setTimeout(function () {
//     clearInterval(intervalId);
//     console.log("Stopped");
// }, 5000);

//------------------------------------------------------


// 💻 Coding Task 3 (Brain Stretch 🚀)

// 👉 Task:

// Ek function likho:

// 1 se 5 tak numbers print kare

// Har number 1 second delay ke baad aaye


// * Solution 

// for (let i = 1; i <= 5; i++) {
//     setTimeout(function () {
//         console.log(i);
//     }, i * 1000);
// }



// 💻 Coding Task (Important Practice)

// 👉 Task:

// Ek program likho:

// "Start" turant print ho

// "Hello" 1 sec baad

// "World" 2 sec baad

// 👉 Condition:

// sirf setTimeout use karna hai

// clean logic likhna (copy paste nahi 😈)


// console.log('Start')
// setTimeout(function () {
//     console.log('Hello')

// }, 1000);
// setTimeout(function () {
//     console.log('World')
// }, 2000);

//--------------------------------------------


// 💻 Task (important)

// 👉 Ek program likho:

// "Start" print ho

// fir 1 sec gap me:

// 1
// 2
// 3

// fir "End" last me aaye

// 👉 Condition:

// setTimeout use karna hai

// loop use karna hai


// * Solution

// console.log('Start')
// for (let i = 1; i <= 3; i++) {
//     setTimeout(function () {
//         console.log(i)

//         if(i === 3){
//             console.log('End')
//         }
//     }, i*1000);
// }

//----------------------------------------------------------

// 💻 Coding Task (Reverse Thinking 🔥)

// 👉 Task:

// Output chahiye:

// 3
// 2
// 1

// 👉 Conditions:

// loop use karo

// setTimeout use karo

// delay logic use karo


// * Solution 

// for(let i = 1; i<=3; i++){
//     setTimeout(function (){
//         console.log(i)
//     }, 3000 - i*1000);
// }


//------------------------------------
// 💻 Final Task (Real-world thinking)

// 👉 Ek program likho:
// "Start" print ho
// "A" aur "B" dono 0 ms delay pe ho
// lekin output me:

// Start
// End
// A
// B

// 👉 Condition:
// sirf setTimeout use karna hai

// * solution

// console.log('Start')
// setTimeout(function () {
//     console.log('A')
// }, 0);
// setTimeout(function () {
//     console.log('B')
// }, 0);
// console.log('End')


//---------------------------------------------

// 💻 Task (Event Loop apply karo)

// 👉 Task:

// Ek program likho:

// "Start" print ho

// "Middle" 0 ms delay pe ho

// "End" last me aaye

// 👉 Expected:

// Start
// End
// Middle

// 👉 Condition:

// setTimeout use karna hai


// * Solution 

// console.log('Start')
// setTimeout(function () {
//     console.log('Middle')
// }, 0);
// console.log('End')

//-----------------------------------------------------
// ? Microtast and Macrotast (Cocept start here)

//----------------------------------------------------

/* 
💻 Task (Brain Stretch 🔥)

👉 Task:

Ek program likho:

"Start" print ho

"A" → Promise se print ho

"B" → setTimeout se print ho

"End" last me aaye (sync)

👉 Expected:

Start
End
A
B

*/
/*
console.log('Start')
Promise.resolve().then(() => console.log('A'));
setTimeout(function () {
    console.log('B')

}, 0);
console.log('End')
*/

//--------------------------------------------------------

/* 

💻 Final Task (Real-world thinking)

👉 Task:

Ek system likho:

"Start" print ho

"Step 1" → Promise se

"Step 2" → setTimeout se

"Step 3" → Promise ke andar se (nested)

👉 Expected:

Start
End
Step 1
Step 3
Step 2


*/

/*
console.log('Start')
Promise.resolve().then(() => {
    console.log('Step1')

    Promise.resolve().then(() => {
        console.log('Step3')
    })
})
setTimeout(function () {
    console.log('Step2')

}, 0);
console.log('End')

*/

// ? Real world use Ansyn 



/*
💻 Practice Task 1

👉 Tum banao:

"Fetching user..." print ho

2 sec baad:

"User found" ya "User not found"

👉 Condition:

random true/false use karo
*/

//* Solution.

/*
console.log('Fetching user...')
setTimeout(function () {
    const user = true
    if (user) {
        console.log('User found')
    } else {
        console.log('User not found')
    }

}, 2000);
*/

// ? questions

/*
let attempts = 0;

function fetchData() {
    attempts++;

    console.log("Trying...", attempts);

    setTimeout(function () {
        const success = Math.random() > 0.7;

        if (success) {
            console.log("Success ✅");
        } else {
            console.log("Failed ❌");

            if (attempts < 3) {
                fetchData(); // retry
            } else {
                console.log("Max attempts reached 🚫");
            }
        }
    }, 1000);
}

fetchData();
*/

//----------------------------------------

/*

💻 Practice Task 2

👉 Tum banao:

max 5 attempts

success hone pe stop

warna "Final Fail"
*/

//* Solution ..

/*
let attempts = 0;

function apiFetch() {
    attempts++;
    console.log('attempt...', attempts);

    const success = Math.random() > 0.8;

    if (success) {
        console.log('Success ✅');
    } else {
        if (attempts < 5) {
            setTimeout(apiFetch, 1000); // retry after delay
        } else {
            console.log('Final Fail ❌');
        }
    }
}

apiFetch();

*/

//---------------------------------
/*   Task 2.
  - Loading... har 1 sec
  - 4 sec baad stop 
  - 'completed'
-------------------------------------
*/

//* Solution 
/*
const id = setInterval(function () {
    console.log(
        'Loading...'
    )
}, 1000);
setTimeout(function () {
    clearInterval(id)
    console.log('Completed')
}, 4000);

*/

//----------------------------------
/*   Task 3 (Fianl thinking taks)
   - Start downloading...
   - Downloading... (repeat)
   - 5 second baad stop
   - downloading complete
*/

// * Solution
/*
console.log('Start Downloading')
const id = setInterval(function () {
    console.log('Downloading...')

}, 1000);

setTimeout(function () {
    clearInterval(id)
    console.log('Downloading Completed')
}, 5000);

*/

// ? Different different Practice 

/*---------------------------------
       Task-1
       👉 Program likho:

"Start" print ho

2 sec baad "Hello"

4 sec baad "World"

👉 Goal:

multiple setTimeout control

---------------------------------
*/
//* Solution

/*
console.log('Start')
setTimeout(function () {
    console.log('Hello')
}, 2000);

setTimeout(function () {
    console.log('World')

}, 4000);
*/
//================================================


/*        Task - 2
------------------------------
     👉 Output chahiye:
3
1
2

👉 Condition:

loop use karo

setTimeout use karo

delay logic se order control karo
------------------------------

*/
/*
Delay Logic codes
3000 - i*1000 = > 2000ms (2sec) =  1
3000 - i*2000 = > 1000ms (1 sec) = 2
3000 - i*3000 = > 0ms (o sec) = 3

*/



// * solution
/*
for (let i = 1; i <= 3; i++) {
    let delay;
    if (i === 3) delay = 0;
    else if (i === 1) delay = 1000;
    else if (i === 2) delay = 2000;

    setTimeout(function () {
        console.log(i)
    }, delay)
}

*/



//===============================================

/*        Task - 3
-----------------------------------------
👉 Program:

"Running..." har 1 sec print ho

exactly 3 baar print hone ke baad stop ho jaye

fir "Stopped" print ho

👉 Goal:

counter + clearInterval
-----------------------------------------
*/

// * Solution
/*
let count = 0
const id = setInterval(function () {
    count++
    console.log('Running...')
    if (count === 3) {
        clearInterval(id)
        console.log('Stoped')
    }

}, 1000);


*/
//-==================================================

/*         💻 Task A (Delay Mastery 🔥)
---------------------------------------------
👉 Output chahiye: (program 1)
2
3
1
👉 Output Chahiye : (program 2)

5
3
4
2
1

👉 Output Chahiye : (Program 3)
4
2
1
3


👉 Condition:

loop use karo

setTimeout

delay logic se control karo
---------------------------------------------

*/

// * Program 1 solution
/*
for (let i = 1; i <= 3; i++) {
    let dealy;
    if (i === 2) dealy = 0;
    else if (i === 3) dealy = 1000;
    else if (i === 1) dealy = 2000;

    setTimeout(function () {
        console.log(i)

    }, dealy);
}

*/





// * Program 2 Solution
/*
for (let i = 1; i <= 5; i++) {
    let delay2;
    if (i === 5) delay2 = 0;
    else if (i === 3) delay2 = 1000;
    else if (i === 4) delay2 = 3000;
    else if (i === 2) delay2 = 4000;
    else if (i === 1) delay2 = 5000;

    setTimeout(function () {
        console.log(i)
    }, delay2);
}
*/

// * Program 3 Solution

/*
for (let i = 1; i <= 4; i++) {
    let delay3;
    if (i === 4) delay3 = 0;
    else if (i === 2) delay3 = 1000;
    else if (i === 1) delay3 = 2000;
    else if (i === 3) delay3 = 3000;

    setTimeout(function () {
        console.log(i)
    }, delay3);
}

*/

//==============================================

/*
------------------------------------------
Task B (Interval + Timeout Combo 🔥)

👉 System:

"Start"

har 1 sec → "Tick"

3 sec baad → "Boom"

Boom ke baad → Tick band
------------------------------------------

*/
// console.log('Start')
// const id = setInterval(function () {
//     console.log('Tick')
// }, 1000);

// setTimeout(function () {

//     console.log('Boom')
//     clearInterval(id)
// }, 3000)/


//=============================================

// console.log("Game Start");

// let score = 0;

// const id = setInterval(function () {
//     score++;
//     console.log("Score:", score);
// }, 1000);

// setTimeout(function () {
//     clearInterval(id);
//     console.log("Game Over");
//     console.log("Final Score:", score);
// }, 5000);


```

