# GraphQL With Etherscan APIs

## Getting Started

1. Sign up for a new Etherscan account to generate your API key if you do not have one.
2. Proceed to clone the git repository.
3. Create a new .env file and create a `ETHERSCAN_API` key variable to insert your Etherscan API key value.
4. Run the `$npm install` command to install the necessary dependencies.
5. Run the `$node index.js` command to initialise the GraphQL server and run your queries.

## Benefits of using GraphQL API

- Fetch data from multiple API endpoints in a single query
- Strongly typed schema
- Flexible query parameters

## Create an Etherscan API Key

1. Navigate to Etherscan.io and create a free account
2. Go to API-KEYs tab under your profile and generate a new API key
3. Add the key to your .env file

## Overview of GraphQL Etherscan API endpoints

The GraphQL API wraps the following Etherscan endpoints:

- etherBalanceByAddress - Get ether balance for an address
- totalSupplyOfEther - Get total supply of ether
- latestEthereumPrice - Get latest ethereum price
- blockConfirmationTime - Get block confirmation time

## How to run Apollo Server

Starting the Apollo GraphQL Server:

1. Open your terminal on VSCode
2. Run the following command to start the server: `node index.js`
3. Upon successful startup, you should see this message: 🚀 Server ready at http://localhost:9000/
4. Access the Apollo Server by navigating to http://localhost:9000 on your browser

## Sample GraphQL Query

Below is a sample GraphQL query to fetch the necessary data from Etherscan
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


