# Migrating from the Deprecated Avalanche Wallet to AVAX Wallet v0.1.5

The official Avalanche Wallet at wallet.avax.network served as the primary interface for managing AVAX from the network's September 2020 launch through March 2024. When Ava Labs deprecated it in favor of Core, thousands of users were left with seed phrases, keystore files, and staking positions tied to a wallet that no longer exists.

This guide covers how to move from the deprecated wallet to [AVAX Wallet v0.1.5](https://avaxwallet.net/) — what transfers automatically, what requires manual steps, and what to verify after migration.

## What Happened and Why Migration Matters

The [full timeline of the Avalanche Wallet deprecation](https://avaxwallet.net/guides/what-happened-to-avalanche-wallet) is covered in a separate guide. The short version: Ava Labs introduced the Durango network upgrade in February 2024, which changed how staking transactions work on the P-Chain. The original wallet's codebase used AvalancheJS v1, which does not support the new Permissionless Transaction types. Rather than update the old wallet, Ava Labs directed users to Core.

The critical point: your funds never moved. The old wallet was a frontend interface that read blockchain data and signed transactions. Your AVAX remains on the Avalanche network at the same addresses. What you need is a compatible wallet to access those addresses.

[AVAX Wallet v0.1.5](https://avaxwallet.net/download) is built from the same open-source codebase as the original, with the transaction layer rebuilt for Durango compatibility. Same derivation paths. Same keystore format. Same seed phrase support.

## Before You Begin: Gather Your Credentials

You need one of the following from your original Avalanche Wallet:

**24-word mnemonic phrase** — the most reliable recovery method. These 24 words were displayed when you first created the wallet. If you followed the backup instructions, you wrote them down in order.

**Keystore file** — a JSON file you exported from the wallet's settings, encrypted with a password you chose at export time.

**Private key** — a raw key string. Less commonly used by Avalanche Wallet users but supported.

If you have none of these, recovery is not possible. Non-custodial wallets have no server-side backup. The [recovery guide](https://avaxwallet.net/guides/recover-avalanche-wallet) covers each method in detail.

## Migration via Mnemonic Phrase

This is the recommended method. The 24-word mnemonic generates all three chain addresses.

**Step 1.** [Download AVAX Wallet v0.1.5](https://avaxwallet.net/download) for your operating system.

**Step 2.** Launch the application and select Import Wallet.

**Step 3.** Choose Mnemonic Phrase as the import method.

**Step 4.** Enter all 24 words in the correct order. Capitalization does not matter. Spelling does — "receive" and "recieve" generate different wallets.

**Step 5.** Set a new local password to encrypt your keys on this device.

**Step 6.** Your wallet loads. Balances appear across all three chains.

The derivation paths in AVAX Wallet match the original Avalanche Wallet exactly. X-Chain and P-Chain addresses derive from the same path. The C-Chain uses a separate Ethereum-compatible path. Both are restored automatically from one mnemonic — no additional configuration needed.

## Migration via Keystore File

If you exported a keystore file from the original wallet's settings:

**Step 1.** Launch AVAX Wallet and select Import Wallet.

**Step 2.** Choose Keystore File.

**Step 3.** Browse to your JSON keystore file.

**Step 4.** Enter the password you set when you originally exported the file.

If you forgot the keystore password but still have your 24-word mnemonic, use the mnemonic method instead.

## Verifying Your Migration

After importing, check these items:

**All three chain balances.** Your AVAX may be distributed across [X-Chain, C-Chain, and P-Chain](https://avaxwallet.net/avalanche-chains). AVAX Wallet displays all three. If a balance appears on a chain you did not expect, it likely arrived from an exchange withdrawal or a cross-chain transfer you performed previously.

**Staking status.** If you had active delegations on the P-Chain when the old wallet was deprecated, those delegations continued on the blockchain regardless of the wallet shutdown. Completed staking periods will show as returned AVAX plus rewards on your P-Chain balance. Active delegations still in progress will show their remaining time.

The [staking feature page](https://avaxwallet.net/staking) explains how to manage existing delegations and create new ones. Current [staking reward rates and validator selection](https://avaxwallet.net/guides/avax-staking-rewards) are covered in the staking rewards guide.

**C-Chain tokens.** Any ERC-20 compatible tokens you held on the C-Chain (wrapped tokens, stablecoins, DeFi positions) should appear when viewing C-Chain assets. If you [bridged tokens from Ethereum](https://avaxwallet.net/bridge) through the old wallet, those wrapped tokens (.e suffix) remain on your C-Chain address.

**X-Chain address rotation.** The X-Chain generates a new receiving address after each deposit. Previous addresses remain valid. All funds sent to any of your past X-Chain addresses are accessible through the same seed phrase. The wallet aggregates the balance across all derived addresses.

## What About Core Users?

If you already migrated to Core and have been using it, you can still import the same seed phrase into AVAX Wallet. Both wallets derive the same addresses from the same mnemonic. There is no conflict — the blockchain does not care which wallet interface you use to sign transactions.

Some users maintain both: Core for mobile and multichain use, [AVAX Wallet for desktop](https://avaxwallet.net/download) and focused Avalanche management. Using the same seed phrase in multiple wallets is technically fine but increases the number of locations where your recovery phrase is entered, which is a security consideration.

The [wallet comparison page](https://avaxwallet.net/compare) details the functional differences between AVAX Wallet and Core for users deciding which to use as their primary tool.

## Post-Migration: What to Do Next

Once your wallet is verified:

**Stake idle AVAX.** If you have unstaked AVAX sitting on the P-Chain, delegate it to earn approximately 7-8% APR. The [staking guide](https://avaxwallet.net/guides/how-to-stake-avax) walks through the process step by step.

**Consolidate if needed.** If your AVAX is spread across chains, use [cross-chain transfers](https://avaxwallet.net/avalanche-chains) to move it where you need it. C-Chain for DeFi. P-Chain for staking. X-Chain for low-fee transfers.

**Back up again.** Store your seed phrase in a secure offline location. If you only had a keystore file from the old wallet, consider writing down the mnemonic phrase as a more durable backup.

**Explore new features.** AVAX Wallet v0.1.5 includes capabilities not present in the original wallet: the [built-in Ethereum bridge](https://avaxwallet.net/guides/bridge-eth-to-avax), address format validation for wrong-chain prevention, and a [staking calculator](https://avaxwallet.net/avax-price) with real-time AVAX price data.

Review the [complete feature list](https://avaxwallet.net/features) and [FAQ](https://avaxwallet.net/faq) for a full overview.

[Download AVAX Wallet v0.1.5](https://avaxwallet.net/download) · [All Guides](https://avaxwallet.net/guides)

---

### Related Articles
- [AVAX Wallet Security: Non-Custodial Architecture and Key Management](avax-wallet-security-non-custodial-architecture-key-management.md)
- [Why Avalanche Needs a Dedicated Desktop Wallet](why-avalanche-needs-dedicated-desktop-wallet.md)
- [Avalanche Three-Chain Architecture: How X-Chain, C-Chain, and P-Chain Work Together](avalanche-three-chain-architecture-x-c-p-chain.md)
- [Getting Started with AVAX Wallet: Download, Setup, and First Transaction](getting-started-avax-wallet-download-setup-first-transaction.md)
