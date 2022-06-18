# Storage_Factory
This repository represents simple storage factory. It explaines how to import and inheritance contracts. Also, how to override functions.

Deploy StorageFactory to test importing.
Deploy ExstraStotage to test inheritance. Also, it contains example how to override (virtual -> override) functions.

### Inheritance

```
contract ExtraStorage is SimpleStorage {
}
```

### Override

Source:

```
function store(uint256 _favoriteNumber) public virtual {
        favoriteNumber = _favoriteNumber;
    }
```

New

```
function store(uint256 _favoriteNumber) public virtual override {
        favoriteNumber = _favoriteNumber + 5;
    }
```

### Import

```
// SPDX-License-Identifier: MIT

pragma solidity 0.8.8;

import "./SimpleStorage.sol";
```
