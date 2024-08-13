# Using GraphQL with Etherscan APIs

## Getting Started

To begin using the GraphQL Etherscan API, follow these steps:

1. **Clone the Repository**: Clone the repository to your local machine.
2. **Install Dependencies**: Run `npm install` to install the necessary dependencies.
3. **Obtain an Etherscan API Key**: Instructions for creating an API key are detailed below.
4. **Start the Apollo Server**: Follow the instructions below to start the Apollo server.
5. **Execute GraphQL Queries**: Use the sample queries provided below to interact with the server.

## Advantages of the GraphQL API

Wrapping the Etherscan REST APIs in a GraphQL API offers several advantages:

- **Combine Multiple Queries**: Fetch multiple related resources in a single API call.
- **Strong Typing**: Benefit from a robust typing system.
- **Intuitive Language**: Use an easy-to-understand query language.
- **Integrated Documentation**: Access built-in documentation for ease of use.

## Generating an Etherscan API Key

To access Etherscan APIs, you need an API key. Follow these steps to generate one:

1. **Register**: Sign up for an account at [Etherscan](https://etherscan.io/register).
2. **Create API Key**: Navigate to [this page](https://etherscan.io/myapikey) to generate your API key.
3. **Configure Your Environment**: Add the API key to a `.env` file with the entry `ETHERSCAN_API=your_api_key`.

## Overview of GraphQL Etherscan API Endpoints

The GraphQL API wraps the following Etherscan REST endpoints:

- `etherBalanceByAddress`: Retrieve the ETH balance for a specific address.
- `totalSupplyOfEther`: Get the total supply of ETH.
- `latestEthereumPrice`: Fetch the most recent ETH price.
- `blockConfirmationTime`: Obtain the estimated time for block confirmations.

Refer to the `schema.graphql` file for more details.

## Running the Apollo Server

To start the Apollo GraphQL Server, follow these steps:

1. **Open Terminal**: Open your terminal in VSCode.
2. **Start the Server**: Execute `node index.js` to launch the server.
3. **Verify Startup**: Look for the message: 🚀 Server ready at http://localhost:9000/
4. **Access the Server**: Navigate to [http://localhost:9000](http://localhost:9000) in your browser.

## Example GraphQL Query

Here’s a sample GraphQL query to retrieve data from Etherscan:

```graphql
query {
  etherBalanceByAddress {
    message
    result
  }
  totalSupplyOfEther {
    message
    result
  }
  latestEthereumPrice {
    message
    result {
      ethbtc
      ethusd
      ethusd_timestamp
    }
  }
  blockConfirmationTime {
    message
    result
  }
}
```
