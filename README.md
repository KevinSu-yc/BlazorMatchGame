# Card Matching Game (Final)

## This is a card matching game that require players to flip and memorize the emojis then find all matching cards.

### What I changed from DRAFT to FINAL:

The modifications I made to the game were mostly implemented in the draft version but there are still some parts I want to adjust for the final version. First, the number of matches found in a game was reset immediately when the time is up or players complete the game. According to the feedback I got in class, I updated the draft version so the number of matches found will be kept at the end of a game and only reset when players start another game. 

In addition, I updated the layout of the interface. I added a brief intro about how to start the game and win. The time that completes a game only appears when players win. Also, I added more visual cues to help players understand what's going on with the game such as reminding players the time left is less than 10 seconds by changing the text color to red and showing a message when the time is up or a player breaks a record.

### Modifications I made to the game:

1. **Use a count-down timer instead (Requirement C)**
    - The game now has a time limit for players to match the cards instead so players won't always win the game. The timer counts down as soon as players click a card to start a game and the remaining time will show under the cards.
2. **Add a slider for players to select the time limit to complete a game (Requirements A and B)**
    - I'd like this modification to be graded for **requirement B**. This is the only modification I made to allow players to take control of a part of the game. I also took time to make sure everything make sense while players use the slider under different situations.
    - Added a variable called `timeLimitDisplay` to show how much time the player is selecting using a slider, so players can control how fast they have to complete a game. Once the player uses the slider to select a time limit, the text next to the slide and the remaining time under the cards will change accordingly. In addition, if a player uses the slider after a game starts, the game will stop immediately and ask the player to start again with the new time limit.
3. **Hide the cards (Requirements A and C)**
    - I'd like this modification to be graded for **requirement C** since it made the game more challenging as players have to memorize the cards. Also, it took me most of my time to figure out when the cards should be hidden or revealed and how to actually make that happen.
    - Added a list called `hiddenCards` to show "?" on the cards before they are clicked. Players now have to memorize the position of the emojis to match the hidden cards. Only show a pair of cards that are clicked. If the pair doesn't match, hide the cards when players click on the next card, otherwise, clear the matched cards.
4. **Calculate the complete time for each round and keep track of the shortest record (Requirement A)**
    - I'd like this modification to be graded for **requirement A**. I added a lot of variables for this modification and learned about how the timer works to calculate the values I wanted.
    - Added one variable called `startTime` to keep the time limit for each round of a game, one called `completeTime` to keep the time to complete a game, and one called `shortestTime` to keep track of the shortest time to complete a game. `startTime` will update while the player uses the slider for the time limit. `completeTime` is calculate by `startTime` - the time remaining when a game is completed. Replace the value `shortestTime` with `completeTime` when it's the first time a player completes a game or `completeTime` is less than `shortestTime`.

### Update to do for week 2:

- Keep the number of matches found when a game ends. (The number of matches found now resets to 0 when a game ends.)
- Learn more about bootstrap to style the page.
- Update some comments and explain more about if else conditions.
