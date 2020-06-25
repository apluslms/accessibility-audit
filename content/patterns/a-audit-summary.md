+++
title = "WCAG-A Summary"
+++

## Perceivable
### Text Alternatives

{{% wcag include="1.1.1" descriptions="true" %}}

Some inappropriately described images are present, for example on the front page and profile page.

Some form fields are not described, including at log in and submitting exercises.

### Time-based Media

{{% wcag include="1.2.1, 1.2.2, 1.2.3" descriptions="true" %}}

No time-based media features in the sample checked (nor anywhere in the platform outside of course-specific content). 

### Adaptable

{{% wcag include="1.3.1" descriptions="true" %}}

There are many cases of mislabelled forms, as covered on {{% pattern "Form Controls" %}}, and missed or misordered heading levels, as mentioned in {{% pattern "Semantic Markup and Sequences" %}}

{{% wcag include="1.3.2" descriptions="true" %}}

The DOM order does not match the reading order in the profile page, and may be broken in some exercises.

{{% wcag include="1.3.3" descriptions="true" %}}

No problems with sensory characteristics were found.

### Distinguishable

{{% wcag include="1.4.1" descriptions="true" %}}

No information on the pages checked was conveyed using only colour.

{{% wcag include="1.4.2" descriptions="true" %}}

No audio is used in the platform, and this audit did not consider specific courses. 

## Operable
### Keyboard Accessible

{{% wcag include="2.1.1" descriptions="true" %}}

The modals displayed when submitting an assignment are not easily keyboard or screen reader accessible. 

{{% wcag include="2.1.2" descriptions="true" %}}

There was no keyboard trap found on any of the pages. 

{{% wcag include="2.1.4" descriptions="true" %}}

No character key shortcuts are used.

### Enough Time

{{% wcag include="2.2.1, 2.2.2" descriptions="true" %}}

The only time limit is the session duration, after which the user is logged out. From inspection of the code, this appears to be around two weeks. This passes the requirements, as it is above the 20 hour exception.

### Seizures and Physical Reactions

{{% wcag include="2.3.1" descriptions="true" %}}

Nothing flashing is present on any of the audited pages.

### Navigable

{{% wcag include="2.4.1" descriptions="true" %}}

Skip links are not present, but currently a work in progress.

{{% wcag include="2.4.2" descriptions="true" %}}

Page titles are present and descriptive. {{% pattern "Page Titles" %}} includes notes on possible improvements.

{{% wcag include="2.4.3" descriptions="true" %}}

The focus order is not always logical. 

{{% wcag include="2.4.4" descriptions="true" %}}

Many pages have inditinguishable link text or non-specific text. For example, the course points page includes the link text "1/5", referring to a submission count, many times. 

## Understandable
### Readable

{{% wcag include="3.1.1" descriptions="true" %}}

The language of the page is stated correctly.

### Predictable

{{% wcag include="3.2.1" descriptions="true" %}}

A focus state is implemented on `master`, but is not yet in production.

### Input Assistance

{{% wcag include="3.3.1" descriptions="true" %}}

{{% wcag include="3.3.2" descriptions="true" %}}

Labels are not always present or visible. It is not possible to always ascertain the label visually or programatically. 

## Robust
### Compatible

{{% wcag include="4.1.1, 4.1.2" descriptions="true" %}}

HTML is generally valid, although some views include repeated IDs. 

Roles of `button` and `link` appear unpredictably and inconsistently. {{% pattern "Links and Buttons" %}} explains more. 
