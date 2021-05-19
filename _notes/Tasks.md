---
title: Tasks
season: summer
tags: TODOs
toc: true
comments: false
---

1. Can now link headers : [[note#header\\|title]], `[[note#header\\|title]]` which is done natively in Obsidian. 
2. Header links that appear on hover. 

## Task List
- [x] Cosmetic changes 
- [x] Alt-text wikilinks (with transclusion!) 
- [x] Meta content in [\_layouts/post.html](_layouts/post.html):
    ```html
    <meta content="My linked notebook" property="og:site_name"/>
    ```
- [x] Copyright in [\_includes/footer.html](_includes/footer.html):
   ```html
   <p id="copyright-notice">Licence MIT</p>
   ```
- [ ] Remove the "seasons" feature for the notes
	- Delete what's inside [\_includes/feed.html](_includes/feed.html) and replace it with:

```liquid
{%- if page.permalink == "/" -%}
    {%- for item in site.notes -%}
        <div class="feed-title-excerpt-block disable-select" data-url="{{site.url}}{{item.url}}">
            <a href="{{ item.url }}" style="text-decoration: none; color: #555555;">
            {%- if item.status == "Ongoing" or item.status == "ongoing" -%}
                <ul style="padding-left: 20px; margin-top: 20px;" class="tags">
                    <li style="padding: 0 5px; border-radius: 10px;" class="tag"><b>Status: </b>{{item.status | capitalize }}</li>
                </ul>
                <p style="margin-top: 0px;" class="feed-title">{{ item.title }}</p>
            {%- else -%}
                <p class="feed-title">{{ item.title }}</p>
            {%- endif -%}
                <p class="feed-excerpt">{{ item.content | strip_html | strip | escape | truncate: 200}}</p>
            </a>
        </div>
    {%- endfor -%}
{%- endif -%}
````

On command-line, you can run `bundle exec jekyll serve` then go to `localhost:4000` to check the result.

## Tutorial of kramdown

### Seasons

Since this jekyll theme aims at mirroring your Obsidian notebook, the note content may note be mature or complete yet.

Therefore, we use front matter to classify the notes in the following categories (in order of appearance in the front page feed) : 

- `season: summer` : the note is near-complete (more than 80% done)
- `season: spring` : the note is in progress and has already good content
- `season: winter` : the note has just started, a summary is present however.
- `season: automn` : the note needs refactoring or some rewriting. It won't appear in the front-page feed.

### Table of Contents

Add `toc: true`

### font-type, font-size, and font-weight

There are classes like *very-small, medium-small, small, small-medium, medium, medium-large, large, very-large*; 

##### Raw Syntax

> {:.regular-sans}
> ```
> {:.large}
> Some text here that needs to be enlarged
> ```
##### Rendered Text
 
`{:.large}`

Some text here that needs to be enlarged


#### Fonts

Similarly there are classes like regular-sans, serif, bold, italic, oblique, bolder, etc for formatting the text.

> **Raw Syntax:**
> 
> ```
> {:.medium .serif .oblique}
> Some text here that needs to be enlarged
> ```
>
> **Rendered Text:**
> 
> {:.medium .serif .oblique}
> Some text here that needs to be enlarged

##### Others

- Other common classes are `.boxit` that is used to wrap the text,
- `.disable-user-select` to disallow users from being able to select a particular piece of text by selecting it, etc.
-  There are more classes like these which you can see in the file `style.css`. Once you figure out which class to use, all you have to do is just add the class before the text you want inside a curl brace like this 


`​{:\<classnames-with-dot-prepended-to-them>​}`

### Highlighting a piece of text

**<u>General Syntax</u>**

- **[​[**​Some Link**::highlight]]**

There is only one color right now in which it highlights, a light bluish color, but you can easily extend it to support multiple colors by tinkering with it in `content.html` file in `_includes` directory.

**Examples**

> **Raw Syntax:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. **[​[**Phasellus mollis lectus id efficitur mollis.**::highlight]]** Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
>
> **Rendered Text:** Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec rutrum tortor in pharetra vehicula. Fusce gravida lacus ac sem luctus congue at id justo. Ut sed tempus ante. [[Phasellus mollis lectus id efficitur mollis.::highlight]] Suspendisse sit amet diam nec justo rhoncus tristique. Ut blandit faucibus nisi vitae rutrum. Vivamus fermentum efficitur justo non facilisis.
