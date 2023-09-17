---
layout: post
title:  "Your options to having privacy in Bitcoin"
date:   2023-09-15 12:07:00 +0300
---

Due to recent events with [mixer being confiscated by authorities][1], or [mixer doing an exit scam][2], or with a [seemingly legitimate pro-privacy company going in the opposite direction][3], I think a clarification of where we are at the moment in protecting the users' privacy is necessary. 

There are three ways to secure privacy of your bitcoins, each of which comes with its own advantages and disadvantages. Pick according to what fits you best.

- <font size="5">CoinJoining</font>
There are three ways to do a [coinjoin][4] with a large liquidity and effectively. Joinmarket, Whirlpool, and Wasabi. We'll break down each.

<font size="4">1. Joinmarket</font>
pros:
- Decentralized; each of you can become your own coordinator if you provide sufficient liquidity. The protocol is designed to work with many takers (those that will take ordinary users' offers). 
- Self-custody.
- Large liquidity for coinjoins. ([orderbook][6])

cons:
- Difficult to setup for the average user.
- Expensive; you're paying for the inputs of the takers. Those inputs are recommended to be more than 9, so you'll be paying for at least a large in size transaction. This can be in the range of $5 to $10 sometimes. 

---
‎
<font size="4">2. Whirlpool</font> 
pros:
- Self-custody.
- Very effective, contains [~8,500 BTC][7] in liquidity and you can make as many coinjoins as you want once you enter a pool.
- Cheap. For amounts within 0.001 and 0.025 BTC, you're paying only 5,000 sat. For larger amounts less than 0.7 BTC, 50,000 sat. (mining fees asides)

cons:
- Not fundamentally decentralized; you'll be using Samurai's whirlpool, as they have the most liquidity.

---
‎
<font size="4">3. Wasabi</font>
pros:
- Self-custody.
- Cheap. A fresh input (that isn't already coinjoined) will only cost 0.3% of the amount with free remixes according to the wiki. (mining fees asides)

cons:
- Not decentralized. Liquidity sits on top of the default coordinator, even though it's theoretically possible connect to other servers (none of which I'm aware of).
- Service treats the currency as non-fungible and might blacklist your inputs without rationale given.
- Software is caught to have flaws with protecting user's privacy: [https://twitter.com/wasabistats][8].
- Funds blockchain analysis company and requests permission from them when user does coinjoin.

---
---
‎

- <font size="5">Mixer services</font> 
In this category falls every Internet service that runs individually. You can find an extended list in here: [2023 List Bitcoin Mixers Bitcoin Tumblers Websites][9]. Each service might come with other benefits, but they all fundamentally share the same pros and cons following:

pros:
- Can be cheap. In fact, some services in the past charged you absolutely nothing.
- Can be very effective. Services in the past used techniques like time travel and cutting of blockchain connection, both of which are impossible to do with coinjoins. 

cons:
- You're forfeiting the custody of your coins.
- Trust that the service isn't a honeypot or doesn't keep logs is needed.

---
---
‎

- <font size="5">Swapping bitcoin with a private cryptocurrency</font> 
The third option is most likely underestimated. Swapping decentralized, cheaply, and with the largest anonymity set currently available ([Monero / XMR][10]), is attractive. Let's look in each pro and con closely.

pros:
- Decentralized, using [Bisq][11], you can trade bitcoin for XMR, and there appear to be lots of offers: [https://bisq.markets/market/xmr_btc][16]
- Very effective; largest anonymity set (about $2.6B in [market cap][12]). You can also take advantage of the time; you can keep the XMR for an indefinite time, and make yourself even more untraceable.
- Self-custody. (if Bisq is used)
- No trust required. Monero is a network resulted from cryptographic achievements like ring signatures and their combination with confidential transactions.

cons:
- Might be a little complicated, as the user has to get along with Monero, and maybe even run a [full node][13] for additional privacy.
- Might come a little more expensive sometimes. Total costs are: Bitcoin on-chain fees ([4 TXs][14]), Monero on-chain fees (nearly zero), Bisq fees ([trading costs][15]).
- You're giving up bitcoin for an altcoin. Some may not like that, and if you keep it for a lot of time, there might be price fluctuations (which can be seen as an advantage too, as they randomize the swapped bitcoin amount).

[1]: https://www.justice.gov/opa/pr/justice-department-investigation-leads-takedown-darknet-cryptocurrency-mixer-processed-over-3
[2]: https://bitcointalk.org/index.php?action=trust;u=3537433
[3]: https://bitcointalk.org/index.php?topic=5389567.80
[4]: https://en.bitcoin.it/wiki/CoinJoin
[5]: https://github.com/JoinMarket-Org/joinmarket-clientserver
[6]: https://nixbitcoin.org/orderbook/
[7]: https://bitcoin.clarkmoody.com/dashboard/
[8]: https://twitter.com/wasabistats
[9]: https://bitcointalk.org/index.php?topic=2827109.0
[10]: https://www.getmonero.org/
[11]: https://bisq.network/
[12]: https://coinmarketcap.com/currencies/monero/
[13]: https://www.getmonero.org/downloads/
[14]: https://bisq.wiki/Trading_costs
[15]: https://bisq.wiki/Trading_costs
[16]: https://bisq.markets/market/xmr_btc