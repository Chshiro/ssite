---
sidebar_position: 6
---

### *Code*
### [TraderPool.sol](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/TraderPoolUpgradable.sol)
#### *Parameter's table*
<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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
			<td>map of references to different class of token Dex system</td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_commissions</td>
			<td></td>
		</tr>
		<tr>
			<td>bool</td>
			<td>_actual</td>
			<td></td>
		</tr>
		<tr>
			<td>bool</td>
			<td>_investorRestricted</td>
			<td></td>
		</tr>
	</tbody>
</table>


### Imports

​https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/utils/structs/EnumerableSet.sol

https://github.com/OpenZeppelin/openzeppelin-contracts/blob/master/contracts/token/ERC20/IERC20.sol

https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/master/contracts/access/AccessControlUpgradeable.sol​

​https://github.com/OpenZeppelin/openzeppelin-contracts-upgradeable/blob/master/contracts/security/PausableUpgradeable.sol 
(ссылка с палёным путем)

​
​
```jsx title="text"
    modifier onlyWhitelistOrBasicToken(address token) {
​
    }
```
```jsx title="text"
    modifier onlyNotWhitelistOrBasicToken(address token) {
​
    }
```
```jsx title="text"
    modifier onlyEnabledRiskSubPool(address token) {
​
    }
```
```jsx title="text"
    modifier onlyDisabledRiskSubPool(address token) {
​
    }
```
```jsx title="text"
    modifier onlyWhiteList(address token) {
​
    }
```
```jsx title="text"
    modifier onlyAdmin() {
​
    }
```
```jsx title="text"
    modifier onlyTrader() {
​
    }
```
```jsx title="text"
    modifier onlyAssetManager() {
​
    }
```
```jsx title="function return version of the contract with uint32 type"
    function version() public view returns (uint32){
​
    }
```
```jsx title="text"
    function createProposal(address riskyToken) external onlyTrader onlyNotWhitelistOrBasicToken(riskyToken) onlyDisabledRiskSubPool(riskyToken) {
​
    }
```
```jsx title="function allowed amount of the buying risk token"
    function totalAllowedLpToBuyRiskToken() public view returns(uint256){
    }
```
```jsx title="text"

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
```jsx title="инициация операции обмена"
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
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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
```jsx title="длина позиций"
    function positionsLength() external view returns (uint256) {

    }
```
```jsx title="функция принимает положение в"
    function positionAt(uint16 _index) external view returns (uint256,uint256,address) {

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
		</tr>
		<tr>
			<td>uint16</td>
			<td>_index</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="функция принимает положение для
    function positionFor(address asset) external view returns (uint256,uint256,address) {
​
    }
```
```jsx title="снимает со счета коммиссию трейдера"
    function withdrawTraderCommission(uint256 amount) public onlyTrader {
​
    }
```
```jsx title="снимает со счета коммиссию дексе"
    function withdrawDexeCommission(uint256 amount) public {
​
    }
```
```jsx title="устанавливает коммиссионный адрес трейдера"
    function setTraderCommissionAddress(address _traderCommissionAddress) public onlyTrader {

    }
```
<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_traderCommissionAddress</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="устанавливает коммиссию"
    function setCommission(uint256 _type, uint16 _nom, uint16 _denom) public onlyAdmin {
 
    }
```
<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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

```jsx title="ставит на паузу"
    function pause() onlyAdmin public {
​
    }
```
```jsx title="снимает с паузы"
    function unpause() onlyAdmin public {
    
    }
```
```jsx title="получает максимальное количество открытых позиций(положений)"
    function getMaxPositionOpenAmount() external view returns (uint256){
​
    }
```
```jsx title="предоставляет информацию юзера"
    function getUserData(address holder) public view returns (uint256, int128, uint256) {
​
    }
```
```jsx title="предоставляет общее количесво закрытия? я ебу?"
    function getTotalValueLocked() public view returns (uint256, uint256){
​
    }
```
```jsx title="получает коммиссию"
    function getCommission(uint256 _type) external view returns (uint16,uint16){
    
    }
```
```jsx title="все позиции активов"
    function _totalCap() internal override view returns (uint256){
    
    }
```

```jsx title="происходит перед депозитом"
    function _beforeDeposit(uint256 amountTokenSent, address sender, address holder) internal override {
​
    }
```

```jsx title="происходит после депозита"
    function _afterDeposit(uint256 amountTokenSent, uint256 amountLiquidityGot, address sender, address holder, int128 tokenPrice) internal override {
​
    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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

```jsx title="получает снимаемую коммиссию"
   function _getWithdrawalCommission(uint256 revenue, address holder, int128 currentTokenPrice) internal override view returns (uint256){

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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

```jsx title="перед снятием со счета"
  function _beforeWithdraw(uint256 amountLiquidity, address holder, address receiver) internal override {

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
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

```jsx title="функция получить коммиссию"
    function _getCommission(uint256 _type) internal view returns (uint16,uint16){

    }
```

<table class="iksweb">
	<tbody>
		<tr>
			<td>Type</td>
			<td>Name</td>
			<td>Definition</td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_type</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="все возможные позиции активов"
    function _totalPositionsCap() internal view returns (uint256) {

}
```