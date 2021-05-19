---
title: Tutorial
season: summer
tags: Theme
toc: true
comments: true
---

## Test Run


Internal links (simple and with alt-text) and LateX delimiters in markdown are compatible with [[Obsidian::https://obsidian.md]].


## The Custom features

### 1. Creating a wiki-style link

**<u>Underlining</u>**

- **Internal links:** **[​[**​Some Link**]]**

- **Internal links with alternative text:** **[​[**​Some Link\\|Alt text**]]**

- **External links:** **[​[​**Some Text::https://address-to-the-website**]]**


==Similarly, for external links all you have to do is add a double colon after the "Alt text" and enter the link to the website after the double colon as seen below.==


### 2. Creating a sidenote or a marginnote

- **Sidenote:** **[​[**Some Text**::keyword-of-the-type-of-the-sidenote]]**

- **Marginnote:** **[​[​**Some Text**::keyword-of-the-type-of-the-marginnote]]**

> |Type of the sidenote/marginnote|keyword|
  |:--|:--|
  |Left Sidenote| `lsn` |
  |Right Sidenote | `rsn` |
  |Left Marginnote| `lmn` |
  |Right Marginnote | `rmn` |


So, all you have to do is type in the keywords of the corresponding type of sidenote or marginnote after the double colon in the above syntax

**Examples**

Example of a sidenote to the right side of the page: 

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. **[​[**Phasellus mollis lectus id efficitur mollis.**::rsn]]** Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. [[Phasellus mollis lectus id efficitur mollis.::rsn]] Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.

Same goes with `lsn`, `rmn`, `lmn`


### 4. Partial Transclusion

Transclusion is just a natural extension of sidenote and marginnote feature.

**<u>General Syntax</u>**

- **Sidenote-transclusion:** **[​[**Some Text**::keyword-of-the-type-of-the-sidenote-transclusion]]**

- **Marginnote-transclusion:** **[​[​**Some Text**::keyword-of-the-type-of-the-marginnote-transclusion]]**

> |Type of the sidenote/marginnote transclusion|keyword|
  |:--|:--|
  |Left Sidenote Transclusion | `lsn-transclude` |
  |Right Sidenote Transclusion | `rsn-transclude` |
  |Left Marginnote Transclusion | `lmn-transclude` |
  |Right Marginnote Transclusion | `rmn-transclude` |


So, all you have to do is type in the keywords of the corresponding type of sidenote or marginnote after the double colon in the above syntax

**Examples**

Example of a transclusion to the right side of the page: 

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. **[​[**Obsidian integration**::rmn-transclude]]** Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. [[Obsidian integration::rmn-transclude]] Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.

Same goes with `rsn`, `lsn`, `lmn`

### 5. Wrapping a text inside a box

**<u>General Syntax</u>**

- **[​[**Some Text**::wrap]]**

**Examples**

> **Raw Syntax:** **[​[**Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis**::wrap]]**.
>
> **Rendered Text:** [[Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.::wrap]]

### 6. Flashcard

**<u>General Syntax</u>**

- **[​[**Some Text**::srs]]**

**Examples**

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. **[​[**Donec rutrum tortor in pharetra vehicula**::srs]]**. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. [[Donec rutrum tortor in pharetra vehicula::srs]]. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.




