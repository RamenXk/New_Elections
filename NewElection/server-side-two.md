# Server Side Two

## Summary
Implement voting behavior, IRV election results, history endpoints, and caching/performance support.

## Responsibilities
- Build ballot submission and voting rules
  - Allow eligible voters to cast votes in assigned elections
  - Allow voters to change or remove their vote while the election is open
  - Prevent vote changes after an election closes
  - Administrators may view elections but must not vote
- Implement IRV tally logic
  - Count rank-1 votes
  - Eliminate the option with the fewest rank-1 votes when no option has a majority
  - Transfer ballots to the next ranked choice for eliminated options
  - Repeat until a winner is found or only one option remains
  - Ensure the algorithm works for full rankings and partial ranking cases if needed
- Create election results endpoints
  - Open election: current winner, option standings, elimination round state
  - Closed election: final winner, elimination sequence, margin versus total votes
  - Provide counts for:
    - eligible voters who voted
    - total eligible voters
    - ballots with each option as current highest rank
  - Clearly mark eliminated options and highlight current/winning option
- Build the history view API
  - Return past election summaries
  - Include owned and unowned election results as required
  - Protect voter identities; do not expose individual ballot voters
- Add caching and performance strategy
  - Cache result snapshots or computed IRV summaries
  - Reduce repeated expensive recomputation for frequently requested election data
- Test voting and result logic
  - Validate IRV correctness
  - Validate open/closed election behavior and permission enforcement

## Dependencies
- Depends on Server Side One for data models, auth, and election CRUD endpoints
- Frontend can target these endpoints once stabilized
