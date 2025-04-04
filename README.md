# Ntekearning

Guide How to Deploy Seismic Devnet Contract

Pre-Requirements
1. Install Rust
curl https://sh.rustup.rs -sSf | sh  
. "$HOME/.cargo/env"
Verify Installation

rustc --version
2. Install jq
For WSL/Ubuntu

sudo apt install jq
For Mac

brew install jq
3. Install sfoundryup
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
4. Run sfoundryup
sfoundryup
🔺This Process can take a while to fully download

Deploy an encrypted contract 🎶
1. Clone & Navigate to The Repo
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
2. Deploy contract (Follow all instructions here)
bash script/deploy.sh
This script will generate a wallet and promt a Faucet Url and the wallet address of that wallet! You have to take the faucet and Done✅

Interact with an encrypted contract 🤖
1. Navigate to home directory:
cd $home
2. Install Bun
curl -fsSL https://bun.sh/install | bash
3. Install node dependencies
cd try-devnet/packages/cli/
bun install
4. Send transactions
bash script/transact.sh

