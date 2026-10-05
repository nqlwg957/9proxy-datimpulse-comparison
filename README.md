# 9proxy review: IP-based vs GB-based plans compared, and a $1/GB pay-as-you-go alternative with non-expiring traffic

Most people searching for a 9proxy review are stuck on the same question: pay per IP, or pay per GB? The pricing page lists both, the numbers look low, and the two models behave completely differently once a real workload hits them. Pick wrong and you either burn a wallet full of IPs that expire before you use them, or you pay $3.00 per gigabyte for traffic when you could have paid a third of that elsewhere.

So this review does three things: explains what 9proxy actually sells, runs the real numbers on both billing models after its June 2026 price increase, and then looks at where a pay-per-GB workload is better served by someone else. That last part matters more than most 9proxy reviews admit, because the GB side of the pricing table is where 9proxy is weakest.

## What 9proxy actually sells

9proxy is a residential proxy provider. The company claims a pool of 20M+ residential IPs across 90+ countries, and it supports the two protocols that matter for scraping and multi-account work: HTTP/HTTPS and SOCKS5. Targeting goes down to city and state level. Nothing exotic there; the interesting part is that 9proxy sells residential access two different ways, and they are not interchangeable.

**Residential proxies by IP.** You buy a fixed number of IPs and get unlimited bandwidth on each one. IPs you don't use don't expire, which is genuinely useful if you buy in bulk and deploy slowly. Two catches: each IP naturally lives somewhere between a few hours and about 24 hours before you regenerate it, and this product requires the 9proxy desktop app, since it works through local port forwarding rather than plain username/password credentials.

**Residential proxies by GB.** You buy traffic instead of IP addresses, generate as many endpoints as you want in the dashboard, and rotate freely across the pool. Validity is 180 days, longer if you're on the Enterprise tier. Authentication is username/password or IP whitelisting, no app required. Sessions can be sticky or rotating. This is the model most automation workflows actually want.

On top of that there's an Enterprise program (unlimited traffic validity, team mode with one owner and up to five members, per-member traffic limits, activity logs) and a set of access tools: Proxy2Web for browser-based use, ProxyHub for managing mobile proxies, and a public API for programmatic session control. A feature called Auto-Refresh Proxy detects offline IPs and swaps them out automatically within 60 seconds.

## 9proxy pricing after the June 2026 increase

9proxy held its prices flat for roughly three years, then raised IP-based and bundle pricing on June 1, 2026. GB-based pricing was left alone. That detail trips people up constantly, because a lot of the 9proxy reviews still floating around quote the old numbers: $20 for 100 IPs, $105 for the 1,000 + 500 bonus tier, a $25 Starter bundle. Those figures are stale. Here's what the tiers look like now.

### IP-based packages (unlimited bandwidth per IP)

| Package | Total price | Effective cost per IP |
| --- | --- | --- |
| 100 IPs | $24 | $0.24 |
| 500 IPs | $72 | $0.144 |
| 1,000 + 500 bonus IPs | $126 | $0.084 |
| 2,500 IPs | $210 | $0.084 |
| 5,000 IPs | $360 | $0.072 |
| 15,000 IPs | $720 | $0.048 |
| 25,000 IPs | $863 | $0.035 |
| 50,000 IPs | $1,438 | $0.029 |
| 100,000 IPs (business) | $2,300 | $0.023 |
| 200,000 IPs (business) | $4,140 | $0.021 |
| 500,000 IPs (business) | $8,625 | $0.018 |

The unlimited bandwidth part is the real selling point here. If a job pushes hundreds of gigabytes through a handful of IPs, this structure costs you nothing extra and you stop watching a traffic counter. If your job pushes small requests through thousands of IPs, it's the wrong model and you'll overpay badly.

### GB-based packages

| Package | Price per GB | Total | Validity |
| --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days |
| 50 + 5 GB bonus | $2.10 | $105 | 180 days |
| 100 GB | $1.50 | $150 | 180 days |
| 200 GB | $1.00 | $200 | 180 days |
| 1,000 GB | $0.80 | $800 | 180 days |
| 2,000 GB | $0.75 | $1,500 | 180 days |

Read that middle column carefully, because it's where the comparison with every other GB-based provider starts. At 5 GB you're paying $3.00 per gigabyte. At 200 GB you've finally reached $1.00 per gigabyte. So 200 GB is the rough crossover point where 9proxy's traffic pricing stops being expensive.

### Bundle packages

Bundles mix IPs and traffic in one purchase, with the bundled traffic valid for 180 days: Starter at $30 for 100 IPs plus 5 GB, Popular at $180 for 1,500 IPs plus 50 GB, Pro at $720 for 5,000 IPs plus 500 GB. These make sense for agencies running two kinds of jobs at once, some needing a stable IP and some just needing volume.

## Where 9proxy holds up, and where it doesn't

The IP-based side is 9proxy's strongest offer. Unlimited bandwidth per IP at $0.018–$0.024 per IP at scale is aggressive, IPs don't expire, and the 60-second auto-replacement keeps a pipeline from stalling when an IP drops. Documentation is better than average for this segment, and the network works with the usual anti-detect browsers, so there's no protocol gymnastics if you're running AdsPower, Dolphin Anty or BitBrowser.

The GB side is where your money goes further elsewhere, for one specific reason: at low volume you're paying $3.00 per GB for traffic that also expires after 180 days. If your monthly usage is 20 or 30 GB rather than 200, 9proxy's GB packs are the most expensive way to buy residential traffic among the well-known providers.

Two more things to weigh before paying:

- **Advanced targeting costs extra.** Country-level routing is standard. City, state, ZIP and ISP-level filters are billed differently on residential products, which changes your effective per-GB cost if local accuracy is the whole reason you're buying.
- **The IP-based product locks you into Windows.** The desktop client is not optional for that model. If your stack is Linux containers or cloud runners, you want the GB product, full stop.

## What third-party trackers say about reliability

This is the part a 9proxy review has to be honest about, and it's also the part where you should be skeptical of the sources.

At least one proxy catalog site that sells competing products has documented two service interruptions in 2026: a roughly two-week outage in June that the company attributed to an infrastructure migration, and a reported second outage later in the summer. A separate URL and reputation scanner that aggregates review data summarizes complaints around the 60-second IP replacement policy and service disruptions, and reports a low average user rating on one review aggregator. Both of those sources have an interest in steering you elsewhere, so treat them as a signal worth checking rather than a verdict.

> If you buy from 9proxy, buy the smallest package first, test your actual targets against it for a few days, and only then top up. The $24 IP tier and the $15 / 5 GB pack are cheap enough to test with, and neither should be your whole quarterly budget.

One practical warning: there's a domain at 9proxy.online that public site-checkers describe as a parked domain registered in September 2025, unrelated to the main product. If a link promising "9proxy" sends you to a page that isn't the main site or dashboard, check where you've landed before entering payment details.

## The GB-based alternative: DataImpulse at a flat $1/GB

If your workload is bandwidth-based, the arithmetic that matters is simple. DataImpulse sells residential traffic at a flat $1/GB with a $5 minimum, no subscription, and traffic that never expires. There's no 180-day clock running on what you buy.

That's not a knock on 9proxy's per-IP product, which is a different tool for a different job. It's an argument about the GB product specifically:

|  | 9proxy (GB-based) | DataImpulse (residential) |
| --- | --- | --- |
| Entry price | $15 for 5 GB ($3.00/GB) | $5 for 5 GB ($1.00/GB) |
| 100 GB | $150 ($1.50/GB) | $100 ($1.00/GB) |
| 1 TB | $800 ($0.80/GB) | $800 ($0.80/GB, Advanced tier) |
| Traffic expiry | 180 days (unlimited on Enterprise) | Never expires |
| Pool | 20M+ IPs, 90+ countries (company figure) | 90M+ first-party IPs, 195 countries |
| Country targeting | Included | Included |
| Advanced targeting | City/state/ISP available, surcharged | City/ZIP/ASN available, billed at 2× on standard residential |
| Protocols | HTTP/HTTPS, SOCKS5 | HTTP/HTTPS, SOCKS5 |
| Refunds | Not publicly stated as a policy | 7-day money-back on first purchase, card payments, under 80% traffic used; crypto non-refundable |

Look at the 1 TB row. At that volume the two providers land on exactly the same $0.80/GB. The difference isn't price any more, it's what happens to unused balance: 9proxy's GB traffic runs out in 180 days, DataImpulse's doesn't. And below 200 GB, the gap is a straight 3× at the entry tier.

DataImpulse's IPs come from first-party pools rather than resold aggregator networks, which matters mainly because the same IPs aren't being rented to five other buyers at once. Proxyway's independent roundup of residential providers describes the pool as decently sized and the infrastructure as performing well, notes the 24/7 human support and budget monitoring tools, and flags two real downsides: advanced targeting doubles the per-GB price, and heavy abuse is possible at rates this low, which is why it's often used as a secondary IP source rather than a single point of failure. That's a fair read, and it matches what you'd expect from the price.

👉 [check DataImpulse's current $1/GB residential plans](https://bit.ly/dataimPulse)

## Every DataImpulse plan currently listed

DataImpulse runs four proxy types, all pay-as-you-go. Here's the complete set of packages on its pricing page, which is worth seeing in one place because the tier names repeat across products and the per-gigabyte rates don't.

| Proxy type and package | Traffic | Price | Effective rate | Billing | Buy |
| --- | --- | --- | --- | --- | --- |
| Residential — Intro | 5 GB | $5 | $1.00/GB | Pay-as-you-go, no expiry | [Start with the $5 Intro plan](https://bit.ly/dataimPulse) |
| Residential — Basic | 50 GB | $50 | $1.00/GB | Pay-as-you-go, no expiry | [Get the 50 GB residential package](https://bit.ly/dataimPulse) |
| Residential — Advanced | 1 TB | $800 | $0.80/GB | Pay-as-you-go, no expiry, dedicated account manager | [Check the 1 TB Advanced tier](https://bit.ly/dataimPulse) |
| Residential — Custom+ | 5 TB+ | From $4,000 | Custom | Pay-as-you-go, no expiry, personalized setup | [Request residential Custom+ pricing](https://bit.ly/dataimPulse) |
| Datacenter — Intro | 10 GB | $5 | $0.50/GB | Pay-as-you-go, no expiry | [Try datacenter proxies from $5](https://bit.ly/dataimPulse) |
| Datacenter — Basic | 100 GB | $50 | $0.50/GB | Pay-as-you-go, no expiry | [Get the 100 GB datacenter package](https://bit.ly/dataimPulse) |
| Datacenter — Advanced | 1 TB | $450 | $0.45/GB | Pay-as-you-go, no expiry, dedicated account manager | [See the 1 TB datacenter tier](https://bit.ly/dataimPulse) |
| Datacenter — Custom+ | 5 TB+ | From $2,250 | Custom | Pay-as-you-go, no expiry | [Request datacenter Custom+ pricing](https://bit.ly/dataimPulse) |
| Mobile — Intro | 2.5 GB | $5 | $2.00/GB | Pay-as-you-go, no expiry | [Start with mobile proxies at $5](https://bit.ly/dataimPulse) |
| Mobile — Basic | 25 GB | $50 | $2.00/GB | Pay-as-you-go, no expiry | [Get the 25 GB mobile package](https://bit.ly/dataimPulse) |
| Mobile — Advanced | 1 TB | $1,600 | $1.60/GB | Pay-as-you-go, no expiry | [See the 1 TB mobile tier](https://bit.ly/dataimPulse) |
| Mobile — Custom+ | 5 TB+ | From $8,000 | Custom | Pay-as-you-go, no expiry | [Request mobile Custom+ pricing](https://bit.ly/dataimPulse) |
| Premium Residential — Intro | 1 GB | $5 | $5.00/GB | Pay-as-you-go, no expiry | [Try the premium residential pool](https://bit.ly/dataimPulse) |
| Premium Residential — Basic | 10 GB | $50 | $5.00/GB | Pay-as-you-go, no expiry | [Get 10 GB of premium residential](https://bit.ly/dataimPulse) |
| Premium Residential — Custom+ | 5 TB+ | From $20,000 | Custom | Pay-as-you-go, no expiry, dedicated manager | [Request premium Custom+ pricing](https://bit.ly/dataimPulse) |

A few notes that don't fit neatly into a table. The minimum purchase across all four product types is $5, so testing datacenter and mobile costs the same as testing residential. The 7-day money-back guarantee applies to first purchases paid by card, provided you've used less than 80% of the traffic; crypto purchases on Intro plans aren't refundable. Volume discounts of roughly 20% kick in at the 1 TB tier on residential and mobile. And one billing quirk worth knowing before you budget: on standard residential, city, ZIP and ASN targeting is charged at twice the standard per-gigabyte rate, while country targeting is free.

## Which option fits which job

- **Running browser profiles or accounts that need a stable IP and heavy traffic:** 9proxy's IP-based packages are the more natural fit, since bandwidth is unlimited and unused IPs don't expire.
- **Rotating residential scraping with uneven monthly volume:** DataImpulse's $1/GB with non-expiring traffic, because a light month doesn't waste a bundle you already paid for.
- **SERP and SEO checks at volume without residential needs:** datacenter proxies at $0.50/GB are the cheap lever, and 9proxy doesn't sell a datacenter product at all.
- **Instagram, TikTok or mobile app data:** mobile proxies at $2/GB, and sticky sessions on both providers cover the session-persistence problem.
- **Need city or ZIP accuracy on a tight budget:** factor the doubling on advanced targeting into both quotes before you compare headline rates.

## Setup, briefly, for both

9proxy by GB: create an account, buy a GB package, open the dashboard's proxy generator, pick country or city, choose sticky or rotating mode, and export endpoints as .txt or .csv. No app needed.

9proxy by IP: install the Windows client, buy an IP package, then forward ports locally and pair it with your browser or automation tool. Optional proxy authentication on top.

DataImpulse: create an account, add $5 or more, choose the proxy type, generate an endpoint with your targeting parameters, and point your scraper or browser profile at it. Country targeting is part of the URL parameters, so you don't need a separate dashboard setting per location. Sticky sessions run from 1 to 120 minutes.

👉 [compare both options from the DataImpulse dashboard](https://bit.ly/dataimPulse)

## FAQ

**Is 9proxy legit?**
By most accounts it's a real provider that issues working IPs, not a scam. The consistent criticism is reliability and support responsiveness during outages rather than fraudulent billing. Test with a small package either way.

**Which 9proxy billing model is cheaper?**
It depends entirely on your traffic profile. Unlimited bandwidth per IP wins when you push a lot of data through few IPs. Per-GB wins when you rotate widely and move little data per request. Do the math on your last month of traffic before choosing.

**Does 9proxy traffic expire?**
Unused IPs on the IP-based plans don't expire. GB plans carry a 180-day validity unless you're on Enterprise, where validity is unlimited.

**Is there a free trial?**
DataImpulse doesn't offer a free trial; the minimum purchase is $5, which is offset by the 7-day money-back guarantee on card payments. 9proxy's entry points are $24 for the smallest IP package and $15 for the smallest GB pack.

**What's the cheapest way to test residential proxies?**
A $5 single purchase. At DataImpulse that buys 5 GB of residential traffic that doesn't expire, which is enough to measure success rates on your own targets rather than trusting a benchmark.

**Do I need special software?**
For 9proxy's per-IP product, yes, a Windows desktop client. For everything else covered here, no. Standard host:port:user:pass credentials and SOCKS5 support are enough for anti-detect browsers, Python scripts and proxy chains.

## The verdict

9proxy's per-IP product is a decent deal for heavy-bandwidth work: unlimited traffic, IPs that don't expire, and per-IP costs that fall to roughly $0.02 at volume. If that describes your workload, buy it, start with 100 IPs at $24, and confirm your targets before scaling.

Its per-GB product is harder to justify. $3.00 per gigabyte at entry, $1.00 only once you reach 200 GB, and a 180-day expiry on the traffic you buy. DataImpulse prices the same traffic at $1.00 per gigabyte from the first $5, doesn't expire what you buy, matches 9proxy exactly at the 1 TB mark, and adds a datacenter tier at $0.50/GB and mobile at $2/GB that 9proxy simply doesn't offer. If you want to know whether that holds up on your own targets, the cheapest honest answer is five dollars.

👉 [open DataImpulse and start with 5 GB of non-expiring residential traffic](https://bit.ly/dataimPulse)
