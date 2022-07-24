# CHAPTER 3 // DAY 4

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Explain, in your own words, the 2 things resource interfaces can be used for (we went over both in today's content)**

Resource Interfaces can be used primarily to (A) define the "requirements" for a specific type of Resource (e.g. a resource must have the pre-defined list of variables or functions in order to be initialized), or (B) to restrict the access of a a Resource's contents (e.g. you can make certain variables or functions public, while others remain private).

**2. Define your own contract. Make your own resource interface and a resource that implements the interface. Create 2 functions. In the 1st function, show an example of not restricting the type of the resource and accessing its content. In the 2nd function, show an example of restricting the type of the resource and NOT being able to access its content.**

<img width="1512" alt="Screen Shot 2022-07-24 at 3 25 15 PM" src="https://user-images.githubusercontent.com/92488787/180668211-7f8fc98a-95a2-408f-ac0d-1be0b5212e79.png">

**3. How would we fix this code?**

We can fix this code in 2 steps (see below):

- 1. We have to add a variable for "Favourite Fruit" in the resource definition, and initialize it.
- 2. We have to initialize the ChangeGreeting() function in the Resource Interface (**just** initialize, not define!)

<img width="1512" alt="Screen Shot 2022-07-24 at 3 27 01 PM" src="https://user-images.githubusercontent.com/92488787/180668299-852e948a-a27f-4929-a880-0d3d4366440e.png">
