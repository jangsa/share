# Secret NFTs backed by functional real assets
Love to have a talk about use cases of Secret NFTs.  
Hopefully it's somehow interesting to you!

## Burn-then-tokenize problem
Banksy has burnt his work before tokenizing it.  
Ownership of drawing might be valuable even after drawing itself is burnt (a little enigmatic to me though).

On the other hand, burning houses, vehicles, ships, planes ... is nothing but irrational behavior.  
Since houses, vehicles, ships, planes, ... are valuable only if they are existing and functioning.  

## Tokenizing by on-demand sealing
Conventional tokenization methods involve unavailability.  
For example:
* Burning drawing for drawing NFT is kinda permanent sealing; Assets can't be recovered.
* Storing USD for USD token is tentative sealing; Amounts can be redeemed later.  
Both nullify the propertie's effect forever or tentatively in order that the value of token is secured.

What I'm suggesting here is on-demand sealing.  
Functional real assets should be available unless it is sealed.

![seal's picture](https://www.ecomare.nl/wp-content/uploads/2017/04/ill-gewone-zeehond-2010-10sw.jpg "seal")

## How to seal?
The way of sealing actually depends on the type of target property.  
For example:
1. Effect of cars can be disabled by smart locks (door locks & engine suspension).
1. Effect of solar panels can be taken by control over power transmission.

The problem is "how to keep asset's availability while it is secured".  
There is conventional (still a little new) auto loan scheme where smart locks (virtual keys) play a role.

It works like below:
### Problem
A consumer wants to buy a new vehicle, but no enough money and not qualified for auto loan.  
Getting qualified for auto loan can be difficult because mortgage is not considered always applicable to automobile.  
One of the reasons is the debtor (borrower) can run away with the mortgaged asset.  
### Solution
Authorize creditor's virtual key to lock car's door & engine.  
If repayment is not done accordingly, the creditor can suspend the functionality of the car.  
That means the borrower (almost) can't run away with it - the creditor can seize the property.  
Virtual keys can enforce Asset-Back in a better way.

## Functional Asset Backed Secret NFTs
I expect Secret NFTs can cover wider assets if "sealing status" can be embedded in Secret NFTs' contract as well as ownership.

This scheme includes 3 entities:
1. Owner - a role who enjoys availability of the property and liquidity of NFTs.
1. Observer - the authorized role who can seal the property in case of misbehavior or for securing loans. Automated or managed by multiple parties through threshold signature; Kleros project can be a reference.
1. Deployer - A trusted party who supplies sealing tools to the owner's property.

In this case, Secret NFTs are required to get extended other than ownership:
* "Sealing status" of the property
* Observer's address which is authorized to execute a function to switch "sealing status"
Depending on the type of asset, additional fields might be required.

"Sealing status" is a financial situation of a person or company, plus the properties are existing in real world ... well, if "sealing status" is public, the asset or belongings can be exposed to fear of theft/intrusion.  
Hence privacy matters.  
I bet Secret NFTs are really suitable to this scheme.

## Further discussion
The value of functional real asset backed NFTs has volatility as well as BTC, ETH and SCRT.  
The gap is, however, that the value of functional real asset backed NFTs decreases as time goes by (depreciation) or in case of boken.

That being said, the most difficult challenge is value estimation of functional real asset backed NFTs.  
It requires to cover depreciation and insurance fee in case of accidents.

If it gets well designed, it's possible to copy or better the conventional models like Reverse Mortgage, Leaseback model within DeFi.

![big picture](https://github.com/jangsa/share/blob/master/SecretNFTs/functional_asset_backed_snfts.png "big picture")

That's abstract of my idea.  
I'm at the very entrance point of Secret NFTs world, so still not sure about feasibility.  
If there are contradictions and technical challenges, please advise kindly.

Thank you and sorry for poor English.
