# dedicated server hosting london: real prices from £49/mo, the fine print most listings skip, and when RackNerd's US bare metal makes more sense

People searching for a dedicated server in London usually want one of three things: low latency to UK users, UK data residency, or both. The good news is that genuine bare metal in the city costs less than its reputation suggests. The verified entry points sit at **£49/month** (Glitch Servers) and **€49/month** (AlphaVPS), with RedSwitches, Ultahost and HOSTKEY covering the mid and premium tiers.

One thing worth saying upfront, because a lot of affiliate pages won't: RackNerd — the budget host this guide is set up with — does not operate a UK datacenter. Its dedicated servers live in US facilities, with Los Angeles as the flagship, and Amsterdam handles its European VPS demand. So this guide does two jobs. It maps the actual London market with current, checkable numbers. And it tells you honestly when skipping the UK entirely and buying cheap US bare metal from RackNerd is the smarter move.

> **In a hurry?** Entry-level London bare metal: **£49/mo** at Glitch Servers (4-hour provisioning, 4-hour hardware-swap SLA) or **€49/mo** at AlphaVPS (deploys in ~5 minutes). RedSwitches' cheapest London-ready instant server is **$133.79/mo** despite a "$70/mo" headline. Ultahost is the fully-managed pick from **$109.80/mo** — but that price requires a 24-month prepay. HOSTKEY covers premium EPYC builds from **€238/mo**. And if UK data residency isn't legally required for you, [👉 check RackNerd's current dedicated server pricing](https://bit.ly/my-rn) — its US bare metal starts well below any of these.

## The real London price ladder, verified from current listings

Genuine, single-tenant bare metal in London currently starts just under £50 a month. Below that price band you're generally looking at VPS with "dedicated resources" marketing, not a physical machine reserved for you. Here's how the five providers sitting at the top of the search results actually compare, plus where RackNerd lands:

| Provider | Entry price | Entry hardware | Billing | Managed? | Standout detail |
| --- | --- | --- | --- | --- | --- |
| Glitch Servers | £49/mo | Single-tenant bare metal, Ryzen or Xeon, NVMe Gen4 | Monthly | Optional managed plans | 4-hour provisioning, 4-hour hardware-swap SLA, Corero DDoS included |
| AlphaVPS | €49/mo | Instant SKUs, OS-ready in ~5 min | Monthly, no setup fee | Self-managed, full IPMI included | Direct LINX peering; ~8 ms to Amsterdam, ~70 ms to New York |
| RedSwitches | $133.79/mo in London (advertised from $70) | Xeon E-2274G, 32 GB RAM, 2×480 GB SSD | Monthly | Self-managed, KVM/IPMI | 99.99% uptime SLA, crypto payments accepted |
| Ultahost | $109.80/mo | Xeon E3-1265L v3, 16 GB DDR3, 256 GB SSD | 24-month term | Fully managed | 30-day money-back, free migration |
| HOSTKEY | €238/mo | 2× Xeon Gold 6140 (36 cores), 256 GB DDR4 | Monthly or annual (−12%) | Unmanaged | Scales to EPYC 9354 with 768 GB RAM; instant cancel to balance |
| RackNerd | Historically from ~$40/mo | Older-gen Xeon entry builds, Ryzen/EPYC above | Monthly | Self-managed | No UK datacenter — see the section below |

A few things in that table deserve a closer look, because they're exactly the details the listing pages tend to gloss over.

**RedSwitches' headline doesn't match its London inventory.** The site advertises UK servers "from $70/mo," but the cheapest London-configured instant server on its own pricing table is **$133.79/month** for a Xeon E-2274G with 32 GB RAM and 2×480 GB SSD. The $70 figure presumably applies to other locations. If your budget estimate was built on the headline number, roughly double it.

**Ultahost's cheapest plan is older than it looks.** The Ulta-X1 at $109.80/mo runs a Xeon E3-1265L v3 — a low-power Haswell chip launched in 2013 — with 16 GB of DDR3 and a 300 Mbit/s port. That's a lot of money for decade-old silicon, even with management included. The first plan with genuinely modern hardware is the Ulta-X3 (Ryzen 7 7700X, 64 GB DDR5, 1 Gbit) at $176.50/mo. If you go with Ultahost, that's the sensible starting point.

**HOSTKEY is a different product category.** Its listed London-available configs start at €238/mo for a dual Gold 6140 with 256 GB RAM and 2×1.92 TB enterprise SSDs, scaling up to EPYC 9354 systems with 768 GB of DDR5. The infrastructure backs it up — 99.982% annual uptime, free basic DDoS protection in Europe, and 1–10 Gbps ports. This is where you go when the workload genuinely needs the hardware, not the postcode.

**The two cheapest entries are legit bare metal.** Glitch Servers sells single-tenant machines with no hypervisor — up to 64 physical cores, 512 GB ECC RAM, five IPv4 addresses and a routed /64 IPv6 subnet via its own AS212868, with LINX and LONAP peering and measured round-trips under 5 ms to central London endpoints. AlphaVPS racks machines a short hop from LINX on its own AS203380 network with Lumen, GTT, Cogent, NTT and Zayo transit, standard 10 Gbit ports (up to 100 Gbit available), and instant SKUs that come online in about five minutes.

## Managed vs unmanaged: the split that decides most purchases

This single line divides the London market into two different products, and most comparison articles don't spell it out.

Ultahost is the only fully managed option in the group — monitoring, security patching, BitNinja protection, free migration and 24/7 support are bundled into the price. Glitch Servers sits in the middle: base plans are self-managed, but managed tiers add proactive OS patching, monitoring and 24/7 emergency response. AlphaVPS, RedSwitches and HOSTKEY are self-managed; HOSTKEY states this explicitly, with administration available as a paid extra. All three hand you full root access plus IPMI/iDRAC/KVM so you can drive the box out-of-band.

The practical decision rule: if nobody on your team wants to patch a kernel at 2 a.m., pay for management (Ultahost, or Glitch's managed tier). If you have someone comfortable with a terminal, self-managed gets you more hardware per pound — and removes a support layer between you and your own server.

One more angle worth knowing: bare-metal isolation itself has compliance value. Because there's no shared hypervisor to document, Glitch notes its London deployments simplify PCI-DSS and Cyber Essentials certification — the auditor doesn't need a lecture on virtualization architecture. If that's your world, physical single-tenancy is a feature in itself.

## What the billing terms actually cost you

Headline prices hide the difference between prepay and monthly, and the gap is bigger than most people expect.

Run the math on Ultahost's entry plan: $109.80/mo "billed for 24 month term" means **$2,635.20 upfront** for the first two years. Compare that to RedSwitches' Xeon E-2274G at $133.79/mo month-to-month — $1,605.48 over the first year, cancel whenever, no setup fee. Yes, Ultahost includes management and a 30-day money-back guarantee, and its renewal stays at $109.80/mo rather than jumping. But you're committing two years of cash to a 2013-era CPU. That trade deserves a conscious decision.

HOSTKEY handles flexibility unusually well: annual billing earns a 12% discount, but you can cancel a server instantly and unused funds get credited back to your account balance for other services. That's a far gentler prepay proposition than most hosts offer. AlphaVPS and RedSwitches both skip setup fees entirely, which keeps trying-a-server cheap.

The takeaway: decide your maximum upfront spend before you start comparing plans, because the advertised monthly number won't tell you whether you're about to be invoiced for one month or twenty-four.

## Where RackNerd fits in a London search — and where it doesn't

RackNerd is a fit when physical location matters less to you than the price tag — and a poor fit the moment UK data residency enters the conversation. Since this is the host behind this guide, here's the blunt version.

**What it is:** a budget-focused, self-managed host best known for aggressive VPS and dedicated pricing, frequent seasonal promos (Black Friday especially), and a team that's unusually visible answering pre-sales questions in public on hosting forums like LowEndTalk. Its dedicated inventory sits in US datacenters — Los Angeles is the main site — with entry-level builds historically starting around the $40/month mark for older-generation Xeon hardware, and faster Ryzen and EPYC systems above that. Stock and pricing rotate constantly, so treat that as the ballpark, not a quote — [👉 browse RackNerd's current dedicated server lineup and prices](https://bit.ly/my-rn) to see what's actually in stock today.

**Where it works:** US-facing workloads. Backups and offsite storage, CI runners, game servers for North American players, lab hardware, staging environments — anything where a London user's ~140 ms round-trip to Los Angeles is irrelevant because your users are in Chicago, not Camden.

**Where it doesn't:** anything touching UK data residency. Providers in the London list market "UK GDPR + Data Protection Act 2018" alignment precisely because the server's physical location is what satisfies those frameworks — and no amount of encryption changes where the disks spin. If your compliance posture requires data to stay in the UK, RackNerd is off the table, full stop. Same logic applies to latency-sensitive trading or any app whose users are primarily in Britain and Western Europe.

There's a partial middle ground: RackNerd runs VPS nodes in Amsterdam, which sits about 8 ms from London. But that's virtualization, not bare metal — fine for a cheap EU Linux box, irrelevant if you specifically need a physical machine.

## Five checks before you click order

1. **Confirm out-of-band access.** Every legitimate provider above includes IPMI or KVM. Ignore the word "dedicated" in the marketing and check for IPMI access instead — it's the fastest way to separate real bare metal from relabeled VPS.
2. **DDoS protection: included or add-on?** Glitch runs Corero Smartwall inline on all uplinks at no extra charge; RedSwitches includes a DDoS shield; Ultahost and HOSTKEY (in Europe) include free protection. AlphaVPS offers it as an add-on. Price the difference if you're a likely target.
3. **Bandwidth terms.** RedSwitches' London SKUs pair 1 Gbps with 30 TB; HOSTKEY guarantees 1–10 Gbps ports with 50 TB outbound; AlphaVPS includes 10 Gbit standard; Ultahost advertises unmetered. Match this to your actual traffic, not the port speed.
4. **Setup time and SLA.** AlphaVPS instant SKUs come online in ~5 minutes; Glitch provisions within 4 hours and swaps failed hardware within 4; RedSwitches guarantees 99.99% uptime with instant automated provisioning.
5. **Refund and commitment terms.** Ultahost offers 30 days money-back; HOSTKEY credits unused funds back on instant cancellation; monthly billing (Glitch, AlphaVPS, RedSwitches) beats any prepay when you're still unsure about a provider.

## Frequently asked questions

**How much does a dedicated server in London really cost?**
Real bare metal starts at £49/mo (Glitch Servers) or €49/mo (AlphaVPS). A realistic mid-range budget is $130–$300/mo for modern hardware, and serious EPYC builds run from €238 to €1,055/mo at HOSTKEY. Anything advertised well under £40 for "London dedicated" is almost certainly a VPS.

**Is a cheaper US server ever a good substitute?**
Yes — when your users, backups or compliance don't care about the UK. From a London desk, Amsterdam responds in ~8 ms, Frankfurt in ~14 ms, New York in ~70 ms, and Los Angeles in roughly 140 ms. If your audience is American, a US bare metal box is the rational buy: [👉 check RackNerd's current dedicated deals](https://bit.ly/my-rn) and compare against the London prices above.

**Will a US server satisfy UK data residency requirements?**
No. If your legal or compliance framework requires UK data residency, the server must physically sit in the UK — that's the entire reason London providers advertise UK GDPR and Data Protection Act 2018 alignment. This is the one requirement no amount of price savings can work around.

**Why is London bare metal pricier than equivalent US hardware?**
A few structural reasons: power and floor space in London cost more than in Dallas or Los Angeles, LINX-adjacent capacity commands a premium, and the UK's used-server supply chain is smaller. The gap narrows at the entry tier — £49 vs ~$40 — and widens for high-core-count configurations.

## Which one should you actually pick?

Match your situation to the option:

- **UK data residency or sub-10 ms to British users is mandatory** → AlphaVPS (€49/mo, fastest deploy) or Glitch Servers (£49/mo, strongest bare-metal SLA terms) at the entry tier. Ultahost if you want it fully managed — start at the X3, and go in knowing it's a 24-month prepay. HOSTKEY or RedSwitches when you need serious EPYC-class hardware.
- **US-facing workload, or you just want the most hardware per pound** → RackNerd, and don't feel bad about it. A US bare metal box at a fraction of London pricing is the correct answer for plenty of projects.
- **Undecided** → buy monthly, wherever you land. Monthly billing is your exit ramp; prepaid terms are a commitment device dressed up as a discount.

Before you commit to anything, do two things: ping the provider's test IP or looking glass from your own network, and re-check the billing term on the checkout page rather than the listing page. If the US route makes sense for you, [👉 see what RackNerd's dedicated servers cost today](https://bit.ly/my-rn) — and if it doesn't, the London table above has your answer.
