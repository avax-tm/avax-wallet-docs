# Getting Started with AVAX Wallet: Download, Setup, and First Transaction

This guide walks through every step from downloading [AVAX Wallet](https://avaxwallet.net/) to completing your first transaction on the Avalanche network. Whether you are creating a fresh wallet or importing an existing seed phrase from the deprecated Avalanche Wallet, this covers the full setup process.

## Step 1: Download AVAX Wallet v0.1.5

AVAX Wallet runs natively on Windows, macOS, and Linux. Visit the [download page](https://avaxwallet.net/download) and select your operating system.

Available installers:
- **Windows 10+** — .exe installer
- **macOS 11+** — .dmg disk image
- **Linux** — .zip archive (Ubuntu 20.04+, Debian, Fedora)

The download page displays SHA-256 checksums for each installer. Verifying the checksum against the downloaded file confirms the installer has not been modified in transit.

Important: only download from [avaxwallet.net](https://avaxwallet.net/download). Phishing sites impersonating wallet download pages are common in crypto. Bookmark the URL after your first visit.

## Step 2: Install and Launch

**Windows:** Run the .exe installer. Follow the standard installation wizard. Launch AVAX Wallet from the Start menu or desktop shortcut.

**macOS:** Open the .dmg file. Drag AVAX Wallet to your Applications folder. Launch from Applications. macOS may display a security warning for apps downloaded outside the App Store — open System Preferences > Security & Privacy to allow the app.

**Linux:** Extract the .zip archive to your preferred location. Run the executable from the extracted folder.

On first launch, AVAX Wallet presents two options: Create Wallet or Import Wallet.

## Step 3: Create or Import

### Creating a New Wallet

Select Create Wallet. The application generates a 24-word mnemonic phrase using the BIP-39 standard. This phrase is your sole recovery mechanism — there is no password reset, no customer support override.

**Write down all 24 words in order.** Use paper, not a digital notes app. Store it in a physically secure location separate from your computer. Consider making a second copy stored in a different location.

After writing down the phrase, the wallet will ask you to verify several words by selecting them from a list. This confirms you recorded the phrase correctly.

Set a local password. This password encrypts your keys on disk and is required each time you open the wallet. It is not the same as your seed phrase — the password protects the local copy, the seed phrase recovers the wallet entirely.

### Importing an Existing Wallet

If you have a seed phrase from the [deprecated Avalanche Wallet](https://avaxwallet.net/guides/what-happened-to-avalanche-wallet), MetaMask, or any BIP-39 compatible wallet:

Select Import Wallet, then choose your import method:
- **Mnemonic Phrase** — enter 24 words in order
- **Keystore File** — select JSON file + enter its password
- **Private Key** — paste the key string

The [recovery guide](https://avaxwallet.net/guides/recover-avalanche-wallet) covers each method in detail, including how derivation paths differ between chains.

After import, AVAX Wallet displays your balances across all three Avalanche chains: X-Chain, C-Chain, and P-Chain.

## Step 4: Understand Your Dashboard

The AVAX Wallet dashboard shows:

**Portfolio Overview** — total AVAX holdings across all three chains, converted to USD at the current market rate. The [AVAX price page](https://avaxwallet.net/avax-price) provides detailed market data and a staking calculator.

**My Assets** — individual chain balances:
- X-Chain: AVAX available for transfers
- C-Chain: AVAX and ERC-20 compatible tokens for DeFi
- P-Chain: AVAX staked or available for staking

**Recent Activity** — transaction history across chains including sends, receives, cross-chain transfers, staking events, and contract interactions.

**Network Health** — current TPS, validator count, and network status.

**Staking Rewards** — current APR and quick access to staking management.

Understanding the three-chain balance display is critical. Your AVAX may be on one chain, split across two, or distributed across all three. The [Avalanche chains explanation](https://avaxwallet.net/avalanche-chains) covers what each chain is for and when to use it.

## Step 5: Fund Your Wallet

If you created a fresh wallet, it starts with zero balance. There are several ways to get AVAX into it:

**From an exchange:** Purchase AVAX on Coinbase, Binance, Kraken, or another exchange. Withdraw to your AVAX Wallet address. Select the correct chain when withdrawing — most exchanges support C-Chain withdrawal.

If you withdraw via C-Chain, paste your C-Chain address (starts with 0x). If the exchange offers "Avalanche" withdrawal (X-Chain), paste your X-Chain address (starts with X-avax). The [chain selection guide](https://avaxwallet.net/guides/avax-chains-explained) explains which to choose.

**From Ethereum via bridge:** If you hold ETH or ERC-20 tokens and want them on Avalanche, use the [built-in bridge](https://avaxwallet.net/bridge). The bridge transfers tokens from Ethereum to the Avalanche C-Chain. The [bridging guide](https://avaxwallet.net/guides/bridge-eth-to-avax) compares methods by cost and speed.

**From another wallet:** Send AVAX from any wallet to your AVAX Wallet address on the appropriate chain.

Always send a small test transaction first to verify the address and chain are correct.

## Step 6: Your First Transaction

### Sending AVAX

Navigate to the Send function. Select the source chain (X, C, or P). Enter the recipient address. The wallet validates the address format against the selected chain — if you paste a C-Chain (0x) address while sending from X-Chain, you will see a warning.

Enter the amount. Review the estimated fee. Confirm the transaction.

C-Chain sends arrive within seconds. X-Chain transfers are near-instant with a fixed 0.001 AVAX fee.

### Cross-Chain Transfer

If your AVAX is on the C-Chain but you want to stake (which requires P-Chain), use Cross-Chain Transfer:

1. Select source: C-Chain
2. Select destination: P-Chain
3. Enter amount (keep some AVAX on C-Chain for future gas fees)
4. Confirm

The wallet handles the two-step export/import process automatically. Your AVAX appears on the P-Chain within seconds.

Understanding [cross-chain transfers vs bridging](https://avaxwallet.net/avalanche-chains) prevents confusion: cross-chain moves AVAX within Avalanche. Bridging moves assets between Avalanche and other blockchains.

## Step 7: Stake Your AVAX (Optional)

Once you have AVAX on the P-Chain, you can delegate to a validator:

1. Open the Staking tab
2. Browse validators — sort by uptime, commission, capacity
3. Select a validator with 98%+ uptime and low commission (2-5%)
4. Enter delegation amount (minimum 25 AVAX)
5. Choose staking period (2 weeks to 1 year)
6. Confirm

Your AVAX is locked for the chosen period. Rewards accumulate and are returned to your P-Chain address when the period ends.

The [staking feature page](https://avaxwallet.net/staking) explains the mechanics. The [staking guide](https://avaxwallet.net/guides/how-to-stake-avax) provides detailed validator selection criteria. Current [staking reward rates](https://avaxwallet.net/guides/avax-staking-rewards) are approximately 7-8% APR with no slashing risk.

## What to Explore Next

With your wallet set up and your first transaction complete:

- **[Features overview](https://avaxwallet.net/features)** — everything AVAX Wallet can do
- **[Wallet comparison](https://avaxwallet.net/compare)** — how AVAX Wallet differs from MetaMask, Core, Trust Wallet, Exodus
- **[FAQ](https://avaxwallet.net/faq)** — 28 questions covering staking, chains, bridging, gas fees, and security
- **[About](https://avaxwallet.net/about)** — the project's open-source foundation and security model
- **[All guides](https://avaxwallet.net/guides)** — step-by-step tutorials for every major workflow

[Download AVAX Wallet v0.1.5](https://avaxwallet.net/download)

---

### Related Articles
- [Why Avalanche Needs a Dedicated Desktop Wallet](why-avalanche-needs-dedicated-desktop-wallet.md)
- [Understanding Avalanche Staking: Validators, Delegation, and Rewards](understanding-avalanche-staking-validators-delegation-rewards.md)
- [Migrating from the Deprecated Avalanche Wallet to AVAX Wallet v0.1.5](migrating-deprecated-avalanche-wallet-to-avax-wallet.md)
- [AVAX Wallet Security: Non-Custodial Architecture and Key Management](avax-wallet-security-non-custodial-architecture-key-management.md)
