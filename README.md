# @thurinlabs/contracts

Solidity library for Thurin SBT verification.

## Installation

### Foundry

```bash
forge install thurinlabs/contracts
```

### npm

```bash
npm install @thurinlabs/contracts
```

## Usage

```solidity
import { IThurinSBT, THURIN_SBT } from "@thurinlabs/contracts/src/interfaces/IThurinSBT.sol";

contract MyDapp {
    function doThing() external {
        require(IThurinSBT(THURIN_SBT).isValid(msg.sender), "Not verified");
        // User is a verified unique human
    }
}
```

## API

### `isValid(address user) → bool`
Check if user has a valid (non-expired) SBT.

### `getExpiry(address user) → uint256`
Get the expiry timestamp for a user's SBT.

### `getMintPrice() → uint256`
Get the current mint price in wei.

### `points(address user) → uint256`
Get user's points balance.

## License

Apache-2.0
