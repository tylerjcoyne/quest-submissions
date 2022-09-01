# CHAPTER 5 // DAY 1

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Describe what an event is, and why it might be useful to a client.**

An "Event" helps broadcast that something has happened to the world outside your code. It's helpful because instead of checking to see if a variable has changed in the contract (e.g. TotalSupply), we can much more simply look to see if an Event has been triggered. This is useful simply for understand the effects of a contract/transaction, but also because we can use Events to implement other things (e.g. updating a site's secondary marketplace-counter every time an NFT "sell" transaction (Event) occurs after the initial mint).

**2. Deploy a contract with an event in it, and emit the event somewhere else in the contract indicating that it happened.**

![Screen Shot 2022-09-01 at 2 13 55 PM](https://user-images.githubusercontent.com/92488787/188014221-d5f29c0f-5461-4dab-b19e-fd4bf31b30dd.png)

**3. Using the contract in step 2), add some pre conditions and post conditions to your contract to get used to writing them out.**

![Screen Shot 2022-09-01 at 2 16 05 PM](https://user-images.githubusercontent.com/92488787/188014529-1716614e-ac82-462d-aed5-f582560b5cfc.png)

**4. For each of the functions below (numberOne, numberTwo, numberThree), follow the instructions.**

- **numberOne**: Yes, it will log because the "name" var meets the condition of needing to be exactly 5 characters in length.
- **numberTwo**: Yes, this will also log, because the length of the name **is** longer than 0 characters before the function executes, and the output **is** equal to "Jacob Tucker" exactly.
- **numberThree**: No, this will **not** log the updated number because the output doesn't meet the condition of being the original number + 1 (the original number is instead equal to the original number **- 1**. The value of self.number after this is run is therefore still 0, because the state didn't change.
