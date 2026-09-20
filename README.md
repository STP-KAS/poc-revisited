> **Experimental only. Not a product.** There is no spendable L1 stable on Kaspa, and no credible alternative on the horizon. Until the unit of account and the sequencing path are settled, production dapps are not a useful allocation of time or capital.
>
> Do not use wallet integrations on this GitHub. STP remains a clown. [DISCLAIMER.md](DISCLAIMER.md)

# PoC revisited

The desk already had the pieces:

- **Parker** — the unit (1 locked sompi)
- **PegLab** — the warning (WILL DEPEG)
- **Ishum** — the pocket (EUR keypad, KAS settlement)
- **Gramlane** — the sequencer bill (grams, wallet closed)
- **sixpack.wtf** — the x402 verdict (native KAS)

What was missing was one working lesson that puts a freeze-capable dollar next to a PoW rail. [grok-heavy-showcase](https://github.com/STP-KAS/grok-heavy-showcase) is that lesson. Grok also reserved a till seat named **kUSD**: a Kaspa dollar *if* someone posts reserves. Not Tether. No free dollar. Not live.

Then BitCoffee0 published [KUSD](https://github.com/bitcoffee0/kusd): a TN10 covenant protocol, KAS-backed, oracle-free by construction.

This repo is the revisit: same problem, two objects, every STP-KAS GitHub mapped.

Showcase: [https://sixpack.wtf/poc.html](https://sixpack.wtf/poc.html)
Review of the protocol: [STP-KAS/kusdt-bitcoffee](https://github.com/STP-KAS/kusdt-bitcoffee)

Not Kaspa core. Not a dollar. Not a token sale.

## Two objects, one name

| | Desk PoC (Ishum / showcase) | BitCoffee KUSD |
| --- | --- | --- |
| What | Till seat. Demo settle. | Covenant protocol. Positions, auctions, KPS. |
| Asset | None | TN10 `a2d81080…f52f32b5` |
| Collateral | “If someone posts reserves” | Native KAS in Position UTXOs |
| Freeze | USDT guest can. Native cannot. | No issuer blacklist in the design |
| Shop-ready | KAS rail yes | No. Unaudited. No wallet pay path |

Do not weld them. Do not mint a third.

## What Grok did, why, sources

**Did:** dual-rail freeze lab; reserved kUSD name so the till would not only speak USDT; refused kUSD as x402 `asset`; kept PegLab as the thing that depegs; bound kaspa-x402 to native KAS; restored original Ishum POS on sixpack.wtf with groks-wallet as receive address; paid a live €2.50 TN10 coffee (`a7a04250…28e7`) and demo-settled kUSD + USDT.

**Why:** dapps sequenced on Kaspa need stable operating costs without importing a freeze king into the unit. Waiting for Tether is waiting for a switch.

**Sources:** Parker kaspa-explained; Ishum; PegLab; Gramlane; sixpack.wtf; Tether blacklist record in grok-heavy-showcase `WHY-NOT-ONLY-TETHER.md`; Sutton on partitioned app state; Luke kaspa-x402; BitCoffee Kas-Smiths post 13 Sep 2026; [X thread](https://x.com/StppStp/status/2099737095065538930).

Kasplex landing USDT/USDC is useful. It imports issuer policy into the money the dapp speaks. If the dapp unit can be frozen, the dapp can be frozen. Proof-of-work cash has held the no-blacklist test since 2009. Kaspa keeps that on native KAS. A KAS-backed covenant dollar is the attempt to keep it while quoting a dollar. BitCoffee is that attempt. It is not done.

## Rails people should be able to choose

1. **Kaspa** — native PoW. Live QR. Always miner fee.
2. **PoC KUSD** — BitCoffee candidate. Demo on the till until wallets pay the Asset ID.
3. **Tether-like** — guest IOU. Labelled. Freeze UX. Never gas.

## Repo map

See [REPOS.md](REPOS.md). Short policy after this pass:

- **Ishum:** KAS live to groks-wallet on TN10. kUSD seat points at BitCoffee as the candidate; still demo. USDT guest labelled.
- **sixpack.wtf:** new tabs (KUSD, PoC, TN10, Rails). x402 remains native KAS.
- **kaspa-x402:** no change. Kill-if KUSD in `asset`.
- **PegLab:** keep WILL DEPEG. BitCoffee’s fixed price can also be a bad price.
- **Gramlane grams:** prepaid mass, not $1.
- **Master file dollars 0–0:** this desk does not issue a dollar. Reviewing BitCoffee is allowed.
- **kaspa-till:** do not grow a fourth till.
- **groks-wallet:** the PoC receive address.
- **wallet-integration:** blocking for a real kUSD rail.

## Capital and keys

| Question | Answer |
| --- | --- |
| Discord / DAGKnight / Rust fund as backing? | No. Users lock KAS. Treasuries may fund audits, not the peg. |
| Core multisig vs covenants? | Covenants hold the money. Humans may veto Modules during bootstrap. Never a freeze key. |

## License

MIT. No warranty.

---

> **Standard disclaimer.** This GitHub, not the topic above.
>
> Intentions are good; thought process is questionable. STP remains delusional. Si vis pacem, para bellum.
>
> Intern at https://sixpack.wtf/  
> X: https://x.com/StppStp · GitHub: https://github.com/STP-KAS
