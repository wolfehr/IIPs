---
iip: tbd
title: Multipreference Quadratic Voting
status: WIP
author: Heath Wolfeld (@wolfehr#3150) <wolfehr>
discussions-to: tbd
created: TBD
updated: TBD
---

# Simple Summary

Allow DAO members to vote for muliple candidates during Illuvium Council elections. The voting weight for each candidate would be the square root of the number of ILV the DAO member assigns to each candidate. This would allow DAO members to better express their preferences about who should be on the Council.

There are no other changes to Council elections. The only change is to how DAO members can allocate their votes.

# Abstract

Update Illuvium Council elections to use multipreference quadratic voting.

# Motivation

* Only allowing one candidate leads to a council that doesn't necessarily represent the DAOs preference by hiding the preferences for non-first choice candidates. For example, if Person A were everyone's second choice, they would get no votes despite everyone in the DAO believing they deserved a seat on the Council (given they only picked one person for a five-seat Council). 
* DAO members can express preferences for the full council (e.g., they can vote for five candidates). 
* It gives more voting power to those who chose to spread their votes amongst multiple candidates and decreases the power of whales to throw all their weight behind one candidate and get them on the Council.


# Specification

* DAO members have votes equal to the ILV holdings in wallets they control.
* DAO members can spread their vote over any number of candidates.
* The votes given to a candidate when a DAO member allocates ILV to them will be equal to the square root of the number of ILV allocated. 
* The core team is accountable for determining how to elect their representative. They do not need approval from the DAO on their method of electing a representative.

### Example

A DAO member has 100 ILV. Candidates A, B, C, and D are running. The DAO member could case their votes as follows.

* Candidate A = 10 vILV (10^2 = 100)
* Candidate A = 5 vILV; Candidate B = 5 vILV; Candidate C = 5 vILV; Candidate D = 5 vILV (5^2 * 4 = 100)
* Candidate A = 8 vILV; Candidate B = 6 vILV (8^2 + 6^2 = 100)

# Rationale

This allows DAO members to better express their preferences for who should represent the DAO on the Council; DAO members gain the ability to express a preference for mulCandidates that have wide support at the DAO but few first-choice votes (e.g., everyone's second choice) have a chance at winning a seat. 

# Test Cases

Stoner Cats (Big Head Studio) has conducted 15 votes on influence.vote using multipreference quadratic voting.