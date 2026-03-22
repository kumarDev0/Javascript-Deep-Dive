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





