#  Case Study 01: Delayed L1 ↔ L2 Cross-Chain Bridge Transaction

---

## Customer Issue
> **User Inquiry:** *"I bridged 0.5 ETH from Ethereum Mainnet to Arbitrum One over 2 hours ago using your bridge dApp. The funds disappeared from my Ethereum wallet, but nothing has arrived on Arbitrum! Is my crypto lost?"*

---

## Investigation & On-Chain Diagnostics

[ User Wallet ] ──► (1. Deposit Tx on L1) ──► [ Bridge Smart Contract ] ──► (2. Relayer Delay) ──► [ Wallet on L2 ]

1. **Requested Information:**
   * Sender Wallet Address (`0x...`)
   * Origin Transaction Hash (L1 TxHash)
   * Destination Chain ID / Network Name (Arbitrum One)

2. **Blockchain Explorer Analysis:**
   * **Etherscan Check (L1):** Paste L1 TxHash. Verified status is **`Success`**. Logs show `Deposit` event emitted to the Bridge Contract with correct destination address.
   * **Arbiscan Check (L2):** Paste wallet address. No incoming L2 execution transaction recorded yet.
   * **Bridge Status Page:** Checked native bridge relayer status; network gas surge on Ethereum caused temporary relayer transaction queuing.

3. **Root Cause Analysis:**
   * Funds are safe in the L1 bridge escrow contract. The transaction is delayed due to high L1 gas spikes delaying the relayer bot from submitting the claim on Arbitrum L2.

---

## 📋 Resolution & Action Plan

* **Support Level:** Tier 1 Support
* **Status:** Resolved (Educated User + Verified Safety)
* **Escalation Trigger (if applicable):** Escalate to Tier 2 Tech Ops ONLY if the L1 deposit shows > 6 hours without relayer pick-up.

---

## 💬 Customer-Facing Response

> **Subject:** Update regarding your Arbitrum Bridge Transaction
> 
> Hi there,
> 
> Thank you for reaching out, and don't worry—**your funds are completely safe!**
> 
> I inspected your L1 transaction on Etherscan (`0x...`), and your deposit of 0.5 ETH was successfully received by the bridge smart contract. 
> 
> **Why is it delayed?**
> Due to high traffic on the Ethereum Mainnet right now, the bridge relayer is experiencing a temporary queue while waiting for gas fees to stabilize before executing the final step on Arbitrum.
> 
> **What you can do:**
> 1. You do **not** need to perform any extra transactions or resubmit.
> 2. You can track your L1 deposit status directly on [Etherscan Link].
> 3. Ensure your wallet (MetaMask) is connected to the **Arbitrum One** network to view your tokens once delivered.
> 
> We appreciate your patience! Please reply to this message if your balance does not reflect within the next 2 hours.
> 
> Best regards,  
> Web3 Support Team
