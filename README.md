# User data verification tool for CELO

> This repo contains the code developed during Celo Camp Batch 7.

## About the project

WalliD is a verification toolkit that makes it easy for CELO developers to customize and add seamless verification flows to their dApps based on Celo network assets (ERC-20s, NFTs, SBTs), Social IDs, Government IDs and We3 IDs.
With it, developers can easily config verification parameters based on IDs or on-chain data and add a seamless flow to their frontends that supports those verifications, while keeping users' privacy.

<b>Ultimately, WalliD can be used for sybil resistence, compliance, trust scores, gated access and much more </b>

![image](https://github.com/walliDprotocol/celo-demo/assets/39834004/70b15199-6742-48ba-8ac3-78488366c51f)

## What we built during Celo Camp?

During the camp WalliD developed the libs and the iframe to connect users' wallets and verify digital IDs and Celo assets' ownership.

- Add Celo RPC, ecossystem wallets and token standards to our aggregator to make them avaiable in verification configs (check our [`core-config`](https://github.com/walliDprotocol/core-config) repo).
- Create Libraries to support the integration of the verification iframe in client systems.
- Develop Frontend code of the iframe with default WalliD UI.

## How to test it

> The demo website is currently using a default config created by WalliD team. You can create try different config parameters in this repo.

1. Launch demo website [here](https://wallid-demo-celo.herokuapp.com/) that simulates a dApp using WalliD verification tool for their users.
2. Click on “claim now” button to launch WalliD verification Modal.
3. At the first step, connect to the twitter to verify account;
4. And at the last step, connect to Metamask wallet account to verify your tokens ownership. Select Metamask wallet and accept the connection request. You will be asked to change to “Alfajores network”. Please make sure that you own some tokens, otherwise you won’t be able to finish the process.

## Launch Verification modal in your development environment

> You can also integrate and launch the verification iframe in your own environment to create customized verification flows.

### Build and deploy

To utilize it within a development environment, the implementation involves employing the `dotenv` module, which allows for the utilization of a `.env` file to incorporate the subsequent environment variables.

Here's an example of the `.env` file:

```
VUE_APP_BACKEND_URL=<backend_url>

pubnub env vars:
VUE_APP_PUBNUB_USER_ID=<pubnub_id>
VUE_APP_PUBNUB_SUBSCRIBE_KEY=<PUBNUB_SUBSCRIBE_KEY>
VUE_APP_PUBLISH_KEY=<PUBLISH_KEY>
```

### Install depencies

```
npm install
```

### build frontend

```
npm run generate
```

### run frontend

```
npm run start
```

## Environment variables

```
BACKEND_URL=<backend_url>
DISCORD_AUTH=<redirect discord url>
DISCORD_GUILD_ID=<discord_server id>
TWITTER_ACCOUNT=<username of account to check nr of followers>
TWITTER_ACCOUNT_ID=<account id of account to check number of followers>
TWITTER_POST_ID=<post id>
```
