# CHAPTER 2 // DAY 2

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Explain why we wouldn't call changeGreeting in a script.**

ChangeGreeting is making a modification to the data on-chain. Scripts are intended for reading _in_ data, whereas transactions are used in actually modifying data.

**2. What does the AuthAccount mean in the prepare phase of the transaction?**

`AuthAccount` is indicative of who will be signing the transaction (and is defined using an Account Number). This is used in the prepare phase to allow the transaction to access data in your account, and make the changes laid out in the code.

**3. What is the difference between the prepare phase and the execute phase in the transaction?**

Functionally, you _could_ perform the entire transaction from within the prepare phase, _but_ separating the phases is helpful in laying out the logic of the transaction code. Anything that's performed to access data in someone's account happens in the `prepare` phase, whereas actual modifications to that data are performed in the `execute` phase.

**4. This is the hardest quest so far, so if it takes you some time, do not worry! I can help you in the Discord if you have questions.**

-**a. Add two new things inside your contract:**

--**i. A variable named myNumber that has type Int (set it to 0 when the contract is deployed)**

--**ii. A function named updateMyNumber that takes in a new number named newNumber as a parameter that has type Int and updates myNumber to be newNumber**

-**b. Add a script that reads myNumber from the contract****

-**c. Add a transaction that takes in a parameter named myNewNumber and passes it into the updateMyNumber function. Verify that your number changed by running the script again.**
