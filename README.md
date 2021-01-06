# Whale Food

![Whale Food logo](assets/whale-food-logo.png)

▶️ [**Play 'Whale Food'**](https://cogpie.github.io/whale-food/)

**Whale Food** is a simple eye-hand coordination game, aimed at younger gamers, where the whale (🐋) has to eat all the other sea life on screen to get to the next round... where they can eat even more.

Hope you or your child enjoys the game 😊

## Help

### How do I play it?

On a computer with a keyboard you can use arrow keys (← ↑ → ↓) to move the whale around. Holding `shift` whilst moving will make the whale go faster. You can also use your mouse, click on the whale and drag them around to eat sea life.

On a mobile/tablet/touch-screen you can touch the whale and drag them around to eat the food.

### Any game options?

Yes, you can:

- choose your round by adding `round=NUMBER` eg. [play 'Whale Food' on round 6 ie. 60 creatures](https://cogpie.github.io/whale-food/?round=6)
  - each round this will increase the number of sea life by 10
- you can also use any other emoji (or text) instead of whale by adding `whaleText=EMOJI` eg. [play 'Whale Food' as a snail](https://cogpie.github.io/whale-food/?whaleText=🐌)
  - it is built for the whale emoji, so some emoji's rotation and collision detection will be off

### Is there a [Konami code](https://en.wikipedia.org/wiki/Konami_Code) or any other cheat codes?

Not yet... [what should they do?](https://github.com/cogpie/whale-food/discussions)

## Troubleshooting

### The font doesn't work?

Oh no! Sorry to hear that! I did try a few fonts out and [I decided that Twitter's Twemoji font in WOFF2 COLOR format was the best](notes/DEVELOPER-NOTES.md)

Please see if you can play 'Whale Food' with:

- [Google's Noto Color Emoji font in TTF CBDT](https://cogpie.github.io/whale-food/?font=noto_cbdt)
- [Twitter's Twemoji font in TTF SVG](https://cogpie.github.io/whale-food/?font=twemoji_svg_13)
- [Twitter's Twemoji font in TTF COLR](https://cogpie.github.io/whale-food/?font=twemoji_colr_12)

If these do not work then [let me know](https://github.com/cogpie/whale-food/issues) what device/operating system/browser and model/versions you are trying to run it on and I'll eventually see if I can fix it or find a font that will work – thank you!

### It takes longer and longer to load later rounds, what's going on?

This is [a known issue](notes/TASKLOG.md). Essentially, the more sea life you have the longer it will take to create them and the more taxing this will be on your device (so the more power it will need too).

I tested the 500th round which has 5000 sea life on my computer and it took about 30s to load!

I will address this in a future release.

### It doesn't load at all! Can you fix it?

How frustrating/annoying, apologies for that. If it is not loading at all then this may indicate a bug/exception. If you are technically able you could open up the browser's console and check for errors. Please [file an issue](https://github.com/cogpie/whale-food/issues) if you find anything – thank you!

If not, then I do not have capacity to provide extensive support, but would be grateful if you could [let me know](https://github.com/cogpie/whale-food/issues) what device/operating system/browser and model/versions you are trying to get it working on for future updates. In the meantime, please try another device or browser and see if that fixes it.

## Tasks, Issues, Feedback

- If you have some idea for improvement then please send a pull/merge request, or [let me know](https://github.com/cogpie/whale-food/discussions) and I'll add it to my [Task Log](notes/TASKLOG.md)
- I collected some [Developer Notes](notes/DEVELOPER-NOTES.md) if you're interested
- Finally, if you find any other issue then [please let me know](https://github.com/cogpie/whale-food/issues), that would be great!

Feel free to [leave any other constructive criticism, feedback, praise, your user stories, etc.](https://github.com/cogpie/whale-food/discussions) Thank you!

## Acknowledgements

Thank you to:
- my child for their ideas and encouragement – I hope your love for whales stays with you for a long time. ❤️
- Photo Storm for the excellent Phaser HTML5 game framework.
- Google, Twitter and Ubuntu for their fonts.
- [Brad Erickson](https://keybase.io/bde), Matrix, and Mozilla for producing font files from Twitter's Twemoji font – let me know if I need any further attribution, iiuc you all inherit Tewmoji's license.
- Adobe for their Web Font Loader library.

And thank you very much to all those who have taken time test it and provided feedback.

## Licensing

This project:
- is released under the MIT license ([see license](LICENSE))
- is distributed with and uses Photon Storm's [Phaser](https://phaser.io/) HTML5 game framework ([see license](licenses/LICENSE-PHASER))
- is distributed with and uses Twitter's [Twemoji](https://twemoji.twitter.com/) font ([see license](licenses/LICENSE-TWEMOJI))
- is distributed with and uses Google's [Noto Color Emoji](https://www.google.com/get/noto/help/emoji/) font ([see license](licenses/LICENSE-NOTOCOLOREMOJI))
- uses Adobe's [Web Font Loader](https://github.com/typekit/webfontloader) ([see license](licenses/LICENSE-WEBFONTLOADER))
- uses Ubuntu's [Ubuntu](https://fonts.google.com/specimen/Ubuntu) font ([see licence](licenses/LICENSE-UBUNTUFONT))