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
Let's start with reviewing conventional ways of tokenization.  
For example:
* Storing USDs for USD tokens is "Tentative Sealing"; Amounts can be redeemed later.
* Burning a drawing for its NFT is kinda "Permanent Sealing"; Assets can't be recovered.

Both nullify propertie's effect tentatively / permanently in order that the value of token is secured while the token exists and is liquidated.  
These conventional methods involve unavailability.  

That's where Lazy Sealing plays a role.  
Its concept is really simple: "Functional real assets should not be unavailable unless it needs to be unavailable (sealed)."

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

Addtional information is required to be attached other than ownership:
* "Sealing status (availability)" of the property
* Observer's address (suspention executor's address ... could be multisig)
Depending on the type of asset, additional fields could be needed.  

The trust of observer is actually the boundary between digital world and physical world.  
It is really difficult to remove this kind of trust.
Still if observer is trusted enough, the tokenized asset can get liquidity. I believe the asset-backed NFTs has potential to be the second stable coin.  

## How it works
![access control by NFT status](https://github.com/jangsa/share/blob/master/SecretNFTs/LazySealing/img/architecture_w.png "access control by NFT status")
What this scheme brings is consistency between "ownership in digital world" and "ownership in physical world".  
Sealing tools (e.g. smart locks) keep physical access control. If sealing tools rely on access control embedded in NFTs (digital access control), we can achieve the consistency.  
That's the point.

1. Bob (Owner of assets) gives Alice (Observer) his own public key. The public key is the pair of secret key in his virtual key app.
1. Alice deploys Secret NFT contract of Bob's asset. The contract includes authorized public keys (access control information) as status, Bob's public key in this case.
1. Alice gives issued viewing key (with NFT's address) to Bob and smart lock system.
1. Smart lock system refers to its own NFT status by viewing key and get authorized public keys.
1. When Bob's smartphone (in which virtual key app is running) approaches his car, smart lock system and the app do authentication protocol (+ UWB location measurement).
1. Door opens and engine launches if authentication succeeds.

Now Bob can enjoy his car.  

If he neglects to obey the contract with Alice (e.g. repayment), Alice can delete Bob's public key from authorized public keys in NFT.  
Now Bob can't utilize his car.

This scheme can be applicable to other assets in a similar way.
* Alice can suspend the reward through selling electricity generated by solar panel.
* Alice can suspend the power supplier of leased devices (really effective to leased items in smart home).

## Secret NFTs' advantage over normal NFTs
Above mentioned scheme can be implemented in conventional NFTs.  
I expect, however, Secret NFTs can cover wider assets from the viewpoint of privacy in real world.

Assets actually exists in real world.  
That means, if status of NFT stays public:
1. Financial condition of people or companies are always public (traceable)  
1. The asset or belongings can be exposed to fear of theft / intrusion.  
1. Anybody can trace the user history of the asset without encryption. What if this information is combined with external information (e.g. location history of cars)?

Hence privacy matters.  
Secret NFTs can keep the status encrypted on-chain and manage access control by viewing keys.  
That's Secret NFTs' advantage against conventional (normal) NFTs.  

## Further discussion
The value of functional real asset backed NFTs has volatility as well as BTC, ETH and SCRT.  
The gap is, however, that the value of functional real asset backed NFTs decreases as time goes by (depreciation) or in case of boken.

That being said, the most difficult challenge is value estimation of functional real asset backed NFTs.  
It requires to cover depreciation and insurance fee in case of accidents.

If it gets well designed, it's possible to copy or better the conventional models like Reverse Mortgage, Leaseback model within DeFi.

![big picture](https://github.com/jangsa/share/blob/master/SecretNFTs/LazySealing/img/overall_w.png "big picture")


