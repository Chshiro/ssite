### *Code*
### [```PoolLiquidityToken.sol```](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/pool/PoolLiquidityTokenUpgradeable.sol)
#### *Parameter's table*
<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
			<th>Name</th>
			<th>Definition</th>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_maxPoolTotalSupply</td>
			<td></td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>amount</td>
			<td></td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>amountLiquidity</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>_owner</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>to</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>from</td>
			<td></td>
		</tr>
		<tr>
			<td>string</td>
			<td>name_</td>
			<td></td>
		</tr>
		<tr>
			<td>string</td>
			<td>symbol_</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="текст"
    function initialize(address _owner, uint256 _maxPoolTotalSupply, string memory name_, string memory symbol_) public override initializer {

    }
```
```jsx title="текст"
// uint256 public maxPoolTotalSupply;
bool public fixedSupply;
```
```jsx title="текст"
    function __PoolLiquidityTokenUpgradeable_init_unchained(address _owner, uint256 _maxPoolTotalSupply) internal initializer {

    }
```

```jsx title="текст"
    function mint(address to, uint256 amount) public override onlyOwner{

    }
```

```jsx title="текст"
    function burn(address from, uint256 amountLiquidity) public override onlyOwner{

}_maxPoolTotalSupply 
```