Metacrafters_ETH+AVAX_Intermediate_Project_01_Submission
The code Voting System a smart contract exception handling using require(), assert(), and revert() statements. Overall The main objective of this smart contract is to demonstrate different ways of handling exceptions and errors in Solidity.

Contract Introduction
The VotingSystem smart contract is a decentralized application designed to manage a proposal-based voting system on the Ethereum blockchain. This contract enables the creation of proposals, allows users to vote on these proposals, and provides mechanisms for finalizing the proposals based on the voting results. The contract ensures only the owner can create and finalize proposals while allowing any address to cast votes. The use of events provides transparency and traceability for proposal creation, voting, and finalization actions
Variables and Structs

Owner: The address of the contract owner, who has special privileges to create and finalize proposals. Proposal Count: A counter tracking the total number of proposals created. Proposal Struct: Defines the structure of a proposal, which includes an ID, description, vote count, and a boolean indicating if it has been finalized. Proposals Mapping: Stores proposals by their unique ID. Votes Mapping: Tracks whether an address has voted on a particular proposal.

Events ProposalCreated: Emitted when a new proposal is created. Voted: Emitted when an address votes on a proposal. ProposalFinalized: Emitted when a proposal is finalized, indicating whether it was accepted based on the vote count.

Modifiers onlyOwner: Ensures that only the owner can execute certain functions, providing a security check.

Constructor Constructor: Sets the deploying address as the owner of the contract.

Functions createProposal: Allows the owner to create a new proposal with a given description. Increments the proposal count and stores the new proposal in the mapping. vote: Allows any address to vote on an existing proposal. Checks if the proposal exists, if it has been finalized, and if the address has already voted. Increments the proposal's vote count and records the vote. finalizeProposal: Allows the owner to finalize a proposal, marking it as finalized. Emits an event indicating whether the proposal was accepted based on the vote count. getProposal: Provides details of a specific proposal, including its ID, description, vote count, and finalized status. transferOwnership: Allows the owner to transfer ownership of the contract to a new address, with a check to prevent transferring to a zero address.

Deploying the Contract
To deploy the VotingSystem contract on the Ethereum blockchain, follow these steps:

Setup Environment: Install and set up a development environment such as Truffle or Hardhat. Ensure you have an Ethereum wallet like MetaMask configured. Compile the Contract: Use the Solidity compiler (solc) to compile the contract, ensuring there are no syntax errors. Deploy Script: Write a deployment script that uses web3.js or ethers.js to deploy the contract. This script should specify the contract's ABI and bytecode. Deploy: Execute the deployment script using a connected Ethereum account with sufficient gas fees. This will deploy the contract to the specified Ethereum network. Verify Deployment: Once deployed, verify the contract address and ensure the owner's address is correctly set.

By following these steps, the VotingSystem contract will be live on the Ethereum network, ready to create proposals, accept votes, and finalize decisions based on decentralized voting.
