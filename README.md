<head>
<link rel="stylesheet" href="pride-palette.css">
<style>
    .column {
        float: left;
        width: 50%;
    }
    .row:after {
        content: "";
        display: table;
        clear: both;
    }
</style>
</head>

# Pride Palette

This CSS file collects the colors of 15 different pride flags in an easy to use, easy to remember color library for use in any html project.

It started as a component of my [IsMightier](https://wwww.IsMightier.org) project. I spun it off into its own repo so that it would be easy for anyone to download and use on its own.


## Class Naming Conventions

The various color classes are named by color and grouped by flag. The groups are identified by the name of the group the flag represents except in cases where there are multiple flag sfor one group. In those cases, eiher a more specific flag name or the name of the flag's creator is used as an identifier (see the Lesbian Pride flags for an example).

## Colors

Every color in the file has two classes associate with it. The first class sets the color as a background with either white or black as the text color, and the second class sets the color as the text color.

Some colors are represented multiple times in the file. <span class="pride-progress-white-text">White</span>, for instance, appears on many pride flags and is include din each group where it does. For the most part, if one flag uses a subset of colors from another flag, only the flag with the greater number of colors is included as a named group (for example, the pink Lesbian Pride flag uses the same stripe pattern as the Lipstick Lesbian Pride flag, merely ommitting the "kiss" image, so it is not included separately). The main exception is the traditional rainbow Pride flag and the Progress Pride flag. Both are included as named groups.

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

<div class="row">
    <div class="column">
        class = <span class="pride-baker-red">pride-baker-red</span>
    </div>
    <div class="column">
        class = <span class="pride-baker-red-text">pride-baker-red-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-baker-orange">pride-baker-orange</span>
    </div>
    <div class="column">
        class = <span class="pride-baker-orange-text">pride-baker-orange-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-baker-yellow">pride-baker-yellow</span>
    </div>
    <div class="column">
        class = <span class="pride-baker-yellow-text">pride-baker-red-yellow</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-baker-green">pride-baker-green</span>
    </div>
    <div class="column">
        class = <span class="pride-baker-green-text">pride-baker-green-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-baker-blue">pride-baker-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-baker-blue-text">pride-baker-blue-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-baker-purple">pride-baker-purple</span>
    </div>
    <div class="column">
        class = <span class="pride-baker-purple-text">pride-baker-purple-text</span>
    </div>
</div>

<br />

### Progress Pride Flag

<a title="Paul2520, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg"><img width="256" alt="LGBTQ+ rainbow flag Quasar &quot;Progress&quot; variant" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg/256px-LGBTQ%2B_rainbow_flag_Quasar_%22Progress%22_variant.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-progress-red">pride-progress-red</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-red-text">pride-progress-red-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-orange">pride-progress-orange</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-orange-text">pride-progress-orange-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-yellow">pride-progress-yellow</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-yellow-text">pride-progress-red-yellow</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-green">pride-progress-green</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-green-text">pride-progress-green-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-blue">pride-progress-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-blue-text">pride-progress-blue-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-purple">pride-progress-purple</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-purple-text">pride-progress-purple-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-white">pride-progress-white</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-white-text">pride-progress-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-pink">pride-progress-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-pink-text">pride-progress-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-light-blue">pride-progress-light-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-light-blue-text">pride-progress-light-blue-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-brown">pride-progress-brown</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-brown-text">pride-progress-brown-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-progress-black">pride-progress-black</span>
    </div>
    <div class="column">
        class = <span class="pride-progress-black-text">pride-progress-black-text</span>
    </div>
</div>

<br />

### Transgender Pride

<a title="SVG file Dlloyd based on Monica Helms design, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Transgender_Pride_flag.svg"><img width="256" alt="Transgender Pride flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Transgender_Pride_flag.svg/256px-Transgender_Pride_flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-trans-blue">pride-trans-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-trans-blue-text">pride-trans-blue-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-trans-pink">pridetrans-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-trans-pink-text">pride-trans-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-trans-white">pride-trans-white</span>
    </div>
    <div class="column">
        class = <span class="pride-trans-white-text">pride-trans-white-text</span>
    </div>
</div>

<br />

### Bi Pride

<a title="Michael Page, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Bisexual_Pride_Flag.svg"><img width="256" alt="Bisexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Bisexual_Pride_Flag.svg/256px-Bisexual_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-bi-pink">pride-bi-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-bi-pink-text">pride-bi-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-bi-purple">pride-bi-purple</span>
    </div>
    <div class="column">
        class = <span class="pride-bi-purple-text">pride-bi-purple-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-bi-blue">pride-bi-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-bi-blue-text">pride-bi-blue-text</span>
    </div>
</div>

<br />

### Pansexuality Pride

<a title="This SVG version: KiwiNeko14. Original idea: Tumblr blog PansexualFlag., Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Pansexuality_Pride_Flag.svg"><img width="256" alt="Pansexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/Pansexuality_Pride_Flag.svg/256px-Pansexuality_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-pan-pink">pride-pan-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-pan-pink-text">pride-pan-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-pan-yellow">pride-pan-yellow</span>
    </div>
    <div class="column">
        class = <span class="pride-pan-yellow-text">pride-pan-yellow-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-pan-blue">pride-pan-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-pan-blue-text">pride-pan-blue-text</span>
    </div>
</div>

<br />

### Labrys Lesbian

<a title="Thespoondragon, CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Labrys_Lesbian_Flag.svg"><img width="256" alt="Labrys Lesbian Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/Labrys_Lesbian_Flag.svg/256px-Labrys_Lesbian_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-labrys-violet">pride-labrys-violet</span>
    </div>
    <div class="column">
        class = <span class="pride-labrys-violet-text">pride-labrys-violet-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-labrys-black">pride-labrys-black</span>
    </div>
    <div class="column">
        class = <span class="pride-labrys-black-text">pride-labrys-black-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-labrys-white">pride-labrys-white</span>
    </div>
    <div class="column">
        class = <span class="pride-labrys-white-text">pride-labrys-white-text</span>
    </div>
</div>

<br />

### Lipstick Lesbian

<a title="xles (SVG file), CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lipstick_lesbian_Pride_Flag.svg"><img width="256" alt="Lipstick lesbian Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/06/Lipstick_lesbian_Pride_Flag.svg/256px-Lipstick_lesbian_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-dark-pink">pride-lipstick-dark-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-dark-pink-text">pride-lipstick-dark-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-dusty-pink">pride-lipstick-dusty-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-dusty-pink-text">pride-lipstick-dusty-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-pink">pride-lipstick-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-pink-text">pride-lipstick-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-lavender">pride-lipstick-lavender</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-lavender-text">pride-lipstick-lavender-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-white">pride-lipstick-white</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-white-text">pride-lipstick-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-pale-red">pride-lipstick-pale-red</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-pale-red-text">pride-lipstick-pale-red-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-brown">pride-lipstick-brown</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-brown-text">pride-lipstick-brown-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-lipstick-red">pride-lipstick-red</span>
    </div>
    <div class="column">
        class = <span class="pride-lipstick-red-text">pride-lipstick-red-text</span>
    </div>
</div>

<br />

### Orange-pink Lesbian

<a title="SVG file by L ke in Inkscape, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Lesbian_pride_flag_2018.svg"><img width="256" alt="Lesbian pride flag 2018" src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Lesbian_pride_flag_2018.svg/256px-Lesbian_pride_flag_2018.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-gwen-dark-orange">pride-gwen-dark-orange</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-dark-orange-text">pride-gwen-dark-orange-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-gwen-orange">pride-gwen-orange</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-orange-text">pride-gwen-orange-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-gwen-light-orange">pride-gwen-light-orange</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-light-orange-text">pride-gwen-light-orange-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-gwen-white">pride-gwen-white</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-white-text">pride-gwen-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-gwen-pink">pride-gwen-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-pink-text">pride-gwen-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-gwen-dusty-pink">pride-gwen-dusty-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-dusty-pink-text">pride-gwen-dusty-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-gwen-dark-rose">pride-gwen-dark-rose</span>
    </div>
    <div class="column">
        class = <span class="pride-gwen-dark-rose-text">pride-gwen-dark-rose-text</span>
    </div>
</div>

<br />

### Intersex Pride

<a title="Morgan Carpenter (SVG file simplification by AnonMoos), CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Intersex_Pride_Flag.svg"><img width="256" alt="Intersex Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Intersex_Pride_Flag.svg/256px-Intersex_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-intersex-yellow">pride-intersex-yellow</span>
    </div>
    <div class="column">
        class = <span class="pride-intersex-yellow-text">pride-intersex-yellow-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-intersex-violet">pride-intersex-violet</span>
    </div>
    <div class="column">
        class = <span class="pride-intersex-violet-text">pride-intersex-violet-text</span>
    </div>
</div>

<br />

### Asexual Pride

<a title="AnonMoos (SVG file); AVEN (flag design), Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Asexual_Pride_Flag.svg"><img width="256" alt="Asexual Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Asexual_Pride_Flag.svg/256px-Asexual_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-ace-black">pride-ace-black</span>
    </div>
    <div class="column">
        class = <span class="pride-ace-black-text">pride-ace-black-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-ace-grey">pride-ace-grey</span>
    </div>
    <div class="column">
        class = <span class="pride-ace-grey-text">pride-ace-grey-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-ace-white">pride-ace-white</span>
    </div>
    <div class="column">
        class = <span class="pride-ace-white-text">pride-ace-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-ace-purple">pride-ace-purple</span>
    </div>
    <div class="column">
        class = <span class="pride-ace-purple-text">pride-ace-purple-text</span>
    </div>
</div>

<br />

### Aromantic Pride

<a title="Cameron Whimsey, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Aromantic_Pride_Flag.svg"><img width="256" alt="Aromantic Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/Aromantic_Pride_Flag.svg/256px-Aromantic_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-aro-green">pride-aro-green</span>
    </div>
    <div class="column">
        class = <span class="pride-aro-green-text">pride-aro-green-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-aro-light-green">pride-aro-light-green</span>
    </div>
    <div class="column">
        class = <span class="pride-aro-light-green-text">pride-aro-light-green-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-aro-white">pride-aro-white</span>
    </div>
    <div class="column">
        class = <span class="pride-aro-white-text">pride-aro-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-aro-grey">pride-aro-grey</span>
    </div>
    <div class="column">
        class = <span class="pride-aro-grey-text">pride-aro-grey-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-aro-black">pride-aro-black</span>
    </div>
    <div class="column">
        class = <span class="pride-aro-black-text">pride-aro-black-text</span>
    </div>
</div>

<br />

### Genderfluidity Pride

<a title="JJ Pole.McLennonSonGarethPW, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderfluidity_Pride-Flag.svg"><img width="256" alt="Genderfluidity Pride-Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b8/Genderfluidity_Pride-Flag.svg/256px-Genderfluidity_Pride-Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-genderfluid-pink">pride-genderfluid-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-genderfluid-pink-text">pride-genderfluid-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-genderfluid-white">pride-genderfluid-white</span>
    </div>
    <div class="column">
        class = <span class="pride-genderfluid-white-text">pride-genderfluid-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-genderfluid-purple">pride-genderfluid-purple</span>
    </div>
    <div class="column">
        class = <span class="pride-genderfluid-purple-text">pride-genderfluid-purple-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-genderfluid-black">pride-genderfluid-black</span>
    </div>
    <div class="column">
        class = <span class="pride-genderfluid-black-text">pride-genderfluid-black-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-genderfluid-blue">pride-genderfluid-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-genderfluid-blue-text">pride-genderfluid-blue-text</span>
    </div>
</div>

<br />

### Polysexuality Pride

<a title="McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Polysexuality_Pride_Flag.svg"><img width="256" alt="Polysexuality Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Polysexuality_Pride_Flag.svg/256px-Polysexuality_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-polysexual-pink">pride-polysexual-pink</span>
    </div>
    <div class="column">
        class = <span class="pride-polysexual-pink-text">pride-polysexual-pink-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-polysexual-green">pride-polysexual-green</span>
    </div>
    <div class="column">
        class = <span class="pride-polysexual-green-text">pride-polysexual-green-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-polysexual-blue">pride-polysexual-blue</span>
    </div>
    <div class="column">
        class = <span class="pride-polysexual-blue-text">pride-polysexual-blue-text</span>
    </div>
</div>

<br />

### Genderqueer Pride

<a title="Marilyn Roxie, McLennonSon, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Genderqueer_Pride_Flag.svg"><img width="256" alt="Genderqueer Pride Flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1f/Genderqueer_Pride_Flag.svg/256px-Genderqueer_Pride_Flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-genderqueer-lavender">pride-genderqueer-lavender</span>
    </div>
    <div class="column">
        class = <span class="pride-genderqueer-lavender-text">pride-genderqueer-lavender-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-genderqueer-white">pride-genderqueer-white</span>
    </div>
    <div class="column">
        class = <span class="pride-genderqueer-white-text">pride-genderqueer-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-genderqueer-green">pride-genderqueer-green</span>
    </div>
    <div class="column">
        class = <span class="pride-genderqueer-green-text">pride-genderqueer-green-text</span>
    </div>
</div>

<br />

### Non-binary Pride

<a title="Kye Rowan, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Nonbinary_flag.svg"><img width="256" alt="Nonbinary flag" src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Nonbinary_flag.svg/256px-Nonbinary_flag.svg.png"></a>

<div class="row">
    <div class="column">
        class = <span class="pride-nonbinary-yellow">pride-nonbinary-yellow</span>
    </div>
    <div class="column">
        class = <span class="pride-nonbinary-yellow-text">pride-nonbinary-yellow-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-nonbinary-white">pride-nonbinary-white</span>
    </div>
    <div class="column">
        class = <span class="pride-nonbinary-white-text">pride-nonbinary-white-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-nonbinary-purple">pride-nonbinary-purple</span>
    </div>
    <div class="column">
        class = <span class="pride-nonbinary-purple-text">pride-nonbinary-purple-text</span>
    </div>
</div>
<div class="row">
    <div class="column">
        class = <span class="pride-nonbinary-black">pride-nonbinary-black</span>
    </div>
    <div class="column">
        class = <span class="pride-nonbinary-black-text">pride-nonbinary-black-text</span>
    </div>
</div>

<br />

## Notes, Acknowledgements, and Sources

The Palette currently contains 15 different flags explicitly. The fact that a particular flag is or is not included in this version of the Palette does not reflect a desire to gatekeep the queer community or to render judgement on who should or should not be included and accepted. It reflects only the fact that I have a finite amount of time in my day and had t ostop somewhere for now. In the future, I aim to expand it to at least all of the flags included on the [Wikipedia Pride Flag page](https://en.wikipedia.org/wiki/Pride_flag).

All flag images in this README are linked from [Wikimedia Commons](https://commons.wikimedia.org).

Colors in the Palette are from <https://www.flagcolorcodes.com/flags/pride> & <https://brandpalettes.com/category/flags/lgbtq-flags/> and may differ slightly from those listed in other sources (including the SVGs on this page).
