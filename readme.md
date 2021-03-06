UTF-8 Helper
------------

I am sure you love and use at least one of the world's amazing writing systems.
I am sure you are intrigued by how the computer terminals, various
applications, web browsers displayed those math symbols, those curvy characters
from eastern scripts. At least I am.

The unicode is a phenomenon, we all know that.
Also, the issues of "character" and "glyph" are philosophical ones. But I
believe in lamda as a concept only when I see λ on my terminal! 

I am a command line junkie on Unix (Linux). We all owe it to the great Ken
Thompson who invented the logical UTF-8 encoding and it's nice that Linux
adopted it.

That means I need a "Unix utility" to quickly tell me the most popular
enconding (UTF-8) of the unicode code points of all characters whose
<b> approximate names </b> I know!

If you had been looking for something like that, your search is over. All you
need is a Ruby interpreter and this script named "utf8". Here is how you could
use it:

<pre>
$ utf8 integral
∫ = 222B (integral)
∬ = 222C (double integral)
∭ = 222D (triple integral)
∮ = 222E (contour integral)
∯ = 222F (surface integral)
∰ = 2230 (volume integral)
∱ = 2231 (clockwise integral)
∲ = 2232 (clockwise contour integral)
∳ = 2233 (anticlockwise contour integral)
⌠ = 2320 (top half integral)
⌡ = 2321 (bottom half integral)
⎮ = 23AE (integral extension)
⨋ = 2A0B (summation with integral)
⨌ = 2A0C (quadruple integral operator)
⨍ = 2A0D (finite part integral)
⨎ = 2A0E (integral with double stroke)
⨏ = 2A0F (integral average with slash)
⨕ = 2A15 (integral around a point operator)
⨖ = 2A16 (quaternion integral operator)
⨗ = 2A17 (integral with leftwards arrow with hook)
⨘ = 2A18 (integral with times sign)
⨙ = 2A19 (integral with intersection)
⨚ = 2A1A (integral with union)
⨛ = 2A1B (integral with overbar)
⨜ = 2A1C (integral with underbar)

$ utf8 summation
⅀ = 2140 (double-struck n-ary summation)
∑ = 2211 (n-ary summation)
⎲ = 23B2 (summation top)
⎳ = 23B3 (summation bottom)
⨋ = 2A0B (summation with integral)

$ utf8 chess white king
♔ = 2654 (white chess king)
$ utf8 music note eight

𝅘𝅥𝅮 = 1D160 (musical symbol eighth note)
𝅘𝅥𝅲 = 1D164 (musical symbol one hundred twenty-eighth note)
...
</pre>

That's right. You just provide as many "approximate" keywords pertaining
to the "character" you are looking for and you get the unicode code point for it.
The characters are printed on the terminal using utf-8 encoding and displayed
correctly if you have a unicode font installed.

The applications are aplenty. You can then take the hex code that it
prints and put it on a web page as a direct entity reference to enliven
your webpages. (e.g. &#x2140 followed by ; i.e & # x 2 1 4 0 ; (without any intervening spaces)
 would display ⅀ on your webpage. Alternatively, on Mac, you can add the U+ keyboard and enter
a Unicode codepoint by keeping the Alt key pressed, on Linux, you can enter the Unicode codepoint
after Ctrl+Shift+U).

Of course there are many webpages that show this information. But
I needed a command line utility and now I've got one!

Enjoy.
Happy utf-8ing.
(A minor annoyance is that you need to have the "fonts" installed that display the glyphs associated with these "real characters". But that's just a Google search away -- Google: Install Unicode Font on Linux.)
