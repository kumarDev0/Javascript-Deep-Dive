Hello Guy's All Closure Project Here 
```
Project - 1 (Basic Banking Account System)
Logics : Requirement :
   - account create 
   - private balance
   - deposite
   - withdraw
   - check balance
---------------------------------------------
```
```javascript

function createAccount(name) {
    console.log('Your Name : ', name)
    let balance = 10000;


    function deposite(amount) {
        balance += amount;
        console.log('Your Amount is deposite successfuly : ', amount)
    }
    function withdraw(amount) {
        if (amount < balance) {
            balance -= amount;
            console.log('Your Amount is Withdraw Successfully : ', amount)

        } else {
            console.log('Insufficient Fund')
        }
    }
    function checkBalance() {
        console.log('Your Current Balance is : ', balance)
    }

    return {
        deposite,
        withdraw,
        checkBalance

    };
}

const user1 = createAccount('Raaz') // closure 1 for user 1
// user1.deposite(2000);
// user1.withdraw(4000)
user1.checkBalance()
user1.withdraw(5000)
user1.checkBalance()
user1.deposite(2000)
user1.checkBalance()

const user2 = createAccount('kumarDev') // closure 2 for user2

```
-----------------------------------------------------------

```
Project 2 - (Level Upgrade - Real Banking System )
 Logics :
    - every Transaction shoude be saved
    - transation = [] 
    - deposite -> push into transation
    - withdra -> push into transation
-------------------------------------------------------
```
```javascript
function createBanking(name) {
    let balance = 10000;
    let transaction = []

    function deposite(amount) {
        balance += amount;
        transaction.push(`Deposite Successfuly : ${amount} username : ${name}`)
        // checking for 
        console.log('Deposite successfuly : ', amount)
    }
    function withdraw(amount) {
        if (amount < balance) {
            balance -= amount;
            transaction.push(`Withdraw Successfully : ${amount} username : ${name}`)
            // checking
            console.log('Withdraw successfully : ', amount)

        } else {

            transaction.push(`Withdraw is Failed : ${amount} username : ${name}`)
            // checking For
            console.log(`Withdraw is Failed : ${amount} Because your Current balance is : ${balance}`)

        }
    }

    function checkBalance() {
        transaction.push(`Balance Enquery : ${balance} username : ${name}`)
        // Checking For
        console.log('Your Current Blance : ', balance)
    }

    function history() {
        console.log('Transation History : ', transaction)
    }

    return {
        deposite,
        withdraw,
        checkBalance,
        history

    };

}

const user1 = createBanking('Raaz chourasia') // create closure 1 have differnt memory
user1.checkBalance()
user1.deposite(3000)
user1.checkBalance()
user1.withdraw(10000)
user1.checkBalance()
user1.withdraw(5000)
user1.checkBalance()
user1.history()
const user2 = createBanking('KumarDev') // create closure 2 have different memory

```
-------------------------------------------------------------------------

```
Project - 3 => Loan System (Advance) 
 * Features :- 
    - user Loan le skta hai
    - loan track hoga.
    * Logics :-
    -loan = 0
    -takeLoan -> loan +=amount
    -repayloan -> loan -=amount
- Hey Guy's in this project loose my focuse ,I have to try to give best, you can fix propery then comment

```
```javascript

function loanSystem(name) {
    console.log('welcome to MkLoan - > ', name)

    let userLoan = []
    let MainLoanBalance = 1000000
    let trackRepayment = []
    let trackLoan = []
    let userLoanAmount1
    let userLoanAmount2
    let userLoanAmount3

    function takeLoan(age, salary, amount) {

        if ((age >= 20 && age < 50) && salary > 20000) {
            console.log('Welcome Mr : ', name)
            console.log('Your are Eligible for loan (30k to 50k)')

            if (userLoan >= 30000 || userLoan <= 50000) {
                userLoanAmount1 = MainLoanBalance -= amount
                console.log(`Your Loan is Approved : ${userLoanAmount1} of Mr ${name}`)
                trackLoan.push(`Approved Amount  : ${userLoanAmount1} of Mr ${name}`)

            } else {
                console.log('Please Enter Valid Amount')
            }
        }
        else if ((age >= 20 && age < 50) && salary > 40000) {
            console.log('Welcome Mr : ', name)
            console.log('You are Eligible For Mediam level loan (1lakh to 3lakh)')

            if (userLoan >= 40000 || userLoan <= 80000) {
                userLoanAmount2 = MainLoanBalance -= amount
                console.log(`Your Loan is Approved : ${userLoanAmount2} of Mr ${name}`)
                trackLoan.push(`Approved Amount : ${userLoanAmount2} of Mr ${name}`)

            } else {
                console.log('Please Enter Valid Amount ')
            }

        }
        else if ((age >= 20 && age < 50) && salary >= 80000) {
            console.log('Welcome mr : ', name)
            console.log('You are Eligible for Higher Loan : (5lakh to 10lakh)')

            if (userLoan >= 100000) {
                userLoanAmount3 = MainLoanBalance -= amount
                console.log(`Your Loan is Approved : ${userLoanAmount3} of Mr ${name}`)
                trackLoan.push(`Approved Amount : ${userLoanAmount3} of Mr ${name}`)

            } else {
                console.log('Please Enter Valid Amount')
            }
        } else {
            console.log('You not Eligible Plese Try Next Time : ', name)
        }

    }


    function repayLoan(amount) {

        if (amount >= 3000) {

            if (userLoanAmount1 < userLoanAmount2) {
                userLoanAmount1 -= amount
                console.log(`Your Emi id done : ${amount} And Remaining Amount is : ${userLoanAmount1} Thank you : ${name}`)
                trackRepayment.push(`EMi Repayment : ${amount} and Remaining Amount : ${userLoanAmount1} of Username : ${name}`)

            } else {
                console.log('User Invalid')
            }
        }

        else if (amount >= 5000) {
            if (userLoanAmount2 < userLoanAmount3) {
                userLoanAmount2 -= amount
                console.log(`You Emi is Done : ${amount} And Remaining Amount is : ${userLoanAmount2} Thank you : ${name}`)
                trackRepayment.push(`EMI Repayment : ${amount} and Remaining Amount : ${userLoanAmount2} of Username : ${name}`)

            } else {
                console.log('User Invalid')
            }

        }
        else if (amount >= 10000) {
            if (userLoanAmount3 > (userLoanAmount1 && userLoanAmount2)) {
                userLoanAmount3 -= amount
                console.log(`You Emi is Done : ${amount} And Remaining Amount is : ${userLoanAmount3} Thank you : ${name}`)
                trackRepayment.push(`EMI Repayment : ${amount} and Remaining Amount : ${userLoanAmount3} of Username : ${name}`)
            } else {
                console.log('User Invalid')
            }
        } else {
            console.log('Please Inter Valid Amount shoud be 3000 and more')
        }


    }

    function loanTrackerHistory() {
        console.log("Loan Tracker History : ", trackLoan)

    }

    function loanRepaymentHistory() {
        console.log('Loan Repayment History : ', trackRepayment)
    }

    return {
        takeLoan,
        repayLoan,
        loanTrackerHistory,
        loanRepaymentHistory

    };
}

const user1 = loanSystem('Raaz')
user1.takeLoan(20, 22000, 40000)

```









