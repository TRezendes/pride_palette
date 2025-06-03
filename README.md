# Pride Palette

This CSS file collects the colors of 43 different pride flags in an easy to use, easy to remember color library for use in any html project.

It started as a component of my [IsMightier](https://wwww.IsMightier.org) project. I spun it off into its own repo so that it would be easy for anyone to download and use on its own.

## Class Naming Conventions

The various color classes are named by color and grouped by flag. The groups are identified by the name of the group the flag represents except in cases where there are multiple flags for one group. In those cases, either a more specific flag name or the name of the flag's creator is used as an identifier (see the [Lesbian Pride flags](#orange-pink-lesbian) for an example).

Some classes have been renamed in this version (e.g., "baker" became "rainbow", "bi" became "bisexual"). In those cases, the new class name is given in the table in this README, but the old class names are still present in the css file for backwards compatibility.

## Colors

Every color in the file has two classes and a variable associated with it. The first class sets the color as a background with either white or black as the text color. These classes set the text color first with an explicit color (either `#ffffff` or `#000000`) and then using the `contrast-color()` function for browsers that support it. The second class sets the color as the text color.

After I created the initial versions of this palette, I found that what I wanted more than color classes were color variables, so the css file now includes a css variable for each color in the palette. Variables are of the form `--pride-{flag}-{color}` and are set on `:root`.

Some colors are represented multiple times in the file. White, for instance, appears on many pride flags and is included in each group where it does. For the most part, if one flag uses a subset of colors from another flag, only the flag with the greater number of colors is included as a named group (for example, the pink Lesbian Pride flag uses the same stripe pattern as the Lipstick Lesbian Pride flag, merely omitting the "kiss" image, so it is not included separately). The main exception is the traditional rainbow Pride flag and the Progress Pride flag. Both are included as named groups.

### Color Sources

I want to offer my heartfelt thanks to flag designers who provide specific color values when sharing their designs. Settling on the specific colors for a given flag was not always easy. Where possible, I have looked to a flag's creator or original introduction to find the right colors. Many flags, however, have a vague origin or were originally shared only as bitmap images in posts where colors were given only as names, not values. In cases where I could not find a more authoritative source, I sourced the colors from a flag's image on Wikimedia Commons—either by looking at the SVG source or by using an eyedropper tool when only a bitmap image was available. In all cases, the source for the included colors is listed below the flag's image in this README.

## Generator

Included in this repo is a Notebook file that can be used to generate CSS code as used in pride-palette.css. Passing in a dictionary of the form:

```python
flags = {
    flagName1: {colorName1a: hexCode1a,colorName1b: hexCode1b},
    flagName2: {colorName2a: hexCode2a,colorName2b: hexCode2b},
    etc…
    }
```

Will generate

```css

:root {
    --pride-flagName1-colorName1a: #hexCode1a;
    --pride-flagName1-colorName1b: #hexCode1b;

    --pride-flagName2-colorName2a: #hexCode2a;
    --pride-flagName2-colorName2b: #hexCode2b;
}

/* flagName1 */
.pride-flagName1-colorName1a {
    color: #ffffff;
    color: contrast-color(#hexCode1a);
    background-color: #hexCode1a;
}

.pride-flagName1-colorName1b {
    color: #ffffff;
    color: contrast-color(#hexCode1b);
    background-color: #hexCode1b;
}


.pride-flagName1-colorName1a-text {
    color: #hexCode1a;
}

.pride-flagName1-colorName1b-text {
    color: #hexCode1b;
}


/* flagName1 */
.pride-flagName2-colorName2a {
    color: #ffffff;
    color: contrast-color(#hexCode2a);
    background-color: #hexCode2a;
}

.pride-flagName2-colorName2b {
    color: #ffffff;
    color: contrast-color(#hexCode2b);
    background-color: #hexCode2b;
}


.pride-flagName2-colorName2a-text {
    color: #hexCode2a;
}

.pride-flagName2-colorName2b-text {
    color: #hexCode2b;
}
```

Appending an asterisk (*) to the end of the colorName will change the text color from #ffffff to #000000 on the class where colorName is the background color.

## Flags, Classes, and Variables

### Original 8 Stripe Rainbow Flag

<a title="Gilbert Baker (Vector graphics by Fibonacci), Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Gay_flag_8.svg"><img width="256" alt="Gay Pride Flag (1978)" src="https://upload.wikimedia.org/wikipedia/commons/5/5e/Gay_flag_8.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Gay_flag_8.svg>

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-baker78-hot-pink  | pride-baker78-hot-pink-text  | --pride-baker78-hot-pink  | #ff69b4 |
| pride-baker78-red       | pride-baker78-red-text       | --pride-baker78-red       | #ff0000 |
| pride-baker78-orange    | pride-baker78-orange-text    | --pride-baker78-orange    | #ff8e00 |
| pride-baker78-yellow    | pride-baker78-yellow-text    | --pride-baker78-yellow    | #ffff00 |
| pride-baker78-green     | pride-baker78-green-text     | --pride-baker78-green     | #008e00 |
| pride-baker78-turquoise | pride-baker78-turquoise-text | --pride-baker78-turquoise | #00c0c0 |
| pride-baker78-indigo    | pride-baker78-indigo-text    | --pride-baker78-indigo    | #400098 |
| pride-baker78-violet    | pride-baker78-violet-text    | --pride-baker78-violet    | #8e008e |

### Rainbow Flag

<a title="Guanaco and subsequent editors, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Gay_Pride_Flag.svg"><img width="256" alt="Gay Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/4/48/Gay_Pride_Flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Gay_Pride_Flag.svg>

| class                | text class                | variable               | hex     |
|----------------------|---------------------------|------------------------|---------|
| pride-rainbow-red    | pride-rainbow-red-text    | --pride-rainbow-red    | #e40303 |
| pride-rainbow-orange | pride-rainbow-orange-text | --pride-rainbow-orange | #ff8c00 |
| pride-rainbow-yellow | pride-rainbow-yellow-text | --pride-rainbow-yellow | #ffed00 |
| pride-rainbow-green  | pride-rainbow-green-text  | --pride-rainbow-green  | #008026 |
| pride-rainbow-blue   | pride-rainbow-blue-text   | --pride-rainbow-blue   | #004dff |
| pride-rainbow-purple | pride-rainbow-purple-text | --pride-rainbow-purple | #750787 |


<br />

### Progress Pride Flag

<a title="Paul2520, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg"><img width="256" alt="LGBTQ+ rainbow flag Quasar &quot;Progress&quot; variant" src="https://upload.wikimedia.org/wikipedia/commons/f/fd/LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg>

| class                     | text class                     | variable                    | hex     |
|---------------------------|--------------------------------|-----------------------------|---------|
| pride-progress-red        | pride-progress-red-text        | --pride-progress-red        | #e40303 |
| pride-progress-orange     | pride-progress-orange-text     | --pride-progress-orange     | #ff8c00 |
| pride-progress-yellow     | pride-progress-yellow-text     | --pride-progress-yellow     | #ffed00 |
| pride-progress-green      | pride-progress-green-text      | --pride-progress-green      | #008026 |
| pride-progress-blue       | pride-progress-blue-text       | --pride-progress-blue       | #004dff |
| pride-progress-purple     | pride-progress-purple-text     | --pride-progress-purple     | #750787 |
| pride-progress-white      | pride-progress-white-text      | --pride-progress-white      | #ffffff |
| pride-progress-pink       | pride-progress-pink-text       | --pride-progress-pink       | #ffafc8 |
| pride-progress-light-blue | pride-progress-light-blue-text | --pride-progress-light-blue | #74d7ee |
| pride-progress-brown      | pride-progress-brown-text      | --pride-progress-brown      | #613915 |
| pride-progress-black      | pride-progress-black-text      | --pride-progress-black      | #000000 |

<br />

### Aceflux Pride Flag

<a title="Pride Flags For Us, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Acefluxflag.svg"><img width="256" alt="Aceflux Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/7/70/Acefluxflag.svg" /></a>

Color Source: <https://www.deviantart.com/pride-flags/art/Aceflux-1-544377703>

| class                 | text class                 | variable                | hex     |
|-----------------------|----------------------------|-------------------------|---------|
| pride-aceflux-rose    | pride-aceflux-rose-text    | --pride-aceflux-rose    | #c62253 |
| pride-aceflux-magenta | pride-aceflux-magenta-text | --pride-aceflux-magenta | #c12678 |
| pride-aceflux-fuchsia | pride-aceflux-fuchsia-text | --pride-aceflux-fuchsia | #c0279a |
| pride-aceflux-violet  | pride-aceflux-violet-text  | --pride-aceflux-violet  | #a928ac |
| pride-aceflux-orchid  | pride-aceflux-orchid-text  | --pride-aceflux-orchid  | #8c26ae |

### Achillean Flag

<a title="Pride-Flags, based on a design by pridenpositivity" href="https://commons.wikimedia.org/wiki/File:Achillean_flag.png"><img width="256" alt="Achillean Flag" src="https://upload.wikimedia.org/wikipedia/commons/e/e9/Achillean_flag.png" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Achillean_flag.png>

| class                       | text class                       | variable                      | hex     |
|-----------------------------|----------------------------------|-------------------------------|---------|
| pride-achillean-blue        | pride-achillean-blue-text        | --pride-achillean-blue        | #99c6ea |
| pride-achillean-cream       | pride-achillean-cream-text       | --pride-achillean-cream       | #f9fdea |
| pride-achillean-light-green | pride-achillean-light-green-text | --pride-achillean-light-green | #acdd4d |
| pride-achillean-dark-green  | pride-achillean-dark-green-text  | --pride-achillean-dark-green  | #659533 |

### Abrosexual Pride Flag

<a title="Kautr, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Abrosexual_flag.svg"><img width="256" alt="Abrosexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/c/c2/Abrosexual_flag.svg" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Abrosexual_flag.svg>

| class                        | text class                        | variable                       | hex     |
|------------------------------|-----------------------------------|--------------------------------|---------|
| pride-abrosexual-dark-green  | pride-abrosexual-dark-green-text  | --pride-abrosexual-dark-green  | #65c286 |
| pride-abrosexual-light-green | pride-abrosexual-light-green-text | --pride-abrosexual-light-green | #b4e4cc |
| pride-abrosexual-white       | pride-abrosexual-white-text       | --pride-abrosexual-white       | #ffffff |
| pride-abrosexual-light-pink  | pride-abrosexual-light-pink-text  | --pride-abrosexual-light-pink  | #e796b7 |
| pride-abrosexual-dark-pink   | pride-abrosexual-dark-pink-text   | --pride-abrosexual-dark-pink   | #d9446e |

### Agender Pride Flag

<a title="Salem Fontana, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Agender_pride_flag.svg"><img width="256" alt="Agender Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/e/ed/Agender_pride_flag.svg" /></a>

Color Source: <https://web.archive.org/web/20220612222135/https://majesticmess.com/encyclopedia/agender-flag/>

| class               | text class               | variable              | hex     |
|---------------------|--------------------------|-----------------------|---------|
| pride-agender-black | pride-agender-black-text | --pride-agender-black | #010204 |
| pride-agender-grey  | pride-agender-grey-text  | --pride-agender-grey  | #bcc4c6 |
| pride-agender-white | pride-agender-white-text | --pride-agender-white | #e9edee |
| pride-agender-green | pride-agender-green-text | --pride-agender-green | #b8f483 |

### Aroace Pride Flag

<a title="Original: Jace 'Aroaes' Vector:  Rummskartoffel, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Aroace_flag.svg"><img width="256" alt="Agender Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/1/12/Aroace_flag.svg" /></a>

Color Source: <https://aroaesflags.tumblr.com/post/181034758671/revised-aroace-flag-after-some-conversation-among>

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-aroace-orange     | pride-aroace-orange-text     | --pride-aroace-orange     | #e28c00 |
| pride-aroace-yellow     | pride-aroace-yellow-text     | --pride-aroace-yellow     | #eccd00 |
| pride-aroace-white      | pride-aroace-white-text      | --pride-aroace-white      | #ffffff |
| pride-aroace-light-blue | pride-aroace-light-blue-text | --pride-aroace-light-blue | #62aedc |
| pride-aroace-dark-blue  | pride-aroace-dark-blue-text  | --pride-aroace-dark-blue  | #203856 |

<br />

### Aromantic Pride

<a title="Cameron Whimsey, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Aromantic_Pride_Flag.svg"><img width="256" alt="Aromantic Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/a/ad/Aromantic_Pride_Flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Aromantic_Pride_Flag.svg>

| class                       | text class                       | variable                      | hex     |
|-----------------------------|----------------------------------|-------------------------------|---------|
| pride-aromantic-green       | pride-aromantic-green-text       | --pride-aromantic-green       | #3da542 |
| pride-aromantic-light-green | pride-aromantic-light-green-text | --pride-aromantic-light-green | #a7d379 |
| pride-aromantic-white       | pride-aromantic-white-text       | --pride-aromantic-white       | #ffffff |
| pride-aromantic-grey        | pride-aromantic-grey-text        | --pride-aromantic-grey        | #a9a9a9 |
| pride-aromantic-black       | pride-aromantic-black-text       | --pride-aromantic-black       | #000000 |

<br />

### Asexual Pride

<a title="AnonMoos (SVG file); AVEN (flag design), Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Asexual_Pride_Flag.svg"><img width="256" alt="Asexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/9/9e/Asexual_Pride_Flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Asexual_Pride_Flag.svg>

| class                | text class                | variable               | hex     |
|----------------------|---------------------------|------------------------|---------|
| pride-asexual-black  | pride-asexual-black-text  | --pride-asexual-black  | #000000 |
| pride-asexual-grey   | pride-asexual-grey-text   | --pride-asexual-grey   | #a3a3a3 |
| pride-asexual-white  | pride-asexual-white-text  | --pride-asexual-white  | #ffffff |
| pride-asexual-purple | pride-asexual-purple-text | --pride-asexual-purple | #800080 |

<br />

### International Bear Brotherhood Flag

<a title="Fibonacci, CC BY-SA 3.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Bear_Brotherhood_flag.svg"><img width="256" alt="International Bear Brotherhood Flag" src="https://upload.wikimedia.org/wikipedia/commons/c/c2/Bear_Brotherhood_flag.svg" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Bear_Brotherhood_flag.svg>

| class                    | text class                    | variable                   | hex     |
|--------------------------|-------------------------------|----------------------------|---------|
| pride-bear-dark-brown    | pride-bear-dark-brown-text    | --pride-bear-dark-brown    | #623804 |
| pride-bear-orange        | pride-bear-orange-text        | --pride-bear-orange        | #d56300 |
| pride-bear-golden-yellow | pride-bear-golden-yellow-text | --pride-bear-golden-yellow | #fedd63 |
| pride-bear-tan           | pride-bear-tan-text           | --pride-bear-tan           | #fee6b8 |
| pride-bear-white         | pride-bear-white-text         | --pride-bear-white         | #ffffff |
| pride-bear-grey          | pride-bear-grey-text          | --pride-bear-grey          | #555555 |
| pride-bear-black         | pride-bear-black-text         | --pride-bear-black         | #000000 |

<br />

### Bigender Pride Flag

<a title="JavacBenny, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Bigender_Flag.svg"><img width="256" alt="Bigender Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/9/92/Bigender_Flag.svg" /></a>

Color Source: <https://www.sexualdiversity.org/edu/flags/1098.php>

| class                     | text class                     | variable                    | hex     |
|---------------------------|--------------------------------|-----------------------------|---------|
| pride-bigender-pink       | pride-bigender-pink-text       | --pride-bigender-pink       | #c479a2 |
| pride-bigender-light-pink | pride-bigender-light-pink-text | --pride-bigender-light-pink | #eda5cd |
| pride-bigender-purple     | pride-bigender-purple-text     | --pride-bigender-purple     | #d6c7e8 |
| pride-bigender-white      | pride-bigender-white-text      | --pride-bigender-white      | #ffffff |
| pride-bigender-light-blue | pride-bigender-light-blue-text | --pride-bigender-light-blue | #9ac7e8 |
| pride-bigender-blue       | pride-bigender-blue-text       | --pride-bigender-blue       | #6d82d1 |

<br />

### Bisexual Pride Flag

<a title="Michael Page, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Bisexual_Pride_Flag.svg"><img width="256" alt="Bisexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/2/2a/Bisexual_Pride_Flag.svg"></a>

Color Source: <https://www.fotw.info/flags/qq-bi.html>

| class                 | text class                 | variable                | hex     |
|-----------------------|----------------------------|-------------------------|---------|
| pride-bisexual-pink   | pride-bisexual-pink-text   | --pride-bisexual-pink   | #d0006f |
| pride-bisexual-purple | pride-bisexual-purple-text | --pride-bisexual-purple | #8c4799 |
| pride-bisexual-blue   | pride-bisexual-blue-text   | --pride-bisexual-blue   | #0033a0 |

<br />

### Demiboy Flag

<a title="Trichromat, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Demiboy_Flag.svg"><img width="256" alt="Demiboy Flag" src="https://upload.wikimedia.org/wikipedia/commons/3/3a/Demiboy_Flag.svg" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Demiboy_Flag.svg>

| class                    | text class                    | variable                   | hex     |
|--------------------------|-------------------------------|----------------------------|---------|
| pride-demiboy-dark-grey  | pride-demiboy-dark-grey-text  | --pride-demiboy-dark-grey  | #7f7f7f |
| pride-demiboy-light-grey | pride-demiboy-light-grey-text | --pride-demiboy-light-grey | #c4c4c4 |
| pride-demiboy-blue       | pride-demiboy-blue-text       | --pride-demiboy-blue       | #9ad9eb |
| pride-demiboy-white      | pride-demiboy-white-text      | --pride-demiboy-white      | #ffffff |

<br />

### Demigirl Flag

<a title="Misc, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Demigirl_Flag.svg"><img width="256" alt="Demigirl Flag" src="https://upload.wikimedia.org/wikipedia/commons/7/73/Demigirl_Flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/7/73/Demigirl_Flag.svg>

| class                     | text class                     | variable                    | hex     |
|---------------------------|--------------------------------|-----------------------------|---------|
| pride-demigirl-dark-grey  | pride-demigirl-dark-grey-text  | --pride-demigirl-dark-grey  | #7f7f7f |
| pride-demigirl-light-grey | pride-demigirl-light-grey-text | --pride-demigirl-light-grey | #c4c4c4 |
| pride-demigirl-pink       | pride-demigirl-pink-text       | --pride-demigirl-pink       | #ffaec9 |
| pride-demigirl-white      | pride-demigirl-white-text      | --pride-demigirl-white      | #ffffff |

<br />

### Demiromantic Pride Flag

<a title="MarcoSnail, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Demiromantic_Pride_Flag.svg"><img width="256" alt="Demiromantic Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/3/36/Demiromantic_Pride_Flag.svg" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Demiromantic_Pride_Flag.svg>

| class                    | text class                    | variable                   | hex     |
|--------------------------|-------------------------------|----------------------------|---------|
| pride-demiromantic-black | pride-demiromantic-black-text | --pride-demiromantic-black | #000000 |
| pride-demiromantic-white | pride-demiromantic-white-text | --pride-demiromantic-white | #ffffff |
| pride-demiromantic-green | pride-demiromantic-green-text | --pride-demiromantic-green | #338a37 |
| pride-demiromantic-grey  | pride-demiromantic-grey-text  | --pride-demiromantic-grey  | #d2d2d2 |

### Demisexual Pride Flag

<a title="Original:  Vimopu Vector:  AnonMoos, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Demisexual_Pride_Flag.svg"><img width="256" alt="Demiromantic Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/a/a7/Demisexual_Pride_Flag.svg" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Demisexual_Pride_Flag.svg>

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-demisexual-black  | pride-demisexual-black-text  | --pride-demisexual-black  | #000000 |
| pride-demisexual-white  | pride-demisexual-white-text  | --pride-demisexual-white  | #ffffff |
| pride-demisexual-purple | pride-demisexual-purple-text | --pride-demisexual-purple | #6E0070 |
| pride-demisexual-grey   | pride-demisexual-grey-text   | --pride-demisexual-grey   | #d2d2d2 |

<br />

### Gay Men's Pride Flag

<a title="gayflagblog, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Gay_Men_Pride_Flag.svg"><img width="256" alt="Gay Men's Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/0/0a/Gay_Men_Pride_Flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/0/0a/Gay_Men_Pride_Flag.svg>

| class                 | text class                 | variable                | hex     |
|-----------------------|----------------------------|-------------------------|---------|
| pride-gay-dark-green  | pride-gay-dark-green-text  | --pride-gay-dark-green  | #078d70 |
| pride-gay-teal        | pride-gay-teal-text        | --pride-gay-teal        | #26ceaa |
| pride-gay-light-green | pride-gay-light-green-text | --pride-gay-light-green | #99e8c2 |
| pride-gay-white       | pride-gay-white-text       | --pride-gay-white       | #ffffff |
| pride-gay-light-blue  | pride-gay-light-blue-text  | --pride-gay-light-blue  | #7bade3 |
| pride-gay-purple      | pride-gay-purple-text      | --pride-gay-purple      | #5049cb |
| pride-gay-indigo      | pride-gay-indigo-text      | --pride-gay-indigo      | #3e1a78 |

<br />

### Genderfluidity Pride Flag

<a title="JJ Pole.McLennonSonGarethPW, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderfluidity_Pride-Flag.svg"><img width="256" alt="Genderfluidity Pride-Flag" src="https://upload.wikimedia.org/wikipedia/commons/b/b8/Genderfluidity_Pride-Flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Genderfluidity_Pride-Flag.svg>

| class                    | text class                    | variable                   | hex     |
|--------------------------|-------------------------------|----------------------------|---------|
| pride-genderfluid-pink   | pride-genderfluid-pink-text   | --pride-genderfluid-pink   | #ff75a2 |
| pride-genderfluid-white  | pride-genderfluid-white-text  | --pride-genderfluid-white  | #f5f5f5 |
| pride-genderfluid-purple | pride-genderfluid-purple-text | --pride-genderfluid-purple | #be18d6 |
| pride-genderfluid-black  | pride-genderfluid-black-text  | --pride-genderfluid-black  | #2c2c2c |
| pride-genderfluid-blue   | pride-genderfluid-blue-text   | --pride-genderfluid-blue   | #333ebd |


<br />

### Genderflux Pride Flag

<a title="deergoths, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderflux_Pride_Flag.png"><img width="256" alt="Genderflux Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Genderflux_Pride_Flag.png" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Genderflux_Pride_Flag.png>

| class                       | text class                       | variable                      | hex     |
|-----------------------------|----------------------------------|-------------------------------|---------|
| pride-genderflux-dark-pink  | pride-genderflux-dark-pink-text  | --pride-genderflux-dark-pink  | #f47694 |
| pride-genderflux-light-pink | pride-genderflux-light-pink-text | --pride-genderflux-light-pink | #f2a3b9 |
| pride-genderflux-grey       | pride-genderflux-grey-text       | --pride-genderflux-grey       | #cecece |
| pride-genderflux-light-blue | pride-genderflux-light-blue-text | --pride-genderflux-light-blue | #7ce0f7 |
| pride-genderflux-dark-blue  | pride-genderflux-dark-blue-text  | --pride-genderflux-dark-blue  | #3ecdf9 |
| pride-genderflux-yellow     | pride-genderflux-yellow-text     | --pride-genderflux-yellow     | #fff48e |

<br />

### Genderqueer Pride

<a title="Marilyn Roxie, McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderqueer_Pride_Flag.svg"><img width="256" alt="Genderqueer Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/1/1f/Genderqueer_Pride_Flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Genderqueer_Pride_Flag.svg>

| class                      | text class                      | variable                     | hex     |
|----------------------------|---------------------------------|------------------------------|---------|
| pride-genderqueer-lavender | pride-genderqueer-lavender-text | --pride-genderqueer-lavender | #b57edc |
| pride-genderqueer-white    | pride-genderqueer-white-text    | --pride-genderqueer-white    | #ffffff |
| pride-genderqueer-green    | pride-genderqueer-green-text    | --pride-genderqueer-green    | #4a8123 |

<br />

### Grey-aromantic Pride Flag

<a title="Enbysapphics, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Gray-aromantic_Pride_Flag.png"><img width="256" alt="Grey Asexuality Flag" src="https://upload.wikimedia.org/wikipedia/commons/f/f3/Gray-aromantic_Pride_Flag.png" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/f/f3/Gray-aromantic_Pride_Flag.png>

| class                     | text class                     | variable                    | hex     |
|---------------------------|--------------------------------|-----------------------------|---------|
| pride-grayromantic-purple | pride-grayromantic-purple-text | --pride-grayromantic-purple | #087D16 |
| pride-grayromantic-grey   | pride-grayromantic-grey-text   | --pride-grayromantic-grey   | #b2b2b2 |
| pride-grayromantic-white  | pride-grayromantic-white-text  | --pride-grayromantic-white  | #ffffff |

<br />

### Grey Asexuality Flag

<a title="Kautr, public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Grey_asexuality_flag.svg"><img width="256" alt="Grey Asexuality Flag" src="https://upload.wikimedia.org/wikipedia/commons/9/95/Grey_asexuality_flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/9/95/Grey_asexuality_flag.svg>

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-graysexual-purple | pride-graysexual-purple-text | --pride-graysexual-purple | #740195 |
| pride-graysexual-grey   | pride-graysexual-grey-text   | --pride-graysexual-grey   | #b2b2b2 |
| pride-graysexual-white  | pride-graysexual-white-text  | --pride-graysexual-white  | #ffffff |

<br />

### Intersex Pride

<a title="Morgan Carpenter (SVG file simplification by AnonMoos), CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Intersex_Pride_Flag.svg"><img width="256" alt="Intersex Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/3/38/Intersex_Pride_Flag.svg"></a>

Color Source <https://morgancarpenter.com/intersex-flag/>

| class                 | text class                 | variable                | hex     |
|-----------------------|----------------------------|-------------------------|---------|
| pride-intersex-yellow | pride-intersex-yellow-text | --pride-intersex-yellow | #ffd800 |
| pride-intersex-violet | pride-intersex-violet-text | --pride-intersex-violet | #7902aa |

<br />

### Leather, Latex, and BDSM Pride Flag

<a title="Tony DeBlase, public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Leather,_Latex,_and_BDSM_pride.svg"><img width="256" alt="Leather, Latex, and BDSM Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/6/62/Leather%2C_Latex%2C_and_BDSM_pride.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/6/62/Leather%2C_Latex%2C_and_BDSM_pride.svg>

| class               | text class               | variable              | hex     |
|---------------------|--------------------------|-----------------------|---------|
| pride-leather-blue  | pride-leather-blue-text  | --pride-leather-blue  | #18186b |
| pride-leather-black | pride-leather-black-text | --pride-leather-black | #000000 |
| pride-leather-red   | pride-leather-red-text   | --pride-leather-red   | #e70039 |

<br />

### Orange-pink Lesbian

<a title="SVG file by L ke in Inkscape, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lesbian_pride_flag_2018.svg"><img width="256" alt="Lesbian pride flag 2018" src="https://upload.wikimedia.org/wikipedia/commons/f/f8/Lesbian_pride_flag_2018.svg"></a>

Color Source <https://web.archive.org/web/20190608151937/https://majesticmess.com/encyclopedia/lesbian-flag-sadlesbeandisaster/>

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-gwen-dark-orange  | pride-gwen-dark-orange-text  | --pride-gwen-dark-orange  | #d52d00 |
| pride-gwen-orange       | pride-gwen-orange-text       | --pride-gwen-orange       | #ef7627 |
| pride-gwen-light-orange | pride-gwen-light-orange-text | --pride-gwen-light-orange | #ff9a56 |
| pride-gwen-white        | pride-gwen-white-text        | --pride-gwen-white        | #ffffff |
| pride-gwen-pink         | pride-gwen-pink-text         | --pride-gwen-pink         | #d162a4 |
| pride-gwen-dusty-pink   | pride-gwen-dusty-pink-text   | --pride-gwen-dusty-pink   | #b55690 |
| pride-gwen-dark-rose    | pride-gwen-dark-rose-text    | --pride-gwen-dark-rose    | #a30262 |

<br />

### Labrys Lesbian

<a title="Thespoondragon, CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Labrys_Lesbian_Flag.svg"><img width="256" alt="Labrys Lesbian Flag" src="https://upload.wikimedia.org/wikipedia/commons/d/dd/Labrys_Lesbian_Flag.svg"></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/d/dd/Labrys_Lesbian_Flag.svg>

| class               | text class               | variable              | hex     |
|---------------------|--------------------------|-----------------------|---------|
| pride-labrys-violet | pride-labrys-violet-text | --pride-labrys-violet | #993399 |
| pride-labrys-black  | pride-labrys-black-text  | --pride-labrys-black  | #000000 |
| pride-labrys-white  | pride-labrys-white-text  | --pride-labrys-white  | #ffffff |

<br />

### Lipstick Lesbian

<a title="xles (SVG file), CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lipstick_lesbian_Pride_Flag.svg"><img width="256" alt="Lipstick lesbian Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/0/06/Lipstick_lesbian_Pride_Flag.svg"></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/0/06/Lipstick_lesbian_Pride_Flag.svg>

| class                     | text class                     | variable                    | hex     |
|---------------------------|--------------------------------|-----------------------------|---------|
| pride-lipstick-dark-pink  | pride-lipstick-dark-pink-text  | --pride-lipstick-dark-pink  | #a40061 |
| pride-lipstick-dusty-pink | pride-lipstick-dusty-pink-text | --pride-lipstick-dusty-pink | #b75592 |
| pride-lipstick-pink       | pride-lipstick-pink-text       | --pride-lipstick-pink       | #d063a6 |
| pride-lipstick-lavender   | pride-lipstick-lavender-text   | --pride-lipstick-lavender   | #e4accf |
| pride-lipstick-white      | pride-lipstick-white-text      | --pride-lipstick-white      | #ededeb |
| pride-lipstick-pale-red   | pride-lipstick-pale-red-text   | --pride-lipstick-pale-red   | #c54e54 |
| pride-lipstick-brown      | pride-lipstick-brown-text      | --pride-lipstick-brown      | #8a1e04 |
| pride-lipstick-red        | pride-lipstick-red-text        | --pride-lipstick-red        | #f30943 |

<br />

### Maverique Flag

<a title="Nikki, public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Maverique_flag.svg"><img width="256" alt="Maverique Flag" src="https://upload.wikimedia.org/wikipedia/commons/3/3d/Maverique_flag.svg" /></a>

Color Source: <http://queerascat.com/2014/06/the-maverique-flag/>

| class                  | text class                  | variable                 | hex     |
|------------------------|-----------------------------|--------------------------|---------|
| pride-maverique-yellow | pride-maverique-yellow-text | --pride-maverique-yellow | #fff344 |
| pride-maverique-white  | pride-maverique-white-text  | --pride-maverique-white  | #ffffff |
| pride-maverique-orange | pride-maverique-orange-text | --pride-maverique-orange | #f49622 |

<br />

### Non-binary Pride

<a title="Kye Rowan, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Nonbinary_flag.svg"><img width="256" alt="Nonbinary flag" src="https://upload.wikimedia.org/wikipedia/commons/7/75/Nonbinary_flag.svg"></a>

Color Source: <https://thejasmineelf-blog.tumblr.com/flagfaq>

| class                  | text class                  | variable                 | hex     |
|------------------------|-----------------------------|--------------------------|---------|
| pride-nonbinary-yellow | pride-nonbinary-yellow-text | --pride-nonbinary-yellow | #fff433 |
| pride-nonbinary-white  | pride-nonbinary-white-text  | --pride-nonbinary-white  | #fff8e7 |
| pride-nonbinary-purple | pride-nonbinary-purple-text | --pride-nonbinary-purple | #9b59d0 |
| pride-nonbinary-black  | pride-nonbinary-black-text  | --pride-nonbinary-black  | #2d2d2d |

<br />

### Omnisexuality Flag

<a title="pastelroswell, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Omnisexuality_flag.svg"><img width="256" alt="Omnisexuality Flag" src="https://upload.wikimedia.org/wikipedia/commons/0/0b/Omnisexuality_flag.svg" /></a>

Color Source: <https://lgbtqia.fandom.com/wiki/Omnisexual#Flag>

| class                       | text class                       | variable                      | hex     |
|-----------------------------|----------------------------------|-------------------------------|---------|
| pride-omnisexual-light-pink | pride-omnisexual-light-pink-text | --pride-omnisexual-light-pink | #fc9ccc |
| pride-omnisexual-pink       | pride-omnisexual-pink-text       | --pride-omnisexual-pink       | #fc54bc |
| pride-omnisexual-black      | pride-omnisexual-black-text      | --pride-omnisexual-black      | #240444 |
| pride-omnisexual-blue       | pride-omnisexual-blue-text       | --pride-omnisexual-blue       | #645cfc |
| pride-omnisexual-light-blue | pride-omnisexual-light-blue-text | --pride-omnisexual-light-blue | #8ca4fc |

<br />

### Pangender Flag

<a title="Nikki, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pangender_flag.svg"><img width="256" alt="Omnisexuality Flag" src="https://upload.wikimedia.org/wikipedia/commons/e/ec/Pangender_flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/e/ec/Pangender_flag.svg>

| class                  | text class                  | variable                 | hex     |
|------------------------|-----------------------------|--------------------------|---------|
| pride-pangender-yellow | pride-pangender-yellow-text | --pride-pangender-yellow | #fff798 |
| pride-pangender-orange | pride-pangender-orange-text | --pride-pangender-orange | #feddcc |
| pride-pangender-pink   | pride-pangender-pink-text   | --pride-pangender-pink   | #ffebfc |
| pride-pangender-white  | pride-pangender-white-text  | --pride-pangender-white  | #ffffff |

<br />

### Pansexuality Pride

<a title="This SVG version: KiwiNeko14. Original idea: Tumblr blog PansexualFlag., Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pansexuality_Pride_Flag.svg"><img width="256" alt="Pansexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/a/a2/Pansexuality_Pride_Flag.svg"></a>

Color Source: <https://web.archive.org/web/20111103184455/http://pansexualflag.tumblr.com/post/1265215452/hex-color-codes-you-dont-have-to-use-these-exact>

| class                  | text class                  | variable                 | hex     |
|------------------------|-----------------------------|--------------------------|---------|
| pride-pansexual-pink   | pride-pansexual-pink-text   | --pride-pansexual-pink   | #ff218c |
| pride-pansexual-yellow | pride-pansexual-yellow-text | --pride-pansexual-yellow | #ffd800 |
| pride-pansexual-blue   | pride-pansexual-blue-text   | --pride-pansexual-blue   | #21b1ff |

<br />

### Polyamory Pride Flag (Pi)

<a title="Jim Evans, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Polyamory_Pride_Flag.svg"><img width="256" alt="Polyamory Pride Flag, Pi Design" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Polyamory_Pride_Flag.svg" /></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Polyamory_Pride_Flag.svg>

| class              | text class              | variable             | hex     |
|--------------------|-------------------------|----------------------|---------|
| pride-evans-blue   | pride-evans-blue-text   | --pride-evans-blue   | #0000ff |
| pride-evans-red    | pride-evans-red-text    | --pride-evans-red    | #ff0000 |
| pride-evans-black  | pride-evans-black-text  | --pride-evans-black  | #000000 |
| pride-evans-yellow | pride-evans-yellow-text | --pride-evans-yellow | #ffff00 |

<br />

### Polyamory Pride Flag (Heart)

<a title="Red Howell, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Tricolor_Polyamory_Pride_Flag.svg"><img width="256" alt="Polyamory Pride Flag, Chevron and Heart Design" src="https://upload.wikimedia.org/wikipedia/commons/9/90/Tricolor_Polyamory_Pride_Flag.svg" /></a>

Color Source: <https://www.polyamproud.com/flag/>

| class                | text class                | variable               | hex     |
|----------------------|---------------------------|------------------------|---------|
| pride-howell-white   | pride-howell-white-text   | --pride-howell-white   | #ffffff |
| pride-howell-gold    | pride-howell-gold-text    | --pride-howell-gold    | #fcbf00 |
| pride-howell-blue    | pride-howell-blue-text    | --pride-howell-blue    | #009fe3 |
| pride-howell-magenta | pride-howell-magenta-text | --pride-howell-magenta | #e50051 |
| pride-howell-purple  | pride-howell-purple-text  | --pride-howell-purple  | #340c46 |

<br />

### Polysexuality Pride

<a title="McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Polysexuality_Pride_Flag.svg"><img width="256" alt="Polysexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/a/ae/Polysexuality_Pride_Flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Polysexuality_Pride_Flag.svg>

| class                  | text class                  | variable                 | hex     |
|------------------------|-----------------------------|--------------------------|---------|
| pride-polysexual-pink  | pride-polysexual-pink-text  | --pride-polysexual-pink  | #f61cb9 |
| pride-polysexual-green | pride-polysexual-green-text | --pride-polysexual-green | #07d569 |
| pride-polysexual-blue  | pride-polysexual-blue-text  | --pride-polysexual-blue  | #1c92f6 |

<br />

### Queer Flag

<a title="pastelmemer, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Queer_Flag.svg"><img width="256" alt="Polyamory Pride Flag, Chevron and Heart Design" src="https://upload.wikimedia.org/wikipedia/commons/8/86/Queer_Flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/8/86/Queer_Flag.svg>

| class                  | text class                  | variable                 | hex     |
|------------------------|-----------------------------|--------------------------|---------|
| pride-queer-black      | pride-queer-black-text      | --pride-queer-black      | #000000 |
| pride-queer-light-blue | pride-queer-light-blue-text | --pride-queer-light-blue | #99d9ea |
| pride-queer-blue       | pride-queer-blue-text       | --pride-queer-blue       | #00a2e8 |
| pride-queer-green      | pride-queer-green-text      | --pride-queer-green      | #b5e61d |
| pride-queer-white      | pride-queer-white-text      | --pride-queer-white      | #ffffff |
| pride-queer-orange     | pride-queer-orange-text     | --pride-queer-orange     | #ffc90e |
| pride-queer-dark-pink  | pride-queer-dark-pink-text  | --pride-queer-dark-pink  | #fd6666 |
| pride-queer-pink       | pride-queer-pink-text       | --pride-queer-pink       | #ffaec9 |

<br />

### Sapphic Flag

<a title="pastelmemer, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Sapphic_Flag_alternate_with_violet.svg"><img width="256" alt="Sapphic Flag" src="https://upload.wikimedia.org/wikipedia/commons/9/93/Sapphic_Flag_alternate_with_violet.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/9/93/Sapphic_Flag_alternate_with_violet.svg>

| class                    | text class                    | variable                   | hex     |
|--------------------------|-------------------------------|----------------------------|---------|
| pride-sapphic-pink       | pride-sapphic-pink-text       | --pride-sapphic-pink       | #fd8ba8 |
| pride-sapphic-white      | pride-sapphic-white-text      | --pride-sapphic-white      | #ffffff |
| pride-sapphic-violet     | pride-sapphic-violet-text     | --pride-sapphic-violet     | #c76bc5 |
| pride-sapphic-yellow     | pride-sapphic-yellow-text     | --pride-sapphic-yellow     | #fff71e |
| pride-sapphic-light-pink | pride-sapphic-light-pink-text | --pride-sapphic-light-pink | #f996c9 |

<br />

### Transfemme Flag

<a title="Rowan Ackerman, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Transfemme_Flag.svg"><img width="256" alt="Transfemme Flag" src="https://upload.wikimedia.org/wikipedia/commons/d/d8/Transfemme_Flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/d/d8/Transfemme_Flag.svg>

| class                          | text class                          | variable                         | hex     |
|--------------------------------|-------------------------------------|----------------------------------|---------|
| pride-transfeminine-blue       | pride-transfeminine-blue-text       | --pride-transfeminine-blue       | #73deff |
| pride-transfeminine-light-pink | pride-transfeminine-light-pink-text | --pride-transfeminine-light-pink | #ffe0ed |
| pride-transfeminine-pink       | pride-transfeminine-pink-text       | --pride-transfeminine-pink       | #ffb5d5 |
| pride-transfeminine-dark-pink  | pride-transfeminine-dark-pink-text  | --pride-transfeminine-dark-pink  | #ff8cbe |

<br />

### Transgender Pride

<a title="SVG file Dlloyd based on Monica Helms design, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Transgender_Pride_flag.svg"><img width="256" alt="Transgender Pride flag" src="https://upload.wikimedia.org/wikipedia/commons/b/b0/Transgender_Pride_flag.svg"></a>

Color Source: <https://commons.wikimedia.org/wiki/File:Transgender_Pride_flag.svg>

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-transgender-blue  | pride-transgender-blue-text  | --pride-transgender-blue  | #5bcefa |
| pride-transgender-pink  | pride-transgender-pink-text  | --pride-transgender-pink  | #f5a9b8 |
| pride-transgender-white | pride-transgender-white-text | --pride-transgender-white | #ffffff |

<br />

### Transmasc Flag

<a title="Rowan Ackerman, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Transmasc_Flag.svg"><img width="256" alt="Transmasc Flag" src="https://upload.wikimedia.org/wikipedia/commons/7/7c/Transmasc_Flag.svg" /></a>

Color Source: <https://upload.wikimedia.org/wikipedia/commons/7/7c/Transmasc_Flag.svg>

| class                           | text class                           | variable                          | hex     |
|---------------------------------|--------------------------------------|-----------------------------------|---------|
| pride-transmasculine-pink       | pride-transmasculine-pink-text       | --pride-transmasculine-pink       | #ff8ABD |
| pride-transmasculine-sky-blue   | pride-transmasculine-sky-blue-text   | --pride-transmasculine-sky-blue   | #cdf5fe |
| pride-transmasculine-light-blue | pride-transmasculine-light-blue-text | --pride-transmasculine-light-blue | #9aebff |
| pride-transmasculine-blue       | pride-transmasculine-blue-text       | --pride-transmasculine-blue       | #74dfff |

<br />

### Xenogender Flag

<a title="pastelmemer, CC BY-SA 4.0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Xenogender_Flag.png"><img width="256" alt="Xenogender Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d2/Xenogender_Flag.png/330px-Xenogender_Flag.png" /></a>

Color Source: <https://www.deviantart.com/pride-flags/art/Xenogender-1-656548427>

<br />

| class                   | text class                   | variable                  | hex     |
|-------------------------|------------------------------|---------------------------|---------|
| pride-xenogender-red    | pride-xenogender-red-text    | --pride-xenogender-red    | #ff6691 |
| pride-xenogender-coral  | pride-xenogender-coral-text  | --pride-xenogender-coral  | #ff9997 |
| pride-xenogender-orange | pride-xenogender-orange-text | --pride-xenogender-orange | #ffb782 |
| pride-xenogender-yellow | pride-xenogender-yellow-text | --pride-xenogender-yellow | #fbffa6 |
| pride-xenogender-blue   | pride-xenogender-blue-text   | --pride-xenogender-blue   | #84bbff |
| pride-xenogender-violet | pride-xenogender-violet-text | --pride-xenogender-violet | #9c84ff |
| pride-xenogender-purple | pride-xenogender-purple-text | --pride-xenogender-purple | #a317ff |
| pride-xenogender-white  | pride-xenogender-white-text  | --pride-xenogender-white  | #ffffff |

<br />

### Disability Pride Flag

<a title="Ann Magill, Public Domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Visually_Safe_Disability_Pride_Flag.svg"><img width="256" alt="Disability Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/5/55/Visually_Safe_Disability_Pride_Flag.svg" /></a>

Color Source: <https://www.urevolution.com/blogs/magazine/disability-pride-flag>

| class                     | text class                     | variable                    | hex     |
|---------------------------|--------------------------------|-----------------------------|---------|
| pride-disability-charcoal | pride-disability-charcoal-text | --pride-disability-charcoal | #585858 |
| pride-disability-green    | pride-disability-green-text    | --pride-disability-green    | #3aaf7d |
| pride-disability-blue     | pride-disability-blue-text     | --pride-disability-blue     | #7ac1e0 |
| pride-disability-grey     | pride-disability-grey-text     | --pride-disability-grey     | #e9e9e9 |
| pride-disability-yellow   | pride-disability-yellow-text   | --pride-disability-yellow   | #eedf77 |
| pride-disability-red      | pride-disability-red-text      | --pride-disability-red      | #cf7280 |

<br />

## Notes, Acknowledgements, and Sources

- The Palette currently contains 43 different flags explicitly. The fact that a particular flag is or is not included in this version of the Palette does not reflect a desire to gatekeep the queer community or to render judgement on who should or should not be included and accepted. The flags included in this palette are drawn from the list of flags on the [Wikipedia Pride Flag page](https://en.wikipedia.org/wiki/Pride_flag). Wikipedia is always changing, so the flags here may not exactly mirror the current state of the Pride Flag page, but I am happy with the collection as it stands, at least for now.

- In addition to 42 LGBTQIA+ pride flags, I have also included the [Disability Pride Flag](https://en.wikipedia.org/wiki/Disability_flag). Queer rights and disability rights go hand in hand. Also, it's a good flag.

- All flag images in this README are linked from [Wikimedia Commons](https://commons.wikimedia.org).

- For more vexillological fun, check out my [Pride War Flags](https://232.software/WarFlags/) project.

- This project was developed on the ancestral land of the Susquehannock people



<br />

---

<br />

![GitHub](https://img.shields.io/github/license/TRezendes/pride_palette?color=d60270&style=flat-square) ![GitHub release (latest by date)](https://img.shields.io/github/v/release/TRezendes/pride_palette?color=0038a8&label=version&style=flat-square)

