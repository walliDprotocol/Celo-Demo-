# User data Verification tool for CELO
> This repo contains the code developed during Celo Camp Batch 7. 

## About the project

WalliD verification toolkit that makes it easy for CELO developers to customize and add seamless verification flows in their dApps based on Celo network assets (ERC-20s, NFTs, SBTs), Social IDs, Government IDs and We3 IDs.
With it, developers can easily config verification parameters based on IDs or on-chain data and add a seamless flow to their frontends that supports those verifications, while keeping users' privacy.

<b>Ultimately, WalliD can be used for sybil resistence, compliance, trust scores, gated access and much more </b> 


## What we're building during Celo Camp?

During the camp WalliD is developing the libs and the modal to connect users' wallets and verify digital IDs and Celo assets' ownership.

- Add Celo RPC, ecossystem wallets and token standards to our aggregator to make them avaiable in verification configs (check our core-config repo)
- Create Libraries to support the integration of the verification Modal in clients' systems
- Develop Frontend code of the Modal with default WalliD UI


## How to test it

>The demo website is currently using a default config created by WalliD team. You can create try different config parameters in this repo.

 1. Launch demo website [here](https://wallid-demo-celo.herokuapp.com/) that simulates a dApp using WalliD verification tool;
 2. Click `WalliD connector`to launch WalliD verification Modal.
 3. Select one of the data sources available
 4. Complete the verification process for each data source selected



## Launch Verification modal in your development environment

You can also integrate and launch the verification modal in your own environment to create customized verification flows.

### Build and deploy

To utilize it within a development environment, the implementation involves employing the `dotenv` module, which allows for the utilization of a .env file to incorporate the subsequent environment variables.

 Here's an example of how the .env file with variables

```
VUE_APP_BACKEND_URL=<backend_url>
VUE_APP_NEAR_SOCIAL_CONTRACT_TESTNET=<contract_address>
VUE_APP_NEAR_SOCIAL_CONTRACT=<social_contract>
VUE_APP_NEAR_NETWORK_TESTNET=testnet
VUE_APP_NEAR_NETWORK=mainnet

# pubnub env vars
VUE_APP_PUBNUB_USER_ID=<pubnub_id>
VUE_APP_PUBNUB_SUBSCRIBE_KEY=<PUBNUB_SUBSCRIBE_KEY>
VUE_APP_PUBLISH_KEY=<PUBLISH_KEY>
```


Install depencies

```
npm install
```

build frontend

```
npm run generate
```

run frontend

```
npm run start
```

## Environment variables

```
BACKEND_URL=<backend_url>
DISCORD_AUTH=<redirect discord url>
DISCORD_GUILD_ID=<discord_server id>
TWITTER_ACCOUNT=<username of account to check follow>
TWITTER_ACCOUNT_ID=<account id of account to check follow>
TWITTER_POST_ID=<post id>
```
