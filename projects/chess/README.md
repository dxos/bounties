# Chess

A local-first tournament app for chess players.

## Goals
- Help validate the plugin API
- Get users interested in DXOS with a real world example
  - Potential for stress testing, understand how many concurrently clients ECHO could currently handle
- Encouraging community involvement through contributions and extensions.

## User Stories

### Essential

Joining and Managing Games: As a **user**, I want to be able to join the space and enter a chess game with a friend easily through invites (pinless), so that I can quickly start playing without friction.

Gameplay Experience: As a **player**, I need an intuitive and comprehensive in-game interface with time control, turn indicators, and the ability to navigate through game history, resign, offer a draw, or request a takeback, ensuring a rich and interactive gameplay experience.

Matchmaking and Player Interaction: As a **participant**, I want a system for basic lobby and user management, along with a matchmaking mechanism, to find opponents.


### Nice to have

Game History and Statistics: As a player, I wish to have access to my game history and player stats to analyze my performance, track my progress, and feel enmeshed as a member of the community.

Community Engagement and Extension: As a community member, I am interested in contributing to the development of the app, suggesting and potentially implementing variants, promoting community involvement and continuous enrichment of the platform.


## Features

### Phase 1
- [x] Create chess component with the following capabilities
  - [x] Time control
  - [x] Turn indicators
  - [x] In game history navigation (previous / next move)
  - [x] Resign
  - [x] Offer draw
  - [x] Take back
- [x] Sync game state via ECHO

### Phase 2
- [ ] Basic lobby and user management
- [ ] Basic game/space navigation
- [ ] Invites to games (pinless?)
- [ ] Game history

### Phase 3
- [ ] Tournaments
- [ ] Matchmaking (agent?)
- [ ] Player stats?
- [ ] Chess bots with agents?
- [ ] Example variant implementation

