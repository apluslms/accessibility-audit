+++
title = "Page Titles"
tags = ["low", "wcag-a"]
+++

## Requirements

The requirements relating to the page titles are being met. All tested pages have descriptive, discernable names, with the most specific information first and the website name last.

{{% wcag include="2.4.1" descriptions="false" %}}

## Possible Improvements

Through testing, it became clear that the use of the `|` (pipe) character as a divider is annoying when using VoiceOver. Page titles are spoken as:

> Results vertical line programming 2 vertical line a plus

The words "vertical line" take approximately as much speech time than the relevant content. 

Replacing this with a `-` (hyphen) results in a short pause and no description, which may be preferable. That said, this is "low" priority, as many websites use the `|` character and screen reader users are generally used to this convention.
