# Emoji icon font

This is an experimental font with ***650 glyphs***. For a live demo, go to [http://jslegers.github.io/emoji-icon-font/](http://jslegers.github.io/emoji-icon-font/).

This icon font pretty much a [proof of concept](https://en.wikipedia.org/wiki/Proof_of_concept) to illustrate the use of standardized [UNICODE planes](http://en.wikipedia.org/wiki/Plane_(Unicode)) for icon fonts.

Most icons originate from [Icomoon](https://icomoon.io/) or [Flaticon](http://www.flaticon.com/). Some originate from [Wikimedia](https://commons.wikimedia.org/wiki/Main_Page) or the [OpenSans font](http://www.fontsquirrel.com/fonts/open-sans). The idea is to be as feature complete as possible, without losing much visual consistency.

Icons typically are re-adjusted to be centered on a square grid.

The font has a focus on icons that are already supported by [standardized UNICODE planes](https://en.wikipedia.org/wiki/Universal_Character_Set_characters) (❤, ☃,❄,★,☂,☭,...)

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
    Press the <span class="icon">&#8635;�</span> button to refresh the page.
<p>

<div class="chat">
   <p class="person1">I ❤ you!!<p>
   <p class="person2">I ❤ you too!!<p>
   <p class="person1">☺☺☺☺☺<p>
   <p class="person2">LOLZ<p>
</div>
```

##### 12 key principles :

1. You use an ***EXACT*** match native unicode character directly in the HTML. It is an exact match either with respect to the meaning of the icon, with respect to the look of the icon or both. There's a multitude of which I ***selected 650 of the most interesting ones [here](http://jslegers.github.io/emoji-icon-font/)***.

2. If your editor can't display the character or you don't like using odd characters in your HTML, you can use an HTML entity instead. For example, you can use both `&#9993;` and `&#x2709;` to display an envelope.

3. Styling icons requires minimal effort. The color, background and other styling of your icons will automaticly match that of the text next to it. Adding an icon to a multi-state `add to favorites` button can be as simple as changing `<button>Add to favorites</button>` to `<button>&#9733; Add to favorites</button>`.

4. Like you would pick a regular font to match the look-and-feel of your site, you'd do the same with an icon font. Different icon fonts are interchangeable because the value of each icon is standardized and defined by UNICODE standards. You can also combine several minifonts or add all the icons you need to an existing regular font, eg. with the easy-to-use and already popular [Icomoon app](https://icomoon.io/app/).

5. 95% of all browsers support `@font-face`. They will produce a consistent look-and-feel for all of your icons. For that 5% that doesn't support `@font-face`, native UNICODE support can be used as a fallback for symbols that have nature support on these devices.

6.  the necessity to support languages like Hindi, Japanese and Mandarin makes support for UNICODE a requirement for every phone out there. The increasing popularity of [Emoji](http://en.wikipedia.org/wiki/Emoji) in countries other than Japan is likely to result in the addition of even more icons with the arrival of UNICODE 8 and up, allowing icon sets to grow in a standardized fashion.

7. Where an exact match native unicode character is not possible, you can use the private use area. This should, however, be standardized as much as possible to ensure future compatibility and icons should move to standard planes when support is added. If this approach were adopted by multiple popular icon fonts, this would also make it more likely for those icons to become part of a future Unicode standard, as happened with the addition of 250 [Emoji](http://en.wikipedia.org/wiki/Emoji) in the UNICODE 7.0 release of June, 2014.

8. All devices are already capable of displaying UNICODE if a font is present to show the characters. All desktop browsers (including IE6-IE8) already have full support for `@font-face`. Browsers not supporting `@font-face` are a small minority. That amounts to about 5% of the global market.

9. The vast majority of that 5% that doesn't support `@font-face` involves cheap low-end phones for third world countries and other budget markets. They can be pretty much ignored if we consider the Western markt only, where anyone not using a somewhat advanced smartphone is considered a fossil by most.

10. In the West, the remaining number of phones not supporting `@font-face` will continue to decrease very rapidly to even more insignificant numbers when considering the replacement rate of mobile phones. 

11. The memory restrictions of budget-aware low-end mobile phones are the only reason some more recent models still don't support `@font-face`. Not only is this totally irrelevant for the Western market, but it's just a matter of little time before memory capacity will have increased enough to provide `@font-face` support for even the most cheap-ass third world cell phones.

12. When screen readers need to be prevented from accessing an icon, a combination of `aria-hidden="true"` and/or `speak: none` should do the trick if you add them to an HTML span element that wraps one or more icons you'd like to hide.

------------------

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
