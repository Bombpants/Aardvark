# Aardvark

Project Aardvark is a placeholder name for a basic machine learning project that I am working on. This project will pit two "AI" in a head-to-head battle, where the AI will be in a 64ft x 64ft grid. For the earliest version, the AI will be allowed to choose one of several weapons, and will have a select number of stats (Health, armour, block chance, movement speed, attack speed, and damage), with a limited number of ability points that the AI can use to best optimize their builds. The AI will all use the same combat algorith for aardvark, where they will move directly towards their opponent if they are out of their range, and will move away from their opponent if they are in range to try to allow them to attack the AI and prevent the AI from attacking them. 

For Aardvark v1, the AI will all use the same weapon (a shortsword), and will not be moving. Movement speed will not be included as a stat, and the AI will have to find the optimal build to defeat their opponent and move on. Surviving AI will move on to the next round (fully healed), and a variation of them will move on (with stats slightly adjusted).

As of now, no rules for this game have been finalized, but base stats are expected to be:
    1 Health
    0 Armour
    0% Block chance
    0 Attack speed (2.5 seconds per attack)
    1 Damage

Increasing Health will increase health to (1 + health) ^ (1 + (1 - (0.995 ^ health)))
    Having 1 point in health will give the AI 2 health
    Having 10 points in health will give the AI 12.368 health
    Having 100 points in health will give the AI 622.994 health

Increasing Armour will reduce incoming damage to (0.9875) ^ (armour)
    Having 1 point in armour will reduce damage by 1.25%
    Having 10 points in armour will reduce damage by 11.81%
    Having 100 points in armour will reduce incoming damage by 71.57%

Increasing Block chance increase the chance to completely block an attack (and take no damage) to (0.9925) ^ (block_chance)
    Having 1 point in block chance will give a 0.75% chance to block an nattack
    Having 10 points in block chance will give a 7.25% chance to block an attack
    Having 100 points in block chance will give a 52.89% chance to block an attack

Increaasing Attack speed will change the time between attacks to 2.5 * (0.98 ^ attack_speed)
    Having 1 point in attack speed lets the AI attack once every 2.45 seconds
    Having 10 points in attack speed lets the AI attack once every 2.04 seconds
    Having 100 points in attack speed lets the AI attack once every 0.33 seconds

Increasing Damage will increase damage to (1 + (damage)) ^ (1 + (1 - (0.9925 ^ health)))
    Having 1 point in damage will let the AI deal 2 damage
    Having 10 points in damage will let the AI deal 11.67 damage
    Having 100 points in damage will let the AI deal 280.64 damage


Stat gain is non-linear, meaning the AI has to weigh the costs of upgrading a higher level skill comparede to a lower level skill. Health will increase at a faster rate than damage. Armour is more effective than block chance when the amount of points in them are equal. 



