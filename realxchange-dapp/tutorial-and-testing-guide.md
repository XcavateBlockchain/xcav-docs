# Tutorial & Testing Guide

## Test Accounts

### Sporran DIDs

Eve Community - Project Manager\
Seed Phase: width replace outside young can blame suffer asset rice kitten basket gown\
Password: WeLoveEve@2024\
\
Charlie Chap - Project NFT Buyer 1\
Seed Phase: awesome just tourist slim hood swamp prison weapon print enforce choose bag\
Password: WeLoveCharie@2024\
\
Dave Chum - Project NFT Buyer 2\
Seed Phase: echo popular trigger envelope effort pig ritual curtain unlock sunset favourite midnight\
Password: WeLoveDave@2024\\

### Polkadot.js Wallet

Eve Community - Project Manager\
Wallet address: 5HGjWAeFDfFCWPsjFQdVV2Msvz2XtMktvgocEZcCj68kUMaw\
Seed Phase: bottom drive obey lake curtain smoke basket hold race lonely fit walk//Eve\
\
Charlie Chap - Project NFT Buyer 1\
Wallet address: 5FLSigC9HGRKVhB9FiEo4Y3koPsNmBmLJbpXg2mp1hXcS59Y\
Seed Phase: bottom drive obey lake curtain smoke basket hold race lonely fit walk//Charlie\
\
Dave Chum - Project NFT Buyer 2\
Wallet address: 5FHneW46xGXgs5mUiveU4sbTyGBzmstUspZC92UhjJM694ty\
Seed Phase: bottom drive obey lake curtain smoke basket hold race lonely fit walk//Dave\\



### **Real exchange testing with polkadot js as frontend**

**1.0 Listing Project**

To interact with the real exchange dApp, the project manager and all other user must have already gone through the DID/KYC/KYB/AML (Kilt DID & Deloitte Verifiable Credentials) process (and be whitelisted) in order to be able to call the extrinsics of the community project pallet.

The listProject function must be called by the project manager

<figure><img src="https://lh7-us.googleusercontent.com/Vq9wgxUGgri9k5MLDw-lgf-S7v3aKo8nt8ImdA-L9sP2JuTYW8r43sPphArmKu7WBDx9r6dKLQi2kqMTlTmyww0W7WswyX9ZRVM5bd_2rNGoCaA5ytylr57hhJ2AS0HFjJwAFcg9d9hjW8lQIzR7Pw" alt=""><figcaption></figcaption></figure>

The various NFT types are the variants that the project manager wishes to sell on the marketplace are required as parameters.

Both the price and the quantity of any type of NFT must be selected.

Each NFT type should have its own metadata. The metadata can be the same, but in order to successfully execute the function, for each NFT type a metadata must be uploaded.

The maximum number of NFT types is 4.

\
The duration is the duration of the project in months. The project manager (owner) must estimate how long the project will take to complete.

The price is the target price the project manager needs to complete the desired outcome for the project (supporting documentation needs to be submitted to support these assumptions so NFT buyers can verify the amount). The total price of all NFT types entered must cover the target funds for the project, otherwise the extrinsic will fail.

The data is the metadata of the collection.

\
**2.0 Listed Project**

Once the project is listed on the real exchange dApp there are two options to support the project.

2.1 The first option is to bond tokens to the project by calling the bondToken function.

<figure><img src="https://lh7-us.googleusercontent.com/d14ykgmCwwFFqw20ztkiljahtCz63m-rd1avIphv2kQ2wHhNH34luNCm8C6JbCtWHpcValdDKwQ0GplgCGDyx6Uph9PlhgoEFwGZHsPDvGvsgRVGwp9fLYEdSYuMLsvKSp3b3kioy8wYZ-G6PUwk0A" alt=""><figcaption></figcaption></figure>

This means that the token is locked for the user and the XCAV tokens in the Community Project Pallet are transferred to the Project Manager after milestones have been reached. XCAV tokens in the Community Project Pallet are allocated by sales of NFTs on the Xcavate real estate dApp NFT marketplace. An amount decided by Governance (initially set to 10%) of these fees go to the Community Project Pallet. A maximum of 10% of the project funding total can be funded by the bonding of XCAV tokens. The parameters required are the collection ID of the project and the amount of XCAV tokens that the user wishes to lock.

\
2.2 The second option is by selling the NFTs.

<figure><img src="https://lh7-us.googleusercontent.com/FCDCm6ZILZr14Ar5okgViRNZcgnM8HIRa1Ia2no0BAv5tpRkPoIuu1reVQRtqGswrqBYncDXP_yb42Xjblc3SjIrI3VKi-vzthu0lMcTmjXnESxx2V92D0niDIPUJ2A7Ogpsl3iGo5AXJwgTyCH1Hg" alt=""><figcaption></figcaption></figure>

The NFTs can be purchased by the marketplace users. To do this, the function buy NFT must be called. It has the parameter collectionId, which is the collection ID of the project. The number of the NFT type that the user selects for purchase and the number of NFTs of that selected type.

\
Users of the realXchange active projects marketplace can only NFTs in a particular project until that project's funding target is reached. They will only be charged for the NFTs when they receive them. The NFTs are paid with XUSD (this represents a test version of a stable coin), and later these funds are forwarded to the project manager in equal tranches based on the number of milestones.

\
**3.0 Active Project**

<figure><img src="https://lh7-us.googleusercontent.com/brTsRMOHdq0aX--XaGM6hzBLtOSiuSkVAbIWKR1-pcjsaJ64bqxovvIsxABcBfLpzv1NKcaTJWyMdH25lMTjdX7hrhtW0gKkHmqasynwPxs3jYnY_adNCDVOAQCoHYA3D3X7KCtuPPqIMja2mDBZcQ" alt=""><figcaption></figcaption></figure>

3.1 Once the funding target has been reached, all remaining NFTs that have not yet been sold will be burned.

3.2 Once the project has been launched, the first milestone period begins. For testing purposes, it only lasts a few blocks. As soon as the milestone period is over, the first voting period begins. During this period, all users with NFTs in that particular project can vote on the milestone. They can vote either Yes or No on the milestone.

<figure><img src="https://lh7-us.googleusercontent.com/8tECwFwJ8C92AVG54A6R6gWwGWY8hsYE8MB_itzN8bTIpvSOSVbmvQgEeWR67ilSmPQkd98V6c1GYjbPsX2mTIg2TmfPVR-c2vKjZLXikeM4BseDipge42vIwpm-6bLaOm7OsbeyDTeZR2r1fe7iOQ" alt=""><figcaption></figcaption></figure>

3.3 Nft holders can vote by calling the voteOnMilestone function. The parameter collectionId is the collection ID of the project and vote is an enum with the value ‘yes’ or ‘no’. The voting power is determined by the value of the NFTs that the user has acquired. If the vote has more ‘yes’ votes than ‘no’ votes, the first milestone tranche of funds is sent to the project

manager's wallet. If it is not reached, the project receives a strike. Once a project receives 3 strikes, the remaining funds are refunded to the NFT owners of the project, the bonding locks are released and the project is deleted. At the end of a milestone the strikes are reset to zero as soon as a vote has taken place.

\
3.4 As soon as all milestones have been reached, the project is deleted and the bonding locks are released.

\
