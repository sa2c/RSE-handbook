---
title: "Common Technical Practices"
weight: 5
---

# Common Technical Practices

This section summarises common technical practices within the team.
It is concerned with very general things
like the use of version control
as well as very concrete aspects
like suggestions for best practices in specific programming languages.
It should be considered one of the most dynamic parts of this handbook
and be extended and adapted as needed.

## Use Version Control

Do always use version control!

We use git to track changes.
The SA2C has a [local GitLab instance][sa2c-gitlab]
but for most of our work we use [GitHub][github],
where we are the [SA2C organisation][sa2c-github],
as it is most probably going to be public anyhow.
The local instance is mostly used for prototyping or small internal stuff.

## Tools and Best Practices

The team is encouraged to use and introduce best practices in any code they touch.
The subsections of this section will
collect suggestions on tools and
cookiecutter templates for languages we touched during our work.
You are strongly encouraged to use them
whenever you start something from scratch.

In most cases, we won't work on a project from scratch.
In these cases,
the project might have its own conventions,
which you are then adviced to follow,
and even if it doesn't,
one should consider that:

- changes in style and (implicit) convention should not be too disruptive,
  so as to not alienate the users from their own code
- changes in favor of best practice will require you
  to put in additional working hours and time
  which is a valuable resource

Conventions are introduced to get tedious decisions
like formatting or capitalisation in your variable names
out of the way.
You are welcome to discuss with the team before introducing new conventions
but in the end you just
configure your editor and/or pre-commit hooks to obey them
and hopefully never again think about them.
So, you don't need to agree with everything in there.

In following these conventions, editor configurations are of great use.
See [Configuring your editor][editor-config] for details.

[editor-config]: {{< relref "configuring_editors" >}}
[github]: <https://github.com/>
[sa2c-github]: <https://github.com/sa2c/>
[sa2c-gitlab]: <https://sa2c-gitlab.swansea.ac.uk>
