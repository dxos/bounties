# Chess Arena

## Discussion

### High level design considerations
The project should be very welcoming to extension. At a minimum, it should be straight-forward to implement new chess variants as an individual contributor. This suggests a certain level of modularity is required around the overall game structure as well as the rules for each variant.

### Modeling Games

Event sourcing chess is a very appealing model here, we already have to store the list of moves, but if we introduce  time control, a list of moves is not enough, we need to know when moves are made. A chess game is two agents interacting over time through the constraints of the game. Representing games with an aggregate might allow the games to be more resilient to peer-peer shenanigans like a user playing multiple moves on multiple clients simultaneously. We can separate user intentions from the current synchronised state of the game.

*Tentative events:

- Game created (initial player + colour + time information + variant)
- PlayerJoined (second player)
- PlayerMoved
- TakeBackAccepted
- Player Resigns
- GameOver (win, loss, draw) + some metadata about how the game ended, checkmate? time out?

Modeling games this way, allows the actions and controls to generalize over many different chess variants. The aggregate can select from multiple rules engines when validating moves / generating the current state, and the view is free to present the game in the manner befitting the variant.

I'm very open to feedback and alternate methods of representation here!

### Growth / platform psychology

@richburdon suggested that getting people into chess-arenas could work as a growth exercise, getting people interested in the underlying technology, contributing new variants, bots, extensions and features. I've been thinking about the psychology of chess platforms and I suspect that having a rating in the space gives the user a stronger reason to stick around, there's a sense that you've gained something through work, effort and skill and people are less likely to relinquish this, vs a platform where you can just challenge people head to head with no evidence of continuity.

ELO systems are somewhat complex and open to abuse, but I think as a stretch goal it's something to be strongly considered.

