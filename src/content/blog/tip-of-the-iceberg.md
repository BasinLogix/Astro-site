---
title: "Tip of the Iceberg"
date: 2020-08-21
draft: false
excerpt: "A few weeks ago I was invited to speak at Substrate Seminar, a weekly meeting where people share what they are working on in the realm of Substrate, a platform for producing unique blockchains."
---

August 21st, 2020

A few weeks ago I was invited to speak at Substrate Seminar, a weekly meeting where people share what they are working on in the realm of Substrate, a platform for producing unique blockchains. A one hour conversation about some of my learnings as a beginner, turned out to actually be a step towards realizing Basin Logix's long term project goals. 


My interest in building with Substrate began in earnest a few months ago, when I completed a blockchain developer course in Ethereum. The course was well run and had polished content, but when I turned around at the end to begin work on Basin Logix using the Ethereum toolset, I was stuck. No amount of tutorials or reading other's code was enabling me to progress. After a few false starts and spending way too much time making sure I had the correct suite of development tools, I started to look elsewhere.  


Reasons for developing a blockchain solution on Substrate are numerous and if you want to learn more I would encourage you to listen to [this podcast episode](https://relaychain.fm/10-building-a-custom-blockchain-with-substrate) which covers just that topic. I found a fit between Basin Logix and Substrate because the concepts being explored and implemented were larger in scope than those that I found on other platforms. 


After I was on Substrate Seminar I was told I would be receiving a monetary tip in the form of KSM, the native token of the Kusama network. I assumed the tipping mechanism was something straight forward and informal, handled by an administrative level person. What followed was an interesting, inspiring, and engaging interaction.

![Voting Machine](/images/pics/voting_machine.jpg)

## Interesting

Voting machines like the one above (likely an educational tool and not a full machine) are great analogies for voting systems like the tipping mechanism built into the [Treasury](https://wiki.polkadot.network/docs/en/learn-treasury) on Kusama and Polkadot. I won't go into the intricacies of either the Treasury's code or the voting machine's mechanics, instead I want to expand on the user's interactions with and perceptions of each of these. 


Starting with the voting machine, we can see there are instructions and buttons clearly visible on the interface. In the instructions there are mentions of how to vote, time allotted to vote and a brief example. We can imagine that if this where a real voting machine, a particularly determined stakeholder could inspect the mechanics of each lever, ensuring that the input corresponded to a guaranteed output on the ballot cast.

In the tipping mechanism built into the Treasury shown above, we observe very similar concepts of how to vote, time allotted to vote and in the documentation a brief example. Just like in the case of the voting machine, a particularly determined stakeholder could with the background context of the Rust level [documentation](https://paritytech.github.io/substrate/master/pallet_treasury/index.html), inspect the [code](https://github.com/paritytech/substrate/blob/master/frame/treasury/src/lib.rs) used in producing the outcome of the vote, therefore providing some level of guarantee about the tipping mechanism. In this current era of widespread allegation concerning voter fraud, election delays and accessibility issues, it seems that blockchain could be particularly well adapted to mitigate these types of issues. 


The most interesting part of the tipping mechanism is the logic behind how it functions, this is for me where the expanded scope of Substrate is on display: 

>A separate subsystem exists to allow for an agile "tipping" process, whereby a reward may be given without first having a pre-determined stakeholder group come to consensus on how much should be paid.
>
>A group of Tippers is determined through the config Trait. After half of these have declared some amount that they believe a particular reported reason deserves, then a countdown period is entered where any remaining members can declare their tip amounts also. After the close of the countdown period, the median of all declared tips is paid to the reported beneficiary, along with any finders fee, in case of a public (and bonded) original report.


This is where the questions begin: 

- Why is it half the deciding amount of tippers to trigger the countdown period? 

- Why is the paid amount based on the median? why not on the mean? 

- Who are the tippers?

- How can I hack on this?

- What parts of this can I apply to my own project?

- etc, etc

## Inspiring and Engaging

From finding the answers to the questions listed above is where the inspiration takes off. The tip itself is also a source of inspiration. As a method of expanding the a network, the tipping mechanism rewards members in a way which engages them further. Just like the Kusama and Polkadot ecosystems need users to achieve their purpose of becoming coordinators of heterogeneous blockchains, Basin Logix will also need continual engagement from stakeholders in order to be an effective tool for managing groundwater. By tying voting with value (KSM) the tipping mechanism has established a method of literally turning an interested party into a stakeholder. 


As Basin Logix progresses toward a live network we will continue to explore, apply and modify the utilities being showcased in the Kusama network and other Substrate based networks.