# Ntekearning

Here’s a cleaned-up and well-formatted version of your **Seismic Devnet Contract Deploy Guide** suitable for a GitHub README:

---

# Seismic Devnet Contract Deploy Guide

## Pre-Requirements

### 1. Install Rust
```bash
curl https://sh.rustup.rs -sSf | sh
. "$HOME/.cargo/env"
```

**Verify Installation**
```bash
rustc --version
```

---

### 2. Install `jq`

**For WSL/Ubuntu**
```bash
sudo apt install jq
```

**For macOS**
```bash
brew install jq
```

---

### 3. Install `sfoundryup`
```bash
curl -L \
  -H "Accept: application/vnd.github.v3.raw" \
  "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```

---

### 4. Run `sfoundryup`

```bash
sfoundryup
```

**Note:** This process can take a while to fully download.

---

## Deploy an Encrypted Contract 🎶

### 1. Clone & Navigate to the Repo

```bash
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```

### 2. Deploy the Contract

```bash
bash script/deploy.sh
```

This script will:
- Generate a wallet
- Prompt a faucet URL and the wallet address  
- Use the faucet to fund the wallet, and you're done ✅

---

## Interact with an Encrypted Contract 🤖

### 1. Navigate to Home Directory

```bash
cd $HOME
```

### 2. Install Bun

```bash
curl -fsSL https://bun.sh/install | bash
```

---

### 3. Install Node Dependencies

```bash
cd try-devnet/packages/cli/
bun install
```

---

### 4. Send Transactions

```bash
bash script/transact.sh
```

---

Let me know if you’d like this as a Markdown file or if you want a badge/status section added.
