# CHAPTER 4 // DAY 1

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Explain what lives inside of an account.**

On Flow, an account can actually store data (vs. Ethereum, where NFT's are store _on_ Smart Contracts, for example). This can include (A) Contract Code (as we've been demonstrating by deploying contracts to specific accounts during this course), and (B) Account Storage, which is broken out into different paths that vary in their privacy (and thus, contents).

**2. What is the difference between the /storage/, /public/, and /private/ paths?**

ALL of an account's data exists at /storage/, and thus it can only be accessed by the account owner (for privacy purposes). /public/, as it sounds, is publicly accessible to anyone writing a script. /private/ is only available to the account owner **and** anyone who the account owner grants access to.

**3. What does .save() do? What does .load() do? What does .borrow() do?**

- .save() allows you to save new data **TO** the /storage/ path of an account.
- .load() allows you to take data **OUT** of the /storage/ path of an account.
- .borrow() allows you to peek **INTO** an account's /storage/ path without modifying its contents.

**4. Explain why we couldn't save something to our account storage inside of a script.**

An account's /storage/ path is private to the account-owner, so we would need the account to sign a transaction in order for us to be granted authority to save new data to it. Scripts are only intended to view on-chain data, not to modify it.

**5. Explain why I couldn't save something to your account.**

To my point above, an account's /storage/ path is private to the account-owner, so in order for you to save something to my account, I would first need to grant you access to do so. This is important on Flow because NFT's and other data are stored **in** the account, so it would be dangerous if anyone could save data to/load data out of anyone else's account.

**6. Define a contract that returns a resource that has at least 1 field in it. Then, write 2 transactions:**

**i. A transaction that first saves the resource to account storage, then loads it out of account storage, logs a field inside the resource, and destroys it.**

<img width="1512" alt="Screen Shot 2022-08-21 at 12 11 51 PM" src="https://user-images.githubusercontent.com/92488787/185807135-9b1a3947-1180-457c-84b2-9276fcaa45b3.png">

**ii. A transaction that first saves the resource to account storage, then borrows a reference to it, and logs a field inside the resource.**

<img width="1512" alt="Screen Shot 2022-08-21 at 12 14 07 PM" src="https://user-images.githubusercontent.com/92488787/185807208-8400e0eb-27c7-4db8-9a48-e56a5ef403e3.png">
