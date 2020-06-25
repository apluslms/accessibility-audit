+++
title = "Form Controls"
tags = ["high", "wcag-a"]
+++

As a web application, A+ depends on forms to take user input for a range of purposes. The following forms were examined in the tests carried out:

- Log in (local users)
- Edit profile
- Create a group
- Submit an exercise requiring textual input
- Submit an exercise requiring a file upload

## Requirements

The following relevant requirements from WCAG were examined:

{{% wcag include="1.1.1,1.3.1,2.5.3,3.3.1,3.3.2" descriptions="false" %}}

In short, any controls present must:

- be labelled in a programatically determinable way
- make use of semantic markup, or, where this isn't possible, have their name and role explicitly stated 
- have a visible label
- make any detected errors in the user's input clear in text

## Issues

The following are examples of the issues found.

### Local user login

No visual indication is given if login fails. A clear error message and styling to match the error states of other text fields in the application would make this more understandable. 

### Submit a text-based exercise

The form control used to type the input to an exercise is associated with a `label`, although the `label` only contains the question number, and no clear indication of what should be entered into the field.

### Profile

There is no indication if updating the user's language suceeded or failed. Introducing an invalid value intentionally doesn't appear to cause an error condition.

### Submit a file upload exercise

This works correctly, however the label points to a field with a "non-unique id", so the correct label cannot be programatically determined.