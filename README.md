# HEY. YOU.
Yeah, you. Are you one of those people that still respect YDKJ:2015?
  Are you one of those people that love to play trivia games with friends and family, and not by yourself like a little loser?
  Are you one of those people that are annoyed that YDKJ:2015 is almost impossible to play on stream?
  Are you one of those people that want a easier way to write and test custom YDKJ:2015 episodes?

  Well, if you are one of these people, or multiple of these people in a trenchcoat, then stop crying about it because a new tool is here!

# YDKJ:2015 Developer Tools
### So, what is this mod?
I'm so glad you asked! (just play along) The YDKJ:2015 Developer Tools are a collection of tools used to aid the pursuit of video-call-friendly YDKJ:2015 gameplay. Obviously, it's not perfect, but to be fair, we aren't working with a whole lot here. All of these tools are accesibile from the DeveloperConsole, which can be enabled by setting "dev-console" to "true" in jbg.config.jet in YDKJ:2015's file directory, and activated by pressing "\`" on your keyboard while in-game. If you are not aware of how else to activate the DeveloperConsole, please learn elsewhere.

### And... what tools are there?
There are a few tools here to enhance your YDKJ:2015 experience. A lot of which are scoring related, however there are a couple others. Here's the full list at a glance:

- `enableUniformDisOrDatBonusPoints(Boolean)`
- `enableUniformShortiePoints(Boolean)`

- `setUniformDisOrDatBonusPointsValue(integer)`
- `setUniformShortiePointsValue(integer)`

- `setJackAttackAnswerRevealTimeMultiplier(Number)`

- `forceQuestion(String, integer)`

- `help()`
- `reset()`

But what do these actually do? Well, I was hoping the command names were obvious enough, but I'll go into detail anyways.

## enableUniformDisOrDatBonusPoints(Boolean) : void
Setting this command to true will alter the distribution of the 'TIME BONUS' the main DisOrDat player recieves upon completing the DisOrDat before time runs out. If this command is set to true, the DisOrDat 'TIME BONUS' the main DisOrDat player recieves will always be the uniform value set by a later command (default is $1,000) regardless of how much time that player took to complete the DisOrDat. Think of it as 'pity points' if you will.
  Setting this command to false will revert 'TIME BONUS' point distribution to its default time-based scoring.

## enableUniformShortiePoints(Boolean) : void
Setting this command to true will alter the distribution of points gained or lost in the Shortie (standard) questions. If this command is set to true, players will always win or lose points in the Shortie segment based on a uniform value set by a later command (default is $1,000) regardless of how fast players buzz in their answers. This uniform value is added or subtracted based on whether you answered correctly or incorrectly respectively, or based on whether you successfully screw a player or you get screwed yourself, respectively. It is also multiplied by the number of rounds elapsed.
  The "Wrong Answer of the Game" prize bonus is unaffected by this command.
  The "It's The Put The Choices Into Order Then Buzz In And See If You Are Right Question" correct answer bonus is unaffected by this command.
  Setting this command to false will revert Shortie point distrubution to its default time-based scoring.

## setUniformDisOrDatBonusPointsValue(integer) : void
If `enableUniformDisOrDatBonusPoints(Boolean)` is set to true, the 'TIME BONUS' given to the main DisOrDat player upon completing the DisOrDat before time runs out is set to the integer value inputted into this particular command.
  Default is $1,000.

## setUniformShortiePointsValue(integer) : void
If `enableUniformShortiePoints(Boolean)` is set to true, all scoring, added, subtracted, or multiplied, will be based on the integer value inputted into this particular command.
  Default is $1,000.
  The "Wrong Answer of the Game" prize bonus is unaffected by this command.
  The "It's The Put The Choices Into Order Then Buzz In And See If You Are Right Question" correct answer bonus is unaffected by this command.

## setJackAttackAnswerRevealTimeMultiplier(Number) : void
This command multiplies the time it takes for possible answers to be selected in the Jack Attack, before a new answer is introduced by the float number value provided in this particular command.
  Default is 1.0.
  For reference, the default 'Match Time' for each answer in the Jack Attack is 2.535 seconds. Multiplying this value by 1.5 for example, would make the 'Match Time' roughly 3.803 seconds.
  Note: Particularly regarding higher multipliers, all answers in the Jack Attack will remain buzzable, even after the text widget visually disappears. It is only when a new answer text visually appears that the answer you'll be buzzing will change.

## forceQuestion(String, integer) : void
This command forces one question, and one question only, to be tested for the entirity of the first two rounds. Useful for testing custom questions, or recording footage.
  Default behaviour doesn't force anything, String value is effectively equal to "".
  The String value refers to the ID of the question you wish to force. These can be found by searching through the path The Jackbox Party Pack\games\YDKJ2015\questions and forcing a question from there.
  The integer value refers to the TYPE of question it is. In YDKJ:2015, since all questions are stored in the same folder, different question types are instead defined by episode metadata. If a question ID is called, but the question type called from the episode metadata doesn't match the question's unique parameters, then the question fails to load. So, what are these question types?
#### 1
Refers to the standard Shortie question type. Special bumpers, Wrong Answers of the Game and such will not interfere with the question type.
#### 2
Refers to the DisOrDat question type. Even though you mostly won't see a DisOrDat more than once, it is still possible to test it for the entirity of the first two rounds.
#### 3
Refers to the Jack Attack question type. These questions can only ever be tested once per game, due to the Jack Attack ActionPackage being directly linked to the final scores/credits sequence.

## help() : void
Upon sending this command, a list of all the above commands will be listed in the logger. If you've ever used the DeveloperConsole in any other Jackbox Party Pack, this should be reasonably familiar to you. Remember, this list won't appear unless "logging" is set to "true" in this game's jbg.config.jet.

## reset() : void
Upon sending this command, all tuneable values will be reset to their defaults. This refers to Booleans in `enableUniform...Points(Boolean)` commands, integers in `setUniform...PointsValue(integer)` commands, and all other values customisable by these DeveloperConsole commands.

## Bonus: "isDemo":"Boolean",
This is a bonus toggle made for this game's jbg.config.jet. Simply type it in and set a Boolean value (and add a comma at the end of quotation marks if necessary) to give the "isDemo" config toggle functionality. When set to true, the game will load in its demo version, with limited episodes and exclusive widgets. Setting this config toggle to false will load the game in its original, commercial state.

### And that's a wrap on the YDKJ:2015 Developer Tools mod overview!
I hope this mod allows you to further enjoy your experience with YDKJ:2015. Whether it be helping you test you custom written episodes, or finally being able to play YDKJ:2015 with your online friends on a video call, I hope this mod can make a positive difference to you.
Be sure to check out my Youtube channel, in case that isn't how you got here in the first place, for more modded Jackbox shenanigains to come.

Have fun out there.

-NgheeApprentice
