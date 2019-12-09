# Meeting minutes：Governance meeting，2019/8/19
The community governance meeting took place on 10 am Beijing time August 18th 2019

## Attendees：
Taylor
carboclanc
BigTreeLiuJie
Talrasha007
Mikefotiaoqing
longyunlyd
juqiangl

## Agenda Review

###Hashrate Derivative Product Initial Design
####1.	Product version 
a.	Mike: POC v0.2
b.	XMM: two-digit v0.2.0
Conclusion with Consensus: start with v0.2.0

####2.	Version definition
a.	Mike: 
i.	v0.2.0 features:  chart, order book, matching engine, trading interface, margins
b.	MM: 
i.	Wallet supported? browser extensions (Metamask)
ii.	Currency for collateral accepted? WBTC，
iii.	Issuance process? Through modification of the MARKET protocol, the minter position has been simplified away, there is only long or short position two roles.

####3.	The Practical Matters
a.	Jie’s proposal:
i.	Jie’s company Monte Carlo is currently designing and developing a full-functioning decentralized exchange on Ethereum, the MCDex, expected to launch in Oct 2019, which can list BME Futures.
ii.	Propose to merge Yellow Hat Community’s effort in building a DEX for BME Futures into Monte Carlo’s MCDex.
iii.	To concentrate liquidity, Monte Carlo’s MCDex should be the only interface for trading BME Futures.
b.	Tina’s concerns:
i.	Limiting trading interface for BME Futures only to MCDex is against the spirit of decentralization, tokenized long-short position pairs should be able to free float.
ii.	Given the specialized nature of BME Futures, Bitmex-like generalized trading interface of MCDex may not be user-friendly enough for miners’ and traders’ to understand the instrument.
c.	Conclusion with consensus: 
i.	MCDex will incorporate a BME Index calculator for miners and traders, as specified in earlier community product discussion.
ii.	Yellow Hat Community can create an intro marketing page for BME Futures on community product “Hashedge”, and links to MCDex.
iii.	Jie will send over the latest UIUX design of MCDex for Yellow Hat community this week for review.

###Governance:
Community project portfolio and organization: thoughts and feedbacks on the summary of current community project portfolio in the updated README:
a.	Mike: What are the criteria for community project selection? Project CoinCow seems a bit out of place. 
b.	Tina: a simple governance scheme for the Yellow Hat Community will be proposed soon, after closing research on comparable organizations’ governance scheme. The proposal will incorporate the following aspects:
i.	Community Mission
ii.	Core values of Community
iii.	Governance process:
1.	Community members’ entry and exit, induction process
2.	Community project criteria, proposals, selection and QA
3.	Peer review of members’ contribution
iv.	How does the Yellow Hat community contributors capture value from contribution to projects and research.
