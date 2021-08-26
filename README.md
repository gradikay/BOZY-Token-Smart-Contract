# BOZY-Token-Smart-Contract
## Bozindo Cryptocurrency Token Smart Contract

This set of interfaces, contracts, and utilities are all related to the https://eips.ethereum.org/EIPS/eip-20[ERC20 Token Standard].

### There a few core contracts that implement the behavior specified in the EIP:

* {ERC20Interface}: The interface all ERC20 implementations should conform to.
* {Context}: The information about the caller including the ( msg.sender, `_msgSender()` ) and ( msg.value, `_msgValue()` ) functions.
* {Bozy}: The implementation of the ERC20 interface including additional functions.

### Additionally there are multiple custom extensions, including:

* {Ownable}: The information about the founder of the contract and none-zero address modifier.
* {Whitelisted}: The ability to block evil users' transactions and to burn their tokens.
* {Pausable}: The ability to pause or unpause trasactions of all tokens.

### Finally, there are some utilities to interact with ERC20 contracts in various ways.

* {BozyICO}: The initial token offering.

The following  are important information about the Token:

- Total Supply `30,000,000,000`: IN ETH that's 30000000000E18 wei
- Token Name `Bozindo.com Currency`
- Token Symbol `BOZY`
- decimals `18`
- Token ICO price `0.00001 eth`: IN ETH that's 10000000000000 wei
