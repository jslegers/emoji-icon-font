# Emoji icon font

This is an experimental font with ***650 glyphs***. For a live demo, go to [http://jslegers.github.io/emoji-icon-font/](http://jslegers.github.io/emoji-icon-font/).

This icon font pretty much a [proof of concept](https://en.wikipedia.org/wiki/Proof_of_concept) to illustrate the use of standardized UNICODE plains for icon fonts.

Most icons originate from Icomoon or Flatfont. Some originate from Wikimedia or the OpenSans font. The idea is to be as feature complete as possible, without losing much visual consistency.

Icons typically are re-adjusted to be centered on a square grid.

The font has a focus on icons that are already supported by [standardized UNICODE planes](https://en.wikipedia.org/wiki/Universal_Character_Set_characters) (❤, ☃,❄,★,☂,☭,⎗, ⎘,...)

The [Icomoon app](https://icomoon.io/app/) was used to build the icon set

##### Note :

For sake of performance and flexibility, this font could be split up into several sub-fonts based on content (eg. 'food icons', 'holiday icons', 'arrows', 'chess icons', ...). They could then be merged or used as individual fonts on a per project basis. As they use standard UNICODE values, there would not be any compatibility issue when combining several of these fonts individually, nor with combining these fonts with regular fonts.

That means you could do something like this :

```css
body {
    font-family: opensans, sans-serif;
}

.rate, .chat {
    font-family: icons-web, opensans, sans-serif;
}

.icon {
    font-family: icons-web, icons-arrows, icons-social,
                 icons-holiday, opensans, sans-serif;
}
```
```html
<div class='rate'>
    I rate this movie ★★★★☆
</div>

<p>
    You'll need to press the <span class="icon">⎗</span>
    button to go to the previous page.
<p>

<div class="chat">
   <p class="person1">I ❤ you!!<p>
   <p class="person2">I ❤ you too!!<p>
   <p class="person1">☺☺☺☺☺<p>
   <p class="person2">LOLZ<p>
</div>
```

IMO, this is a much cleaner, much more flexible and much more futureproof way to use icons in HTML/CSS than any other technique I've seen so far.

Of course, you will need UTF-8 support to make optimal use of this technique, but UTF-8 is already more or less the standard globally.

##### Note :
You could still use the oldschool `.icon-print:before` syntax if you don't want to use a cheat sheet for copy-pasting unicode values or the actual glyphs. This, however, should not be the recommended way if you're using [standardized UNICODE planes](https://en.wikipedia.org/wiki/Universal_Character_Set_characters) for your icon fonts.

##### Examples :

![Screenshot](http://jslegers.github.io/emoji-icon-font/screenshot1.png)
![Screenshot](http://jslegers.github.io/emoji-icon-font/screenshot2.png)
![Screenshot](http://jslegers.github.io/emoji-icon-font/screenshot3.png)
![Screenshot](http://jslegers.github.io/emoji-icon-font/screenshot4.png)
![Screenshot](http://jslegers.github.io/emoji-icon-font/screenshot5.png)

## Author

| [![twitter/johnslegers](https://en.gravatar.com/avatar/bf4cc94221382810233575862875e687?s=70)](http://twitter.com/johnslegers "Follow @johnslegers on Twitter") |
|---|
| [John slegers](http://www.johnslegers.com/) |