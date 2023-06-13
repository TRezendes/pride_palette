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
| pride-baker-red    | pride-baker-red-text    | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#e40303">#e40303</text></svg> |
| pride-baker-orange | pride-baker-orange-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ff8c00">#ff8c00</text></svg> 
| pride-baker-yellow | pride-baker-yellow-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffed00">#ffed00</text></svg> 
| pride-baker-green  | pride-baker-green-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#008026">#008026</text></svg> 
| pride-baker-blue   | pride-baker-blue-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#004dff">#004dff</text></svg> 
| pride-baker-purple | pride-baker-purple-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#750787">#750787</text></svg>

<br />

### Progress Pride Flag

<a title="Paul2520, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg"><img width="256" alt="LGBTQ+ rainbow flag Quasar &quot;Progress&quot; variant" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg/256px-LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg.png"></a>

| class                     | text class                     | hex     |
|---------------------------|--------------------------------|---------|
| pride-progress-red        | pride-progress-red-text        | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#e40303">#e40303</text></svg> |
| pride-progress-orange     | pride-progress-orange-text     | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ff8c00">#ff8c00</text></svg> |
| pride-progress-yellow     | pride-progress-yellow-text     | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffed00">#ffed00</text></svg> |
| pride-progress-green      | pride-progress-green-text      | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#008026">#008026</text></svg> |
| pride-progress-blue       | pride-progress-blue-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#004dff">#004dff</text></svg> |
| pride-progress-purple     | pride-progress-purple-text     | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#750787">#750787</text></svg> |
| pride-progress-white      | pride-progress-white-text      | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-progress-pink       | pride-progress-pink-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffafc8">#ffafc8</text></svg> |
| pride-progress-light-blue | pride-progress-light-blue-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#74d7ee">#74d7ee</text></svg> |
| pride-progress-brown      | pride-progress-brown-text      | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#613915">#613915</text></svg> |
| pride-progress-black      | pride-progress-black-text      | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#000000">#000000</text></svg> |

<br />

### Transgender Pride

<a title="SVG file Dlloyd based on Monica Helms design, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Transgender_Pride_flag.svg"><img width="256" alt="Transgender Pride flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Transgender_Pride_flag.svg/256px-Transgender_Pride_flag.svg.png"></a>

| class             | text class             | hex     |
|-------------------|------------------------|---------|
| pride-trans-blue  | pride-trans-blue-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#5bcefa">#5bcefa</text></svg> |
| pride-trans-pink  | pride-trans-pink-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#f5a9b8">#f5a9b8</text></svg> |
| pride-trans-white | pride-trans-white-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |

<br />

### Bi Pride

<a title="Michael Page, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Bisexual_Pride_Flag.svg"><img width="256" alt="Bisexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Bisexual_Pride_Flag.svg/256px-Bisexual_Pride_Flag.svg.png"></a>

| class           | text class           | hex     |
|-----------------|----------------------|---------|
| pride-bi-pink   | pride-bi-pink-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#d60270">#d60270</text></svg> |
| pride-bi-purple | pride-bi-purple-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#9b4f96">#9b4f96</text></svg> |
| pride-bi-blue   | pride-bi-blue-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#0038a8">#0038a8</text></svg> |

<br />

### Pansexuality Pride

<a title="This SVG version: KiwiNeko14. Original idea: Tumblr blog PansexualFlag., Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pansexuality_Pride_Flag.svg"><img width="256" alt="Pansexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/Pansexuality_Pride_Flag.svg/256px-Pansexuality_Pride_Flag.svg.png"></a>

| class            | text class            | hex     |
|------------------|-----------------------|---------|
| pride-pan-pink   | pride-pan-pink-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ff218c">#ff218c</text></svg> |
| pride-pan-yellow | pride-pan-yellow-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffd800">#ffd800</text></svg> |
| pride-pan-blue   | pride-pan-blue-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#21b1ff">#21b1ff</text></svg> |

<br />

### Labrys Lesbian

<a title="Thespoondragon, CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Labrys_Lesbian_Flag.svg"><img width="256" alt="Labrys Lesbian Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/Labrys_Lesbian_Flag.svg/256px-Labrys_Lesbian_Flag.svg.png"></a>

| class               | text class               | hex     |
|---------------------|--------------------------|---------|
| pride-labrys-violet | pride-labrys-violet-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#792491">#792491</text></svg> |
| pride-labrys-black  | pride-labrys-black-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#000000">#000000</text></svg> |
| pride-labrys-white  | pride-labrys-white-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |

<br />

### Lipstick Lesbian

<a title="xles (SVG file), CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lipstick_lesbian_Pride_Flag.svg"><img width="256" alt="Lipstick lesbian Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Lipstick_lesbian_Pride_Flag.svg/256px-Lipstick_lesbian_Pride_Flag.svg.png"></a>

| class                     | text class                     | hex     |
|---------------------------|--------------------------------|---------|
| pride-lipstick-dark-pink  | pride-lipstick-dark-pink-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#a40061">#a40061</text></svg> |
| pride-lipstick-dusty-pink | pride-lipstick-dusty-pink-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#b75592">#b75592</text></svg> |
| pride-lipstick-pink       | pride-lipstick-pink-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#d063a6">#d063a6</text></svg> |
| pride-lipstick-lavender   | pride-lipstick-lavender-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#e4accf">#e4accf</text></svg> |
| pride-lipstick-white      | pride-lipstick-white-text      | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-lipstick-pale-red   | pride-lipstick-pale-red-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#c54e54">#c54e54</text></svg> |
| pride-lipstick-brown      | pride-lipstick-brown-text      | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#8a1e04">#8a1e04</text></svg> |
| pride-lipstick-red        | pride-lipstick-red-text        | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#eb1449">#eb1449</text></svg> |

<br />

### Orange-pink Lesbian

<a title="SVG file by L ke in Inkscape, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lesbian_pride_flag_2018.svg"><img width="256" alt="Lesbian pride flag 2018" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Lesbian_pride_flag_2018.svg/256px-Lesbian_pride_flag_2018.svg.png"></a>

| class                   | text class                   | hex     |
|-------------------------|------------------------------|---------|
| pride-gwen-dark-orange  | pride-gwen-dark-orange-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#d52d00">#d52d00</text></svg> |
| pride-gwen-orange       | pride-gwen-orange-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ef7627">#ef7627</text></svg> |
| pride-gwen-light-orange | pride-gwen-light-orange-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ff9a56">#ff9a56</text></svg> |
| pride-gwen-white        | pride-gwen-white-text        | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-gwen-pink         | pride-gwen-pink-text         | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#d162a4">#d162a4</text></svg> |
| pride-gwen-dusty-pink   | pride-gwen-dusty-pink-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#b55690">#b55690</text></svg> |
| pride-gwen-dark-rose    | pride-gwen-dark-rose-text    | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#a30262">#a30262</text></svg> |

<br />

### Intersex Pride

<a title="Morgan Carpenter (SVG file simplification by AnonMoos), CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Intersex_Pride_Flag.svg"><img width="256" alt="Intersex Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Intersex_Pride_Flag.svg/256px-Intersex_Pride_Flag.svg.png"></a>

| class                 | text class                 | hex     |
|-----------------------|----------------------------|---------|
| pride-intersex-yellow | pride-intersex-yellow-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffd800">#ffd800</text></svg> |
| pride-intersex-violet | pride-intersex-violet-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#7902aa">#7902aa</text></svg> |

<br />

### Asexual Pride

<a title="AnonMoos (SVG file); AVEN (flag design), Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Asexual_Pride_Flag.svg"><img width="256" alt="Asexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Asexual_Pride_Flag.svg/256px-Asexual_Pride_Flag.svg.png"></a>

| class            | text class            | hex     |
|------------------|-----------------------|---------|
| pride-ace-black  | pride-ace-black-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#000000">#000000</text></svg> |
| pride-ace-grey   | pride-ace-grey-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#a3a3a3">#a3a3a3</text></svg> |
| pride-ace-white  | pride-ace-white-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-ace-purple | pride-ace-purple-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#800080">#800080</text></svg> |

<br />

### Aromantic Pride

<a title="Cameron Whimsey, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Aromantic_Pride_Flag.svg"><img width="256" alt="Aromantic Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/Aromantic_Pride_Flag.svg/256px-Aromantic_Pride_Flag.svg.png"></a>

| class                 | text class                 | hex     |
|-----------------------|----------------------------|---------|
| pride-aro-green       | pride-aro-green-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#3da542">#3da542</text></svg> |
| pride-aro-light-green | pride-aro-light-green-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#a7d379">#a7d379</text></svg> |
| pride-aro-white       | pride-aro-white-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-aro-grey        | pride-aro-grey-text        | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#a9a9a9">#a9a9a9</text></svg> |
| pride-aro-black       | pride-aro-black-text       | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#000000">#000000</text></svg> |

<br />

### Genderfluidity Pride

<a title="JJ Pole.McLennonSonGarethPW, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderfluidity_Pride-Flag.svg"><img width="256" alt="Genderfluidity Pride-Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b8/Genderfluidity_Pride-Flag.svg/256px-Genderfluidity_Pride-Flag.svg.png"></a>

| class                    | text class                    | hex     |
|--------------------------|-------------------------------|---------|
| pride-genderfluid-pink   | pride-genderfluid-pink-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ff76a4">#ff76a4</text></svg> |
| pride-genderfluid-white  | pride-genderfluid-white-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-genderfluid-purple | pride-genderfluid-purple-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#c011d7">#c011d7</text></svg> |
| pride-genderfluid-black  | pride-genderfluid-black-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#000000">#000000</text></svg> |
| pride-genderfluid-blue   | pride-genderfluid-blue-text   | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#2f3cbe">#2f3cbe</text></svg> |

<br />

### Polysexuality Pride

<a title="McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Polysexuality_Pride_Flag.svg"><img width="256" alt="Polysexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Polysexuality_Pride_Flag.svg/256px-Polysexuality_Pride_Flag.svg.png"></a>

| class                  | text class                  | hex     |
|------------------------|-----------------------------|---------|
| pride-polysexual-pink  | pride-polysexual-pink-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#f714ba">#f714ba</text></svg> |
| pride-polysexual-green | pride-polysexual-green-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#01d66a">#01d66a</text></svg> |
| pride-polysexual-blue  | pride-polysexual-blue-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#1594f6">#1594f6</text></svg> |

<br />

### Genderqueer Pride

<a title="Marilyn Roxie, McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderqueer_Pride_Flag.svg"><img width="256" alt="Genderqueer Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1f/Genderqueer_Pride_Flag.svg/256px-Genderqueer_Pride_Flag.svg.png"></a>

| class                      | text class                      | hex     |
|----------------------------|---------------------------------|---------|
| pride-genderqueer-lavender | pride-genderqueer-lavender-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#b57edc">#b57edc</text></svg> |
| pride-genderqueer-white    | pride-genderqueer-white-text    | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-genderqueer-green    | pride-genderqueer-green-text    | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#4a8123">#4a8123</text></svg> |

<br />

### Non-binary Pride

<a title="Kye Rowan, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Nonbinary_flag.svg"><img width="256" alt="Nonbinary flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Nonbinary_flag.svg/256px-Nonbinary_flag.svg.png"></a>

| class                  | text class                  | hex     |
|------------------------|-----------------------------|---------|
| pride-nonbinary-yellow | pride-nonbinary-yellow-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#fcf434">#fcf434</text></svg> |
| pride-nonbinary-white  | pride-nonbinary-white-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#ffffff">#ffffff</text></svg> |
| pride-nonbinary-purple | pride-nonbinary-purple-text | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#9c59d1">#9c59d1</text></svg> |
| pride-nonbinary-black  | pride-nonbinary-black-text  | <svg xmlns="http://www.w3.org/2000/svg" fill="none" width="80px" height="1.5rem" font-size="1.3rem"><text x="0" y="20" fill="#2c2c2c">#2c2c2c</text></svg> |

<br />

## Notes, Acknowledgements, and Sources

The Palette currently contains 15 different flags explicitly. The fact that a particular flag is or is not included in this version of the Palette does not reflect a desire to gatekeep the queer community or to render judgement on who should or should not be included and accepted. It reflects only the fact that I have a finite amount of time in my day and had t ostop somewhere for now. In the future, I aim to expand it to at least all of the flags included on the [Wikipedia Pride Flag page](https://en.wikipedia.org/wiki/Pride_flag).

All flag images in this README are linked from [Wikimedia Commons](https://commons.wikimedia.org).

Colors in the Palette are from <https://www.flagcolorcodes.com/flags/pride> & <https://brandpalettes.com/category/flags/lgbtq-flags/> and may differ slightly from those listed in other sources (including the SVGs on this page).
