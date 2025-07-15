#  Graphite Dev Starter Kit — All-in-One Trust-First SDK & Network Guide

> The official all-in-one starter kit for building **trust-first decentralized applications** on the Graphite Network using the `@atgraphite/web3-plugin`.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D16.0.0-brightgreen)](https://nodejs.org/)
[![Web3.js](https://img.shields.io/badge/Web3.js-Compatible-blue)](https://web3js.org/)

---

<div align="center">
  <h3>✅ Connect to Graphite • 🧱 Build Trust-First dApps • 🚀 Ship Real Products</h3>
</div>

---

## 👋 Welcome

Welcome to the Graphite Dev Starter Kit — your all-in-one hub for building decentralized applications with built-in trust and reputation systems.

Instead of treating all users equally, your dApps can make intelligent decisions based on verified identity and trust scores.

Whether you're a beginner, a hackathon builder, or a team going into production, this repo gives you everything you need to launch powerful dApps on Graphite.

---

## ⚙️ Network Setup (Graphite Testnet)

### ✅ Add Graphite Network to MetaMask

| Setting          | Value                                              |
|------------------|----------------------------------------------------|
| **Network Name** | Graphite Testnet                                   |
| **RPC URL**      | https://anon-entrypoint-test-1.atgraphite.com     |
| **Chain ID**     | 54170                                              |
| **Currency**     | @G                                                 |
| **Explorer**     | https://test.atgraphite.com                        |

<details>
<summary>📱 Step-by-step MetaMask Setup</summary>

1. Open MetaMask and click the network dropdown  
2. Click **Add Network**
3. Choose **Add Network Manually**
4. Fill in the details above
5. Click **Save**
</details>

---

### 🪙 Get Test Tokens

You’ll need @G tokens to interact with Graphite Testnet.

- 💧 Visit the [Graphite Faucet](https://faucet.atgraphite.com)
- Paste your wallet address
- Receive free test tokens

---

## 🔧 Development Environment

### Setup Instructions

```bash
# 1. Clone the repository
git clone https://github.com/your-org/graphite-dev-starter-kit.git
cd graphite-dev-starter-kit

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env
# Edit .env with your API keys (instructions included in file)

# 4. Run the lending app example
node examples/lending-app.js

# 5. Run the marketplace app example  
node examples/marketplace-app.js
```

---

## 📁 Project Structure

```bash
graphite-dev-starter-kit/
├── src/
│   └── GraphiteClient.js          # Core client powered by Web3.js and @atgraphite/web3-plugin
├── examples/
│   ├── lending-app.js             # Trust-based lending demo
│   └── marketplace-app.js         # Seller verification demo
├── .env.example                   # Pre-configured environment template
├── package.json                   # Dependencies and scripts
└── README.md                      # You are here!
```

---

## 🔧 Environment Setup

Your `.env` file should include:

```env
# Wallet configuration
PRIVATE_KEY=your_private_key_here

# Graphite network endpoints
GRAPHITE_NODE_URL=https://anon-entrypoint-test-1.atgraphite.com
GRAPHITE_API_URL=https://api.main.atgraphite.com/api

# Optional: Custom contract addresses
LENDING_CONTRACT_ADDRESS=0x...
MARKETPLACE_CONTRACT_ADDRESS=0x...
```

> 🔒 **Security Note:** Never commit your private key to GitHub or share it publicly.

---

## 💡 Trust-First dApp Examples

### 🏦 Trust-Based Lending App

```javascript
// Run: node ending-app.js
const graphite = new GraphiteClient();

// Check borrower's trust score before approving loan
const borrower = await graphite.getUser('0x...');
if (borrower.trustScore > 750) {
    // Approve loan with favorable terms
    console.log('✅ Loan approved - high trust score');
} else {
    // Request additional collateral or deny
    console.log('⚠️ Additional verification required');
}
```

---

### 🛒 Marketplace with Seller Verification

```javascript  
// Run: node marketplace-app.js
const graphite = new GraphiteClient();

// Verify seller before listing expensive items
const seller = await graphite.getUser('0x...');
const isVerified = await graphite.isKYCVerified(seller.address);

if (isVerified && seller.trustScore > 600) {
    console.log('✅ Verified seller - can list high-value items');
} else {
    console.log('📝 Basic seller - limited to small transactions');
}
```

---

## 🎓 Learning Goals

By working through this starter kit, you'll learn:

- **Trust Integration**: How to query and use trust scores in your dApp logic
- **KYC Verification**: Implementing identity checks without storing personal data
- **Risk Assessment**: Building algorithms that adapt to user reputation
- **Web3 Best Practices**: Clean patterns for blockchain application development
- **Graphite Network**: Understanding the trust layer and its capabilities

---

## 📚 Developer Resources

| Resource | URL | Description |
|----------|-----|-------------|
| Documentation | https://docs.atgraphite.com/ | Official developer documentation |
| Block Explorer | https://test.atgraphite.com | Search transactions, blocks, and addresses |
| Faucet | https://faucet.atgraphite.com | Get testnet tokens |
| Plugin | https://www.npmjs.com/package/@atgraphite/web3-plugin | Official Web3 SDK |

---

## 🤝 Contributing

We welcome contributions from the community!

### 💡 What to Contribute

- New trust-first dApp examples  
- Documentation improvements  
- Dev utilities or CLI tools  
- Testing scripts or deployment helpers  

### 📦 How to Contribute

1. **Fork** the repository  
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`  
3. **Add** your example or improvement  
4. **Test** your changes with both example apps  
5. **Commit** with clear messages: `git commit -m 'Add: new trust scoring example'`  
6. **Push** to your branch: `git push origin feature/amazing-feature`  
7. **Open** a Pull Request

---

## 👨‍👩‍👧‍👦 Support & Community

- 📖 **Docs**: https://docs.atgraphite.com  
- 💬 **Discord**: https://discord.gg/k6kNNeQGv7  
- 🚀 **Telegram**: https://t.me/+Fwq1LXJqf2Q1ZWE0  
- 🐦 **Twitter**: https://twitter.com/GraphiteNetwork  
- 📧 **Email**: support@graphite.com  

---

## 📜 License

This repository is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

## 🙌 Acknowledgments

- Built on the robust foundation of **Web3.js**
- Powered by **Graphite Network**'s trust infrastructure
- Inspired by the amazing **Web3 developer community**

---

**Want help, updates, or to connect with other builders?**  
👉 [Join the Graphite Developer Community on Telegram](https://t.me/+Fwq1LXJqf2Q1ZWE0)

Or check out our [documentation](https://docs.atgraphite.com) to start building today!
