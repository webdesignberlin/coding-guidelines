# ZEIT ONLINE CSS and Sass Coding Guidelines

## Definition
```css
.block {
    margin: 0;
}
```

- The above mentioned code example covers one **css rule**.
- `.block` in this case is the **selector**.
- `margin: 0;` is a **declaration**,
- where `margin` is the property
- and `0` is the value.

## Notation
All classes and ids in the html should be written lowercased. Therefor all selectors should be written lowercased. Also all declarations have to be written in lowercase.

## Indentation
We use tabs for indentation.

## Whitespace
Remove trailing whitespace (i.e. tell your text editor to do so automatically). Never mix spaces and tabs for *indentation*.

## Naming convention
The overall used naming convention used on ZON webpages should be following the [BEM][1] naming scheme. BEM in this case stands for `block, element, modifier`, which refers to the the three levels of differentiation this convention uses. If you are not familiar with this naming convention, [read this article][2] now.

### Naming Pattern
The naming convention follows this pattern:
```css
.block {}
.block__element {}
.block--modifier {}
```

- `.block` represents the higher level of an abstraction or component.
- `.block__element` represents a descendent of .block that helps form .block as a whole.
- `.block--modifier` represents a different state or version of .block.

The double underscores and hyphens are used cause block, element or modifier themselves can contain single hyphens or underscores.

### HTML Example
A typical HTML construct following this convention looks like this:
```html
<form class="site-search  site-search--full">
    <input type="text" class="site-search__field">
    <input type="submit" value ="Search" class="site-search__button">
</form>
```

While `.block` and `.block__element` can be assign to elements seperately, `.block--modifier` is always used together with the element it modifies. In this case `site-search  site-search--full`. The modifier css rule may only contain *additional* declarations.

### No IDs
You must not use any `#id` as a selector.

[1]: http://bem.info/ "BEM – Technology for creating web applications"
[2]: http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/ "MindBEMding – getting your head ’round BEM syntax"
