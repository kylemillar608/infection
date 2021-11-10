# infection
Web3 infection game - winners get a unique NFT

## Overview
10,000 players join as their unique NFT avatar. Upon starting the game, each player receives 5 tokens. The game is played in rounds where each player has to strategize how to use their tokens effectively to avoid being infected. The last 100 players are the survivors and are allowed to keep their NFT. The other 9,900 players' NFTs will be destroyed.

## Rules
### Objective
Outlast 9,900 players and be one of the final 100 players to remain un-infected.
### Game Mechanics
#### Rounds
Each day is a new round. At the start of each day, each player is given 5 tokens. At the end of each day, the round ends and players are eliminated based on the mechanics below.
#### Attacking
To attack, a player sends any amount of tokens to another player. If the player under attack does not defend themselves, they will be eliminated. The number of players a given attacker can attack is only limited by the number of tokens that the attacker possesses. Multiple attackers can attack the same player.
#### Defending
A player's defense is the number of tokens that they DO NOT use to attack.
#### Outcomes of attacking
- If a player's defense is equal or larger than the total attack on them, they survive and all the tokens that were used to attack them become available for them to use for next round.

Example:
Player A (Defense=5)     <----Attacked with 4 tokens---- Player B (Defense=1)
At the end of the round, Player A survives because defense 5 > attack 4. 
Next round, Player A will have 14 tokens. 5 tokens from their defense, 4 tokens received from B, and 5 tokens for the start of the next round. 
Player B will have 6 tokens. 1 from their defense and 5 for the start of the next round.

- If a player's defense is lower than the total attack on them, they are eliminated. The attacker will receive all coins used for the attack back. They will also receive Player A's defense tokens, propportional to how much they contributed to the total attack. There are no fractions. All token calculations will be truncated and any remaining coins will go un-distributed. **what happens to coins that should go to a player but they are also eliminated

Example 1:
Player A (Defense=4)     <----Attacked with 5 tokens---- Player B (Defense=0)
At the end of the round, Player A is eliminated because defense 4 < attack 5. 
Player B is the only attacker, so Player B accounted for 100% of the total attack on Player A. Player B will receive 100% of Player A's defense tokens. 4 * 100% = 4. Next round, Player B will have 14 tokens. 5 from their attack, 4 from Player A's defenses, and 5 from the start of the next round

Example 2:
Player A (Defense=4)     <----Attacked with 2 tokens---- Player B (Defense=3)
                         <----Attacked with 4 tokens---- Player C (Defense=1)
At the end of the round, Player A is eliminated because defense 4 < attack 6.
Player B accounted for 2/6 (33%) of the total attack on Player A. Player B will receive 33% of Player A's defense tokens. 4 * 33% = 1 (truncated). Next round, Player B will have 10 tokens. 2 from their attack, 3 from their defense, 1 from Player A's defense, and 5 for the start of the next round
Player C accounted for 4/6 (66%) of the total attack on Player A. Player C will receive 66% of Player A' defense tokens. 4 * 66% = 2 (truncated). Next round, Player C will have 12 tokens. 4 from their attack, 1 from their defense, 2 from Player A's defense, and 5 for the start of the next round  

- Attack winnings are awarded transitively. If a player is eliminated, but they were supposed to receive attack winnings, the attack winnings go to the player that eliminated them.

Example:
Player A (Defense=1)     <----Attacked with 2 tokens---- Player B (Defense=3)     <----Attacked with 4 tokens---- Player C (Defense=1)   
At the end of the round, Player A and Player B are eliminated. Player B would have won 1 defense token, but that will go to player C instead.
Next round, Player C will have 14 tokens. 4 from their attack, 1 from their defense, 3 from their attack winnings for Player B, 1 from their attack winnings for Player A, and 5 for the start of the next round.

#### Mass Extinction (better name)
If 50% or more of players leave 50% or more of their tokens for defense, 50% of total remaining players will be eliminated in order of largest defense. Ties will be broken randomly. Players who did not defend with 50% of their tokens are not eligible for elimination. No attacks are evaluated this round, so all players who survive will receive their full attack refund.

Example:
Player A (Defense=5,Total=7)
Player B (Defense=4,Total=5)
Player C (Defense=10,Total=22)
Player D (Defense=4,Total=6)

Player A, Player C, and Player D defended with greater than 50% of their tokens. This is > 50% of remaining players. So, a mass extinction is triggered.
50% of the total remaining players (2 players) will be eliminated in order of highest defense
Player C has the highest defense, but is ineligible for elimination because they did not stack their defenses.
Player A has the next highest defense, they are eliminated.
Player B and D are tied for the next highest defense after A is eliminated. One of them will be chosen randomly as the last player to be eliminated as a part of this mass extinction.

### How the game starts
Upon reaching 10,000 players, all players will be notified (how?) when the game will start. This will be 3 days from when all players have chosen their NFT avatar. The exact start time will be detailed in the communication. The first round will begin and each player will receive their 5 tokens.

### How the game ends
When there are only 100 survivors, the game ends and the survivors will keep their NFT and any tokens they still own.

## How to join

***What happens when evaluating attacks and we get down to 100 players (could be less than 100)
***What happens when evaluating mass extincation and we get down to 100 players (could stop there)

***Add better terminology - attack refund, attack winnings, reduce redundancy, formatting
