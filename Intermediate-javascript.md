Welcome to intermidiat javascript (50%) + privious (50%) of javascripfoundation
------------------------------------------------------------------------------------
i am sharing each and every concept with easy expalnation and example or output 
................................................................................
Let's Start here 

--------------------------------------------------------------
# Primitive datatype vs non-primitive datatype in javascript
--------------------------------------------------------------
```
first you need to understand (mutalble , mutation , immutable)
1.
- mutable : all non-Primitive dataType in javascript is mutable (array , object ,Function)
- Defination : mutable means change and modify the original value of variable is called mutable
- always remember :  array is an act of object in javascript and function bhi internally ye ek object hi hota hai

2.
-immutable : all primitive datatype is immutable in javascript you can not able to change and modify original value
-mutation : means take a action to modify the original value ,when you write the code is called mutation.
```

```
hey guy's mian yaha se function and memory dekhne ja rha hu previous ko cover karenge baad me

```

```javascript

// ? scope in javascript

const username = 'deepak' // here is the declare const varible which is store in script scope that is global
let userage = 25 // here is the declare let let varibale which is store in script scope in the chrome devtool and that's also a global
var userCity = 'Mumbai'// here is the declare var which is strore inside a Global scope in chrome devtool that's also a global varibale and you can say global context ya global window
console.log(userCity) // * original value (mumbai) lekin maine function me ye vrible ka value alag hai jake dekho 

function userDetails3() {

    user1 = 'i love that my pains'
    console.log(user1)

    console.log(user1) // give an undefined because it hoist varibel
    // console.log(user2)// user2 is not define error 
    // console.log(user3)// ye line ko check hi nhi krega kyuki privious line me error toh next line pe jane ka matlab nhi banta hai
}

userDetails3()

user1 = 'i love you very much ...'
console.log(user1)

// console.log(user1 + ' of rajaram') // * the varibale is hoist , assign the undefind - ouput(undefined of rajaram)


// * create a block , block means loop ka block condition if else ka block 
{
    //? block ka scope local hoga ya global
    var user1 = 'raam'
    let user2 = 'mohan'
    const user3 = 'rani'
    console.log(user1)
    console.log(user2)
    console.log(user3)

}

//* can i access the block var varible outside of this block , can i access inside of a function or not let's try and see what happening


console.log(user1) // we can access var varible which is declare inside a block 
// user1 = user1 + 'ayan' // * yes you can assign 
// console.log(user1)


// *can i access the block let varible outside of this block , can i access or not , and can i access inside of a function or not let's try and see what happening


// console.log(user2) // Error : user2 is not define , you can not access outside from the block
user2 = 'monjolika' // * Assign new value in user2 which is define inside a block why, the line no 30 give an error when we try to access but the line is 31 not giving an error why?.
console.log(user2)

user2 = user2 + 'janeman' // * we are assign again and add janeman Why,
console.log(user2)

//*access the block const variable outside of this block , and also can i aceess a block cost varible inside a function let's see 


// console.log(user3) // giva an error : user3 is not defined , we can not access ouside of block 
user3 = 'mona' //* what happening here mona is assign into user3 which is declare inside a block that const valarible , why and how it's possible
console.log(user3)

user3 = user3 + ' Darling'// * also reAssign Again why and how it's work
console.log(user3)


function userDetails() {
    const username1 = 'raaz chourasia'
    let username2 = 'mausham chourasia'
    var username3 = 'Nandanee ranavat'
    const userAge1 = 26
    const userCity1 = 'Bihar'

    console.log(username1)
    console.log(userAge1)
    console.log(userCity1)

    // i know a function is an object because none primitive datatype is array and object and function and it is mutable always that's means i can modify the original value , it is work and not

    // username1 = 'i love india' // typeError: Assignment to constant varible , why we are not able to assign 
    // console.log(username1)

    // username2 = 'i love ' + username2 // yes you can re-Assign
    // console.log(username2)


    // username3 = 'mohan' // yes you can re-Assign 
    // console.log(username3)


    // * i want to access global varibel in this function

    console.log(username) // yes you can access with const , question can i change the original value of the global varible of const from inside this function yes ya no let's check

    // username = 'Raaz samanee' // Error : Assignment to constant variable , why we can not able to re-Assign the value
    // console.log(username)

    console.log(userage) // yes you can access with let

    // userage = 300 // yes you can change / Re-Assign in the case of let global variable
    // console.log(userage)

    console.log(userCity)// yes you can access with var

    // userCity = 'dehradun' // yse you can change / Re-Assign in case of var
    // console.log(userCity)


    // * i want to Access a block varible here , let's try can I access or not

    console.log(user1) // we can access 
    console.log(user2)// we can access
    console.log(user3) //we can access

    // * can i change original value and modify is this possible or not in the case of var

    // user1 = 'queen' // *we can change 
    // user1 = user1 + 'ayan' // *we can modify aldo
    // console.log(user1)


    // * can i change original value and modify is this possible or not in the case of let

    // user2 = 'i hate you' // *yes we can change the value 
    // console.log(user2)
    // user2 = user2 + ' i love ' //* yes we can also modify 
    // console.log(user2)

    // * can i change original value and modify is this possible or not in the case of const

    // user3 = 'i love you' // * we can assign into the const
    // console.log(user3)
    user3 = user3 + ' I love you'
    console.log(user3)



}
userDetails()
// console.log(username1) // username1 is a const type varibale which is defined in the function that become a local variable it's can not access outside of the function
// console.log(username2) //Refference Error : username2 is not defined why happening occure the error because let type varible declare in a function which can not aceess out side of the function
// console.log(username3) // the error is username3 is not Defined , can not access outside of the function which variable declare inside a function
// * observation : if you declare a varible which type a const and let , var inside a function , we can not able to access the variable outside of the function

function userDetails2() {
    // can I access another function varible it is possible or not 

    // console.log(username1) // you can not access why?
    // console.log(username2) // you can not access why?
    // console.log(username3)// you can not access why 

}
userDetails2()


// *? etna sab maine practice kiya but dev tool me ye sab ho rha hoga

// * - global scope me (var , userDetails,userDetaisl2,userDetails3) 
// * - script scop me (let , const) memory creation phase me undefined store ho gya hoga
// * - Block scope (jisme hamra ) block ke sabhi varible store honge 
// * - when i try to access global varible inside a function then it is called global access even block level bhi global access ke andar aata hai 

```

```
-------------------------------------------
-function vs method
- function declaration
- function expression
- arrow function expression
- (for of loop) and (for in loop)
- i am sharing all pracice code
--------------------------------------------------
```
```javascript
// Practice javascript
// * Function vs method

// 

/*
const math = {
    add: function (a, b) {
        return a + b
    },

    sub: function (a, b) {
        return a - b
    },
    square: function (x) {
        // return x * x
        return x ** 2
    },

    // ES6 me new tarika aaya 
    substract(a, b) {
        return a - b
    },
    cube(num){
        return num ** 3
    }

}

console.log(math.add(10, 20))
console.log(math.sub(20, 30))
console.log(math.square(10))
console.log(substract(10, 2)) // error Substract is not define console me aap direct print kr skte ho okay 


*/


// ? Arrow Function  dekhne se pehle hum 2 function aur dekhnege

// * Function Declaration 

// function cube(num) {
//     return num ** 3
// }

// * function Expresssion

// const cube = function (num) {
//     return num ** 3
// }

// * Arrow Function Expression

// const cube = (num) => {
//     return num ** 3
// }

// * Jab hum Arrow main return nhi krenge fir bhi ye kaam krega kyuki ye implicit return ho rha hai

const cube = (num) => num ** 3 // bilkul easy hai and above function ki tarah same kaam krega 

// * Let's see different different Example

// const sub = (num1, num2) => num1 - num2
// console.log(sub(10, 20)) // output -10

// const squre = (num3) => num3 * num3
// console.log(squre(10, 10))

// const add = (a, b) => a + b
// console.log(add(20, 30))




// ? (For of Loop) and (For in Loop)

// * one think must be remember , array and string are Iterabal object but object is not iterable
// * what is the normal loop how, they itrate of array Let'look

const fruits = ['Mango', 'graphes', 'guava', 'Apple', 'Orange']

// for (let i = 0; i <= fruits.length - 1; i++) {
//     console.log(fruits[i])
// }
// * i am using (for of loop) for Array 
/*
for (const fruit of fruits) {
    // ? console.log(fruit)
    console.log('----------------------------')
    // ? if want to print only orange value from fruits Items then 
    if (fruit === 'Orange') {
        console.log(fruit) // only return oranges 
    }

}

*/

// * i ma using (for of loop) for string
/* 
const str = 'Villan raaz'
for (const it of str) {
    console.log(it)
}

*/

// * i ma usnig (for In loop ) for Object 
const user = {
    username: 'kumarDev',
    userpassword: '9877@VK',
    userAge: 34,
    userMobileNo: 997565325
}

//* Access keys and Value , but performace is bad  
/*
for (const key in user) {
     console.log(key) // only return key not value
    console.log(key, ':', user[key]) // return key and value both 
}

*/

// * Different Way to best performance

/*
const userkey = Object.keys(user) // all keys store in userKey varible
const userValue = Object.values(user) // all value store in uservalue varibel

const userEntities = Object.entries(user) // it return an array in the stroe key and value both
console.log(userEntities)

for (const key of userkey) {
     console.log(key) // only key access
     console.log(user[key]) // only value access of key
    // ? you can set the condition also
    if (user[key] === '34') {
        console.log('userage : ', user[key])
    }


}

*/

```



