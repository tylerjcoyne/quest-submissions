# CHAPTER 5 // DAY 2

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Explain why standards can be beneficial to the Flow ecosystem.**

Standards are helpful because they keep everyone on the same-page, whether you're the creator of an NFT collection, or someone interacting with one. Contract interfaces in particular allow us to know that an implementing contract meets a set of standards without even looking at the code, because we know that it wouldn't have been deployed if it hadn't accounted for the needs laid out in the Standard/Interface. It's also a big deal for DApps or NFT Marketplaces, because instead of having to implement new functionality for every single Collection's Contract that comes their way, there's some uniformity that allows them to apply the same approach to all Collections.

**2. What is YOUR favourite food?**

Thanks so much for asking! There's this small chain of Taquerias in Boston where I went to school called "Amelia's Taqueria", and I swear to god their Nachos are the greatest thing on this god foresaken Earth. Go try them with Carnitas, Corn, Chipotle Mayo, Cheese, and anything else you want. Your stomach will regret it but your heart will be so happy.

**3. Please fix this code (Hint: There are two things wrong):**

**Contract Interface:**
- The Contract interface attempts to define a Resource interface & a Resource that **uses** that interface, but it's currently missing that implementation. It should be updated to the below.

<img width="355" alt="Screen Shot 2022-09-02 at 12 22 24 PM" src="https://user-images.githubusercontent.com/92488787/188223206-bf4e63dd-1934-48ee-a70f-ee2d2a4addbe.png">

**Implementing Contract:**
- For one thing, the "implementing" contract isn't actually implementing the Interface as claimed. If it were implementing the Contract Interface, we would want to change the first couple lines of those code to look like this:

<img width="270" alt="Screen Shot 2022-09-02 at 12 17 10 PM" src="https://user-images.githubusercontent.com/92488787/188222442-739344b8-ca40-4b2d-9ed2-04bb5f758c09.png">

- The implementing contract shouldn't be creating a NEW Resource interface, it should instead be referencing the interface from the Contract Interface, like so:

<img width="528" alt="Screen Shot 2022-09-02 at 12 19 06 PM" src="https://user-images.githubusercontent.com/92488787/188222692-337fddaa-bea1-4fd6-ac06-469091918151.png">

- The updateNumber() function also **isn't** actually doing anything with the input that it takes. If it were up to me, I would adjust per the below. As it stands now, if I were to try and update the `self.number` to 5 via the function, we wouldn't meet the post-condition, because the function is **always** setting `self.number` to 5. This isn't technically "wrong", but I'm sure it's not the intended use of the function.

<img width="319" alt="Screen Shot 2022-09-02 at 12 20 41 PM" src="https://user-images.githubusercontent.com/92488787/188222904-3e1ba20a-6c2c-4fd4-9993-8b46259e740a.png">
