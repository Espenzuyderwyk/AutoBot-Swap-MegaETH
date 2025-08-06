# Automated ETH ⇄ cUSD Swapping Bot for MegaETH (GTE DEX)

This Node.js bot automatically swaps between ETH and cUSD on GTE DEX (MegaETH). It uses randomized amounts, intervals, and transaction volumes to simulate realistic on-chain activity, making it ideal for testing, analytics, or stress simulations on the MegaETH network.

<img width="1200" height="675" alt="image" src="https://github.com/user-attachments/assets/46e117c6-e8e4-4225-8ee6-937ea13728ec" />

## Features:

- Two-way swaps: ETH → cUSD and cUSD → ETH via GTE DEX.
- Randomized trade sizes.
- Organic timing: Random delays (10–60 seconds) between swaps.
- Dynamic daily volume: 10,000–100,000 swaps per run.
- Allowance handling: Automatically resets and updates allowances for each cUSD → ETH swap.
- Customizable gas fees: Configure maxFeePerGas and maxPriorityFeePerGas.
- Detailed logging: Timestamps, TX hashes, and error handling for every swap.

## Installation & Setup:

Clone the project and install dependencies:

```bash
screen -S MegaETH
```

```bash
git clone https://github.com/Espenzuyderwyk/AutoBot-Swap-MegaETH.git
```

```bash
cd AutoBot-Swap-MegaETH
```

```bash
npm install
```

## ⚙️ Environment Setup
Create a .env file in the root directory:

```bash
nano .env
```

Input your private key and wallet address

```bash
RPC_URL=https://carrot.megaeth.com/rpc
PRIVATE_KEY=0xYour_PrivateKey
MY_ADDRESS=0xYour_Wallet_Address
ROUTER_ADDRESS=0xa6b579684e943f7d00d616a48cf99b5147fc57a5
WETH_ADDRESS=0x776401b9bc8aae31a685731b7147d4445fd9fb19
CUSD_ADDRESS=0xe9b6e75c243b6100ffcb1c66e8f78f96feea727f
```

Ctrl + X -> Y -> Enter

## ▶️ Run the Bot
Start

```bash
node index.js
```

## How It Works

1. Picks a random direction: ETH → cUSD or cUSD → ETH.
2. Generates a random swap amount within the configured range.
3. Executes the swap via GTE DEX Router on MegaETH.
4. Waits for a random delay before the next transaction.
5. Repeats until all daily swaps are completed.

## Disclaimer

This script is created for educational and personal experimentation purposes. It is not to be used for illegal activities, spam, or violations of GitHub rules.

- Be mindful of gas fees, slippage, and token volatility.
- This script is intended for testing and simulation purposes only.
- Use of this script is entirely the responsibility of the user.
- Do not use it to violate GitHub's Terms of Service.

#MegaETH #GTE
