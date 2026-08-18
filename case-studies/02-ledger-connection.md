# Case Study 02: Ledger Hardware Wallet Connection & Blind Signing Errors

---

## Customer Issue
> **User Inquiry:** *"I'm trying to swap USDC for ETH on Uniswap using my Ledger Nano S via MetaMask, but the transaction fails instantly with 'User Rejected' or keeps freezing at the signing prompt."*

---

## Investigation & On-Chain Diagnostics

1. **Requested Information:**
   * Hardware Wallet Model & Firmware Version
   * MetaMask Extension Version & Browser (Chrome/Brave)
   * Error message screenshot/logs from Browser Console (`F12 -> Console`)

2. **Diagnostic Protocol:**
   * **Ledger Live Conflicts:** Verified if Ledger Live application is actively running in the background (holds HID device connection priority).
   * **App Configuration:** Checked if "Blind Signing" (formerly Contract Data) is enabled inside the Ethereum app on the physical Ledger device.
   * **Derivation Path:** Verified if the user recently imported a custom RPC or derivation path setting in MetaMask.

3. **Root Cause Analysis:**
   * Swapping tokens on a Decentralized Exchange (DEX) like Uniswap requires signing complex smart contract payload data. By default, Ledger disables **Blind Signing** for security, causing the device to reject DEX interaction payloads automatically.

---

## Resolution & Action Plan

* **Support Level:** Tier 1 Support
* **Status:** Resolved (Configuration Guidance)

---

## Customer-Facing Response

> **Subject:** Resolving Uniswap & Ledger Transaction Signing
> 
> Hi there,
> 
> Thanks for contacting support! This issue usually happens when smart contract signing permissions are disabled on your physical Ledger device.
> 
> Please follow these quick troubleshooting steps to resolve it:
> 
> **Step 1: Close Ledger Live**
> * Ensure the **Ledger Live** app is completely closed on your computer, as it can conflict with browser extensions like MetaMask.
> 
> **Step 2: Enable "Blind Signing" on your Ledger**
> 1. Connect and unlock your Ledger device.
> 2. Navigate to the **Ethereum (ETH)** app on your device screen.
> 3. Go to **Settings** -> **Blind Signing**.
> 4. Change setting from *Disabled* to **Enabled** (Press both buttons to select).
> 
> **Step 3: Clear Browser Cache & Retry**
> * Refresh the Uniswap tab, reconnect via MetaMask, and initiate the swap again.
> 
> 🛡️ **Security Reminder:** *Our support team will NEVER ask for your 24-word Recovery Phrase or Private Keys. Keep them private and secure at all times!*
> 
> Let me know if you run into any further prompts!
> 
> Best regards,  
> Web3 Support Team
