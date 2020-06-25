+++
title = "Links and Buttons"
tags = ["high", "wcag-a"]
+++

## Requirements

One key requirement is that names, roles and values can be determined programmatically. The roles are most often deduced from HTML elements (so, for example, a `<button>` tag can safely be assumed to be a "button").

{{% wcag include="4.1.2" descriptions="false" %}}

In several places, A+ used buttons and links in a different way to the expectation.

Users typically expect that clicking a link takes the user to another page, and clicking a button performs an action. 

## Examples

### Front Page

{{% note %}}
This is being fixed at the time of writing, but is a good example. 
{{% /note %}}

Each course on the front page contains a block which looks like this:

![Partial screenshot showing the links to one course](../images/course_block.png "One course links")

This contains a link (the title text) and a button. Both behave link links. Since they have different roles, VoiceOver announces one as a link and one as a button. 

Additionally, if a user wants to navigate by headings or form elements, these links will appear in both lists. 

### Course Index

On the course index page, when the recent results are shown, there is something that appears to be a text link, labelled as:

> Show older assignments.

This is marked up as a link, but changes the content of the current page. Users may expect to be taken to a different page, instead the content of this pages with no clear indication. 

If this were labelled as a button, it would give a much clear indication that "clicking this does something". There could also be benefits to users not using assistive technology to acheive a highler level of consistency in how interface elements are used.