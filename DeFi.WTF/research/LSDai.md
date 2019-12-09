**Open request for comments. Please refer to [Issues](https://github.com/carboclan/pm/issues) for most updated discussions, and post your questions and comments as an Issue. You may follow the best practice set by reviewer @anthonyleezhang in this brilliant thread of dicussion on Issue #39 [Thoughts on MARKET vs UMA protocols](https://github.com/carboclan/pm/issues/39).**

# LSDai: Get High on Interest!
An EthBerlinZwei hackathon winning project.
www.LSDai.Market

![Technical overview of how the LSDai system works](https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/000/829/681/datas/gallery.jpg)

## Inspiration
In a world of roller-coaster crypto volatility, we turned to Dai for stability. With the emergence of interest generating instruments born through layers of collateralization on crypto native synthetic assets, we are entering a phase of interest rate volatility. Introducing LSDai, for your escape to a peace of mind: earn Compound interest on your collateral with rDai, while providing liquidity for hedges against variable Compound interest.

Empirical studies from traditional finance have shown the adverse impact of variability in interest rates (the “price” of money) on the real economy. Accordingly, interest rate swap, used by non-financial firms in the management of the interest rate risk of their debt, is one of the most important fixed-income instrument in the trading and hedging of interest rate risk. An alternative to interest rate swap, Eurodollar futures, is the biggest and most liquid futures market traded in the US by volume.

We have seen recent wild swings of Compound interest on Dai, going from 5% to peaking over 16% within a month. With the emergence of DeFi stack, more synthetic crypto assets composed of native assets are created and then rebundled on the Ethereum tech stack, enabling new possibilities while introducing complex interdependencies into the system. This is why we are creating LSDai.market, for hedgers and speculators to take leveraged long and short positions on Dai interest rates without borrowing by simply buying and selling LongDi and ShortDi tokens.

## What it does
LSDai creates a [Eurodollar](https://en.wikipedia.org/wiki/Eurodollar)-style derivative that is a future on the Dai lending rate on Compound over the duration of the contract. By leveraging [Market Protocol](https://marketprotocol.io), LSDai takes the approach of de-coupling the risk of the two sides.

LSDai creates a [Eurodollar](https://en.wikipedia.org/wiki/Eurodollar) like construct, that is a future on the Compound Dai lending rate over the duration of the contract. By leveraging Market Protocol which takes on the approach of constructing index futures via "iron-cross options" approach, LSDai de-couples the risk of the two sides via long and short position tokens.
It enables three different types of users to gain the kind of exposure to the interest rate fluctuation that fits their profile, while aligns incentives.



It enables three different types of users to gain the kind of exposure to the interest rate fluctuation that fits their profile, while also aligning their incentives:

* **Hedgers**: Hedgers are lending out their Dai on Compound and earn interest, but fear that the interest rate — thus, their passive income — will drop. LSDai’s Market Makers mint and sell them **Short** **D**ai **i**nterest tokens (*ShortDi*) in exchange for Dai, enabling Hedgers to hedge their interest-earning position. This means they will offset the rate fluctuation through gains in ShortDi: if the interest rate drops, they profit from the short position. If the rate goes up, the extra interest makes up for their loss of value in ShortDi. In essence, hedgers can insure themselves against a loss of income, reaching an altered state of peace.

* **Speculators**: These players have no stake in the lending business, they just want to bet on the changes in the interest rate. Speculators expect Dai’s lending interest rate on Compound to either to go up or down, and buy Long or Short Dai interest tokens (*LongDi* or *ShortDi*) from the LSDai Market Makers. They gain or lose, depending on where the interest rate goes and how clear their mind was when they made their bet. *(feature coming soon)*

* **Market Makers**: Market Makers enable the whole LSDai flow. They provide the initial capital to seed market liquidity. They also manage the minting and selling of the LongDi and ShortDi tokens to Hedgers and Speculators. In exchange for their role in supplying, Market Makers sell the tokens at a slight premium and earn the spread. They also earn the interest on the whole collateral pool. But sharing is caring: Market Makers can easily set someone else as the beneficiary of that interest (such as a rehabilitation center). *(feature coming soon)*

## How we built it
We took a decentralized approach, adopting Market Protocol in decoupling the interest rate swap positions into margin-embedded long and short position tokens, LongDi and ShortDi. We used Airswap to aid the price discovery of these tokens. Given the importance of liquidity in the model, we programmed a bot to arbitrage the spread across the Market Makers of the token pairs and the Hedgers/Speculators.

Lastly, in order to create a virtuous loop to further incentivize the Market Makers, we implemented rDai as the collateral in Market Protocol backing the position token pair. Thus, Market Makers will be able to earn interest from the rDai collateral in addition to earning the spread.

During the EthBerlinZwei hackathon we started from scratch and were able to launch LSDai on the Ethereum mainnet. Since we are the first Market Maker in this product, we have decided to donate the interest accrued from rDai in the collateral pool to EthBerlin. (This is not to imply that EthBerlin is a rehab. Okay, well, in some sense it is.)

## Challenges we ran into
We had to figure out how to make a contract that is written to provide assets priced in dollars, and invent a pricing structure for the interest rate swap. We also had to think about how the pricing structure may fit into the existing Market Protocol smart contract that we have already deployed on Kovan. 

In addition, we encountered a hard-coded Infura key in the Airswap widget that hit its rate limit on the day of the hackathon submission, and the widget code is not open source. We downloaded each file until we got to the one that had the hard coded Infura key, replaced the key with our own and uploaded the entire file structure to private services to re-serve it to our app. 

## Accomplishments that we're proud of
1. Built it from scratch and launched on mainnet!
2. Created an innovative solution of decentralized interest rate swaps for DeFi.
3. Aligned a global team from 3 continents. We met at EthBerlin, brainstormed, built the project and launched it together in less than 30 hours.

## What's next for LSDai
We plan to fix up the frontend bug and roll out a new version based on the updates in the rDai 2.0 contract in September. And — drumroll, please — a truly **stable-revenue-stable-value synthetic token** is coming! Stay tuned and have a nice trip!

## Updates!!!
LSDai.Market creates a unique mechanism to tokenize on-chain variable rates, which allows the market to take leveraged long and short positions against the movement of variable rates without borrowing. Simultaneously, it also enables market makers — who seed liquidity to the system — to earn interest on collateral, in addition to spreads. We start with the variable Dai interest rate, a financial primitive currently most common in the Ethereum DeFi space. This way, we’re creating the first tokenized Eurodollar-style futures on the Dai interest rate. Positions are represented by the LongDi and ShortDi tokens (Long and Short Dai interest). Establishing a liquid market for these is significant for the DeFi space beyond trading or hedging: it can inform the market of the expectations about the future interest rate. For example, in MakerDAO’s case, it can serve as a signal to the MKR governance (who set the stability fee) and Dai users (who are affected by the peg). In the future, we will extend our market to interest rates beyond stablecoins, creating long/short token pairs for indices of other crypto-native variable rates (e.g. variable staking rewards).

DApp Interface: www.lsdai.market
Documentation (working draft): https://github.com/carboclan/pm/blob/master/research/LSDai.md
GitHub repos: https://github.com/carboclan/LSDai-dapp https://github.com/carboclan/LSDi-airswap-bot

As a next step, we plan on offering structured products such as tokenized fixed rates and term-limited lending and borrowing, while leveraging the liquidity of existing variable rate DeFi lending products. We are currently designing a stable-revenue-stable-interest rate token, the LSDai token. This will be backed by a rate insurance pool called the LSDao, with a simple interface and ease of UX, similar to that of a certificate of deposit that may be redeemed at any time or traded on secondary markets. LSDao members will seed the liquidity of LSDai tokens and earn the best available variable interest on their collateral, along with a spread (insurance premium). When LSDai holders redeem their tokens, the LSDao will automatically buy them back. Essentially, these tokens behave as puttable bonds. The fixed interest rate of newly issued LSDai tokens and the LSDao insurance premium can be algorithmically priced and dynamically adjusted. These values are functions of the capital supply in the LSDao collateral pool and the fixed-rate lending pool.
