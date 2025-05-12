# Stacks-Bitcoin Interoperability Smart Contract

## Overview

This project implements a smart contract that enables secure interoperability between the Stacks blockchain and the Bitcoin network, focusing on payment verification and transaction management.

## Features

- Bitcoin Address Registration
- Bitcoin Payment Submission
- Payment Verification
- Payment Refund Mechanism
- Transaction Tracking

## Technical Specifications

### Contract Functions

1. **`register-btc-address`**
   - Allows users to register their Bitcoin addresses
   - Stores the mapping between Stacks addresses and Bitcoin hash160 addresses

2. **`submit-btc-payment`**
   - Submit proof of Bitcoin payments
   - Validates the payment against registered addresses
   - Confirms transactions based on block height

3. **`refund-payment`**
   - Provides a refund mechanism for unconfirmed or timed-out transactions
   - Ensures user funds are protected

4. **`get-registered-btc`**
   - Retrieve registered Bitcoin address for a Stacks address
   - Read-only function for querying address mappings

5. **`get-btc-payment`**
   - Retrieve payment status and details
   - Read-only function for transaction verification

### Key Components

- **`btc-owners`**: Map storing registered Bitcoin addresses
- **`btc-payments`**: Map tracking payment details
- **`total-payments`**: Counter for tracking total transactions
- **`refund-timeout`**: Configurable block height for payment confirmation

## Installation

### Prerequisites

- Stacks development environment
- Clarinet (Stacks smart contract development tool)
- Node.js and npm

### Setup

1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/stx-stack-bitcoin.git
   cd stx-stack-bitcoin
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Compile the smart contract
   ```bash
   clarinet contract build
   ```

## Testing

The project uses Vitest for comprehensive unit testing.

### Running Tests

```bash
npm test
```

### Test Coverage

The test suite covers:
- Bitcoin address registration
- Payment submission
- Payment verification
- Refund mechanisms
- Error handling scenarios

## Security Considerations

- Validates Bitcoin address ownership
- Implements timeout mechanism for payment confirmation
- Provides refund option for unconfirmed transactions

## Use Cases

- Cross-chain payments
- Bitcoin transaction verification
- Secure interoperability between Stacks and Bitcoin networks

## Limitations

- Relies on block height for transaction confirmation
- Requires accurate block height reporting
- Limited to Bitcoin hash160 address format

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Project Link: [https://github.com/emilytom819/stx-stack-bitcoin](https://github.com/yourusername/stx-stack-bitcoin)

## Acknowledgments

- Stacks Blockchain
- Bitcoin Network
- Clarinet Development Tools