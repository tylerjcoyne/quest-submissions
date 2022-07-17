# CHAPTER 2 // DAY 3

Name: Tyler Coyne  
Discord Handle: tcoyne#4231


**1. In a script, initialize an array (that has length == 3) of your favourite people, represented as Strings, and log it.**

<img width="1509" alt="Screen Shot 2022-07-17 at 2 01 42 PM" src="https://user-images.githubusercontent.com/92488787/179424619-7052a1cf-680e-48ce-b52a-a744686a6c21.png">

**2. In a script, initialize a dictionary that maps the Strings Facebook, Instagram, Twitter, YouTube, Reddit, and LinkedIn to a UInt64 that represents the order in which you use them from most to least. For example, YouTube --> 1, Reddit --> 2, etc. If you've never used one before, map it to 0!**

<img width="1509" alt="Screen Shot 2022-07-17 at 2 05 05 PM" src="https://user-images.githubusercontent.com/92488787/179424728-883b25f5-0af7-4d8d-a435-5a006c6f3bfe.png">

**3. Explain what the force unwrap operator ! does, with an example different from the one I showed you (you can just change the type).**

The "Force Unwrap" operator takes an "Optional" and either (A) returns it to a non-optional Type, or (B) PANICS! if the returned item is `nil`. 

For example, in the below line of code, we're initializing an Integer as an optional:

`var number: Int? = 17`

To unwrap this, we can use the `!` operator:

`var unWrappedNumber: Int = number!`

BUT if we had actually initialized this `number` variable as `nil`, the same line of code above would have thrown an error when we attempted to unwrap it using the `!` operator.

**4. Using this picture below, explain...**
**-- a. What the error message means**

The error message is telling us that the function's return-type is `String`, but that the current state of the code returns a variable with the `Optional` type `String?`

**-- b. Why we're getting this error**

We're getting this error because in Cadence, dictionaries always return `Optional` types by default.

**-- c. How to fix it**

We can fix this by using the `!` operator to unwrap the returned value. So we'd revise the final line of the function from `return thing[0x03]` to `return thing[0x03]!`
