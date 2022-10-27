---
# Page title as it appears in the navigation menu
title: "Record"
# Adjust the weight to reorder menu items (lower numbers appear first)
weight: 2
# Uncomment to hide nested pages in a collapsed menu
# bookCollapseSection = true
# Uncomment to hide this page from the navigation menu
# bookHidden = false
# Uncomment to exlude this page from the search
# bookSearchExclude = true
---

# Record

[Record][record] is a private GitHub repository
where we keep track of things that we have done
at a higher level of detail but a lower level of granularity
than is done in Azure DevOps.
Members of SA2C should automatically have access.

## Optimisation projects

For optimisation projects,
we keep track of benchmarking data here so we can compare before and after.
Where possible we also keep any notes on what was done,
to make it easier to pick up work again later.
(This is an area for improvement; we have not been rigorous about this.)
Each project gets a subdirectory.

Where possible we keep raw data.
Having a PNG file of a plot is far less useful
when we want to do something with data in 18 months’ time
than having all of the output files that were scraped to generate the plot.
For reports,
we keep the LaTeX source so that the report can be updated later.

## Support items

For one-to-one ad-hoc support,
we have the support subdirectory.
Each person we have support interactions with gets a Markdown file
named after the person’s surname.
The file has brief details about the person
(name, department, what kind of research they do, how they first encountered us,
things that are useful to know that give context to the support),
followed by one or more subheadings oftimes they have got in touch with support,
what they asked, and how we answered.

If we have e.g. written a job script,
then a copy of this can be included in a code block.

If larger amounts of code are worked with,
or other files are generated,
then a subdirectory within the support subdirectory is created
with the person’s surname as its name,
and the markdown and any other files are placed into this subdirectory instead.

## Efficiency monitoring

When users are identified as having low efficiency on SUNBIRD,
then a line is added to the table under efficiency_monitoring/README.md.
Data to include immediately are:

- the date this was identified,
- the user’s name and their username,
- the efficiency and number of idle node-hours (with the number that was concerning marked in bold),
- the name of the RSE responsible for investigating and following up on this.

Where a guess at the cause can be made from the output of sacct,
then this can be listed as the cause.
The action will initially be to contact the user,
or to monitor and contact if the problem recurs.
Once the user has responded to contact and worked through the issue,
then the cause and action can be updated.

There are some tools for working with the output of `sacct`
in a submodule within this directory.

## Other files

Other useful files in the root of the repository:

- A list of projects that have been requested
  but did not at the time have available capacity,
  in pending_projects.md.
- A list of metrics that we want to consider investigating
  when preparing performance reports on an application are in performance-report-metrics.md.
- The shared configuration for the Emacs Azure DevOps client
  is stored as azdev_config.el.
  Emacs users should add source this from their personal Emacs initialisation
  to set up the correct current project list.

<!-- markdown-link-check-disable-next-line -->
[record]: https://github.com/sa2c/record
