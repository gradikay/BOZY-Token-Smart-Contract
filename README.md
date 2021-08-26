# BOZY-Token-Smart-Contract
## Bozindo Cryptocurrency Token Smart Contract

This set of interfaces, contracts, and utilities are all related to the https://eips.ethereum.org/EIPS/eip-20[ERC20 Token Standard].

There a few core contracts that implement the behavior specified in the EIP:

* {ERC20Interface}: The interface all ERC20 implementations should conform to.
* {Context}: The information about the caller including the <<msg.sender,`_msgSender()`>> and <<msg.value,`_msgValue()`>> functions.
* {Bozy}: The implementation of the ERC20 interface including additional functions.

Additionally there are multiple custom extensions, including:

* {Ownable}: The information about the founder of the contract and none-zero address modifier.
* {Whitelisted}: The ability to block evil users' transactions and to burn their tokens.
* {Pausable}: The ability to pause or unpause trasactions of all tokens.
* {ERC20Snapshot}: efficient storage of past token balances to be later queried at any point in time.
* {ERC20Permit}: gasless approval of tokens (standardized as ERC2612).
* {ERC20FlashMint}: token level support for flash loans through the minting and burning of ephemeral tokens (standardized as ERC3156).
* {ERC20Votes}: support for voting and vote delegation.
* {ERC20VotesComp}: support for voting and vote delegation (compatible with Compound's token, with uint96 restrictions).
* {ERC20Wrapper}: wrapper to create an ERC20 backed by another ERC20, with deposit and withdraw methods. Useful in conjunction with {ERC20Votes}.

Finally, there are some utilities to interact with ERC20 contracts in various ways.

* {SafeERC20}: a wrapper around the interface that eliminates the need to handle boolean return values.
* {TokenTimelock}: hold tokens for a beneficiary until a specified time.

The following related EIPs are in draft status.

- {ERC20Permit}

NOTE: This core set of contracts is designed to be unopinionated, allowing developers to access the internal functions in ERC20 (such as <<ERC20-_mint-address-uint256-,`_mint`>>) and expose them as external functions in the way they prefer. On the other hand, xref:ROOT:erc20.adoc#Presets[ERC20 Presets] (such as {ERC20PresetMinterPauser}) are designed using opinionated patterns to provide developers with ready to use, deployable contracts.

== Core

{{IERC20}}

{{IERC20Metadata}}

{{ERC20}}

== Extensions

{{ERC20Burnable}}

{{ERC20Capped}}

{{ERC20Pausable}}

{{ERC20Snapshot}}

{{ERC20Votes}}

{{ERC20VotesComp}}

{{ERC20Wrapper}}

{{ERC20FlashMint}}

== Draft EIPs

The following EIPs are still in Draft status. Due to their nature as drafts, the details of these contracts may change and we cannot guarantee their xref:ROOT:releases-stability.adoc[stability]. Minor releases of OpenZeppelin Contracts may contain breaking changes for the contracts in this directory, which will be duly announced in the https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/CHANGELOG.md[changelog]. The EIPs included here are used by projects in production and this may make them less likely to change significantly.

{{ERC20Permit}}

== Presets

These contracts are preconfigured combinations of the above features. They can be used through inheritance or as models to copy and paste their source code.

{{ERC20PresetMinterPauser}}

{{ERC20PresetFixedSupply}}

== Utilities

{{SafeERC20}}

{{TokenTimelock}}
