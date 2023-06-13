# Pride Palette

This CSS file collects the colors of 15 different pride flags in an easy to use, easy to remember color library for use in any html project.

It started as a component of my [IsMightier](https://wwww.IsMightier.org) project. I spun it off into its own repo so that it would be easy for anyone to download and use on its own.

## Class Naming Conventions

The various color classes are named by color and grouped by flag. The groups are identified by the name of the group the flag represents except in cases where there are multiple flags for one group. In those cases, eiher a more specific flag name or the name of the flag's creator is used as an identifier (see the [Lesbian Pride flags](#labrys-lesbian) for an example).

## Colors

Every color in the file has two classes associate with it. The first class sets the color as a background with either white or black as the text color, and the second class sets the color as the text color.

Some colors are represented multiple times in the file. White, for instance, appears on many pride flags and is included in each group where it does. For the most part, if one flag uses a subset of colors from another flag, only the flag with the greater number of colors is included as a named group (for example, the pink Lesbian Pride flag uses the same stripe pattern as the Lipstick Lesbian Pride flag, merely ommitting the "kiss" image, so it is not included separately). The main exception is the traditional rainbow Pride flag and the Progress Pride flag. Both are included as named groups.

## Generator

Included in this repo is a Notebook file that can be used to generate CSS code as used in pride-palette.css. Passing in a dictionary of the form:

```python
flags = {
    flagName1: {colorName1a: hexCode1a,colorName2a: hexCode2a},
    flagName2: {colorName1b: hexCode1b,colorName2b: hexCode2b},
    etc…
    }
```

Will generate

```css
.pride-flagName1-colorName1a {
    color: #ffffff;
    background-color: #hexCode1a;
}
.pride-flagName1-colorName2a {
    color: #ffffff;
    background-color: #hexCode2a;
}

.pride-flagName1-colorName1a-text {
    color: #hexCode1a;
}
.pride-flagName1-colorName2a-text {
    color: #hexCode2a;
}

.pride-flagName2-colorName1b {
    color: #ffffff;
    background-color: #hexCode1b;
}
.pride-flagName2-colorName2b {
    color: #ffffff;
    background-color: #hexCode2b;
}

.pride-flagName2-colorName1b-text {
    color: #hexCode1b;
}
.pride-flagName2-colorName2b-text {
    color: #hexCode2b;
}
```

Appending an asterisk (*) to the end of the colorName will change the text color from #ffffff to #000000 on the class where colorName is the background color.

## Flags and Classes

### Rainbow Flag

<a title="Guanaco and subsequent editors, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Gay_Pride_Flag.svg"><img width="256" alt="Gay Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Gay_Pride_Flag.svg/512px-Gay_Pride_Flag.svg.png"></a>
| class              | text class              | hex     |
|--------------------|-------------------------|---------|
| pride-baker-red    | pride-baker-red-text    | #e40303 |
| pride-baker-orange | pride-baker-orange-text | #ff8c00 |
| pride-baker-yellow | pride-baker-yellow-text | #ffed00 |
| pride-baker-green  | pride-baker-green-text  | #008026 |
| pride-baker-blue   | pride-baker-blue-text   | #004dff |
| pride-baker-purple | pride-baker-purple-text | #750787 |

<br />

### Progress Pride Flag

<a title="Paul2520, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg"><img width="256" alt="LGBTQ+ rainbow flag Quasar &quot;Progress&quot; variant" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg/256px-LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg.png"></a>

| class                     | text class                     | hex     |
|---------------------------|--------------------------------|---------|
| pride-progress-red        | pride-progress-red-text        | #e40303 |
| pride-progress-orange     | pride-progress-orange-text     | #ff8c00 |
| pride-progress-yellow     | pride-progress-yellow-text     | #ffed00 |
| pride-progress-green      | pride-progress-green-text      | #008026 |
| pride-progress-blue       | pride-progress-blue-text       | #004dff |
| pride-progress-purple     | pride-progress-purple-text     | #750787 |
| pride-progress-white      | pride-progress-white-text      | #ffffff |
| pride-progress-pink       | pride-progress-pink-text       | #ffafc8 |
| pride-progress-light-blue | pride-progress-light-blue-text | #74d7ee |
| pride-progress-brown      | pride-progress-brown-text      | #613915 |
| pride-progress-black      | pride-progress-black-text      | #000000 |

<br />

### Transgender Pride

<a title="SVG file Dlloyd based on Monica Helms design, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Transgender_Pride_flag.svg"><img width="256" alt="Transgender Pride flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Transgender_Pride_flag.svg/256px-Transgender_Pride_flag.svg.png"></a>

| class             | text class             | hex     |
|-------------------|------------------------|---------|
| pride-trans-blue  | pride-trans-blue-text  | #5bcefa |
| pride-trans-pink  | pride-trans-pink-text  | #f5a9b8 |
| pride-trans-white | pride-trans-white-text | #ffffff |

<br />

### Bi Pride

<a title="Michael Page, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Bisexual_Pride_Flag.svg"><img width="256" alt="Bisexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Bisexual_Pride_Flag.svg/256px-Bisexual_Pride_Flag.svg.png"></a>

| class           | text class           | hex     |
|-----------------|----------------------|---------|
| pride-bi-pink   | pride-bi-pink-text   | #d60270 |
| pride-bi-purple | pride-bi-purple-text | #9b4f96 |
| pride-bi-blue   | pride-bi-blue-text   | #0038a8 |

<br />

### Pansexuality Pride

<a title="This SVG version: KiwiNeko14. Original idea: Tumblr blog PansexualFlag., Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pansexuality_Pride_Flag.svg"><img width="256" alt="Pansexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/Pansexuality_Pride_Flag.svg/256px-Pansexuality_Pride_Flag.svg.png"></a>

| class            | text class            | hex     |
|------------------|-----------------------|---------|
| pride-pan-pink   | pride-pan-pink-text   | #ff218c |
| pride-pan-yellow | pride-pan-yellow-text | #ffd800 |
| pride-pan-blue   | pride-pan-blue-text   | #21b1ff |

<br />

### Labrys Lesbian

<a title="Thespoondragon, CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Labrys_Lesbian_Flag.svg"><img width="256" alt="Labrys Lesbian Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/Labrys_Lesbian_Flag.svg/256px-Labrys_Lesbian_Flag.svg.png"></a>

| class               | text class               | hex     |
|---------------------|--------------------------|---------|
| pride-labrys-violet | pride-labrys-violet-text | #792491 |
| pride-labrys-black  | pride-labrys-black-text  | #000000 |
| pride-labrys-white  | pride-labrys-white-text  | #ffffff |

<br />

### Lipstick Lesbian

<a title="xles (SVG file), CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lipstick_lesbian_Pride_Flag.svg"><img width="256" alt="Lipstick lesbian Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Lipstick_lesbian_Pride_Flag.svg/256px-Lipstick_lesbian_Pride_Flag.svg.png"></a>

| class                     | text class                     | hex     |
|---------------------------|--------------------------------|---------|
| pride-lipstick-dark-pink  | pride-lipstick-dark-pink-text  | #ffffff |
| pride-lipstick-dusty-pink | pride-lipstick-dusty-pink-text | #b75592 |
| pride-lipstick-pink       | pride-lipstick-pink-text       | #d063a6 |
| pride-lipstick-lavender   | pride-lipstick-lavender-text   | #e4accf |
| pride-lipstick-white      | pride-lipstick-white-text      | #ffffff |
| pride-lipstick-pale-red   | pride-lipstick-pale-red-text   | #c54e54 |
| pride-lipstick-brown      | pride-lipstick-brown-text      | #8a1e04 |
| pride-lipstick-red        | pride-lipstick-red-text        | #eb1449 |

<br />

### Orange-pink Lesbian

<a title="SVG file by L ke in Inkscape, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lesbian_pride_flag_2018.svg"><img width="256" alt="Lesbian pride flag 2018" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Lesbian_pride_flag_2018.svg/256px-Lesbian_pride_flag_2018.svg.png"></a>

| class                   | text class                   | hex     |
|-------------------------|------------------------------|---------|
| pride-gwen-dark-orange  | pride-gwen-dark-orange-text  | #d52d00 |
| pride-gwen-orange       | pride-gwen-orange-text       | #ef7627 |
| pride-gwen-light-orange | pride-gwen-light-orange-text | #ff9a56 |
| pride-gwen-white        | pride-gwen-white-text        | #ffffff |
| pride-gwen-pink         | pride-gwen-pink-text         | #d162a4 |
| pride-gwen-dusty-pink   | pride-gwen-dusty-pink-text   | #b55690 |
| pride-gwen-dark-rose    | pride-gwen-dark-rose-text    | #a30262 |

<br />

### Intersex Pride

<a title="Morgan Carpenter (SVG file simplification by AnonMoos), CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Intersex_Pride_Flag.svg"><img width="256" alt="Intersex Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Intersex_Pride_Flag.svg/256px-Intersex_Pride_Flag.svg.png"></a>

| class                 | text class                 | hex     |
|-----------------------|----------------------------|---------|
| pride-intersex-yellow | pride-intersex-yellow-text | #ffd800 |
| pride-intersex-violet | pride-intersex-violet-text | #7902aa |

<br />

### Asexual Pride

<a title="AnonMoos (SVG file); AVEN (flag design), Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Asexual_Pride_Flag.svg"><img width="256" alt="Asexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Asexual_Pride_Flag.svg/256px-Asexual_Pride_Flag.svg.png"></a>

| class            | text class            | hex     |
|------------------|-----------------------|---------|
| pride-ace-black  | pride-ace-black-text  | #000000 |
| pride-ace-grey   | pride-ace-grey-text   | #a3a3a3 |
| pride-ace-white  | pride-ace-white-text  | #ffffff |
| pride-ace-purple | pride-ace-purple-text | #800080 |

<br />

### Aromantic Pride

<a title="Cameron Whimsey, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Aromantic_Pride_Flag.svg"><img width="256" alt="Aromantic Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/Aromantic_Pride_Flag.svg/256px-Aromantic_Pride_Flag.svg.png"></a>

| class                 | text class                 | hex     |
|-----------------------|----------------------------|---------|
| pride-aro-green       | pride-aro-green-text       | #3da542 |
| pride-aro-light-green | pride-aro-light-green-text | #a7d379 |
| pride-aro-white       | pride-aro-white-text       | #ffffff |
| pride-aro-grey        | pride-aro-grey-text        | #a9a9a9 |
| pride-aro-black       | pride-aro-black-text       | #000000 |

<br />

### Genderfluidity Pride

<a title="JJ Pole.McLennonSonGarethPW, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderfluidity_Pride-Flag.svg"><img width="256" alt="Genderfluidity Pride-Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b8/Genderfluidity_Pride-Flag.svg/256px-Genderfluidity_Pride-Flag.svg.png"></a>

| class                    | text class                    | hex     |
|--------------------------|-------------------------------|---------|
| pride-genderfluid-pink   | pride-genderfluid-pink-text   | #ff76a4 |
| pride-genderfluid-white  | pride-genderfluid-white-text  | #ffffff |
| pride-genderfluid-purple | pride-genderfluid-purple-text | #c011d7 |
| pride-genderfluid-black  | pride-genderfluid-black-text  | #000000 |
| pride-genderfluid-blue   | pride-genderfluid-blue-text   | #2f3cbe |

<br />

### Polysexuality Pride

<a title="McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Polysexuality_Pride_Flag.svg"><img width="256" alt="Polysexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Polysexuality_Pride_Flag.svg/256px-Polysexuality_Pride_Flag.svg.png"></a>

| class                  | text class                  | hex     |
|------------------------|-----------------------------|---------|
| pride-polysexual-pink  | pride-polysexual-pink-text  | #f714ba |
| pride-polysexual-green | pride-polysexual-green-text | #01d66a |
| pride-polysexual-blue  | pride-polysexual-blue-text  | #1594f6 |

<br />

### Genderqueer Pride

<a title="Marilyn Roxie, McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderqueer_Pride_Flag.svg"><img width="256" alt="Genderqueer Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1f/Genderqueer_Pride_Flag.svg/256px-Genderqueer_Pride_Flag.svg.png"></a>

| class                      | text class                      | hex     |
|----------------------------|---------------------------------|---------|
| pride-genderqueer-lavender | pride-genderqueer-lavender-text | #b57edc |
| pride-genderqueer-white    | pride-genderqueer-white-text    | #ffffff |
| pride-genderqueer-green    | pride-genderqueer-green-text    | #4a8123 |

<br />

### Non-binary Pride

<a title="Kye Rowan, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Nonbinary_flag.svg"><img width="256" alt="Nonbinary flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Nonbinary_flag.svg/256px-Nonbinary_flag.svg.png"></a>

| class                  | text class                  | hex     |
|------------------------|-----------------------------|---------|
| pride-nonbinary-yellow | pride-nonbinary-yellow-text | #fcf434 |
| pride-nonbinary-white  | pride-nonbinary-white-text  | #ffffff |
| pride-nonbinary-purple | pride-nonbinary-purple-text | #9c59d1 |
| pride-nonbinary-black  | pride-nonbinary-black-text  | #2c2c2c |

<br />

## Notes, Acknowledgements, and Sources

The Palette currently contains 15 different flags explicitly. The fact that a particular flag is or is not included in this version of the Palette does not reflect a desire to gatekeep the queer community or to render judgement on who should or should not be included and accepted. It reflects only the fact that I have a finite amount of time in my day and had t ostop somewhere for now. In the future, I aim to expand it to at least all of the flags included on the [Wikipedia Pride Flag page](https://en.wikipedia.org/wiki/Pride_flag).

All flag images in this README are linked from [Wikimedia Commons](https://commons.wikimedia.org).

Colors in the Palette are from <https://www.flagcolorcodes.com/flags/pride> & <https://brandpalettes.com/category/flags/lgbtq-flags/> and may differ slightly from those listed in other sources (including the SVGs on this page).
