# Card Matching Game (Draft)

## This is a card matching game that require players to flip and memorize the emojis then find all matching cards.

### For week 1 draft I worked on the following enhancements:

1. **Use count down timer**
    - Requirement C
    - The game now has a time limit for players to match the cards instead so players won・t always win the game
    - Fully implemented. The timer counts down as soon as players click a card and the remaining time will show under the cards.
2. **Add a slider for players to select the time limit to complete a game**
    - Requirements A and B
    - Added a variable called `timeLimitDisplay` to show how much time players are selecting using a slider, so players can control how fast they have to complete a game.
    - Fully implemented. Once players use the slider to select a time limit, the text next to the slide and the remaining time under the cards will change accordingly. In addition, if a player uses the slider after a game starts, the game will stop immediately and ask the player to start again with the new time limit.
3. **Hide the cards**
    - Requirements A and C
    - Added a list called `hiddenCards` to show ：?； on the cards before they are clicked. Players now have to memorize the position of the emojis to match the hidden cards.
    - Fully implemented. Only show a pair of cards that that are clicked. If the  pair doesn・t match, hide the cards when players click on a next card, otherwise, clear the matched cards.
4. **Calculate complete time for each round and keep track of the shortest record**
    - Requirement A
    - Added one variable called `startTime` to keep the time limit for each round of a game, one called `completeTime` to keep the time to complete a game, and one called `shortestTime` to keep track of the shortest time to complete a game.
    - Fully implemented. `startTime` will update while player uses the slider for time limit. `completeTime` is calculate by `startTime` - the time remaining when a game is completed. Replace the value `shortestTime` with `completeTime` when it・s first time a player completes a game or `completeTime` is less than `shortestTime` .

### Update to do for week 2:

- Keep the number of matches found when a game ends. (The number of matches found now resets to 0 when a game ends.)
- Learn more about bootstrap to style the page.
- Update some comments and explain more about if else conditions.
