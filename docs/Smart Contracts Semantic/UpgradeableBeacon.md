### *Code*
### [```UpgradeableBeacon.sol```](https://github.com/dexe-network/dexe-asset-management/blob/js-tests-new-contract-with-pass/contracts/upgradeable/UpgradeableBeacon.sol)
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
			<td>address that can be used as a delegate call target</td>
		</tr>
	</tbody>
</table>        

```jsx title="Returns the current implementation address."

    function implementation() public view override returns (address) {
    }
```
```jsx title="Upgrades the beacon to a new implementation."
    function upgradeTo(address newImplementation) public onlyOwner {

    }
```
```jsx title="Sets the implementation contract address for this beacon."
    function _setImplementation(address newImplementation) private {

    } 




