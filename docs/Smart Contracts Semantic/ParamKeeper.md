### *Code*
### [```ParamKeeper.sol```](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/ParamKeeper.sol)

#### *Parameter's table*
<table class="iksweb">
	<tbody>
		<tr>
			<th>Type</th>
            <th>Name</th>
		</tr>
		<tr>
			<td>uint16</td>
			<td>_key</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_value</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_address</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_manager</td>
		</tr>
		<tr>
			<td>address</td>
			<td>_token</td>
		</tr>
	</tbody>
</table>


```jsx title="initializes accounts of social trade participants and fixes them in storage"
function setParamAddress(uint16 _key, address _value) public onlyManager {
  
}

function setParamUInt256(uint16 _key, uint256 _value) public onlyManager {
}
```

```jsx title="swap to pool"
function setAssetAutomaticExchangeManager(address _address) public onlyManager {
}
```

```jsx title="creating a pair"
function setAssetValuationManager(address _address) public onlyManager {=
}
```

```jsx title="adding an asset manager"
function addAssetManager(address _manager) public onlyManager {=

}
```

```jsx title="removing an asset manager"
function removeAssetManager(address _manager) public onlyManager {=

}
```

```jsx title="includes a token in the white list"
function whitelistToken(address _token) public onlyManager {=

}
```
```jsx title="excludes a token from the white list"
function delistToken(address _token) public onlyManager {=

}
```


