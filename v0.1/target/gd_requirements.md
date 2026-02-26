Here are discussed what are the game design key components we want to express through this prototype.  
These are specific situations, challenges and feelings that we try to express in the player.

These components are really the essential components of the final project, beside this first v0.1. The goal in this prototype is to just express them with not much more candy, and make it so in the most constrained environment possible to make it achievable with the less resources possible.

- [Tempo](#tempo)
  - [General movements](#general-movements)
  - [Point A to Point B](#point-a-to-point-b)
    - [Why this happens](#why-this-happens)
    - [How this happens](#how-this-happens)
  - [Rest](#rest)
    - [Consequence on level design](#consequence-on-level-design)
    - [Game design approach](#game-design-approach)
      - [Player Health](#player-health)
      - [Consequence of Shield](#consequence-of-shield)
      - [Consequence of Flesh](#consequence-of-flesh)
      - [Other rests](#other-rests)


# Tempo

A general concept that is exploited with many of the following game design components is tempo.  

In such a game where the main point of interest is fundamentals mechanics, moving around and shooting enemies seems to be the only point, but if it was, it'd get boring quickly.

What makes this mechanic expression interesting in multiplayer games is the constant switch of tempo. You're aggressive because you're at advantage, and suddenly something unexpected happens and you're in danger, so you switch to a much more defensive play style, maybe even hiding, or completely focusing on your movements, and then there is an interest point to proclaim, and various other events can happen to drastically change the tempo of the game continuously.

This is the idea of tempo. Yes, the main tempo phase, and the one the player wants to get in to create value (like score) is the one where he is purely shooting enemies. But first, he should not be able to reamin in this phase all the time, second, this tempo phase has constraints too, and disallows some other interractions.

## General movements

The design of general movements are thought in that tempo intend. Unlike many solo FPS, the focus is not that much on speed, but more on control.

The player can of course try to fight at high speed, but the enemies movements, time to kill, hit boxes, and general game design, should make it hard, and incentivize the player to fight like he would it most multiplayer games.

That is, at relatively low speed, mostly anchored in the ground, and eventually using **control** based skilled movements (wall bouncing, straffing, lurching ...) to enhance their survivability, but not so much of **speed** based movements.

## Point A to Point B

We want the player to have gameplay phases where he stops fighting to fully commit to a *displacement*. From a point A to a point B, most likely some point of interest.

### Why this happens

That could be for various reasons :
- Picking common resources (amos, health packs)
- Picking temporary resources like temporary power ups or other bonuses
- Get to a wave of enemies, in intend to get back in the shooting phase

Some more intricated ones could be :
- A direct game objective, like picking something up, protecting something, etc.
- Safety, for example if an area becomes explicitly too dangerous (explosions, fire, undeafeatable temporary enemy ..) Think of it as battle royale rings.

### How this happens

These A -> B moments can be as short as possible to allow the smallest map design, as long as the player get this clear feeling of tempo change - I'm fighting, now I'm leaving fight to move to next interest point.

The player also has a role on how he wants to proceed - he should always have multiple options, that are both situation, and skill-dependant.
- The most efficient route (consumes less resources)
- The fastest route
- The safest route
- Intermediate choices (for example, with a small detour to an another smaller point of interest)
  
With more skill or some specific situations, he get access to more options.


## Rest

We want the player to have some rest phases. These are defensive, intense phases where the player is at high disadvantage and does not have the resource to remain in the combat phase.

Concretely, this would probably mostly express through the need to heal up.

### Consequence on level design

The map must provide places to hide, covers, and enough distance to allow the player to leave a dangerous situation.

In more details, it must provide a terrain of expression for the situations explained above, in the Game design approach section.

### Game design approach

#### Player Health

For now, the idea of health is as follows - 

The player as volatile shield as the first health layer. It's a layer of health that regenerates automatically after a little while spent without taking damage.

Below that layer, is the main health, the flesh layer. This one do not regenerate automatically, and some consumable must be used for that.

#### Consequence of Shield

This allows the player to play fully agressively, since losing shield is not a big deal, but to some extent as losing flesh is a lot more punitive.
This naturally creates an incentive to constantly switch between exposed agression and defensive rest, to optimize the health.

That will create the first type of rest, micro-rest, to let shield regenerate.

The handles for that are :
- Shield regen stale - how much time with no hit before the shield starts regenerating
- Shield regen speed - how fast it regenrates once it does

Higher stale will sharpen the agression-rest contrast, speed will balance it out.

If these handles are not enough to get the right feeling, for example, the micro-rests are too long but adjusting the handles to fix that would make shield too strong, we could eventually introduce an active fast cast consumeable too, that can speed up the process when the player has access to it.

This is much more specific and will depend on the general rythm of the game, might not be necessary.

#### Consequence of Flesh

The other type of rest, will happen when the player do not manage his shield well, and must heal his flesh up.

Healing flesh will require a long animation cast, like in typical battle royales.

This is intended to create this kind of rest punishment. During this animation, the player cannot do anything but wait, and move. They must thus actively hide, and spend a little bit of time protected to be back in the fight.

#### Other rests

Some other rests phases could happen for other reasons. Waiting for something to happen to start acting.

It could be, because the player has low health, but does not have healing packs, and must wait for a healing pack to spawn. He will hide and jump on it as soon as it does spawn.

It could be, he's letting the enemies come to him, or move to specific location, maybe because he's waiting for a power up to spawn and commit with it, or because he'd rather fight in a different place.

There's probably other possibilities, but these are the main ideas.

