# PupperCoin
## Applications Used
1. Remix - where we will write our code for Solidity
2. MetaMask - a GoogleChrome extension where we are able to store and manage our accounts and keys
3. EtherScan - to see if our transaction has processed, is pending, or successful

## Processes and Procedures
1. Import the following files into Remix:
    - PupperCoin.sol
    - PupperCoinCrowdsale.sol

2. Next you will complete to code by clicking 'Compile' in remix or by doing the command + S function, like saving the files.

3. Make sure both files compile correctly.

4. Make sure that your MetaMask is on the Kovan or Ropsten network, which ever you used to first build your wallet. I will be using the Ropsten Network.

5. Next, get ready to deploy your contract. 
    - Make sure that 'Environment' is set to 'Injected Web3'. 'Ropsten (3) network' will pop up underneath 'Injected Web3'.
    - Check that 'Account' is the account that has funds in it in MetaMask. 
    - Leave 'Gas Limit' as is.
    - Leave 'Value' as '0'.
    - Make sure that 'Contract' is set to 'PupperCoinSaleDeployer'.
    - In 'Deploy':
            - 'Name' will be set to 'PupperCoin'.
            - 'Symbol' will be set to 'PUP'.
            - 'Wallet' will be the address that shows up in 'Account' and can be easily copied from MetaMask. 
            - 'Goal' will be set to '300'.

6. Click 'Transact' and MetaMask should pop up, looking something like this. 
![Deployment of PupperCoinSaleDeployer](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/deployment.png)

7. Click 'Confirm' to proceed. 

8. At the bottom of Remix, a notification should pop up and say 'creation of PupperCoinSaleDeployer pending...' with a link, like this:

![Remix Notification of Pending Creation](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/etherscan-link.png)

9. Click on the link. This will take you to EtherScan so you can see the pending creation of your contract. 

![Pending Creation of PupperCoinSaleDeployer](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/transaction-pending.png)

10. Once the creation or transaction has successfully gone through:
    - It will look like this in Remix: 
    ![Successful in Remix](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/successful-in-remix.png)

    - It will look like this in EtherScan:
    ![Successful in EtherScan](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/transaction-successful.png)

11. Then navigate back to Remix and go to the 'Deployed Contracts' section. Click the down arrow of 'PupperCoinSaleDeployer at 0x...".

12. Click 'pupperTokenAddress', we will need this in a second when we add PupperCoin to our wallet. This should show at the bottom of the Remix screen:
![Calling of pupperTokenAddress](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/call-pupperTokenAddress.png)

13. After you have successfully deployed your PupperCoin, you want to navigate to your MetaMask.
    - In the 'Assets' section, at the bottom should be a button called 'Add Token'. Click 'Add Token'.
    - Change from the 'Search' section to 'Custom Token'.
    ![Adding Custom Token](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/add-custom-token.png)

    - 'Token Contract Address' is what we just called in Remix, copy and paste that address here.
    - 'Token Symbol' will be set to 'PUP'.
    - 'Decimals of Precision' will be set to 18 since that is what was decided in our 'PupperCoin.sol' file with ERC20 standards.
    - Click 'Next'.

14. You shold now be able to see 'PUP' in MetaMask. 
![PUP in MetaMask](https://github.com/jtmcginley123/unit21/blob/master/Screenshots/puppercoin-in-metamask.png)

15. You can continue by creating more PupperCoin tokens with a longer time frame in your PupperCoinCrowdsale.sol contract. 
