# Loan Testing

1. Deploying the loan smart contract at the node.
2. The caller of the deployment can be anyone(deployment account). As the pallet Id we need to enter the account id of the community\_loan\_pool pallet. The repayment of the loan will get transferred to this account id.
3. `5EYCAe5ijiYetqpEJnhXGV57uEiEy6ghW6qnub8TxmLaZfuC`
4.

    <figure><img src="https://lh5.googleusercontent.com/S9aQCFQbRAI-P3vzc135qAkTtsxaTuZr3WX4CMKadE7xoGjKRhh0TYY0JFzAQCgUE7LKNT8orCY4X2n82lVRqEjtXCoxkzq7UEic9wl0sKcNiy27kXI6rfVuheXhrYqEw78VW7L1VNLbOqaGmLDYpw" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://lh3.googleusercontent.com/oOrj1vjnYHRus3_wnvvnLeSvvjRlhd60ACpr8gYFSBej0fjD4NHEvZwwDzRGps9_oV1UnxJBKKMTgvc10HpRFI-7UoHiTinIfpbsGe7woz4xUF8ZO1nHtf7f2jkTsHKuoewgGnsv_OX-D9g0Q0u9vw" alt=""><figcaption></figcaption></figure>
5. We need to add committee member for voting process by going to “Developer” tab… then choosing “Sudo”. then go to “submit the following change” dropdown and choose “communityLoanPool”.
6.  Calling the addCommitteeMember function in the community loan pool pallet with sudo and entering the account address of the member we want for the voting



    <figure><img src="https://lh4.googleusercontent.com/uSOrI_VLZaOmBgTh1beWryNNTKvLk62UIIcSH3Vq_ntjlgx6ea_GZlSsjH5iEs6DucDeZu9_SJW19GbACw5pt-Si0vMIT2vVopxumN1znzK5obEHn8keA11hWw4A7rLpzvHMrjl3uS_5O7xCr-nWaw" alt=""><figcaption></figcaption></figure>
7. We are calling the propose function in the community loan pool pallet to propose a loan by going to “Developer” tab… then choosing “Extrinsics”. then go to “submit the following extrinsic” dropdown and choose “communityLoanPool”.
8. Two arguments need to be entered. First the amount that needs to be borrowed and the beneficiary who should be able to withdraw the loan amount.

<figure><img src="https://lh4.googleusercontent.com/REv_XSww5KxUJHd4USZwEF1xmK-UudOC2qYLorYmwN5HrFuYA_MpIuQOPocLIlwJOrCeP18B3bJae1X_j2t_f_1mM3haPPUNnwaDYeYHCd3CU8WjqNUgUOg2M10_wwl4-X77D-oHCly7OTp0_1cFNg" alt=""><figcaption></figcaption></figure>

9. The committee member can now vote on the proposal with the vote on proposal function.
10. You need to enter the proposalIndex & your vote decision of the committee member.
11. A majority of votes is needed for the proposal to be approved. If the majority is not reached the proposal is automatically rejected. The voting period is for testing purposes 20 blocks.&#x20;

<figure><img src="https://lh5.googleusercontent.com/7_yyZQFrut3qXifOrY4EVem4-hG7lDG7rtGfJsPI_bA5QXvQL7SGLecCvQtGfIwAtoxL8RYb3F3tzz-wdNi23R1LCXzZS91KWstQmZZWKWpWSjF02gEq2f_iESg8dvftyTsPBptrA4OEhwcPNCZt-g" alt=""><figcaption></figcaption></figure>

12. If the proposal got enough yes votes the proposal can still be rejected by calling the reject proposal function with sudo.  &#x20;

<figure><img src="https://lh6.googleusercontent.com/6I2NrnewmBLmVEv5LlEimMC3X4GkgJ1aXhtpsHRq8EWwBdPY78Xq-nKIL2_Qsw1dAkJ6pZcDT0gaGrRECCCkt_-GdmnnUefqc5AuMUFI5hdCjjjY9jbtdZTP5CAaBvTbJru9oW5K4COlWfSuAQDoCw" alt=""><figcaption></figcaption></figure>

13. The proposal can be executed with the approve proposal function if the voting succeeded. As arguments the proposal index, collection id (choose the collection id that you want - this relates to the land nft), collateral price (in practice this should cover the value of the loan), value of funds (should be loan value - 12 zeros need to be added due to the decimals of the node), item id (choose a number for the nft item id), loan apy (choose high number for demo purpose to observe the interests being generated per block), destination account address (select “loan” option in “contracts”), admin account address (choose user as admin for this particular loan) and set gas limits (to at least 5,000,000,000). &#x20;

<figure><img src="https://lh6.googleusercontent.com/VImArlNnTH9TjbxSy9GgygmNgc1xLVZ5VFCTzR8B7Q324Ta9N4JAyP2Q9u9IDcPb5MxcollFbRC537aKgCE8lgl8DlR3i58RM34ghJF2jwXg10svLry7n62E55gX3g2JFqTkVcBNw8KurYbchH7-Jg" alt=""><figcaption></figcaption></figure>

14. Once the proposal gets executed the loan info will be on the smart contract and the beneficiary of the loan will be able to withdraw the funds from the smart contract. The loan information can be viewed by calling the get loan info by selecting “Contracts” option then view “Messages” then scroll to getLoanInfo and click “read”.&#x20;

    <figure><img src="https://lh3.googleusercontent.com/FQdcbmDzlrofryd2SCy5sYUkWgCPdU_Op1Z5aDW-8xy8ZPFehnyhUYeJsBj34a7GbN2GoaqnjAiRdpO38SqQetezivJNpNNfzimjT-u1O5OfPvVpzmkUSWlPPBWgtZEgIlUdNAEGxqtgIbI4Cxn4Hw" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://lh6.googleusercontent.com/2ijVxqc1j9q3lrJTheLkwN80UUDj1nBJ2xiVuqgthFOTdhdFJHshwevNiyOAiRWZrzczN4UocW1eWSvvIeO8LduJk1hyHnq1PTIvvk2sFJiRbiPemXQPFAUuUcUpJArkwT_vJIS4bqRowej7g00wrg" alt=""><figcaption></figcaption></figure>
15. The funds can be withdrawn from the beneficiary by calling the withdrawFunds function by clicking “execute”... Then enter the following arguments; loan id and the amount the beneficiary wishes to withdraw. Ensure the caller of this function is the same as the beneficiary of the loan.

<figure><img src="https://lh6.googleusercontent.com/szsNVWwMER2oOSPeatL3oxkqI2THWFR4Ga8YM7LhHozyy-hYIJTFlUd9sBTd8iEljz9OjKH3UJi_6dyjyHBMWf0NJ7jb3OefjvtSGgrknzzInmQRnGK9JjA1SVb8d8NybkGOIjnLAHzPdSoxa7ODow" alt=""><figcaption></figcaption></figure>

16. &#x20;To repay the loan, call the repay function by clicking “execute”. As arguments we need the loan id, the repay amount and the value that should be transferred. The repay amount needs to be equal or smaller than the value that should be transferred (pay the full amount of the loan then pay the interest to avoid interest being added to the total by block). Anyone can repay the loan but only the beneficiary can withdraw. The repay amount will be sent to the community loan pool pallet fund to be used for future loans.

<figure><img src="https://lh4.googleusercontent.com/mPzVeuTl_tAY6SOXfIn7v0FN27gKsiuF4ymf-roOUSCB8VgFZWE3FQ6sX76a9Wrz0zV0MDWj-p_MHCaEdU6LkA-LmfK-_99nNoRrTujjB9gO8HHQR7gHtea7GyLL36MQ2zXRMhGeo5gBt2BJViY1Mw" alt=""><figcaption></figcaption></figure>

17. Once the loan is paid back (check in getLoanInfo that the borrowedAmount is zero), the loan can now be deleted by the admin user of the loan by calling the deleteLoan function in “Contracts” and entering the correct loan ID (Due to the high interest example its advisable to withdraw and repay the whole loan amount since the interests will be charged every block). The loan will be deleted on the smart contract and on the community loan pool pallet (this can be checked by going to getLoanInfo and enter the loan ID - if an error is shown then the loan does no longer exist). Any remaining amount of the loan that is still available but has not been borrowed will be sent back to the community loan pool pallet. The collateral NFT will be burned by calling this function. &#x20;

<figure><img src="https://lh3.googleusercontent.com/Due4YxjitAWLmoxhyC3HYMOMNHW6k2lGhfuEGvhm-KINg3n7Ax38Su5DCy6D17oAAxTEtY1TZT4H_cs1Jog2N4pxP0kWSpedqpmRWQadL5t3LeLsFQDYN7XtJcDcDH3WlREucdq_12KTxjjBTSytkw" alt=""><figcaption></figcaption></figure>
