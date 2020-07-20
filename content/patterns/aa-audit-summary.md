+++
title = "WCAG-AA Summary"
+++

## Perceivable
### Time-based Media

{{% wcag include="1.2.4, 1.2.5" descriptions="true" %}}

The interfaces examined don't use any live media or prerecorded video, so there is nothing to require captions or audio description. 

### Adaptable

{{% wcag include="1.3.4" descriptions="true" %}}

All pages work equally well in either mobile orientation, except the "Results" page, which is inaccessible on certain mobile screen sizes (tested using iPhone Simulator) in portrait (notably, the smartphones available for testing were all bigger than this size).

{{% wcag include="1.3.5" descriptions="true" %}}

No forms have [`autocorrect` attributes](https://www.w3.org/TR/html52/sec-forms.html#sec-autofill). This complies with the requirements except for;

- **Login** - local user login should explicitly identify the `username` and `password` to enable assistive technology to autofill the fields.
- **Profile** - the `language` field may benefit from identification.

Further to this, it may be worth considering adding `autocomplete="off"` to questionnaire forms, where accidental submission consumes available submissions from a limited pool.

### Distinguishable

{{% wcag include="1.4.3" descriptions="true" %}}

There are many elements with too low colour contrast. The footer, which is visible on every page is one of these, as well as many of the badges, buttons and alerts.

Most of these are unstyled Bootstrap components, so it may make sense to re-assess this once there is a new Bootstrap theme in place, to find which need addressing once the theme colours are eliminated.

{{% wcag include="1.4.4" descriptions="true" %}}

Adjusting the text size independently of the page zoom does not work.

{{% wcag include="1.4.5" descriptions="true" %}}

No images of text could be found.

{{% wcag include="1.4.10" descriptions="true" %}}

The responsive design means that reflow works as intended up to 400% (also tested at 500%). The only exception is the table on the course results page, which overflows horizontally.

{{% wcag include="1.4.11" descriptions="true" %}}

Most pages met the "non-text contrast" requirement. The elements that did not were;

- `input` text fields, which have too low a border colour (this can likely be addressed with the Bootstrap theme)
- Classes `.badge` and `.label` do not always have sufficient contrast against their background.


{{% wcag include="1.4.12" descriptions="true" %}}

Adjusting text spacing works corretly (this was tested using the [text spacing bookmarklet](https://codepen.io/stevef/full/YLMqbo)). The only exception was the `<dl>` at the top of course content pages (tested using `course-template`), which caused some horizontal overflow.

This was also tested with the front page from the current `master` branch - note that the previous implementation failed. 

{{% wcag include="1.4.13" descriptions="true" %}}

Very few cases of content (like tooltips) appearing on hover were found in the pages sampled. Those that were found always had an element of reduncancy, although they did not meet these requirements (usually as they were not hoverable).

## Operable

### Navigable

{{% wcag include="2.4.5" descriptions="true" %}}

Generally, if we consider courses to be "subsites", these criteria are basically met. It's possible to navigate course pages either;

- From a "contents" list of chapters and pages
- From a list of point-bearing exercises, grouped by page
- Using "back" and "next" links within the pages.

It's always possible to reach the front page and other key pages, and the menu of the user's own courses provides quick links to the pages the user is most likely to want to access.

Navigation within courses, and jumping from one course to another is provided in at least two ways. 

{{% wcag include="2.4.6" descriptions="true" %}}

Throughout all pages, except "log out" and the front page, there are mismatched heading levels. These can be examined most easily in WAVE, and should create a logical, nexted tree structure. 

## Understandable

### Readable

{{% wcag include="3.1.2" descriptions="true" %}}


The version of the front page on `master` is the only part where the language of parts is correctly identified. The same technique should be applied to the course archive page. Additionally, the language names are present in the profile page.

No other pages use multiple languages which are visible simeltaneously  (some courses do, but specific courses were out of scope for this review).

### Predictable

{{% wcag include="3.2.3" descriptions="true" %}}

The navigation is present in the same location on every page.

The only element which is unpredictable is the menu which allows users to choose a group to submit with, as it is related to the course, but appears in the main navigation area, and may appear differently in different courses. 

{{% wcag include="3.2.4" descriptions="true" %}}

Most elements can be identified consistently. Issues have been identified in the previous audit about the use of {{% pattern "Links and Buttons" %}} . 

An important note here is that teachers are free to override the CSS within courses. This allows individual courses to use inconsistent identification for elements, and is outside of the scope of this audit. It may be worth producing documentation for teachers covering the importance of not overriding some of the default styles, or to consider limiting the effect of teacher styles to only the content area. 

### Input Assistance

{{% wcag include="3.3.3" descriptions="true" %}}

Forms don't always show error messages when fields are missed or in the incorrect format. Those that do may have unclear error messages.

{{% wcag include="3.3.4" descriptions="true" %}}

No pages cause legal or financial consequences, however since submissions are finite and contribute to university grades, they may meet the definition of "testing".

Submissions are not reversible. No mechanism to check values before submission are provided. No confirmation step is used. Any of these would meet the criteria. This has already been discussed earlier in [GitHub issue #508](https://github.com/apluslms/a-plus/issues/508) and [MOOC-grader issue #56](https://github.com/apluslms/mooc-grader/issues/56). 

## Robust

### Compatible

{{% wcag include="4.1.3" descriptions="true" %}}

The majority of sampled pages do not contain "live" status messages.

The status messages shown, when submitting an exercise, are not marked up appropriately or highlighted to assistive technology.
