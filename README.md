# Variable Icons

*Icons empowered by the capabilities of **typography** and **OpenType** features*

---

## Overview
The future of icon packs will be very exciting and fascinating with the advanced capabilities of OpenType, allowing the creation of icons with various styles within a single file, along with advanced typographical features. These features help us create remarkable and fully customizable icon packs.

## What we are going to *achieve*

We aim to create diverse icon packs by leveraging the capabilities of OpenType and Variable fonts. This involves developing a singular icon font that allows control over various axes of icon shapes. For instance, users can modify the icon weight or utilize OpenType features to store alternate versions of each icon within a single file.

## Why Variable icons

- single font file containing over `65,000` Glyphs (icons)
- Create any custom style like (caps, rotate, flip,...)
- create 999 axes of styles within a single file
- modify and control styles using `font-variation-settings` and `font-feature-settings`

## What possibilities are available with variable icons?


With technologies like variable fonts or OpenType, we can create diverse styles and features for icons. Here, we explore some of them together to understand what variable icons are and how appealing they can be for a project.

### adjust icon thickness using font-weight

![icon-weight](https://github.com/illustrayking/variable-icons/assets/25862601/8c60f086-9c47-4e0b-9441-3595836ecddb)

We can design an icon pack similar to a typeface with various weights, and manage the icon thickness by utilizing the CSS property "font-weight."

<div dir="ltr">

```css
.icon {
    font-family: 'myIcon';
    font-weight: 400; /*using css standard property*/
    font-variation-settings: 'wght' 400; /*or using css low level property*/
}
```
</div>

## Rotate the icon

![rotate](https://github.com/illustrayking/variable-icons/assets/25862601/a417f523-22be-4a8d-81d6-ed27efe6b23e)

We can also generate a unique style by employing rotation to orient the glyph at the desired angle.

in this case i can rotate an *arrow icon* to create different style of arrow without having another codepoint just for rotation

<div dir="ltr">

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'RTAT' 45; /*show my glyph in 45 degree*/
    font-variation-settings: 'RTAT' 180; /*show my glyph in 180 degree*/
}
```
</div>

## Caps the icon

![caps](https://github.com/illustrayking/variable-icons/assets/25862601/56a56518-b3c7-47ab-9c89-22b86dba8687)

We can establish a boolean style to determine whether an icon's endpoint should be rectangular or rounded.

<div dir="ltr">

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'CAPS' 0; /*rect end-point*/
    font-variation-settings: 'CAPS' 1; /*round end-point*/
}
```
</div>

## Flip the icon

if we can flip the icon horizontaly or vertically only with style variation

<div dir="ltr">

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'HFLP' 0; /*don't flip my icon horizontally*/
    font-variation-settings: 'HFLP' 1; /*flip my icon horizontally*/
}
```
</div>

As shown in the image below, we horizontally flip the icon to position the Chimney on the left side of the home icon, reflecting the desired orientation.

![flip](https://github.com/illustrayking/variable-icons/assets/25862601/723eba3c-a49e-44f6-b289-7c9047753efd)

or even flip vertically

<div dir="ltr">

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'VFLP' 0; /*don't flip my icon vertically*/
    font-variation-settings: 'VFLP' 1; /*flip my icon vertically*/
}
```
</div>

![flip-vertically](https://github.com/illustrayking/variable-icons/assets/25862601/45279239-d8a8-4363-b27b-53754cc5cef1)

## using stylistics sets to store alternatives

In OpenType fonts, activating alternative glyphs through stylistic sets is feasible. This feature can be utilized to store different versions of icons as well.

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'wght' 400, 'CAPS' 1;
    font-feature-settings: 'ss01' 1; /*show the next version of my glyphs*/
}
```

In this case, activating stylistic sets in OpenType fonts transforms all icons into an alternate version.

like image below

![ss01](https://github.com/illustrayking/variable-icons/assets/25862601/ba9d9c3a-e572-42e3-9406-88273af8266d)

With 20 stylistic sets for my icons, it implies that if an icon has more than 2 different versions, we can store them using additional sets labeled as ssXX.

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'wght' 400, 'CAPS' 1;
    font-feature-settings: 'ss03' 1; /*enable third version of my icons*/
}
```
![other-ss](https://github.com/illustrayking/variable-icons/assets/25862601/ccac0b0d-2dbb-4a54-af3f-b6c0b8643ea5)

## multiple color fonts
Color fonts (also known as chromatic fonts) can use multiple colors in a single glyph

with ability of opentype we can also have icons with multiple colors

![colorful-icons](https://github.com/illustrayking/variable-icons/assets/25862601/461eedb5-3627-4162-beec-e036f1132c74)

we can even change the color or set the default color scheme for my entire icons using CSS

```css
@font-palette-values --dragon {
    font-family: 'myIcon';
    base-palette: 3; /*choose the third color scheme as a default for dragon identifier*/
}
@font-palette-values --alpha {
    font-family: 'myIcon';
    override-colors:
      0 #003F55;
      1 #7FD6FF;
}

.icon {
    font-family: 'myIcon';
    font-palette: --alpha;
}
```

## conclusion

With OpenType capabilities and CSS, we can create versatile font icon packs with numerous styles and features, all within a single file.