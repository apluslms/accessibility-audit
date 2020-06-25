+++
title = "A+ Accessibility and Inclusive Design Audit"
+++

This report documents an audit of the [A+ Learning Management System](https://apluslms.github.io/), carried out in the summer of 2020. The aim is to identify any shortcomings which may prevent students and instructors from using A+ as intended on the basis of disability or assistive technology use, and to provide guidance on fixing these. 

{{% note %}}
A+ gives course creators a great deal of power - they can import their own CSS and Javascript. The audit only considers the platform, and used the "course template" as a benchmark.
{{% /note %}}

While A+ comprises a number of components, this testing has been carried out focusing on the typical student journey though the [A+ portal](https://github.com/apluslms/a-plus/).

This includes some views created by [mooc-grader](https://github.com/apluslms/mooc-grader), and content created by [a-plus-rst-tools](https://github.com/aalto-letech/a-plus-rst-tools/). Content from the [course-templates](https://github.com/apluslms/course-templates) was used for the testing. 

## Next Steps

At this time, the audit concerns the requirements of WCAG-A. A summary of compliance can be found on the {{% pattern "WCAG-A Summary" %}} page.

Some significant, frequently occuring problems are noted alongside some suggestions to address them, and grouped by their severity, under 'Things to Fix'. In due course, GitHub issues for these will be added to the relevant repositories.

Once there are plans to fix these, an audit at WCAG-AA will be completed. 