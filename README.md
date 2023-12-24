# Metaplex Candy Machine Reference UI

This guide aims to assist you in setting up the user interface (UI) for your Candy Machine, enabling users to mint NFTs using the SPL token you've created. The UI will integrate the SPL token as the payment method, allowing users to mint NFTs by connecting their Phantom wallet.

## Prerequisites

Before initiating the setup process, ensure that you have the following prerequisites:

1. A configured Candy Machine with specific details in its `config.json` file:
   - `price`: 0.01
   - `number`: 10
   - `symbol`: "NB"
   - `sellerFeeBasisPoints`: 500
   - `splTokenAccount`: "Your_SPL_Token_Account_Address"
   - `splToken`: "Your_SPL_Token_Address"
   - `goLiveDate`: "2022-07-24T00:00:00Z"
   - `creators`: an array with creator details

2. A Phantom wallet to be used as the minting wallet.

## Steps

### 1. SPL Token Setup

If not done previously, create the SPL token by following the guidelines in Lesson Three. Remember to note down the SPL token's address.

### 2. Update Candy Machine Configuration

Access the `config.json` file of your Candy Machine and update the following fields:
- `splTokenAccount`: Replace this field with the address of the created SPL token account.
- `splToken`: Replace this field with the address of the SPL token.

### 3. User Interface (UI) Setup

Follow the instructions provided in the "Quick Node: Set Up a Minting Site" tutorial to generate a user interface for your Candy Machine. This UI will enable users to connect their Phantom wallets and mint NFTs by utilizing the SPL token as payment.

### 4. Adjust Minting Logic

Within your SPL project's minting logic (as per Lesson Three), modify the process to mint NFTs to the Phantom wallet address instead of the `fromWallet`. Alternatively, adapt the transfer function to direct the minted NFTs to your Phantom wallet.

### 5. Testing

Thoroughly test the entire setup by transferring or minting your SPL token to one of your Phantom accounts. Then, utilize the created UI to mint NFTs. Ensure that users can successfully mint NFTs by paying with the designated SPL token.

## Conclusion

Following these steps will enable you to set up a Candy Machine UI, allowing users to mint NFTs using the SPL token you've created. Users can connect their Phantom wallets and utilize the designated SPL token for NFT minting from your Candy Machine. Before deploying for public use, thoroughly test the setup to ensure its functionality.
