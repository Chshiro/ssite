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


```jsx title="инициализирует аккаунты участников социального трейда и фиксирует их в storage"
function setParamAddress(uint16 _key, address _value) public onlyManager {
  
}

function setParamUInt256(uint16 _key, uint256 _value) public onlyManager {
}
```

```jsx title="swap to pool"
function setAssetAutomaticExchangeManager(address _address) public onlyManager {
}
```

```jsx title="создание пары"
function setAssetValuationManager(address _address) public onlyManager {=
}
```

```jsx title="swap to pool"
function addAssetManager(address _manager) public onlyManager {=

}
```

```jsx title="добавление менеджера"
function removeAssetManager(address _manager) public onlyManager {=

}
```

```jsx title="удаляет менеджера"
function whitelistToken(address _token) public onlyManager {=

}
```
```jsx title="вставить текст(хуй)"
function delistToken(address _token) public onlyManager {=

}
```


