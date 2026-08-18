#  Case Study 03: Malicious Token Allowance & Phishing Triage

---

##  Customer Issue
> **User Inquiry:** *"I clicked an official-looking AIRDROP link on Twitter/X, connected my wallet, and now 1,000 USDT suddenly disappeared from my balance! Did I get hacked? Can you reverse the transaction?"*

---

##  Investigation & On-Chain Diagnostics

1. **Requested Information:**
   * Affected Wallet Address
   * Transaction Hash (TxHash) of the unexpected outgoing transfer
   * URL of the site visited

2. **Blockchain Explorer & Allowance Audit:**
   * **Etherscan Approval Audit:** Searched wallet on Etherscan Token Approvals tool. Identified an active `SetApprovalForAll` / `Unlimited Allowance` granted to an unverified spender contract (`0xBAD...`).
   * **Transaction Log Inspection:** The malicious dApp tricked the user into signing an `eth_signTypedData` or `IncreaseAllowance` transaction, allowing the attacker contract to call `transferFrom()` and drain funds remotely.

3. **Immutability Assessment:**
   * Transactions on public blockchains are irreversible. Support cannot undo or roll back on-chain transactions.

---

##  Resolution & Action Plan

* **Support Level:** Tier 1 Support (Triage & Containment) → Tier 3 Security (Domain Blacklisting)
* **Status:** Contained & Escalated
* **Immediate Mitigation:** Guide user to revoke active token allowances to prevent further loss of remaining assets.

---

##  Customer-Facing Response

> **Subject:** URGENT: Security Assessment & Wallet Containment
> 
> Hi there,
> 
> I am very sorry to hear about this situation. I have analyzed your wallet address on the blockchain to inspect what occurred.
> 
> **What Happened:**
> The website you interacted with contained a malicious contract script. When connected, you signed an **Unlimited Token Approval**, which granted the spender address permission to withdraw USDT directly from your wallet.
> 
> **CRITICAL IMMEDIATE STEPS:**
> 1. **Revoke Active Approvals Immediately:**
>    * Go to **[Revoke.cash](https://revoke.cash)** or **[Etherscan Token Approvals](https://etherscan.io/tokenapprovalchecker)**.
>    * Connect your wallet and **Revoke/Cancel** all active allowances for USDT and other tokens immediately.
> 2. **Abandon This Wallet for Future Storage:**
>    * Because this wallet's approval state was compromised, we strongly recommend creating a **brand new wallet** with a new seed phrase and moving remaining assets there.
> 
> **Can funds be returned?**
> Due to the decentralized and immutable nature of blockchain technology, transactions cannot be paused, reversed, or refunded once confirmed on-chain.
> 
> We have submitted the phishing URL to our Security Team to block it across our app's security blacklist.
> 
> Stay safe,  
> Web3 Support Team
