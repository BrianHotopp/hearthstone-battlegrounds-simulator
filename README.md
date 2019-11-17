Hearthstone Battlegrounds Battle Simulator
-----------------------------------------

A simulator for battles in the HS battlegrounds.
This program can quickly run over a battle many times, and give statistics on the results

Example output:

    Turn 8
    * 4/6 Cave Hydra
    * 8/2 Kaboom Bot
    * 10/4 Kaboom Bot
    * 9/6 Nightmare Amalgam
    * 2/2 Lightfang Enforcer
    * 4/6 Imp Gang Boss
    VS
    * 2/2 Kaboom Bot
    * 2/2 Kaboom Bot
    * 6/3 Cobalt Guardian, divine shield
    * 2/6 Security Rover
    * 4/2 Micro Machine
    * 1/5 Junkbot
    * 5/6 Psych-o-Tron, taunt, divine shield
    --------------------------------
    win: 2%, tie: 2%, lose: 95%
    mean score: -6.661, median score: -7
    percentiles: -14 -11 -9 -8 -8 -7 -6 -5 -4 -3 8
    actual outcome: -9, is at the 21-th percentile

The score at the end is the number of stars of the remanining minions of the first player, or negative the stars of the second player.
So a positive score means the first player wins by that many stars, a negative score means that the first player loses.
This score corresponds to damage dealt or taken, excluding damage from the character's level.
The program reports mean and median of the scores, and the 0%, 10%, .., 100% percentiles

A better user interface is a work in progress.


Input format
----
The input files consist of a series of commands to define the board state. See examples/run1.txt, or start the program and type `help`.


FAQ
----

Q: How do I put in a board state
A: Currently in C++ code, see test.cpp.
The dream is to eventually make an image recognizer to do this automatically, but that might not be worth the effort.

Q: What about Bob's tavern?
A: Currently only actual battles are simulated, the program doesn't know about buying, selling, leveling etc.

Q: What can I do with this?
A: 
* You can see how lucky you are
* You can learn to better position your minions
* (future) you can see how well your board is expected to do at a certain turn of the game

Q: Known bugs
A:
* Old Murk Eye only counts friendly minnions

