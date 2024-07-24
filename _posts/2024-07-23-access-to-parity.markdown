---
layout: post
title:  "From Access to Parity"
date:   2024-07-23 00:00:00 -0400
categories: engineering, fintech
---

> ✍️ A brief background on myself: my engineering career has taken me from working at a large bank, to being the first engineer at a consumer crypto startup, to scaling a fast-growing financial health company. I’ve been interested in the history of money, credit, and banking longer than my professional career - I’ll eventually publish old social lending or crypto banking braindumps from high school and college. I’m writing now to snapshot my perspective over time, and better guide the topics I dig into.

> ☕ Some readers might think that my thoughts are either (1) wrong or (2) obvious. If so - please reach out on LinkedIn, X, wherever! I’ll buy you a virtual coffee (or in-person if you’re in NYC) in exchange for your point of view.

> 🇺🇸 I’m writing purely within the scope of America. While I spent a few years working on consumer finance largely outside the United States, I don’t believe my perspective is relevant enough to share. Any mention of “everyone” should be taken to mean “most Americans.”


### **_My perspective on how financial access has improved, and what this means for individuals and startups alike_**

I think it’s important to start with my definition of “financially underserved,” as much of this post revolves around that definition. To me, an underserved person is someone who lacks cheap and easy access to:
* **Custody**: Where your financial assets (investments, debt, savings, etc) live. Historically, the role of custodian was filled by banks, credit unions, or trading platforms.
* **Money Movement**: How your assets move between custodians. Historically, the role of money-mover was filled by card networks, ACH, checks, and cash.

A core fintech narrative is that rent-seeking custodians and money-movers limit financial access, and inherently exclusive financial infrastructure leaves people financially underserved, and startups unable to help them. However, this narrative is largely solved.

Throughout the 2000s, the jobs of traditional custodians and money-movers greatly “unbundled.” Now, custodians can be neobanks (Chime, Column, Revolut), digital wallets (PayPal, Coinbase), investment apps (Acorns, Wealthfront), earned wage access products (Dave, Earnin), and more. Money-movers can be P2P networks (Apple Cash, Venmo), blockchain L2s (Polygon, Base), open banking APIs (Link, Plaid, Astra), remittance platforms (Wise, Revolut), payroll middleware (DailyPay, Argyle), and more. Even the Fed is getting into the game with FedNow, although initial results are far worse than Brazil’s PIX or India’s UPI.

Today’s financial system provides basic access to everyone, and the proliferation of companies leveraging this new infrastructure means that everyone with an internet connection is no longer underserved. Now, three budding financial narratives are
1. Aligning the risks and costs of financial services with its inherently digital nature
2. Deploying new use cases of this latent financial access to achieve financial parity
3. Helping individuals make intelligent financial decisions in light of new use cases

I’ll break out what this could mean for startups, what this new world looks like for consumers, and what some interesting spaces to build in might look like.

#### **Opportunities and pitfalls for startups**
Financial infrastructure and basic access is largely solved, but it’s solved poorly. Many of the trickiest incidents I deal with as an engineer involve issues with either a custodian or a money-mover. However, innovating at the infrastructure level is once again becoming increasingly difficult for smaller companies to do. Companies that solved the infrastructure problem did so in a vastly different regulatory climate. Whether due to some catastrophic regulatory failures, larger companies using regulations as a moat, or both, improving financial access is a problem currently best-suited for large companies with deep pockets.

Just because this new financial infrastructure has enabled financial access for all, doesn’t mean that it’s available to everyone. We’re still a long way from financial parity, and most people are still, obviously, struggling to make ends meet. Most fintechs today are using new financial infrastructure (a.k.a., embedded finance) to “onboard the next billion” or “democratize finance.” Finance is becoming a low-margin, high-volume business, with availability as the primary goal. For much of the 2010s, spinning up a neobank or issuing cards was as easy as integrating an API. Finance was commoditizing a bit too quickly. Finance is far more digital than other real-world verticals like healthcare or real estate, but the costs and risks of holding and moving money are much greater than pure software. If a single website goes down, most people’s lives aren’t heavily impacted. If CrowdStrike goes down, society slows but inevitably recovers. If Silicon Valley Bank (SVB) goes down, a lot of people are in immediate, real, and possibly permanent peril.

This changed the course of how teams leverage financial infrastructure, but its impact is in no way reversing. For example, custodian partnership marketplaces and developer-first custodians are gaining popularity compared to off-the-shelf banking-as-a-service APIs. Every product that money touches will still become a financial service with balances or loans or cards. The line between bank account, digital wallet, and crypto wallet will continue to blur, as will the way money moves between them.
#### **Effect on consumers**
Increased financial access has already led to ultra-personalized products with clear incentives for specific user niches, faster transaction settlement, and a race to the bottom for junk fees (overdraft, network, interchange, etc). As this trend of increased availability continues, financial services will continue to become more bespoke. The ability to easily utilize banking infrastructure has led to savings accounts for hourly workers, neobanks purpose-built for senior citizens and Latin American immigrants and indigenous peoples and climate activists, and payment networks optimizing for remittance or even weddings (I discovered Marley Finance while planning my wedding). People have a far greater variety of financial services to choose from, and have the general availability to choose a stack that works for them.

This availability can also lead to information overload, and while access to choose from many available financial services is great, the business models of most services haven’t changed much. Custodians still need to maximize capital, and money-movers still need to maximize volume. In an era of little competition, one stack of financial tools (really just a bank and an investment platform) wouldn’t work much better than another for most people. The proliferance of financial services means that one stack of tools could truly be better suited for one person than another. However, the onus of knowing which stack is best, knowing when it might be time to swap out one tool in the stack for another, and even knowing how to make that swap, have all been passed onto the individual. No standalone tool has any interest in making these answers clear when their goal remains locking up capital or increasing volume.

#### **Opportunities for individuals or small teams**
The following ideas range from half-baked to farfetched, but I hope they paint a picture of where I see some entry points into innovation in the current state of fintech. While big companies slowly improve infrastructure, small groups of builders can help both improve existing availability and move more people from financial access, through availability, towards true parity.
* The rapid introduction of new custodians and money-movers is creating a veritable crisis of inclusion. There are simply too many options for where to store and how to move your assets. This presents challenges ensuring individuals pick the right custodian or money-mover for them, and also opportunities if they pick the correct hyper-personalized service for them. What if you’re new to America, or you’re 14 years old, or you don’t have a car, or you’re planning a wedding? While custodians want to lock people in, people won’t be new to America forever, or 14 years old forever. How can we make the process of “graduating” to a new custodian, or picking the correct custodian in the first place, easier?
* While it’s trivial to build new financial products in a sandbox environment, going live is still a non-technical mess of red tape. I built a mini neobank proof-of-concept in a weekend, but can’t go live with it because I don’t have $30,000+ to put up as reserves, nor do I have a team of compliance analysts. Access to capital formation and compliance are two major blockers for anyone looking to spin up a fully-integrated financial product. These concerns are valid (just look at the Synapse / Evolve drama, or SVB), capital formation and compliance are mainly digital problems that haven’t stood up well against the correct solution in other industries.
* Improved financial infrastructure makes finance more composable. Are there any new financial primitives we can build into this increasingly-open financial infrastructure? Can ledgers become more easily readable by lending, investment, or credit platforms that make decisions from interpreted cash flow data? Can we build an abstraction or aggregation of credit opportunities? Can we take a page from the crypto space and build semi-self-sustaining lending or investment protocols (for example, I see Fragment’s Ledger API as an incredible application of distributed ledger technology in the “real” financial services space).

---

#### References:
* [The Great Bank Unbundling](https://research.contrary.com/deep-dive/great-bank-unbundling)
* [Ayo Omojola on the Future Proof podcast](https://www.youtube.com/watch?v=O80EnZCSPNw)
* [Tabapay has a great writeup on Visa+ and how it’s connecting P2P networks](https://blog.tabapay.com/introducing-visa-plus/)
* [My little “weekendproject” server](https://github.com/SomeMoosery/weekendbank)
* [Marc Andreessen’s thread on “Little Tech” outlines how big tech companies pull up the ladder behind them, oftentimes to the detriment of startups](https://x.com/pmarca/status/1809340686879322354)
* [JPMorgan Warns Customers: Prepare to Pay for Checking Accounts](https://www.wsj.com/finance/regulation/jpmorgan-financial-regulations-charge-customers-d86ca9e4?st=gxhe2n25dr7jqvt&reflink=desktopwebshare_permalink)
* “Crisis of inclusion” is a quote from David Graeber’s book Debt: The First 5000 Years. I found this quote particularly prescient. Graeber used this term to describe the “democratization of finance” in 2011, only a year after Stripe was founded and before fintechs like Plaid or Coinbase had even come into existence.
* [Synapse’s Downfall Provides Hard Lessons for Its B2B Partners](https://www.pymnts.com/business/2024/synapses-downfall-provides-case-study-in-b2b-partner-management/)
* [Visa+ aims to unify P2P networks](https://blog.tabapay.com/introducing-visa-plus/)
* Some applications of new financial infrastructure I mention in the customer section: [Ezra](https://tryezra.com), [Charlie](https://charlie.com), [Comun](https://en.comun.app), [Totem](https://mytotem.app), [Aspiration](https://aspiration.com), [Fragment](https://fragment.dev), [Marley](https://www.marleyfinance.com)
