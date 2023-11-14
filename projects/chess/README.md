# Chess

A local-first tournament app for chess players.

## Goals
- Help validate the plugin API
- Get users interested in DXOS with a real world example
  - Potential for stress testing, understand how many concurrently clients ECHO could currently handle
- Encouraging community involvement through contributions and extensions.

## Features

### Phase 1
- [ ] Create a new package `apps/arena` using the app template
- [ ] Import the existing chess plugin and get it displayed by default
- [ ] Invites to games (pinless?)
- [ ] Host on `arena.dxos.com/chess` (or similar domain)
- [ ] Reuse composer layout (e.g., Spaces sidebar/navtree)

### Phase 2

- [ ] Basic lobby and user management
- [ ] Basic game/space navigation

### Phase 3

- [ ] Matchmaking (agent?)
- [ ] Game history
- [ ] Player stats?
- [ ] In game capabilities
  - [ ] Time control
  - [ ] Turn indicators
  - [ ] In game history navigation (previous / next move)
  - [ ] Ability to resign, offer draw, takeback
  - [ ] Premove?
- [ ] Chess bots with agents?