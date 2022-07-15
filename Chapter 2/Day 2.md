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

<img width="1508" alt="Screen Shot 2022-07-15 at 12 56 24 AM" src="https://user-images.githubusercontent.com/92488787/179179076-3dc580b0-74eb-44d8-9e12-147aa3eb22ae.png">

-**b. Add a script that reads myNumber from the contract****

<img width="1512" alt="Screen Shot 2022-07-15 at 12 57 17 AM" src="https://user-images.githubusercontent.com/92488787/179179223-6345d0c9-ab7d-42af-afb4-0d282e6fd7c1.png">

-**c. Add a transaction that takes in a parameter named myNewNumber and passes it into the updateMyNumber function. Verify that your number changed by running the script again.**

<img width="1512" alt="Screen Shot 2022-07-15 at 1 00 16 AM" src="https://user-images.githubusercontent.com/92488787/179179854-df61ec6e-2b6b-45ed-99f7-4fdff1751ac0.png">

<img width="1512" alt="Screen Shot 2022-07-15 at 1 00 29 AM" src="https://user-images.githubusercontent.com/92488787/179179874-10cc7e57-6ccd-4fd2-97a7-9ceb8d46c0c3.png">
