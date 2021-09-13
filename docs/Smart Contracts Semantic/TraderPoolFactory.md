### *Code*
### [```TraderPoolFactory.sol```](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/TraderPoolFactoryUpgradeable.sol)
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
			<td>_admin</td>
			<td>dexeAdmin</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_traderContractBeaconAddress</td>
			<td>traderContractAddress</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_pltBeaconAddress</td>
			<td>PoolLiquidityTokenAddress</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_paramkeeper</td>
			<td>token, which is implemented from the white list in IParamStorage</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_positionToolManager</td>
			<td></td>
		</tr>
		<tr>
			<td>address</td>
			<td>_weth</td>
			<td>address of wrapped eth</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_dexeAdmin</td>
			<td></td>
		</tr>
	</tbody>
</table>

```jsx title="text"
modifier onlyAdmin() {

    }
```

```jsx title="инициализирует трейдеров в пуле"
  function initialize() public initializer {

  }
```

```jsx title="инициализирует адрес контракта трейдера"
  function setTraderContractBeaconAddress(address _traderContractBeaconAddress) public onlyAdmin {
  
  }
```

```jsx title="администратор dexe network"
  function setDexeAdminAddress(address _dexeAdmin) public onlyAdmin {
  }
```

```jsx title="создает контракт трейдера"
  function createTraderContract() public returns (address)
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
			<td>_traderWallet</td>
			<td>trader's wallet</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_basicToken</td>
			<td>basicToken for trader contract</td>
		</tr>
		<tr>
			<td>uint256</td>
			<td>_totalSupply</td>
			<td>maxTotalSupply of Trader Contract liquidity token</td>
		</tr>
		<tr>
			<td>uint16</td>
			<td>_comm</td>
			<td>commissions</td>
		</tr>
		<tr>
			<td>bool</td>
			<td>_actual</td>
			<td>flag for setting up "actual portfolio"</td>
		</tr>
		<tr>
			<td>bool</td>
			<td>_investorRestricted</td>
			<td>flag to enable investor whitelist</td>
		</tr>
		<tr>
			<td>string</td>
			<td>_name</td>
			<td>Trader ERC20 token name</td>
		</tr>
		<tr>
			<td>string</td>
			<td>_symbol</td>
			<td>Trader ERC20 token symbol</td>
		</tr>
	</tbody>
</table>

```jsx title="функция возвращает адрес страхового фонда"
  function getInsuranceAddress() public view returns (address) {
  }
```

```jsx title="возвращает адрес на который переводится комиссия dexe network"
  function getDexeCommissionAddress() public view returns (address) {
  }
```
