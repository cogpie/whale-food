# Task Log

## version alpha/beta
- Initial version...

## version 1: Set Whale Free
- Reduce size and center location of collision box of whale
- Ensure sea life cannot be 0px in size... in fact, tiny fonts are invisible too (min of 4 pixels, maybe more)
- Whale drag picks appropriate rotation to align with direction
- Add shift key to make whale move faster when using keys
- Add game help text
- Use known external font
   - Update Twemoji to unicode 13 to bring in seal
- Add mermaid and merman, and oysters
- Allow any key to restart game
- Ensure further input events will not try to reload next level after the first event has started
- Have it automatically reload when the whale vanishes
- (Aaron) Larger drag-hit box for whale, esp. for phones

## Potential tasks for later versions...
...This is a bit like a product backlog.

- Add indication that it is loading, some of the later rounds take a while to create the sea life atm
  - Improve performance by not reloading page, but start a new round and add in just the new creatures?
  - Can a font be drawn once then cloned? So cache images in advance
- More fluid sea life motion
  - Different movement for each type?
  - Do things in a more Phaser way – animations, velocities, etc.
  - (Aaron) Sea life can swim away from whale
- (Andi/Aaron) Spawn more sea life over the game? Currently, more spawned each round
- (Carles) Does whale die if it doesn't eat? Not in the game, but when all things are eaten it is ambiguous until the next round starts... however, in a game if the player deliberately starves the whale it stays alive atm
- Use custom font file with only glyphs needed to reduce size of it
- Fix sea life hiding in border when small? or is it just small grey sea life that match background an hard to see...
- Use multiple fonts in Phaser text so whale in help text is the same as the one in the game
- Only display title and help for first invocation of the game
- In later rounds introduce 'plastics' that 'harm' the whale in some way
  - (Tania) should the mild eco message [at the end of a round] be made stronger, linked to websites in this space?
  - Dark outcome: have the level of plastics increase, and food decrease, such that eventually you can no longer win th game :'( ... is this too much?
- Keep a record for how long each round took and maybe hold onto the best one (or best three...)
- (Jess) have different sea life 'worth' more, and a time limit so the skill aim is to eat higher value things
  - Related to Carles' comment, maybe the 'time' is more about the whale essentially starving
- Add music and sound effects to increase engagement (trialed successfully with my child and my voice – early proto)
- scale game for size of viewport