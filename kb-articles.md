#  Knowledge Base & Troubleshooting Guides (SOP)

---

##  Article 01: Fixing "Wrong Network / RPC Failures"
* **Category:** Wallets / RPC
* **Symptoms:** dApp displays "Wrong Network Connected" or balance fails to load.

### Step-by-Step Fix:
1. Open MetaMask / Wallet settings -> **Networks**.
2. Select target network (e.g., Polygon / Arbitrum / Base).
3. If network fails to respond, update the **RPC URL** to a reliable public endpoint via [Chainlist.org](https://chainlist.org).
4. Refresh dApp browser tab and clear cache (`Ctrl + F5`).

---

##  Article 02: Missing NFT Metadata on Marketplaces
* **Category:** NFTs
* **Symptoms:** Purchased NFT shows as a blank box or "Content Not Available" on OpenSea/Blur.

### Step-by-Step Fix:
1. Open the NFT item page on OpenSea.
2. Click the **"Refresh Metadata"** button at the top right corner.
3. Wait 2–5 minutes for IPFS gateway indexing.
4. If image remains broken, verify IPFS URI status via Pinata IPFS gateway tracker.
