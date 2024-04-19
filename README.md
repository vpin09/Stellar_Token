# Soroban Token Contract

This contract is a sample implementation of the Soroban token interface. It provides functionalities for token minting, setting administrators, managing allowances, transferring tokens, burning tokens, and retrieving token metadata such as name, symbol, and decimals.

## Getting Started

To deploy and interact with this contract, you will need to set up a Soroban environment and have access to the Soroban SDK.

## Features

### Initialize

- **Function:** `initialize`
- **Purpose:** Initializes the token contract with the provided parameters, including the administrator address, decimal precision, token name, and symbol.
- **Access:** Only callable once during contract initialization.
- **Parameters:**
  - `admin`: Address of the administrator.
  - `decimal`: Decimal precision for token amounts.
  - `name`: Name of the token.
  - `symbol`: Symbol of the token.

### Mint

- **Function:** `mint`
- **Purpose:** Mints new tokens and assigns them to a specified account.
- **Access:** Only callable by the administrator.
- **Parameters:**
  - `to`: Address of the recipient.
  - `amount`: Amount of tokens to mint.

### Set Admin

- **Function:** `set_admin`
- **Purpose:** Sets a new administrator for the token contract.
- **Access:** Only callable by the current administrator.
- **Parameters:**
  - `new_admin`: Address of the new administrator.

### Allowance

- **Function:** `allowance`
- **Purpose:** Retrieves the amount of tokens that the spender is allowed to spend on behalf of the owner.
- **Parameters:**
  - `from`: Address of the owner of the tokens.
  - `spender`: Address of the spender.

### Approve

- **Function:** `approve`
- **Purpose:** Approves the spender to spend a specified amount of tokens on behalf of the owner.
- **Access:** Only callable by the owner of the tokens.
- **Parameters:**
  - `spender`: Address of the spender.
  - `amount`: Amount of tokens to approve.
  - `expiration_ledger`: Expiration ledger for the approval.

### Balance

- **Function:** `balance`
- **Purpose:** Retrieves the token balance of a specified account.
- **Parameters:**
  - `id`: Address of the account.

### Transfer

- **Function:** `transfer`
- **Purpose:** Transfers tokens from one account to another.
- **Access:** Only callable by the owner of the tokens.
- **Parameters:**
  - `from`: Address of the sender.
  - `to`: Address of the recipient.
  - `amount`: Amount of tokens to transfer.

### Transfer From

- **Function:** `transfer_from`
- **Purpose:** Transfers tokens from one account to another on behalf of the owner.
- **Access:** Only callable by the approved spender.
- **Parameters:**
  - `spender`: Address of the spender.
  - `from`: Address of the owner of the tokens.
  - `to`: Address of the recipient.
  - `amount`: Amount of tokens to transfer.

### Burn

- **Function:** `burn`
- **Purpose:** Burns a specified amount of tokens from the owner's account.
- **Access:** Only callable by the owner of the tokens.
- **Parameters:**
  - `from`: Address of the token owner.
  - `amount`: Amount of tokens to burn.

### Burn From

- **Function:** `burn_from`
- **Purpose:** Burns a specified amount of tokens on behalf of the owner.
- **Access:** Only callable by the approved spender.
- **Parameters:**
  - `spender`: Address of the spender.
  - `from`: Address of the token owner.
  - `amount`: Amount of tokens to burn.

### Metadata

- **Functions:**
  - `decimals`: Retrieves the decimal precision of the token.
  - `name`: Retrieves the name of the token.
  - `symbol`: Retrieves the symbol of the token.

## Testing

The contract provides unit tests for certain functionalities, including allowance-related functions. These tests can be run using the appropriate testing framework.

## Dependencies

This contract depends on the Soroban SDK and related modules such as `admin`, `allowance`, `balance`, and `metadata`. Ensure that these dependencies are properly installed and configured before deploying the contract.

