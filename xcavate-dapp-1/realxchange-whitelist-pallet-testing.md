# RealXchange Whitelist Pallet - Testing

### Whitelist pallet testing with polkadot js as frontend

The whitelist pallet allows us to add and remove accounts from the whitelist. This is a short term fix until the DIP Pallet (from Kilt) is available and set up (which should be in Jan 2024). To interact with our custom pallets, all user must have already gone through the DID/KYC/KYB/AML (Kilt DID & Deloitte Verifiable Credentials) process (and be whitelisted) in order to be able to call the extrinsics of the pallets.

**1.0 Add accounts to the whitelist**

To add an account to the whitelist, the sudo account must call the addToWhitelist function.

This function only requires the AccountId of the user to be added to the whitelist as a parameter.

<figure><img src="https://lh7-us.googleusercontent.com/0qVq8m0BU_RYARsBzhPn0yBouFwdZDLvuA-K9grCwY0dCzUyDgBYDP-6inwts2fSkAoaYovBvVAIqf5Xxbw8M9QeOZ9I3xDEyNUsjHqZlI5BQgVgf2eVMEdb08f83-wnTO2865G4eeiocm4gLHB__Q" alt=""><figcaption></figcaption></figure>

\
**2.0 Remove accounts to the whitelist**

To add an account to the whitelist, the sudo account must call the addToWhitelist function.

This function only requires the AccountId of the user to be added to the whitelist as a parameter.

<figure><img src="https://lh7-us.googleusercontent.com/sx6AHztDeT_24QggjucMt5u0WrF5ngoD8dG8uuSjVTqC0ZBHgm3959Nhtj4l-YoHCQlEe4tOdKGCzTO_mu8SAnGB--I36ir-IQzsRigi-WNLGpouEk8kTuBYREYRGCw5u1lJLTItjAT5nEfD9WBdeA" alt=""><figcaption></figcaption></figure>

\
