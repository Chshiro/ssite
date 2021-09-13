### *Code*
### [```TraderPool.sol```](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/TraderPoolUpgradable.sol)
#### *Parameter's table*
<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>address</td>
			<td>riskyToken</td>
			<td>new asset token address</td>
		</tr>
		<tr>
			<td>address</td>
			<td>token</td>
			<td>token address</td>
		</tr>
		<tr>
			<td>address</td>
			<td>user</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>_traderAddress</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>_investors</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>iaddr</td>
			<td>map of references to different pairs of token Dexe system</td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_commissions</td>
			<td>Array of 3 commissions, specified in a form of natural fration each (i.e. nominator and denominator.). Format: [traderCommDenom, traderCommNom, investorCommDenom, investorCommNom, platformCommDenom, platformCommNom]</td>
		</tr>
		<tr>
			<td>bool</td>
			<td>_actual</td>
			<td>flag for setting up "actual portfolio". Set to true to enable.</td>
		</tr>
		<tr>
			<td>bool</td>
			<td>_investorRestricted</td>
			<td>flag to enable investor whitelist. Set to true to enable.</td>
		</tr>
	</tbody>
</table>


### Imports

[EnumerableSet.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/structs/EnumerableSet.sol)

[IERC20.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/IERC20.sol)

[AccessControlUpgradeable.sol](https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/master/contracts/access/AccessControlUpgradeable.sol%E2%80%8B)

[PausableUpgradeable.sol](https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/master/contracts/security/PausableUpgradeable.sol)
​
​
```jsx title="it functions only when in White list Or Basic Token""
    modifier onlyWhitelistOrBasicToken(address token) {
​
    }
```
```jsx title="it functions only when not in White list Or Basic Token"
    modifier onlyNotWhitelistOrBasicToken(address token) {
​
    }
```
```jsx title="it functions only when RiskSubPool is enabled"
    modifier onlyEnabledRiskSubPool(address token) {
​
    }
```
```jsx title="it functions only when RiskSubPool is disabled"
    modifier onlyDisabledRiskSubPool(address token) {
​
    }
```
```jsx title="can manage only when white listed"
    modifier onlyWhiteList(address token) {
​
    }
```
```jsx title="can manage only Admin"
    modifier onlyAdmin() {
​
    }
```
```jsx title="can manage only Trader"
    modifier onlyTrader() {
​
    }
```
```jsx title="can manage only Asset Manager"
    modifier onlyAssetManager() {
​
    }
```
```jsx title="function return version of the contract with uint32 type"
    function version() public view returns (uint32){
​
    }
```
```jsx title="creates Proposal"
    function createProposal(address riskyToken) external onlyTrader onlyNotWhitelistOrBasicToken(riskyToken) onlyDisabledRiskSubPool(riskyToken) {
​
    }
```
```jsx title="function allowed amount of the buying risk token"
    function totalAllowedLpToBuyRiskToken() public view returns(uint256){
    }
```
```jsx title="sets Allowance For Proposal"

    function setAllowanceForProposal() external onlyEnabledRiskSubPool() {
​
    }
```
```jsx title="moves risk token to white list"
    function moveRiskTokenToWhiteList(address token) external onlyTrader onlyWhiteList(token) onlyEnabledRiskSubPool(token) {
​
    }
```
```jsx title="initialize parameters which were introduced to create Pool an' made pair of Assets"
    function initialize(address[9] memory iaddr, uint256 _commissions, bool _actual, bool _investorRestricted) public override initializer{
​
    }
```
```jsx title="adding trader address"
    function addTraderAddress (address _traderAddress) public onlyTrader {
​
    }
```

```jsx title="remove trader address"
    function removeTraderAddress (address _traderAddress) public onlyTrader {
​
    }
```

```jsx title="adds investor address"
    function addInvestorAddress (address[] memory _investors) public onlyTrader {
​
    }
```
```jsx title="removes investor address"
    function removeInvestorAddress (address[] memory _investors) public onlyTrader {
​
    }
```
```jsx title="initiating an exchange operation"
    function initiateExchangeOperation(
        address fromAsset,
        address toAsset,
        uint256 fromAmt,
        address caller,
        bytes memory _calldata
    )
```
<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>address</td>
			<td>fromAsset</td>
			<td>address of the ERC20 token that will be exchanged</td>
		</tr>
		<tr>
			<td>address</td>
			<td>toAsset</td>
			<td>address of the ERC20 token that fromAsset will be exchanged to</td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>fromAmt</td>
			<td>amount of received value</td>
		</tr>
		<tr>
			<td>address</td>
			<td>caller</td>
			<td>address of the Exchange Manager that will be invoked (same approach to flashloans)</td>
		</tr>
		<tr>
			<td>bytes""32""</td>
			<td>_calldata</td>
			<td>calldata that Exchange Manager will be provided with (same approach to flashloans)</td>
		</tr>
	</tbody>
</table>

```jsx title="sells risk token"
    function _sellRiskToken(
        address riskyToken,
        uint256 riskyTokenAmount,
        uint256 riskyBalanceBefore,
        uint256 basicTokenAmount
    )
```

<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>address</td>
			<td>riskyToken</td>
			<td></td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>riskyTokenAmount</td>
			<td></td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>riskyBalanceBefore</td>
			<td></td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>basicTokenAmount</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="deletes the position"
    function _deletePosition(address token) private {

    }
```
```jsx title="length of positions"
    function positionsLength() external view returns (uint256) {

    }
```
```jsx title="the function takes the position in"
    function positionAt(uint16 _index) external view returns (uint256,uint256,address) {

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint16</td>
			<td>_index</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="the function takes the position for"
    function positionFor(address asset) external view returns (uint256,uint256,address) {
​
    }
```
```jsx title="withdraws the trader's commission from the account"
    function withdrawTraderCommission(uint256 amount) public onlyTrader {
​
    }
```
```jsx title="withdraws the dexe commission"
    function withdrawDexeCommission(uint256 amount) public {
​
    }
```
```jsx title="sets the trader's commission address"
    function setTraderCommissionAddress(address _traderCommissionAddress) public onlyTrader {

    }
```
<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>address</td>
			<td>_traderCommissionAddress</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="sets the commission"
    function setCommission(uint256 _type, uint16 _nom, uint16 _denom) public onlyAdmin {
 
    }
```
<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_type</td>
			<td>commission type (1 for trader commission, 2 for investor commission, 3 for platform commission)</td>
		</tr>
		<tr>
			<td>uint16</td>
			<td>_nom</td>
			<td>nominator of the commission fraction</td>
		</tr>
		<tr>
			<td>uint16</td>
			<td>_denom</td>
			<td>denominator of the commission fraction</td>
		</tr>
	</tbody>
</table>

```jsx title="puts it on pause"
    function pause() onlyAdmin public {
​
    }
```
```jsx title="removes the pause"
    function unpause() onlyAdmin public {
    
    }
```
```jsx title="gets the maximum number of open positions"
    function getMaxPositionOpenAmount() external view returns (uint256){
​
    }
```
```jsx title="provides user information"
    function getUserData(address holder) public view returns (uint256, int128, uint256) {
​
    }
```
```jsx title="get a total value lock"
    function getTotalValueLocked() public view returns (uint256, uint256){
​
    }
```
```jsx title="receives a commission"
    function getCommission(uint256 _type) external view returns (uint16,uint16){
    
    }
```
```jsx title="all asset positions"
    function _totalCap() internal override view returns (uint256){
    
    }
```

```jsx title="occurs before the deposit"
    function _beforeDeposit(uint256 amountTokenSent, address sender, address holder) internal override {
​
    }
```

```jsx title="occurs after the deposit"
    function _afterDeposit(uint256 amountTokenSent, uint256 amountLiquidityGot, address sender, address holder, int128 tokenPrice) internal override {
​
    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint256</td>
			<td>amountTokenSent</td>
			<td></td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>amountLiquidityGot</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>sender</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>holder</td>
			<td></td>
		</tr>
		<tr>
			<td>int128</td>
			<td>tokenPrice</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="receives the commission to be withdrawn"
   function _getWithdrawalCommission(uint256 revenue, address holder, int128 currentTokenPrice) internal override view returns (uint256){

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint256</td>
			<td>revenue</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>holder</td>
			<td></td>
		</tr>
		<tr>
			<td>int128</td>
			<td>currentTokenPrice</td>
			<td></td>
		</tr>
		<tr>
			<td>uint16</td>
			<td>investorCommissionPercentNom</td>
			<td></td>
		</tr>
		<tr>
			<td>uint16</td>
			<td>investorCommissionPercentDenom</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="before withdrawing from the account"
  function _beforeWithdraw(uint256 amountLiquidity, address holder, address receiver) internal override {

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint256</td>
			<td>
amountLiquidity
</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>receiver</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="get commission function"
    function _getCommission(uint256 _type) internal view returns (uint16,uint16){

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_type</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="all possible asset positions"
    function _totalPositionsCap() internal view returns (uint256) {

}
```