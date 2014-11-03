JSON data description
========

This repository contains the data used in the paper **"Quantifying long-range correlations and 1/f patterns in a minimal experiment of social interaction"** (Front. Psychol. | doi: 10.3389/fpsyg.2014.01281) by  Manuel G. Bedia, Miguel Aguilera, Tomas Gomez, David G. Larrode and Francisco Seron.
http://journal.frontiersin.org/Journal/10.3389/fpsyg.2014.01281/abstract

This data is being released under the terms of the Creative Commons Zero (CC0 1.0) waiver
http://creativecommons.org/publicdomain/zero/1.0/

Each json file records contains the information recorded by the computer of each individual participants, storing information about him and his opponent
In each round of the experiment, a message containing precise information about the players is sent from participants to the server. Messages are stored in a text file (one per client) which is built with lines of JSON objects. These fields with the information stored are shown below.

{"roundInfo":{

**"matchId"**: matchIdValue
Numeric identifier for a pair of players in game 

**"player"**: playerValue
Name of a player

**"playerId"**: playerIdValue
32-digit hexadecimal label of a player

**"pairPlayer"**: pairPlayerValue
Name of the player's opponent

**"pairPlayerId"**: pairPlayerIdValue
32-digit hexadecimal label of the player's opponent

**"round"**: roundValue,
Current round

**"collisions"**: collisionsValue
Number of collisions suffered by a player as a result of his crossings with other players

**"timeDelay"**: timeDelayValue,
Delay (miliseconds) between the opponent bot and the player (taken the last as the reference). This field is used when the type of bot is SHADOW.

**"pixelDelay"**: pixelDelayValue,
Delay (miliseconds) between the opponent bot and the player (taken the last as the reference). This field is used when the type of bot is SHADOW.

**"oscillatoryList"**: [oscillatoryListValue],
List of 2-element objects: instant of time and position of the receptor. It contains the trace made by the opponent OSCILLATORY bot during that round.

**"pairFile"**: pairFileValue,
When the opponent player is a human, this label contains the URL of the file with information of the round.

**"maxTime"**: maxTimeValue,
Number of seconds per round.

**"squareSide"**: squareSideValue,
Side length (pixels) of a square-receptor.

**"lineSize"**: lineSizeValue,
Number of pixels of the line.

**"list"**: [listValue],
List of 3-element objects: time instant, position of the receptor and collision index (boolean). It is the trace made by the player during that round.

**"reply"**: reply,
Player's response at the end of the round, which can be:
 - 'human': the opponent is a human
 - 'almost-human': the probability that the opponent were a human is high 
 - 'almost-bot': the probability that the opponent were a bot is high 
 - 'bot': the opponent is a bot

**"success"**: success
It indicates the result of the response:
 - 'true': right answer
 - 'false': wrong answer

}}