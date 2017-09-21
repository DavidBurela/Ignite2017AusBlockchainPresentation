# Blockchain development on Azure BaaS 
* Twitter @DavidBurela
* Blog https://DavidBurela.Wordpress.com
* GitHub https://github.com/DavidBurela
* Videos of my Blockchain presentations delivered at Microsoft Ignite Australia https://davidburela.wordpress.com/2017/05/10/videos-and-notes-of-my-blockchain-presentations-at-microsoft-ignite-australia/

## Setting up your development environment
* Installing on Windows https://davidburela.wordpress.com/2016/11/18/how-to-install-truffle-testrpc-on-windows-for-blockchain-development/
* **(Preferred!)** Installing on Windows 10 using Ubuntu bash, or Ubuntu https://davidburela.wordpress.com/2017/05/12/how-to-install-truffle-testrpc-on-ubuntu-or-windows-10-with-windows-subsystem-for-linux/
* Configuring VS Code https://davidburela.wordpress.com/2016/11/18/configuring-visual-studio-code-for-ethereum-blockchain-development/
* DevOps with VSTS https://davidburela.wordpress.com/2017/09/06/ethereum-devops-with-vsts-easier-now-with-new-truffle-installer-npx/

## Truffle framework
* http://truffleframework.com/
* https://truffle-box.github.io/
* TestRPC https://github.com/ethereumjs/testrpc
* writing tests with async/await https://davidburela.wordpress.com/2017/09/21/writing-truffle-tests-with-asyncawait/

## Azure Etherum consortium
* Marketplace offering https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft-azure-blockchain.azure-blockchain-service
* More advanced template https://github.com/EthereumEx/ethereum-arm-templates/blob/master/ethereum-consortium/docs/setupWalkthrough.md
```
.\geth --datadir .\ --networkid 10101010 --rpc
```

### additional links
* Ethereum https://ethereum.org/
* Geth Ethereum client https://geth.ethereum.org/
* Metamask (wallet) https://metamask.io/
* .net ethereum library http://www.nethereum.com/
* uPort (identity) https://www.uport.me/
* DevOps https://davidburela.wordpress.com/2016/12/23/ethereum-devops-with-truffle-testrpc-visual-studio-team-services/

### info sources
* Ethereum documentation http://www.ethdocs.org/
* Truffle documentation http://truffleframework.com/docs/
* Solidity documentation https://solidity.readthedocs.io/
* Creator of Ethereum https://twitter.com/VitalikButerin
* Consensys https://twitter.com/ConsenSysLLC
* Consensys projects https://consensys.net/ventures/core-components/

## Code snippets
### getting started in Truffle Console
``` 
// get accounts
web3.eth.accounts

// get reference to deployed contract
var metaCoin;
MetaCoin.deployed().then(function(deployed) {metaCoin = deployed;});

// get balance of account 0
metaCoin.getBalance.call(web3.eth.accounts[0])

// send coins
var account0 = web3.eth.accounts[0];
var account1 = web3.eth.accounts[1];
metaCoin.sendCoin(account1, 1000, {from: account0});
metaCoin.getBalance.call(account0);

```
