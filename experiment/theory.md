<u><h3>Theory</h3></u>
<b><p> Proxy contract</p></b>
<p>Traditional smart contracts encapsulate both the contract interface and its implementation. Once deployed, their logic cannot be modified without redeploying the entire contract. This can be problematic for decentralized applications (DApps) as it disrupts user interactions and may require users to switch to a new contract address.

Proxy contracts, on the other hand, separate the contract interface from its implementation. The proxy contract acts as an intermediary, forwarding transactions to and from the target contract, which holds the actual logic.
</p>

<p><b>Proxy contracts offer several benefits:</b>

<b>Upgrades without Disruptions:</b> Proxy contracts allow you to modify the logic of a smart contract without changing its address. This means you can improve or fix the contract without disrupting user interactions.

<b>Logic Separation:</b> Proxy contracts separate the contract's interface from its implementation. You can change the implementation without affecting the interface, ensuring compatibility for users.

<b>Enhanced Security: </b>Proxy contracts add an extra layer of protection, making it harder for attackers to exploit vulnerabilities in the target contract.

<b>Gas Optimization:</b> Proxy contracts can optimize gas costs by delegating certain tasks to other contracts, reducing computational overhead.

<b>Modular Design:</b> Proxy contracts promote modular design, making complex smart contracts easier to manage and maintain.

<h4>Proxy Contract VsSmart Contract</h4>


| Features          | Proxy Contract     | Smart Contract    |
|-------------------|--------------------|-------------------|
| Functionality  |Acts as a middleman, forwarding transactions to and from another contract|  Encapsulates both the interface and implementation of a specific functionality.
|Logic Modifiability|Can be upgraded without changing the contract address|Requires redeployment of the entire contract to modify logic.|
|Implementation Separation |Separates the interface from the implementation, allowing for independent changes.| Interface and implementation are tightly coupled.
|Modular Design| Promotes modularity by separating concerns between the proxy and the target contract.|Less modular due to the tight coupling of interface and implementation.|
|Typical Use Cases  |Managing token contracts, DEXs, NFTs, and governance contracts.|Used for various purposes such as tokenization, crowdfunding, and DAOs.|


<p><b>different types of proxy contracts</b></p>
<p>Transparent Proxy: Simple proxy, reveals the target contract it interacts with.</p>
<p>Upgradeable Proxy: Allows updating the logic contract while maintaining the same proxy address.</p>
<p>Storage Proxy: Handles storage for the target contract, separating it from the logic layer.</p>
<p>Hybrid Proxy: Combines features of multiple types for specific needs.</p>


<p><b>What Are Upgradeable Smart Contracts?</b></p>
smart contracts are unchangeable once deployed. This immutability builds trust among DeFi parties since even the contract’s creator can’t alter it. However, this also means they can’t be updated, posing risks if security or other issues arise.
Upgradeable Smart Contracts (USC) solve these issues by allowing updates without the need to migrate all activity to a new address.
The earliest and most intuitive method of updating smart contracts with no state migrations is the data-separation pattern. Here, we separate a smart contract into logic and storage contracts, storing and changing the state respectively. The problem with this method is evident: constant calls between logic and storage require gas.
