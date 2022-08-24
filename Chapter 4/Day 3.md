# CHAPTER 4 // DAY 3

Name: Tyler Coyne  
Discord Handle: tcoyne#4231

**1. Why did we add a Collection to this contract? List the two main reasons.**

1. One reason is to help make accessing the NFT storage more efficient - if we **didn't** use a Collection, we would be stuck remembering new Storage paths every time that we wanted to view a new NFT in our accounts. With a collection, we can store multiple NFTs at the same storage path.
2. The other main reason is that by using a Collection, we allow others to "deposit" NFTs to our account. If we store all of our NFTs in our account storage, the public wouldn't be able to access it, so we would never be able to receive NFTs.

**2. What do you have to do if you have resources "nested" inside of another resource? ("Nested resources")**

If you have nested resources in your code, you HAVE to `destroy` any instances of a nested resource before closing the code.

**3. Brainstorm some extra things we may want to add to this contract. Think about what might be problematic with this contract and how we could fix it.**

**i. Idea #1: Do we really want everyone to be able to mint an NFT? 🤔.**

In many cases, probably not! For example, in the case of an Allowlist-gated Pre-sale, we would want to validate that the minter **is** actually on our Allowlist before allowing them to mint. To do this, we could create a priv Array in our contract in-advance that contains all of the Accounts which we're permitting to mint. The createNFT() function's definition would then include a check to make sure that the minter's Account exists within this Array before allowing the function to be called. If the account address **wasn't** on the list, it would throw an error.

_Edit: After Day 4 I realize that there's probably better ways to do that, since we don't NEED the Allowlist array to live on forever in Blockchain history. One alternative would be to include the createNFT() function within a Minter resource, as suggested in the next lesson, and then apply the Allowlist logic on the **front-end** of our minting-site, so that the only people who can access the contract are people who we validate access for._

**ii. Idea #2: If we want to read information about our NFTs inside our Collection, right now we have to take it out of the Collection to do so. Is this good?**

No, this is not ideal - especially if we destroy the resource at the end of the code! A fix here would be to use a **reference** in-place of the resource itself. This way we can still access public information about the NFT, without involving any risk of loss.
