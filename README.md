# Human Standard Multi Collectible ABI

A simple node module that exports the Ethereum ABI for ERC 1155 compatible tokens.

## Use

```javascript
import Web3 from 'web3';

const abi = require('human-standard-multi-collectible-abi');
const web3 = new Web3(Web3.givenProvider || 'http://localhost:8545');

const collectible = new web3.eth.Contract(abi, contractAddress);

// Get token's balance
const balance = await collectible.methods.balanceOf(walletPublicAddress,tokenId).call()
```

## References

* [EIP-1155: Multi Token Standard](https://eips.ethereum.org/EIPS/eip-1155)
* [ERC1155 - OpenZeppelin Docs](https://docs.openzeppelin.com/contracts/3.x/erc1155)
