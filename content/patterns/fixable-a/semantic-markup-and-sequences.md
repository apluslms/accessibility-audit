+++
title = "Semantic Markup and Sequences"
tags = ["high", "wcag-a"]
+++

## Semantic markup

When users of screen readers navigate pages, some may rely on the structure of the document to move around. This may mean taking an "outline", made up of the nested headings, or using landmarks, such as `nav` and `main` to jump around the web page.

Luckily, these often don't need defining explicitly, as many native HTML5 elements have an implied role. In some places, these could be easily swapped into the layout. For example, `<div class="section">` could be easily substituted for `<section>`. to be made by using HTML5 elements in place of some classes. 

This would improve compliance with the following success criteria:

{{% wcag include="1.1.1, 1.3.1" descriptions="false" %}}

## Sequences

Since users may replace some of the styles offered by the page, or may move through the page using the keyboard or a screen reader, it's iportant that the page makes sense if some style information is missing.

Ensuring that the items appear in the DOM in a logical order  will help accomplish this, as defined in:

{{% wcag include="1.3.2" descriptions="false" %}}

## Examples and solutions

This list is likely not exhaustive:

### Course archive

The **course archive** uses `h3` tags to represent courses. These are wrapped in `li`s. 

First, there is no `h2`, so they're nested directly under the page's `h1`. 

Also, they don't behave like headings, it doesn't make sense to encourage users to jump to them within the page as they would subheadings in a document, since there is no further content to explore, only the link to follow.

The formatting could be maintained without using a heading tag, and since the courses are sorted chronologically, subheadings could be used to, for example, group the courses by year. 

### Profile

The sequence of elements in the profile page does not match reading order. Looking at the page visually, the user might follow from the avatar, to the blue "info" block on the right which explains how to change it. 

Following the DOM order, as a screen reader would, the user first passes the avatar, before continuing through the next fields, and then returns to the block explaining how to change their avatar.

