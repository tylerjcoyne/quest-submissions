# CHAPTER 5 // DAY 3

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. What does "force casting" with as! do? Why is it useful in our Collection?**

Force casting allows us to "down-cast" the type of a variable. For example, if we have a variable that's a very generic type (e.g. only let's us see the "ID" variable within it), we might want to "force cast" that in order to get more info about it (by converting it to a more specific type). It's useful because it allows us to leverage interaces/more general types for security & privacy purposes, but still gives us the option to transition between types when we're looking to view more specific info.

**2. What does auth do? When do we use it?**

`Auth` is necessary in cases where you're attempted to "force cast" a **reference.** 

**3. This last quest will be your most difficult yet. Take this contract: and add a function called borrowAuthNFT just like we did in the section called "The Problem" above. Then, find a way to make it publically accessible to other people so they can read our NFT's metadata. Then, run a script to display the NFTs metadata for a certain id.**

**You will have to write all the transactions to set up the accounts, mint the NFTs, and then the scripts to read the NFT's metadata. We have done most of this in the chapters up to this point, so you can look for help there :)**

1. Deploy the NFTStandard Contract Interface & adjusted CryptoPoops Contract

![Screen Shot 2022-09-02 at 4 26 17 PM](https://user-images.githubusercontent.com/92488787/188245994-dfd5c0ce-e549-49bc-8298-55973a201dae.png)
![Screen Shot 2022-09-02 at 4 26 24 PM](https://user-images.githubusercontent.com/92488787/188245938-4eefa123-b742-44ff-b488-3342f7240522.png)
![Screen Shot 2022-09-02 at 4 26 31 PM](https://user-images.githubusercontent.com/92488787/188245946-9e076d1c-6252-48f4-bed3-fded10993a48.png)

2. Set up the CryptoPoops Collection

![Screen Shot 2022-09-02 at 4 45 33 PM](https://user-images.githubusercontent.com/92488787/188246982-477faded-33f3-40ed-9a47-3d4110f188bb.png)

3. Mint an NFT & Deposit It to an Account (while grabbing the NFT's ID)

![Screen Shot 2022-09-02 at 4 51 32 PM](https://user-images.githubusercontent.com/92488787/188247278-726fc161-a66a-4044-aa93-be912606c3f4.png)

4. Read the NFT's Metadata

![Screen Shot 2022-09-02 at 4 51 52 PM](https://user-images.githubusercontent.com/92488787/188247284-46292d12-3f22-4f27-8073-3f19153a9b0b.png)
