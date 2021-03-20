# Secret NFTs backed by functional real assets

## Burn-then-tokenize problem
Banksy has burnt his drawing before tokenizing it.  
Ownership of drawing might be valuable even after the asset itself is burnt (a little enigmatic to me though).

Burning houses, vehicles, ships, planes ... is, however, nothing but irrational behavior.  
Since houses, vehicles, ships, planes, ... are valuable only if they are existing and functioning.  

So how can they be tokenized?
In other words, how can we keep consistency between "ownership in digital world" and "ownership in physical world" while assets keep existing and functioning?
That's the problem.

## Tokenizing by "Lazy Sealing"
Let's start with reviewing conventional tokenization methods.  
For example:
* Storing USDs for USD tokens is "Tentative Sealing"; Amounts can be redeemed later.
* Burning a drawing for its NFT is kinda "Permanent Sealing"; Assets can't be recovered.

Both nullify propertie's effect tentatively / forever in order that the value of token is secured while the token exists.  
All of the conventional methods involve unavailability.  

That's where Lazy Sealing plays a role.  
Its concept is really simple.
"Functional real assets should not be unavailable unless it needs to be unavailable (sealed)."

![ways of tokenization](https://github.com/jangsa/share/blob/master/SecretNFTs/LazySealing/img/comparison_w.png "ways of tokenization")

## How to seal?
The problem is "how to keep asset's availability while it is secured".  
Answer actually depends on the type of target property.  
For example:
1. Effect of cars can be disabled by smart locks (door locks & engine suspension).
1. Effect of solar panels can be taken by control over power transmission.

There is conventional (still a little new) scheme in auto loan industry where smart locks (virtual keys) work very well.

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

Lazy Sealing is more general concept by which availability is revoked only when problem is detected.
For automobile assets, the tool can be smart locks.
For solar panels, the tool can be power transmitter / supply wire.
Misbehavior e.g. no repayment triggers switching sealing status on so that the owner can't enjoy the effect of assets.

![seal's picture](https://www.ecomare.nl/wp-content/uploads/2017/04/ill-gewone-zeehond-2010-10sw.jpg "seal")

## Entities of the scheme
This scheme involves 3 roles:
1. Owner - a role who enjoys availability of the property and liquidity of NFTs.
1. Observer - the authorized role who can seal the property in case of misbehavior or for securing loans. Automated or managed by multiple parties through threshold signature; Kleros project can be a reference.
1. Deployer - A trusted party who supplies sealing tools to the owner's property.

In this case, contract of NFTs is required to get extended other than ownership:
* "Sealing status" of the property
* Observer's address is actually executor's address which is authorized to switch "sealing status" on / off
Depending on the type of asset, additional fields might be required.  

The trust of "Observers (executors)" is the boundary between digital world and physical world.  
I believe it is really difficult to remove this kind of trust to widespread practical usecases of NFTs.  

## Secret NFTs keep privacy belonging to assets in real world
I expect Secret NFTs can cover wider assets if "sealing status" can be embedded in Secret NFTs' contract as well as ownership.  

Assets are existing in real world.
If "sealing status" is public:
1. Financial condition of people or companies are always public (traceable)  
1. The asset or belongings can be exposed to fear of theft / intrusion.  
Hence privacy matters.  
I bet Secret NFTs are really suitable infrastructure for this scheme.

## How it works

TODO  

## Further discussion
The value of functional real asset backed NFTs has volatility as well as BTC, ETH and SCRT.  
The gap is, however, that the value of functional real asset backed NFTs decreases as time goes by (depreciation) or in case of boken.

That being said, the most difficult challenge is value estimation of functional real asset backed NFTs.  
It requires to cover depreciation and insurance fee in case of accidents.

If it gets well designed, it's possible to copy or better the conventional models like Reverse Mortgage, Leaseback model within DeFi.

![big picture](https://github.com/jangsa/share/blob/master/SecretNFTs/LazySealing/img/overall_w.png "big picture")

That's abstract of my idea.  
I'm at the very entrance point of Secret NFTs world, so still not sure about feasibility.  
If there are contradictions and technical challenges, please advise kindly.

Thank you and sorry for poor English.
