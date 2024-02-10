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

in this case i can rotate an *arrow icon* to create different style of arrow without having another icon variation just for rotation

<div dir="ltr">

```css
.icon {
    font-family: 'myIcon';
    font-variation-settings: 'RTAT' 45; /*show my glyph in 45 degree*/
    font-variation-settings: 'RTAT' 180; /*show my glyph in 180 degree*/
}
```
</div>
