#### This contract implements a proxy that gets the implementation address for each call from a {UpgradeableBeacon}.

### *Code*
### [```BeaconProxy.sol```](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/upgradeable/BeaconProxy.sol)
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
			<td>beacon</td>
			<td></td>
		</tr>
		<tr>
			<td>bytes</td>
			<td>data</td>
			<td></td>
		</tr>
	</tbody>
</table>        

### Developer comment:

#### This abstract contract provides a fallback function that delegates all calls to another contract using the EVM instruction ```delegatecall()```. 
#### We refer to the second contract as the implementation behind the proxy, and it has to be specified by overriding the virtual ```_implementation()``` function. 
#### Roles are referred to by their ```bytes32``` identifier. These should be exposed in the external API and be unique. ###

```jsx title="Returns the current beacon address."
    function _beacon() internal view returns (address beacon) {
    
}
```
```jsx title="Returns the current implementation address of the associated beacon."
    function _implementation() internal view override returns (address) 

{
```

```jsx title="Changes the proxy to use a new beacon."
    function _setBeacon(address beacon, bytes memory data) internal {
    
}
```