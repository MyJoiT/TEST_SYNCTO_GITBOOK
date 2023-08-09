# Tako Recommendation Protocol

The Tako Recommendation Protocol serves Web3 social graphs by providing a variety of bid-to-curate functionalities within its smart contracts. The [integration](../integration/tako-recommendation-protocol/) of this peer-to-peer recommendation protocol into a dApp allows users to boost the visibility of their content. They can offer curation bids on targeted profiles whose followers they seek to engage.

It could be a sufficiently inclusivized recommendation/advertisement solution as an effective alternative to the traditional centralized, algorithm-based, platform-curated solutions. By sharing content through these value-matching curations, it enhances the engagement of diverse content within an ecosystem. This allows niche yet valuable content and their creators to be easily discovered. It also offers improved monetization opportunities for content creators, allowing them to leverage their social influence.

Basically, there are two roles in this recommendation system: Bidder and Curator:

#### Bidder

Login with a wallet address or creator profile (e.g. Lens handle). They can:

* Create a bid: set up a curation bid by specifying the curation type, target Curator, bid amount, and bid duration. Curation types can include share (mirror in Lens protocol), comment, post, or quote post.
* Update a bid: modify the bid data before a bid is expired, such as extending the duration or increasing the bid amount.
* Cancel a bid (Withdraw): withdraw the funds from the smart contract when a bid has expired.

#### Curator

Login with a creator profile (e.g. Lens handle). They can:

* Audit a bid: decide on a status change, i.e., whether to recommend it, to a received curation bid by evaluating the content and the bid amount.
* Claim: claim the funds after accepting and executing a curation.
* Set a minimum bid: set the minimum bid amount the Curator wants to receive.
* Set disabled audit types: specify the curation types that the Curator does not want to receive.
