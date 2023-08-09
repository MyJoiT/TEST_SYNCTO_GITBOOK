# Admin Functions

## whitelistBidToken

Set a whitelist of token types that can be used in transactions

`function whitelistBidToken(address token, bool whitelist) external onlyOwner`

<table><thead><tr><th width="213.33333333333331">Name</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>token</td><td>address</td><td>The contract address of token</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" represents adding to the whitelist, while "false" represents removing from the whitelist.</td></tr></tbody></table>

## whitelistRelayer

`function whitelistRelayer(address relayer, bool whitelist) external onlyOwner`

<table><thead><tr><th width="211.33333333333331">Name</th><th width="105">Type</th><th>Description</th></tr></thead><tbody><tr><td>relayer</td><td>address</td><td>The address of relayer</td></tr><tr><td>whitelist</td><td>bool</td><td>"true" represents adding to the whitelist, while "false" represents removing from the whitelist.</td></tr></tbody></table>

## setLensHub

Use for interacting with Lens APIs

`function setLensHub(address hub) external onlyOwner`

<table><thead><tr><th width="208.33333333333331">Name</th><th width="108">Type</th><th>Description</th></tr></thead><tbody><tr><td>hub</td><td>address</td><td>The address of contract LensHub Proxy, go to the Lens docs for more detail. <a href="https://docs.lens.xyz/docs/deployed-contract-addresses">https://docs.lens.xyz/docs/deployed-contract-addresses</a></td></tr></tbody></table>

## setLensFreeCollectModule

Tako will auto-submit a publication while the curator accepts the bids. Lens publication needs an address of CollectModule, so the administrator must set a collect module. Now only can set the FreeCollectModule.

`function setLensFreeCollectModule(address collectModule) external onlyOwner`

<table><thead><tr><th width="205.33333333333331">Name</th><th width="107">Type</th><th>Description</th></tr></thead><tbody><tr><td>collectModule</td><td>address</td><td>The address of contract FreeCollectModule, go to the Lens docs for more detail. <a href="https://docs.lens.xyz/docs/deployed-contract-addresses">https://docs.lens.xyz/docs/deployed-contract-addresses</a></td></tr></tbody></table>

## setFeeCollector

The administrator can collect the fee from every bid. When one bid is complete, the FeeCollect address will collect the fee, and the rest will send to the curator.

`function setFeeCollector(address newsFeeCollector) external onlyOwner`

<table><thead><tr><th width="198.33333333333331">Name</th><th width="113">Type</th><th>Description</th></tr></thead><tbody><tr><td>newsFeeCollector</td><td>address</td><td>An EVM-compatible address for collecting fees</td></tr></tbody></table>

## setFeeRate

Fee = BidTokenAmount \* FeeRate / FEE\_DENOMINATOR

Go to the tako contract for more detail

`function setFeeRate(uint256 newFeeRate) external onlyOwner`

<table><thead><tr><th width="200.33333333333331">Name</th><th width="114">Type</th><th>Description</th></tr></thead><tbody><tr><td>newFeeRate</td><td>uint256</td><td>Fee rate charged after a bid is executed</td></tr></tbody></table>

## setToProfileLimit

The bid can be sent to multiple curators, and this function can limit the number of curators.

`function setToProfileLimit(uint8 counter) external onlyOwner`

<table><thead><tr><th width="200.33333333333331">Name</th><th width="117">Type</th><th>Description</th></tr></thead><tbody><tr><td>counter</td><td>uint8</td><td>Maximum number of target curators</td></tr></tbody></table>

## setMaxDuration

Bids can be set with a valid duration, and this method can restrict the maximum valid time

`function setMaxDuration(uint256 max) external onlyOwner`

<table><thead><tr><th width="203.33333333333331">Name</th><th width="115">Type</th><th>Description</th></tr></thead><tbody><tr><td>max</td><td>uint256</td><td>Maximum valid duration for a bid</td></tr></tbody></table>
