# MyToken Smart Contract

This repository contains the Solidity smart contract code for `MyToken`, an ERC-20-like token with minting and burning functionalities. The contract allows for the creation, destruction, and management of tokens on the Ethereum blockchain.

## Contract Details

### Public Variables

- `string public tokenName`: The name of the token (e.g., "Ethereum").
- `string public tokenAbbrv`: The abbreviation of the token (e.g., "ETH").
- `uint public totalSupply`: The total supply of tokens currently in circulation.

### Mappings

- `mapping(address => uint) public balances`: A mapping of addresses to their respective token balances.

### Functions

#### `mint(address to, uint value)`

Increases the total supply of tokens and assigns the newly minted tokens to the specified address.

- `to`: The address to which the tokens will be minted.
- `value`: The number of tokens to mint.

#### `burn(address from, uint value)`

Decreases the total supply of tokens and removes the specified number of tokens from the specified address, given that the address has sufficient balance.

- `from`: The address from which the tokens will be burned.
- `value`: The number of tokens to burn.

### Events

- `event Mint(address indexed to, uint value)`: Triggered when tokens are minted.
- `event Burn(address indexed from, uint value)`: Triggered when tokens are burned.

## Usage

To interact with this contract, you can use Ethereum development environments such as [Remix](https://remix.ethereum.org/), [Truffle](https://www.trufflesuite.com/), or [Hardhat](https://hardhat.org/).

### Deploying the Contract

1. Open Remix or your preferred Solidity development environment.
2. Copy the contract code into a new Solidity file.
3. Compile the contract.
4. Deploy the contract to your desired Ethereum network (e.g., Mainnet, Ropsten, Rinkeby, etc.).

### Interacting with the Contract

After deploying the contract, you can interact with it by calling the `mint` and `burn` functions to manage the token supply. Use the events `Mint` and `Burn` to monitor these actions.

### Example

Here is an example of how to mint and burn tokens using the contract:

```solidity
// Mint 100 tokens to address 0x123...
myToken.mint(0x123..., 100);

// Burn 50 tokens from address 0x123...
myToken.burn(0x123..., 50);
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes or improvements.

## Acknowledgements

This project is inspired by the basic principles of ERC-20 tokens and aims to provide a simple implementation for educational purposes.

## Contact

For any inquiries, please contact [Tanmay Garg] at [gargtanmay32@gmail.com].

