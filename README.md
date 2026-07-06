# ART-CENTER-DAO

Solidity DAO contract prototype for an art center in Istanbul Beyoglu.

The contract lets members submit proposals, vote once per proposal, execute
approved proposals, contribute ETH, and withdraw their own contributed balance.

## Contract

`ART-CENTER-DAO.sol` defines `ArtCenterDAO`.

## Proposal Flow

1. Submit a proposal with `submitProposal(string proposalDescription)`.
2. Vote once with `voteProposal(uint256 proposalId, bool vote)`.
3. Execute a proposal with `executeProposal(uint256 proposalId)` when votes for
   are greater than votes against.

## Funding Flow

- `contribute()` accepts ETH contributions greater than zero.
- `withdrawFunds(uint256 amount)` lets contributors withdraw from their own
  recorded balance.
- `totalContributions` tracks the total amount contributed through the DAO.

## Events

- `ProposalSubmitted`
- `Voted`
- `ProposalExecuted`
- `ContributionReceived`
- `FundsWithdrawn`

## Notes

This is an educational DAO sample. A production DAO should add membership rules,
proposal execution actions, voting periods, quorum, and stronger treasury
controls.
