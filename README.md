# Project Oblio: Mobile Populism

Mobile Populism is Project Oblio's economic theory that the "wisdom of the crowds" prevails. It also states that people are just as, if not more,  incentivized by a combination of financial security and social respect as they are wealth accumulation. It does create financial incentives for nearly every component of this network, but it does them in a way that rely on biological barriers to computation. The financial incentive for "faking-out" block producers is smaller than the cost of 1) computation 2) losing OBL to the challenger-verifiers market. 

<div style="text-align:center"><img src ="http://projectoblio.com/wp-content/uploads/2018/07/figure14-1.png" /></div>

(Under private development -- all constants here are not their latest version, and every aspect described herein is subject to change.)

## Table of Contents
1. Summary
2. Detailed Overview
	a. Key Terms
	b. Roles
		i. Voting Roles
			o. Wealth-based voter
			oo. Democracy-based voter
			ooo. Representative-based voter
		ii. Biometric Trust Roles
			o. Block-Producer
			oo. Challenger
			ooo. Verifier 
3. Voting Components
	a. Funding Proposals
		i. Wealth-Based Component
		ii. Democracy-Based Component
		iii. Representative-Based Component
		iv. Example
	b. Checks and Balances
		i. Checking Wealth-Based Component Voters
		ii. Checking Democracy-Based Component Voters
		iii. Checking Representative-Based Component Voters
		iv. Lower-Level and Meta Checks
4. Biometric Trust Components
	a. Challenger-Verifier Markets
	b. Block Producers
5. Karma
	a. Affecting Karma scores
	b. Karma as an OBL Interest Rate
6. Conclusion


## Summary

A function exists for submitting proposals:
- [x]  Proposals can be a String
- [x]  They cost 10 OBL to submit 
- [x]  They are then voted on by combining votes from the budget system

Three Functions for Budget Systems (Functions):
- [x] Wealth-based Component (1/3 of final votes): Here, one OBL counts as one vote. An account holder must have at least the biometric trust level of karma (default: 10) in its account to count their OBL as a vote. 

- [x]  Democracy-based Component (1/3 of final votes): A user with a karma score of at least the biometric trust threshold has exactly 1 vote. A user with a karma score of more than the biometric trust threshold still has 1 vote. 

- [x] Representative-based Component (1/3 of final votes): A representative is a user with at least 1000 karma.  One representative  counts as 1 vote.

These votes are add together to pass or not pass a proposal. Each component is counted separately, then weighted to 1/3 of the final votes. 

User structure (an object): 
	Karma (integer). 
	OBL (token account value)
	Biometric trust threshold: 10 karma (Default). If a user is above this, they get priviledges:
		Someone with 10 karma can vote in Wealth and Democracy based cmponents
		Someone with 1000 karma can vote in Wealth, Representative, and Democracy based components
	Backers (an array of ethereum addresses)
	totalOblDonated (an integer)
	... 



## Detailed Overview

Mobile Populism consists of six roles and three key terms.


### Key terms

* OBL. A measure of wealth. A traditional token. Not intended to be proof-of-individual, although the initial distribution is intended to be mostly proof-of-individual.
* Karma. NOT a token. Just a "Score" associated with an account. The calculation for the karmic stream is explained at the end. 
* Biometric trust level. The minimum amount of biometricity needed to vote. Based on selfie videos, voice recordings, brainwaves, muscle movements, and any provably unique fluid biometric. May be added to based on uPort identities and "acceptances" from other users already accepted. The "link" between the upper and lower levels of the government.

### Roles
Two systems exist for running the network's engine. The first is an upper-level voting system with three components. It is slower and more secure. The next is a lower-level system for verifying additions and subtractions to a user's karma level. It is fast in the block-producing component, but slower in the challenging and verification markets. 

#### Voting Roles (Upper-Level)
<div style="text-align:center"><img width="500" height="500" src =".gif" /></div>
A proof-of-individual voting system *must* take into account tragedy of the commons. Every voter is required to be provably unique (re: biometric trust level), but some voters can have weights counted as more if they are trusted more by the network (representative-based) or have more invested in the network's success (wealth-based).
* Wealth-based voter. A wealth-based voter has at least 10 Karma. If they have at least 10 Karma, each of their OBLs counts as one vote. Additionally, any OBL that a user has donated back to the budget system counts as one vote. The maximum amount of OBL votes a user can have is 1,300. 
* Democracy-based voter. A democracy-based voter has at least 10 karma. Their account receives exactly one vote.
* Representative-based voter. A representative-based voter has at least 10 democracy-based voters "Backing" them, and at least 1000 karma in their account. 

#### Biometric Trust Roles (Lower-Level)

A financially incentivized challenger/verifier market keeps block-producers honest. 
* Block-producer. This is an array of ethereum accounts that do commands at a lower-level, not within the smart contracts. The only thing to know about them right now is that this array can be added to or removed by a 60% majority vote of representatives and democrats.
* Challenger. This is a person who challenges the decisions of the block-producer. 
* Verifier. This is a person who verifies the results of the challenge, and rewards the challenger, while removing OBL from the 

## Voting Components (Upper-Level)

The budget system allows users to make proposals and vote on whether they should be funded by OBL. It also elects the underlying block producers for the network, who ultimately determine the karma values (or biometric trust levels) for the overrall government system. Ultimately, this is a system of checks and balances,  similar to the U.S. Constitution, where each component of the system relies on a different style of voting (1/3 wealth, 1/3 democratic, and 1/3 representative).

In each component of this consensus algorithm, a given voter must have at least the biometric trust level of karma (default: 10) in their account to vote. There is no such thing as voting if you have less than the biometric trust level of karma, even in the wealth-based voting system. This effectively makes this an all-around proof-of-individual voting system, just with an added hierarchial system of checks and balances. In a perfect society we could just do a pure proof-of-individual (> 10 karma) voting system for everything, but it is well-documented that crypto governments often have participation rates of less than 10% due to Tragedy Of the Commons. This means a system of checks and balances (some degree of hierarchy) is necessary in order to reward those who are contributing and participating regularly. 

Thus, the consensus algorithm has two main functions:
** Creating and self-funding proposals, experiments, and services with OBL, as well as payments to those who are running the network
** Ensuring the network reflects an accurate measure of consensus among its members, including checks and balances of all major voting populations

1. Funding Proposals. 
2. Checks and balances. This describes the interplay between all three major populations on the network, as well as block producers.
3. Token definitions (OBL, Karma).
4. Karma as an OBL interest rate (Altruism)

### Funding proposals (Standard voting):

This describes the three-tier voting system used as the default across the network for changing network constants and funding experiments.

#### Wealth-based Component (1/3)
<div style="text-align:center"><img width="220" height="120" src ="http://projectoblio.com/wp-content/uploads/2018/07/wealth-based.png" /></div>
- [x] Here, a "committed" OBL counts as one vote, while an "absentee" OBL counts as 1/5th of a vote, split between "yes, fund this", and "no, don't fund this. An account holder can elect to vote / not vote for a budget proposal based on the amount of OBL it has in their account address. 
- [x]  An account holder must have at least the biometric trust level of karma (default: 10) in its account to count their OBL as a vote. 
- [x]  Additionally, any OBL that a user has donated back to the budget system counts as one vote (see later section).   
- [x]  One OBL = One Vote *within* the wealth-based component (1/3 of the final decision).  
- [x] The maximum amount of OBL votes a user can have is 1,300. 
---> What happens if an OBL doesn't vote? An OBL that does not vote is considered to be "split" --> half their vote counts towards yes, and half their vote counts towards no, but it is weighted at 1/5th the value of a comitted vote. Thus, the smart contract must keep a total running tally of all the OBL that is held within accounts within at least 10 karma, because this is the only OBL that is eligible to vote. Then, it must take those that OBL that were voted, and split the remaining OBL 50-50.
---> Typical crypto governance systems have 2-15% participation based on token values. If 10 OBL vote yes, 5 OBL vote no, and 85 OBL didn't vote, the total wealth-based component is (10 + 85/5) "yes" and (5 + 85/5) "no". Percentage-wise, this looks like 54% yes.
---> I
---> The value ("1/5th") is a value to be decided in the system of checks and balances by a function of (1) a constant determined by democracy based voters and representative based voters as well as (2) the number of recent active OBLs in the voting system. 

#### Democracy-based Component (1/3) 
<div style="text-align:center"><img width="120" height="120"  src ="http://projectoblio.com/wp-content/uploads/2018/07/Picture16_people.png" /></div>
- [x] A user with a karma score of at least the biometric trust threshold has exactly 1 vote. 
- [x] A user with a karma score of more than the biometric trust threshold still has 1 vote. 
- [x] The first 10 karma a user are earned is based on their biometricity (determined by the "block producers", explained later), so this is effectively a one-person-one-vote democracy. 
---> What happens if a person doesn't vote?  A valid person who does not vote, does not have their vote counted by the network at all (abstain). 
---> This means if only 2 people vote and they vote yes, then the total democracy-based component is 100% yes and 0% no.

#### Representative-based Component (1/3)
<div style="text-align:center"><img width="120" height="120"  src ="http://projectoblio.com/wp-content/uploads/2018/07/Picture34_building.png" /></div>
- [x] A representative is a user with at least 1000 karma who has at least 10 unique backers, with each backer having karma at or above the biometric trust threshold.  
- [x] One representative counts as 1 vote within the representative-based component. See later for discussions of the "multiplication constant" for these values.
---> What happens if a representative doesn't vote? Unlike democracy and wealth-based components, a representative who does not vote is automatically considered a "no". This encourages democracy-based users to only back active representatives.
---> If 2 representatives vote, and 2 vote no, and 6 don't vote at all, the total representative-based component is 20% yes and 80% no. 

#### Example
Let's walk through what happens when someone submits a budget proposal and votes are tallied over a period of, say, 3 days. 
- [x] In the wealth-based component, if 2 OBL vote yes, but 98 OBL didn't vote, the total wealth-based component yes is (20 + 32.6) yes and (0 + 32.6) no. Percentage-wise, this looks like 61% yes.
- [x] In the democracy-based component, if only 2 people vote and they vote yes, then the total democracy-based component is 100% yes and 0% no.
- [x] In the representative-based component, if 2 representatives vote, and 2 vote no, and 6 don't vote at all, the total representative-based component is 20% yes and 80% no. 
---> (61% + 20% +100%)  is more than  (39% + 0% +80%) , so the budget passes

No matter how many votes are in each component, 1/3 of the votes for a proposal or issue are made up based of wealth-based voting, 1/3 of the votes are democracy-based, and 1/3 are representative-based. For example, if 1000 OBL and 3 democrats and 3 representatives are used to vote in a proposal, the wealth-based voting system still makes up 1/3 of the total final vote calculation, even though it had 1000 OBL as its numerical vote total. If only 1 person votes in the individual-based-component, the individual-based voting system still makes up 1/3 of the total final vote calculation. Thus, votes within each of these domains are counted separately, and used to create a fractional vote of 1/3. This goes the same for checks and balances votes where only two components may be participating.

If a budget proposal wants to be funded by OBL, they need to get approved by this three-tiered system of wealth, democratic, and representative components.  By default, a 50+% vote is required in a triple-check vote for it to be considered succesful. 

Most of the contract's constants should be able to be changed by a three-tier vote.

### Checks and balances:

To ensure that constants for "special" things like the biometric trust threshold are fairly calculated, and that the governing system does not become corrupt, a system of checks and balances is also implemented.

#### Checking wealth-based component voters.
- [x] The wealth-based check vote is a special vote conducted only by democrats and representatives. 
- [x] It is a value calculated similar to the three-component system described earlier, except with only two components (50% democratic, 50% representative). 
This vote may be used, among other things, d to:
--> Remove OBL from an account in the case of hacking. This OBL must be able to be re-assigned to a user or added to the budget system.
--> Remove OBL from an account in the case of corruption, or fake account generation to attack the Karmic value system. This OBL can be destroyed or added to the budget system.
--> Remove OBL from an account that appears to be causing significant, irreparable harm to the network. This OBL can be destroyed or added to the budget system. (same as last bullet from a development perspective)
--> Determine the inflation rate of OBLs. Right now, 1000 OBL is expected to be generated each month and input into the budget system. (More OBL is also generated as a karma interest rate, discussed later). The monthly generation value of the budget system can be changed by a 50% democratic and 50% representative vote. 
--> Again, ALL of these constants are very rough, and very fluidly votable, and will be changed in the coming months.

#### Checking democracy-based component voters
- [x]  The most important part of the network, democratic voters are always checked by themselves, in addition to other components.
- [x]  Triple-check: A check among all three components (33% democratic, 33% wealth, 33% representative) can be used to increase the biometric trust threshold. Note that this value can only be increased, and the maximum amount it can be increased by for each vote is 5. This is a "check" because it makes it harder for a user to be considered a democracy-based voter.
- [x]  Double-check: A check among two components (50% democratic (a self-check), 50% representative) is used to add and remove the list of block-producers, or the members of the "ordained". This is a "check" on democracy based voters since the ordained are heavily involved in giving a user its first 10 karma.  

####  Checking representative-based component voters
The representative-based check vote (50% democratic, 50% wealth-based) can be used to:
--> Increase a multiplication constant to be considered a representative. This constant is by default 1. When increased to 2, for example, the number of backers required to become a representative is 20, each backer must have 2 times the biometric trust threshold of karma, and each representative must have at least 2000 karma to be considered a representative. This value can only be increased, and by a maximum of 0.05 with each vote. 
---> Another check is singular. Democracy-based voters have the power to elect and fire representatives by backing  or not backing them. Thus, they provide a singular check on representatives that is not contributed to by wealth-based voters.
 
#### Lower-Level And Meta Checks
A triple-based check vote is used to fund block producers who run the network. (default: 10 OBL to each block-producer every month)
A triple-based check vote is used to fund representatives who vote on the network. (default: 1 OBL to each representative every month)
A triple-based check vote is used to determine interest rates for Karma values, as described in a later section. (default: 1% at 10 Karma, 2% and 100 Karma, 3% and 500 karma).
On a lower level (not within this smart contract), the ordained/ the block producers can vote out other block producers who are spamming the network without a representative vote. This is primarily because conducting a 3-day vote to prevent a belligerent node would be too slow to maintain the network's efficiency.

## Biometric Trust Components
To be completed, mainly because Truebit and a number of other really good projects are already working on algorithms to verify data in a decentralized way. 
### Challenger-Verifier Markets

A market exists to create a financial incentive to "check" the decisions made by block producers, who run the biometric verification algorithms. 

### Block Producers
<div style="text-align:center"><img width="120" height="120"  src ="http://projectoblio.com/wp-content/uploads/2018/07/Picture13_factory.png" /></div>
As described prevously, any account is eligible to apply to be a block producer. This is a separate account flag (or array) that is "under-the-hood". On the lower levels (not to be worried about until the go-oblio implementation), a block producer can be voted out by a vote within the other members of the block producers. This is necessary to quickly kick out spammers among block producers.

Block producers use a lot of computational power to verify identities. They will likely be paid as part of the budget contract when go-oblio launches. 

## Karma
Karma is a measure of "trustworthiness". It cannot be transferred from user to user. 

Karma is also used to cross-implement Nash's theory of equillibrium  with leading research into the neuroscience of happiness. It is is based on the theory that intelligent humans care as much or more about financial stability and social benefits than wealth accumulation.

Additionally, each user over a karma threshold is decidedly a unique human, enabling high-liquidity movement of oblios. This becomes relevant in the go-oblio implentation of Mobile Populism, although a purely smart-contract based implementation is likely to be launched as a standalone on Ethereum.

### Affecting Karma Scores
The only way to affect a user's karma value is in the following way:
- [x]  When an ethereum account has less than 10 karma, the only way it can have karma added/lowered to it is by a member of the "block producers" (one of the ethereum accounts in the special array) adding karma to their score. 
- [x]  When an ethereum account has more than 10 karma, karma can be added to in the following way:
---> By filling out a uPortProfile. For this, in the smart contract, you can just have a string called "uPortID". A user who links their uPortID can then submit a proposal to the budget system asking for an increase in their karma. In this way, a user's karma can be increased by a triple-checked vote / budget system approval
---> Karma can also be earned by donating OBL back to the central smart contract. See next section.
---> Karma maybe may also be earned by interaction with the experiments/subjects smart contract. A user can earn 0.1 Karma for every experiment that they parcipate in. In the smart contract, just make this a value called "subjectsTrust". Add a function for adding to this value. Leave a field called "subjectsSmartContractID". The subjectsSmartContractID is the only Ethereum address that can add to this field. 
---> "AdditionalKarma" is karma earned for participating in the cryptoKickstarter. This numerical value can also be added to by triple-checked budget system vote.  
---> So, in summary, the three people who have control over a user's karma value are:
------> 1) The block producers (accounts listed in the ordained array) who add to a user's biometric trust level (even beyond the initial 10 OBLio)
------> 2) The account holders themselves (by donating Karma back to the budget contract, up to 500 karma).
------> 3) A triple-checked vote. This can be in the form of a uPortProfile, or adding additional karma. 

Up until the biometric trust level, Karma is a measure of biometricity. After the biometric trust level, Karma is a measure of "trustworthiness", or a user's history of overrall contribution to the network. 

### Karma as an OBL interest rate

An interest rate provides financial security in the case of a hack, lost keys, or necessary recovery of biometric identity. Remember, biometrics exist outside the world of private keys, so ideally one would be able to use their biometricity to recover any lost accounts, although the OBL in those accounts may be more difficult to recover (see wealth-based check component above).

A separate metric called "totalOBLdonated" is kept as part of a parameter tied to an ethereum account. An account with 100 karma earns 1% of their total donated OBL back every month. The next threshold is 1,000 karma, after which a user earns 2% of their total donated OBL back every month. The last threshold is  10,000 karma, after which 3% of their donated karma is earned back every month. Over time, a user can earn back more OBL than they originally donated. It is likely that we will limit the total amount of OBL that can be generated as an interest rate and have it split among those with karma proportionall to their total values, meaning these percentages may lowered or such a scheme may be re-developed entirely. This OBL is newly generated and separate from the 1000 OBL which is generated every month to fund budget contracts. However, the total amount of OBL they can earn over time is limited only by the total amount of OBL that can ever be generated. 

A user who wishes to donate to the budget system has two options. They can either donate directly to the "budget system bank", allowing it to be spent however the community chooses, and receive karma in return. However, if a user wishes to have more control over their donated funds, they can propose their own task to the budget system, which must be approved by the community by a lesser vote. This may be the case in running a private experiment in the experiments.sol smart contract (see decentralized-neuroscience-smart-contracts repo). 

## Conclusion
The conclusion is, we need *your* help in coding these smart contracts, and we're currently *hiring* developers on Upwork to help us do so. Join our discord to describe your idea for implenting Mobile Populism into smart contracts, and any other violations of Game Theory you may have noticed in reading.









