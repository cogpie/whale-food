# Developer Notes

## Emoji font support information

- Fonts I tried:
    - https://github.com/googlefonts/noto-emoji/ – does not work in most browsers, looks ok, however bitmap will have scaling issues
    - https://github.com/eosrei/twemoji-color-font/releases based on https://twemoji.twitter.com/ v13 – does not work in most browsers, looks really good, vector based with SVG spec
    - https://github.com/mozilla/twemoji-colr/releases based on https://twemoji.twitter.com/ v12 – seems to have the greatest support (chrome, silk, android, ios), solid-color 'flat' vectors but look pretty good, makes it feel more child-like which works for this game; only missing seal
        - https://github.com/matrix-org/matrix-react-sdk/pull/4672 based on https://twemoji.twitter.com/ v13 – I could have rebuilt for v13 Unicode emojis but found it done, also woff2 is much smaller than ttf and seems to have wide support https://caniuse.com/woff2
- COLR format most supported color font type - https://www.colorfonts.wtf/#w-node-85d8080e63a6-0134536f
- Sea life emoji https://www.emojis.com/animals/marine/

## Possible Phaser 3.50 bugs

### Font parsing bug

#### Noticed
So the 'font-family' cannot be three words long to work eg. "my named font" will fail, but "my_named font" will work!

#### Investigation
Nothing stopping this in [the definition](https://www.w3.org/TR/2018/REC-css-fonts-3-20180920/#font-family-desc), they even have an example "New Century Schoolbook" which they have quoted, but it didn't need to be...

So this is a bug in the setFont function of the TextStyle object in Phaser3, [the _else_ section](https://github.com/photonstorm/phaser/blob/v3.50.0/src/gameobjects/text/TextStyle.js#L572). It
only accepts the 2nd or 3rd token (' ' delimited) as the font family.

#### Speculation
But how does this work for "my_named font" then?

So for a string such as `'123px "my_named font"'` we would get a result of `{ fontStyle='123px', fontSize='"my_named', fontFamily='font"' }`. I suspect these get recombined as a string to form `'123px "my_named font"'` before being passed to render, so it gets correctly interpreted downstream. Whereas `'123px "my named font"'` would become `{ fontStyle='123px', fontSize='"my', fontFamily='named' }` which would be recombined as `'123px "my named'` and so fail. I didn't check the render code but I imagine it is something like this.

### Text canvas size if 0 bug? 

#### Noticed
When creating sea life, sporadically I would get a DOMException

#### Investigation
Some digging found that the canvas size was 0 when the text was going to be written to it. However, since using a workaround and then taking it out to investigate further I've not been able to reproduce it.

So it may be my initial weaker use of Phaser that I've since corrected and didn't realise it fixed this too. Sadly it wasn't under source control in those early stages, so can't go back. A lesson in this. I've removed the workaround (a try-catch for DOMException in a while loop checking for a defined text object)