+++
title = "Modal Dialogs"
tags = ["critical", "wcag-a"]
+++

The interface makes heavy use of modal dialogs, for example when a user submits an exercise, the grader results appear in a modal window and when a user views a previous submission, it opens in one. Sometimes, links from modals trigger other modals to open. 

Presently, these are not navigable to keyboard users and break the logical focus order. This causes failures in:

{{% wcag include="1.3.2, 2.4.3" descriptions="false" %}}

## Mouse-users' experience

Presently, mouse users can click a link or button (these should likely be buttons, as addressed in #TODO), and the modal fills the page. The rest of the page is "dimmed". Clicking the background closes the modal, and a close button is present. It's not possible to scroll the background page.

## Keyboard-users' experience

It's possible to follow the links that open the modal with the keyboard, however focus does not move to inside the modal. Continuing to navigate around the page using the tab button is possible, and the background page moves underneath the overlay.

The user can enter the modal by tabbing all the way to the end of the page.

Upon exiting the modal, either using ESC or the close button, focus is typically at the top of the page, rather than the point where the user might be expecting it, at the point they left.

## Suggestions

1. Double-check all of these functions are best served by modal dialogs, rather than opening a new page
2. Consider the action that opens the modal. A link may not be the most appropriate option here, as the user isn't being taken to a new page.
3. Record the item the user activates when they open the modal, return focus there when they close it.
4. Ensure keyboard users can only focus on the elements inside the visible modal, and can't interact with the background page while it is open. Take a look at the _proposed_ [`inert` attribute](https://github.com/WICG/inert).