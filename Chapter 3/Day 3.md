# CHAPTER 3 // DAY 3

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Define your own contract that stores a dictionary of resources. Add a function to get a reference to one of the resources in the dictionary.**

<img width="1512" alt="Screen Shot 2022-07-24 at 3 02 21 PM" src="https://user-images.githubusercontent.com/92488787/180667623-e7a2af18-5dee-4e61-bdbf-01daedc61d37.png">

**2. Create a script that reads information from that resource using the reference from the function you defined in part 1.**

<img width="1512" alt="Screen Shot 2022-07-24 at 3 04 04 PM" src="https://user-images.githubusercontent.com/92488787/180667624-34260ce6-07f3-44e9-9c70-df835390f4eb.png">

**3. Explain, in your own words, why references can be useful in Cadence.**

One reason that references are useful in Cadence because, as we discussed earlier in the chapter, Resources by-design are very difficult to work with, and have to be **moved** in order to view their contents. The beauty of references is that they allow us to peek into a Resource from any transaction/script without having to actually move the Resource around. More broadly, references are useful for this reason: because they allow us to interact with a piece of data that we may not have direct access to.
