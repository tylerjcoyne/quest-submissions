# CHAPTER 3 // DAY 1

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. In words, list 3 reasons why structs are different from resources.**

(1) Structs can be copied (vs. Resources, which can not)
(2) Structs can be lost/overwritten (vs. Resources, which can not)
(3) Structs can be created anywhere (vs. Resources, which can only be created in Contracts)

**2. Describe a situation where a resource might be better to use than a struct.**

A resource would be a more appropriate use-case in a scenario where you're creating a contract to determine ownership over an NFT that's worth a ton of money, or anything else that's otherwise confidential/shouldn't be lost. Using a resource here helps to ensure that the data won't be accidentally destroyed or lost without explicit direction to do so (if/when the time comes) from the Dev. In the case of a struct, mistakes like this are much more easily possible.

**3. What is the keyword to make a new resource?**

The keyword is `create`.

**4. Can a resource be created in a script or transaction (assuming there isn't a public function to create one)?**

No, resources can **only** be made within Contract code.

**5. What is the type of the resource below?**

The type of this resource is `@Jacob`.

**6. Let's play the "I Spy" game from when we were kids. I Spy 4 things wrong with this code. Please fix them.**

<img width="782" alt="Screen Shot 2022-07-24 at 2 16 45 PM" src="https://user-images.githubusercontent.com/92488787/180666170-9c2ac6a0-e46c-427f-8762-e2368b59f9d1.png">
