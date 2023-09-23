# Loan Testing

1. Deploying the loan smart contract at the node.
2. As the pallet Id we need to enter the account id of the community\_loan\_pool pallet. The repayment of the loan will get transferred to this account id.
3. `5EYCAe5ijiYetqpEJnhXGV57uEiEy6ghW6qnub8TxmLaZfuC`
4.

    <figure><img src="https://lh6.googleusercontent.com/8OgfSXYgLDnqtUIEPeZNyWtpDxAAmMeT-oHuNL1F-ZjixY8pq1KgDfWknZKYTorYlszvhZ4xF3K57311uZ-9s5ixDpntVmpSWi0qWr_qzWNHljrEM2VutZH3x4Ec59o0LU_n3cOjizUUJPGprQz2Ng" alt=""><figcaption></figcaption></figure>
5. We need to add committee member for voting process by going to “Developer” tab… then choosing “Sudo”. then go to “submit the following change” dropdown and choose “communityLoanPool”.
6.  Calling the addCommitteeMember function in the community loan pool pallet with sudo and entering the account address of the member we want for the voting



    <figure><img src="https://lh4.googleusercontent.com/uSOrI_VLZaOmBgTh1beWryNNTKvLk62UIIcSH3Vq_ntjlgx6ea_GZlSsjH5iEs6DucDeZu9_SJW19GbACw5pt-Si0vMIT2vVopxumN1znzK5obEHn8keA11hWw4A7rLpzvHMrjl3uS_5O7xCr-nWaw" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://lh4.googleusercontent.com/i7GXdDJfZ5eYxkmLyJSKDaY5P_vIub-Wp_EBXB0W_i0qv9OckdHX-BeZVTBN3tTcKBY2adImz0PQXxf5JmH3EImEHsIV0qOQ-0Cq73a5R--zlirduuL5CC-cT0c3gY-4rsERZUcyB41HL0shEWk5QQ" alt=""><figcaption></figcaption></figure>
7. We are calling the propose function in the community loan pool pallet to propose a loan by going to “Developer” tab… then choosing “Extrinsics”. then go to “submit the following extrinsic” dropdown and choose “communityLoanPool”.
8. Two arguments need to be entered. First the amount that needs to be borrowed and the beneficiary who should be able to withdraw the loan amount.

<figure><img src="https://lh4.googleusercontent.com/REv_XSww5KxUJHd4USZwEF1xmK-UudOC2qYLorYmwN5HrFuYA_MpIuQOPocLIlwJOrCeP18B3bJae1X_j2t_f_1mM3haPPUNnwaDYeYHCd3CU8WjqNUgUOg2M10_wwl4-X77D-oHCly7OTp0_1cFNg" alt=""><figcaption></figcaption></figure>

9. The committee member can now vote on the proposal with the vote on proposal function.
10. You need to enter the proposalIndex & your vote decision of the committee member.
11. A majority of votes is needed for the proposal to be approved. If the majority is not reached the proposal is automatically rejected. The voting period is for testing purposes 20 blocks.&#x20;

<figure><img src="https://lh5.googleusercontent.com/7_yyZQFrut3qXifOrY4EVem4-hG7lDG7rtGfJsPI_bA5QXvQL7SGLecCvQtGfIwAtoxL8RYb3F3tzz-wdNi23R1LCXzZS91KWstQmZZWKWpWSjF02gEq2f_iESg8dvftyTsPBptrA4OEhwcPNCZt-g" alt=""><figcaption></figcaption></figure>

12. If the proposal got enough yes votes the proposal can still be rejected by calling the reject proposal function with sudo.  &#x20;

<figure><img src="https://lh6.googleusercontent.com/6I2NrnewmBLmVEv5LlEimMC3X4GkgJ1aXhtpsHRq8EWwBdPY78Xq-nKIL2_Qsw1dAkJ6pZcDT0gaGrRECCCkt_-GdmnnUefqc5AuMUFI5hdCjjjY9jbtdZTP5CAaBvTbJru9oW5K4COlWfSuAQDoCw" alt=""><figcaption></figcaption></figure>

13. The proposal can be executed with the approve proposal function if the voting succeeded. As arguments the proposal index, collection id, collateral price, value of funds (12 zeros need to be attached due to the decimals of the node), item id, loan apy, destination account address, admin account address and the gas limits. &#x20;

<figure><img src="https://lh6.googleusercontent.com/VImArlNnTH9TjbxSy9GgygmNgc1xLVZ5VFCTzR8B7Q324Ta9N4JAyP2Q9u9IDcPb5MxcollFbRC537aKgCE8lgl8DlR3i58RM34ghJF2jwXg10svLry7n62E55gX3g2JFqTkVcBNw8KurYbchH7-Jg" alt=""><figcaption></figcaption></figure>

14. Once the proposal gets executed the loan info will be on the smart contract and the beneficiary of the loan will be able to withdraw the funds from the smart contract. The loan information can be viewed with by calling the get loan info at the smart contract.&#x20;

<figure><img src="https://lh5.googleusercontent.com/NgLg_h-4SaNtFmajnLeHNo-RU6Z4fowoPAlc6Lt0xCpCJz4w_IPvxypaIJw1wzCXTehNog9Pir0YyCWbv_ft7IqqvEGwV549ZjJmvEJRrvH2K367Y-LXWqG6-radHiPNgS3CSZlmPdBfUMyI2Se9jA" alt=""><figcaption></figcaption></figure>

15. The funds can be withdrawn from the beneficiary by calling the withdraw funds function at the smart contract. As arguments we need the loan id and the amount the beneficiary wants to withdraw.&#x20;

<figure><img src="https://lh6.googleusercontent.com/szsNVWwMER2oOSPeatL3oxkqI2THWFR4Ga8YM7LhHozyy-hYIJTFlUd9sBTd8iEljz9OjKH3UJi_6dyjyHBMWf0NJ7jb3OefjvtSGgrknzzInmQRnGK9JjA1SVb8d8NybkGOIjnLAHzPdSoxa7ODow" alt=""><figcaption></figcaption></figure>

16. For repaying the loan the repay function of the smart contract needs to be called. As arguments we need the loan id, the repay amount and the value that should be transferred. The repay amount needs to be equal or smaller than the value that should be transferred. Everybody can repay the loan but only the beneficiary can withdraw. The repay amount will be sent to the community loan pool pallet. &#x20;

<figure><img src="https://lh4.googleusercontent.com/mPzVeuTl_tAY6SOXfIn7v0FN27gKsiuF4ymf-roOUSCB8VgFZWE3FQ6sX76a9Wrz0zV0MDWj-p_MHCaEdU6LkA-LmfK-_99nNoRrTujjB9gO8HHQR7gHtea7GyLL36MQ2zXRMhGeo5gBt2BJViY1Mw" alt=""><figcaption></figcaption></figure>

17. Once the loan is paid back the loan can be deleted by the admin of the loan by calling the delete loan function of the smart contract. As an argument only the loan id is needed. The loan will be deleted on the smart contract and on the community loan pool pallet. Any remaining amount of the loan that is still available but has not been borrowed will be sent back to the community loan pool pallet. The collateral NFT will be burned by calling this function. &#x20;

<figure><img src="https://lh3.googleusercontent.com/Due4YxjitAWLmoxhyC3HYMOMNHW6k2lGhfuEGvhm-KINg3n7Ax38Su5DCy6D17oAAxTEtY1TZT4H_cs1Jog2N4pxP0kWSpedqpmRWQadL5t3LeLsFQDYN7XtJcDcDH3WlREucdq_12KTxjjBTSytkw" alt=""><figcaption></figcaption></figure>
