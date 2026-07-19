# Alex Zambrano

**Blockchain Engineer in Training** · Solidity · Foundry · Smart Contract Security Testing

Guayaquil, Ecuador · Open to Junior Smart Contract Developer roles

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alexzambrano-web3/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:alchzamb@gmail.com)

---

## About me

Electronics & Telecommunications Engineer (ESPOL) with a Master's in Artificial Intelligence (VIU, Spain), transitioning into Solidity smart contract development after 8+ years of experience teaching technical reasoning and diagnosing problems in engineering and robotics education.

I'm building a security-first Solidity portfolio through the **Blockchain Accelerator** program, using **Foundry** to design and test smart contracts with a focus on:

- Secure design patterns: Checks-Effects-Interactions (CEI), reentrancy protection, safe ERC-20 transfers (SafeERC20), pull-payment accounting
- Automated testing: unit tests, fuzz tests, access-control tests
- Real bug discovery and documentation — not just passing tests, but understanding *why* a contract is safe

I write about what I'm learning and the security decisions behind each project — you'll find the reasoning documented in each repo's README, not just the code.

---

## Featured projects

### 🔄 Swap App — *in progress*

**A Foundry contract integrating Uniswap V2 for token swaps with slippage and deadline protection.**

Building a swap contract on top of `IUniswapV2Router02`, covering `swapExactTokensForTokens`, single- and multi-hop paths, the allowance/approve flow, and `amountOutMin` as slippage protection — with the mempool-level attack surface (sandwich attacks) studied and documented as the reasoning behind those design decisions.

**Demonstrates:** DEX/AMM integration · router trust boundaries · slippage protection · allowance flow
**Stack:** Solidity 0.8.24 · Foundry · Uniswap V2

[Source code](https://github.com/alchzamb/swapping-app-foundry)

---

### 🛒 NFT Marketplace

**A non-escrow NFT marketplace with a full fee system and pull-payment accounting.**

Implements listing, cancellation, and purchase flows using the CEI pattern and indexed events. Includes a basis-point selling fee with a hard-coded cap, a pull-payment pattern for fee withdrawal (`accumulatedFees` / `withdrawFees()`), and a re-validation check at purchase time to close a "ghost listing" vulnerability — stale listings left behind after an NFT is transferred or its approval revoked outside the marketplace.

**Demonstrates:** CEI pattern · pull-payment accounting · stale-state revalidation · fee systems
**Stack:** Solidity 0.8.24 · Foundry · OpenZeppelin v5.x

[Source code](https://github.com/alchzamb/nftmarketplace-foundry)

---

### 🖼️ NFT Collection

**An ERC-721 collection deployed and verified on Arbitrum One.**

IPFS metadata hosted via Pinata, deployed to Arbitrum One (L2), verified on Arbiscan, and listed on OpenSea.

**Demonstrates:** ERC-721 · IPFS metadata · L2 deployment · contract verification
**Stack:** Solidity · Foundry · Arbitrum One

[Source code](https://github.com/alchzamb/nft-collection) · [View on OpenSea](https://opensea.io/)

---

### 💰 Staking App

**An ERC-20 staking contract with reward-accrual accounting.**

Covered by a Foundry unit + fuzz test suite, applying OpenZeppelin v5.x's explicit `initialOwner` pattern.

**Demonstrates:** reward-accrual logic · fuzz testing · access control
**Stack:** Solidity · Foundry · OpenZeppelin v5.x

[Source code](https://github.com/alchzamb/staking-app-foundry)

---

### 🏦 CryptoBank

**A deposit/withdraw contract demonstrating a classic reentrancy vulnerability — and its fix.**

Built around the historical DAO hack context: a `VulnerableBank` contract with the exploit, and a `SafeBank` contract with the CEI pattern and `ReentrancyGuard` applied, with before/after tests proving both the exploit and the patch.

**Demonstrates:** reentrancy vulnerabilities · CEI pattern · exploit-then-patch testing
**Stack:** Solidity · Foundry

[Source code](https://github.com/alchzamb/cryptobank-foundry)

---

### 🧮 Calculadora

**An arithmetic contract with a full Foundry test suite.**

Unit, access-control, overflow, and fuzz tests. Found and fixed a real bug — division by zero silently returning 0 instead of reverting — documented in the README.

**Demonstrates:** fuzz testing · bug discovery and documentation
**Stack:** Solidity · Foundry

[Source code](https://github.com/alchzamb/calculadora-foundry)

---

## Technical focus

| Area | Technologies |
|---|---|
| **Smart contracts** | Solidity, Foundry (Forge, Cast, Anvil, Chisel), OpenZeppelin v5.x, ERC-20 / ERC-721 |
| **Secure contract design** | CEI pattern, ReentrancyGuard, SafeERC20, pull-payment patterns, access control |
| **Testing** | Unit tests, fuzz tests, cheatcodes, `forge coverage`, CI with GitHub Actions (`forge fmt` / `forge test` gates) |
| **DeFi protocols** | Uniswap V2 (router integration, multi-hop paths, slippage protection) |
| **Infrastructure** | Anvil (local node simulation), Cast (JSON-RPC), Arbitrum One, Arbiscan, IPFS (Pinata) |
| **Tools** | Python, Git/GitHub (`gh` CLI), VS Code, Remix IDE, MetaMask |

---

## How I approach engineering

- Understand the concept before implementing it — I don't ship code I can't explain line by line.
- Document the security reasoning, not just the working code: what could go wrong, and why the fix addresses it.
- Be explicit about project maturity — in-progress work is labeled as such, and gaps (missing tests, no audit, no production deployment) are stated directly rather than implied away.
- Treat every project as a learning artifact for whoever reads it next, including future me.

---

## Currently learning

- Uniswap V2 internals (`swapExactTokensForTokens`, router/pair architecture)
- Mempool-level attack surfaces (sandwich attacks, front-running) and how contract-level parameters defend against them

---

## Let's connect

Open to **Junior Smart Contract Developer** and **Blockchain Security** roles.

[LinkedIn](https://www.linkedin.com/in/alexzambrano-web3/) · [alchzamb@gmail.com](mailto:alchzamb@gmail.com)
