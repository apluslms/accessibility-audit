+++
title = "Audit Scope"
+++

## Pages

The audit has been completed in **June 2020* using the `master` branch running locally. The following pages have been audited:

- **Front page**
- **Course archive**
- **Log in** and **you have logged out**
- **User profile**

Additionally, using the `course-template`, the following pages have been audited:

- **Course index**
- **Course content**
- **Exercise results**
- **Submit an exercise** both for exercises that require typed input and for file uploads
- **View a submission**

## Technology

At this stage, the amount of technology used for testing is quite narrow. 

{{% tested using="Chrome + Voiceover, Firefox + Orca, Safari iOS" %}}

Hopefully this gives a good enough indication of the general state of the interfaces. In the future, it would be desirable to test more deeply with a range of common assistive technologies.

Many tests do not require assistive technology, these have been completed using Chrome on macOS. 

## Target level

So far, these tests relate to all guidelines of **WCAG-A**.

It is the plan to extend this to include all guidelines within **WCAG-AA** during Summer 2020.
