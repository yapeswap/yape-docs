# $veYAPE Rewards

![The distribution function for $veYAPE rewards can be found on the 'Mine' tab inside the DAO page](<../.gitbook/assets/image (2).png>)

When the window shown above surfaces inside the DAO User Interface, it indicates that there are $YAPE rewards available in the protocol to be distributed to $veYAPE holders. This function is being called from the Token Emitter contract whose address can be found along with all other Yapeswap contracts inside the DAO page.

The function can be called permissionlessly by anyone willing to pay the gas. It is not recommended to pay the gas necessary to execute the function unless you are sure that your wallet is holding a large enough $veYAPE lock to receive a $YAPE reward large enough to make paying the gas worthwhile.

Once distributed, those holding $veYAPE locks must visit the 'Gov' tab on the DAO page, then click 'Claim Dividend' where they can then initiate and execute a transaction to send their accumulated $YAPE rewards tokens to their wallet. If the rewards are not 'Claimed' they will remain here and accumulate each time the 'Distribute' function is called.

All protocol revenue (Protocol fee + Yields generated from Yearn vaults) is used to buy back $YAPE. All $YAPE bought back is paid to $veYAPE holders as dividends. The rewards are made available to be distributed once per epoch, where an epoch is approximately one week.
