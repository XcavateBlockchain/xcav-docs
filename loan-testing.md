# Loan Testing

1.  Deploying the loan smart contract at the node.

    1. The caller of the deployment can be anyone(deployment account). As the pallet Id we need to enter the account id of the community\_loan\_pool pallet. The repayment of the loan will get transferred to this account id.
    2. `5EYCAe5ijiYetqpEJnhXGV57uEiEy6ghW6qnub8TxmLaZfuC`

    &#x20;

    <figure><img src="https://lh4.googleusercontent.com/aC6sjEWcWiTpA0eQOsNgCBZsLn2gnjJz6DgnPXgU6IPWnfIRRBQ246CsVUV_v7CFV3J2MyfSZC4sChaW-Ht9_RlCKjfAIzus78h_yMe8E5cRckxgyuj50qCeg6Fr4_YCxNJMrwN12tJMmOkYE1vahg" alt=""><figcaption></figcaption></figure>



    <figure><img src="https://lh3.googleusercontent.com/vuBp7-xBSn-dabM-gOWOFylSA6eIEgtOkTKJZ3bJqJOXP8QvNuHb1KMFnmYIg3nbkJsrJgoAZDjWqkPjbl8NsB-R8wrIS1iIzsseGmS2nsZW81AJ1Ht19ZmWsucTrn2Wd38Epnhk1-pzHTpfDbxvdw" alt=""><figcaption></figcaption></figure>
2.  We need to add committee member for the voting process by going to the “Developer” tab… then choosing “Sudo”. then go to “submit the following change” dropdown and choose “communityLoanPool”.

    1. Calling the addCommitteeMember function in the community loan pool pallet with sudo and entering the account address of the member we want for the voting.



    <figure><img src="https://lh6.googleusercontent.com/vCc-uUKa5EldaFTPwgewhlOPO-A0IhnL8uYAxmzsSpOd9q1D4e6Rnngl6MKFTvaL56w6v53ZUAyy4X7Q1rY9Y4Cf_-SGMJ082r5tt10xHxKPA4mWbumdAGrwl-DiLCkEZslE_MQYnyhDv8rRjwuG2A" alt=""><figcaption></figcaption></figure>
3.  We are calling the propose function in the community loan pool pallet to propose a loan by going to “Developer” tab… then choosing “Extrinsics”, then go to “submit the following extrinsic” dropdown and choose “communityLoanPool”.

    1. Two arguments need to be entered. First the amount that needs to be borrowed and the beneficiary who should be able to withdraw the loan amount.



    <figure><img src="https://lh5.googleusercontent.com/iafsFNO7HKedT74tJnjTb6TnL6z3-hfyfq32v2In-KbcluIXs8Yx0zyD3flBIWLtqPWutClTBp-Bw9c7-elp-tKf617LyBQLElIHC9_NeYbvIIOeTU_kRRAlDD9Xe_kiu8rmJWWOzGYnZB3UpDE5WQ" alt=""><figcaption></figcaption></figure>
4.  The committee member can now vote on the proposal with the vote on proposal function.

    1. You need to enter the proposalIndex & your vote decision of the committee member.
    2. A majority of votes is needed for the proposal to be approved. If the majority is not reached the proposal is automatically rejected. The voting period is for testing purposes 20 blocks.



    <figure><img src="https://lh3.googleusercontent.com/awErak5kHHuVnk5WYSvOsWcFJMWjIRjeUMqUHzzloRlrsSjd6wgqzWm4iJElpHaAQPr_eyIVP2L_1g36f_cDgbxEhDmTG44hWCxbyg-u7plT9xZP2aUCB8P5eYIJRZEMf1QbQ1VPKHA1AIqcnGbnsg" alt=""><figcaption></figcaption></figure>
5.  If the proposal got enough yes votes the proposal can still be rejected by calling the reject proposal function with sudo.



    <figure><img src="https://lh6.googleusercontent.com/SO2k7n0JPfUoe5yu2dV87qSBkH7xNdju2ZnH6OOiFFzcjop9IFoXASqGw8SkoWI4TwwaeIh0SIwTbCCNBmH1qGtSCwnvMbhj1vxesLvTj9bENMf_bQv7tLM0y2Lgh5DwWWdXfgF6Lw4r_u8Cale6uA" alt=""><figcaption></figcaption></figure>
6.  The proposal can be executed with the approve proposal function if the voting succeeded. As arguments the.

    1. proposal index
    2. collection id (choose the collection id that you want - this relates to the land nft)
    3. collateral price (in practice this should cover the value of the loan)
    4. value of funds (should be loan value - 12 zeros need to be added due to the decimals of the node)
    5. item id (choose a number for the nft item id)
    6. loan apy (choose high number for demo purpose to observe the interests being generated per block), destination account address (select “loan” option in “contracts”), admin account address (choose user as admin for this particular loan) and set gas limits (to at least 5,000,000,000)



    <figure><img src="https://lh6.googleusercontent.com/YidwWI7qAEq1JzvjoiSo1d0bn9gJxFwQ6vMg0lVZAEbTmEX9T-NAgqULKSTCRub1MWz8NumnlhImKhbmI3Ghf9rEJtM7b2E8qXW3kVxfJ0m6YyGsABZpeoyE7ZlVlmsUeNCp8pjDPt-_cAWtHIwXNA" alt=""><figcaption></figcaption></figure>
7.  Once the proposal gets executed the loan info will be on the smart contract and the beneficiary of the loan will be able to withdraw the funds from the smart contract. The loan information can be viewed by calling the get loan info by selecting “Contracts” option then view “Messages” then scroll to getLoanInfo and click “read”.



    <figure><img src="https://lh3.googleusercontent.com/faIYim63wB2zW1Cr8oMAzBmJB8wiUYJT0d9sDCn2Ls3Y6Vfddm0nV8d0ytF0Ytrg0FTmxXXLym8oERiHkvd52bz5KQ6W6FeYA3J0PLSS01kDE0R9cOxZyZDHpBPhD-ke7NZWHm_f6oPlJn9jwvCrXQ" alt=""><figcaption></figcaption></figure>



    <figure><img src="https://lh3.googleusercontent.com/zL5YP5PM3aP1whEDzqLngZYKk2o09Td3F8J42E1v2aRu-3OQsjO6_Yg1DGeCg6c_kXR0wCNKhsYCZ4ZClWRoTlVteh9A3zjwx_erz5aH48USB2kT21osMTNLWJ1_9K0O3oU71ZndbR3IN_1Q_xE6IQ" alt=""><figcaption></figcaption></figure>
8.  The funds can be withdrawn from the beneficiary by calling the withdrawFunds function by clicking “execute”... Then enter the following arguments; loan id and the amount the beneficiary wishes to withdraw. Ensure the caller of this function is the same as the beneficiary of the loan.



    <figure><img src="https://lh5.googleusercontent.com/E1I2QZ0Wa-s-jp8-zg9e6HZLTeVOp81d438QrCicfV7Bx8E8wpHCubYKRRbv_BQdutrcIcmcmYJeqcDeAXdeEBf-N2FXTgq7M2SGk4yoZPQCO9oBqZgN0c0Ne45qblpCXtDmN_f6Zxh2-lzb6dR-NQ" alt=""><figcaption></figcaption></figure>
9.  To repay the loan, call the repay function by clicking “execute”. As arguments we need the loan id, the repay amount and the value that should be transferred. The repay amount needs to be equal or smaller than the value that should be transferred (pay the full amount of the loan then pay the interest to avoid interest being added to the total by block). Anyone can repay the loan but only the beneficiary can withdraw. The repay amount will be sent to the community loan pool pallet fund to be used for future loans.



    <figure><img src="https://lh3.googleusercontent.com/HHbH-rDQBU8Z64LWFVdWKLqCvnlySdQ_AfJGm7vO_AR0PfOMTlVhJsl3vEn3o35ptmV4f6vZ2YpgK5MH51f8n9VuqMuW0swPepUWkjx97uLuSLkPIaGA_WsGiEactgm-aDKgcrbsJAVNkxt90cH1lg" alt=""><figcaption></figcaption></figure>
10. Once the loan is paid back (check in getLoanInfo that the borrowedAmount is zero), the loan can now be deleted by the admin user of the loan by calling the deleteLoan function in “Contracts” and entering the correct loan ID (Due to the high interest example its advisable to withdraw and repay the whole loan amount since the interests will be charged every block). The loan will be deleted on the smart contract and on the community loan pool pallet (this can be checked by going to getLoanInfo and enter the loan ID - if an error is shown then the loan does no longer exist). Any remaining amount of the loan that is still available but has not been borrowed will be sent back to the community loan pool pallet. The collateral NFT will be burned by calling this function.



    <figure><img src="https://lh6.googleusercontent.com/13K_UtZBDtrCHdAw8BcfYBJtxg6Nh3f3BXXWGeaBJj7Ms8H5vO8BpbEucxpoVGWqvzEO7jvQqDLQeU8GJ0BOeJQwbUlF9B1giSj90iNsij5xTt9BbKQ7GkEgAaPLeYTzPkfUrFXnITavHG1gxVOkJg" alt=""><figcaption></figcaption></figure>
