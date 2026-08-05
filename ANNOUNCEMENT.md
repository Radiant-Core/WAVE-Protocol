# WAVE Names Now Available in Photonic Wallet

## The DNS of UTXO — All On-Chain, Fully User-Owned

We're excited to announce that **WAVE names** are now live and available directly in **Photonic Wallet**!

---

## What is WAVE?

**WAVE** is a peer-to-peer naming service built natively on the Radiant blockchain. It replaces traditional DNS with a completely decentralized, blockchain-based naming system where names are secured by proof-of-work and owned by you—no registrars, no centralized authorities. Names are registered for a two-year term and renewed permissionlessly on-chain, so abandoned names return to the pool instead of being lost forever.

**Think of it as the DNS of UTXO.**

---

## Key Features

- **All On-Chain** — Every name registration, update, and resolution happens directly on the Radiant blockchain. No external databases. No off-chain dependencies.

- **User Owned** — Your name is a Layer-1 NFT (Claim Token) secured by your private key. No registrar can revoke, censor, or reassign it — only the key holder controls it for the life of its term.

- **Decentralized Resolution** — Names resolve by traversing a prefix tree of transactions from root to Claim Token. No DNS servers required.

- **Human-Readable Payments** — Send and receive Radiant to names like `alice.rxd` instead of long addresses.

- **Mutable Metadata** — Store arbitrary data with your name: payment addresses, avatars, contact info, and custom key-value records.

- **Future: Flexible Zone Records** — DNS-like record types (A, MX, TXT, CNAME) coming in protocol updates. The infrastructure is there.

- **Future: Subdomain Delegation** — Hierarchical name management with delegated subdomains planned for future releases.

---

## How It Works

1. **Registration** — Names are registered as a chain of transactions forming a prefix tree. Each character (a-z, 0-9, hyphen) is a UTXO output.

2. **Claim Token** — The final output is your Claim Token—a Layer-1 NFT proving ownership.

3. **Resolution** — Resolvers traverse the prefix tree from root to your Claim Token, following spends to find the latest unspent output.

4. **Updates** — Modify your name's target address or stored metadata by spending your Claim Token to a new output with updated data.

---

## Name Lifecycle

Names are held for a **two-year term** and renewed on-chain — permissionlessly, with no registrar in the loop:

- **Registration** — a one-time, length-based fee registers the name for two years.
- **Renewal** — any transaction that spends the name's Claim Token and pays the name's registration price to the protocol treasury extends the term. Renewing early never wastes time already paid for: the new term stacks on top of the current expiry (`max(current expiry, now) + 2 years`).
- **Grace period** — after expiry, the owner has a **30-day grace window** in which the name still resolves and can still be renewed.
- **Lapse** — once the grace period passes without renewal, resolution stops and the name returns to the available pool. The next registration becomes the new canonical holder.
- **Voluntary release** — burning the Claim Token releases the name immediately, with no grace period.

Renewal fees use the same length-based tiers as registration and fund continued protocol development. Term-based ownership keeps the namespace healthy: names whose keys are lost or abandoned recycle back to the community instead of being locked forever.

---

## Roadmap

| Status | Feature | Description |
|--------|---------|-------------|
| ✅ Live | Name Registration | Register names 3-63 chars (a-z, 0-9, hyphen) for a 2-year term |
| ✅ Live | Address Resolution | Resolve names to Radiant addresses for payments |
| ✅ Live | Mutable Metadata | Store arbitrary key-value records with names |
| ✅ Live | Renewal & Expiry | On-chain renewals, 30-day grace period, lapsed names return to the pool |
| 🔄 Planned | DNS Records | Structured support for A, MX, TXT, CNAME records |
| 🔄 Planned | Subdomains | Hierarchical delegation (e.g., `pay.alice.rxd`) |
| 🔄 Planned | Multi-Target | Resolve to multiple addresses or services |

---

## Available Now in Photonic Wallet

Photonic Wallet now fully supports WAVE names:

- Register new names directly in the wallet
- Resolve names to addresses for payments
- Update your zone records
- Transfer names to other users
- View and manage your name portfolio

---

## Why WAVE Matters

| Traditional DNS | WAVE Today | WAVE Future |
|---------------|-----------------|-------------|
| Centralized registrars | Decentralized blockchain registration | — |
| Annual renewal fees | One-time registration cost | — |
| DNS server infrastructure | Peer-to-peer resolution | Same infrastructure, more record types |
| Censorable & revocable | Censorship-resistant & immutable | — |
| ICANN controlled | User controlled | User + delegated subdomain control |
| Complex record management | Basic key-value metadata | Full DNS record support |
| Domain leasing | True ownership (NFT) | Ownership with delegation rights |

---

## Get Started

1. Download or open **Photonic Wallet**
2. Navigate to the **WAVE Names** section
3. Search for available names
4. Register your name on-chain
5. Start receiving payments to your human-readable name

---

## Technical Resources

- **Protocol Specification:** [WAVE Protocol Whitepaper](./README.md)
- **Wallet:** [Photonic Wallet](https://github.com/RadiantBlockchain/Photonic-Wallet)
- **Blockchain:** [Radiant](https://radiantblockchain.org)

---

**WAVE: Decentralized naming for a decentralized world.**

*Powered by Radiant. Secured by proof-of-work. Owned by you.*
