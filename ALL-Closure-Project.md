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






