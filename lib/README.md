
![StreamPay Logo](streampay-logo.png)

# StreamPay Web3 Node.js Library

The Stream**Pay** Node.js library allows you to easily integrate StreamPay's payment processing capabilities into your Node.js applications. With this library, you can handle payments on the Solana blockchain and streamline your e-commerce platform's payment processing.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Features](#features)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

Install the Stream**Pay** Node Web3.js library using npm or yarn:

```shell
npm install stream-pay-web3.js
# or
yarn add stream-pay-web3.js
```

## Usage

Here's a basic example of how to use the Stream**Pay** node library to process web3 payments:

```javascript
const streamPay = require('streampay-node');

// Initialize StreamPay with your configuration
const config = {
  solanaNetwork: 'devnet',
  // Add other StreamPay configuration options here
};

const paymentProcessor = new streamPay.PaymentProcessor(config);

// Create a payment intent
const orderTotal = 100; // Replace with your actual order total
const paymentIntent = paymentProcessor.createPaymentIntent(orderTotal);

// Process the payment
paymentProcessor.processPayment(paymentIntent)
  .then((result) => {
    // Handle successful payment
    console.log('Payment successful:', result);
  })
  .catch((error) => {
    // Handle payment error
    console.error('Payment error:', error);
  });
```

## Configuration

To use the Stream**Pay** library, you need to configure it with your Solana network settings and other options. You can do this by creating a configuration object and passing it to the `PaymentProcessor` constructor.

```javascript
const config = {
  solanaNetwork: 'devnet',
  // Add other StreamPay configuration options here
};

const paymentProcessor = new streamPay.PaymentProcessor(config);
```

For detailed configuration options, refer to the [Configuration Documentation](docs/configuration.md).

## Features

- **Solana Integration**: Seamlessly integrate with the Solana blockchain for secure and fast payment processing.
- **Merchant Wallet Management**: Create and manage merchant wallets easily with built-in functions.
- **Fee Calculation**: Calculate merchant fees and Solana transaction fees based on your business logic.
- **MedusaJS Integration**: Integrate StreamPay with MedusaJS for a complete e-commerce solution (optional).

For a detailed list of features and capabilities, visit our [Features Documentation](docs/features.md).

## Examples

Check out the [examples](https://) directory for more usage examples and integration with MedusaJS.

## Contributing

Welcome contributions from the community. If you'd like to contribute to the Stream**Pay** Node.js library, please review our [Contribution Guidelines](CONTRIBUTING.md).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
