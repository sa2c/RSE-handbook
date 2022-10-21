---
# Page title as it appears in the navigation menu
title: "Code Review"
# Adjust the weight to reorder menu items (lower numbers appear first)
weight: 1
# bookCollapseSection = true
# Uncomment to hide this page from the navigation menu
# bookHidden = false
# Uncomment to exclude this page from the search
# bookSearchExclude = true
---

# Code Review

Code reviews are used by most sucessful tech companies and generally propagated
as a useful tool for several reasons:
  - Better code quality
  - Learning effects for the coder and the reviewer
  - Increasing the lottery factor

There are numerous discussions and opinions of good code reviews out there in
every imaginable way of presentation (see ...) but as code reviews are
practically non-existent in our group at the time of writing, this document
shall only provide some very simple guidelines that can be expanded on when the
basics are established.

## When and How to Use Code Reviews

Given the smallness and diversity of our projects as well as the current
(non-existent) status, we shouldn't try to enforce code reviews on everything. As
a first step, we should try to make them common practice for all projects that
have at least two people working on it and on request. It is explicitly
encouraged to submit such requests to a particular person or the team in
general.

We should aim for a tight feedback cycle. That means that the code submitted
should have a reasonable size such that the reviewer can understand and review
it in roughly an hour or two (shorter is fine if the project as a whole or this
aspect of it is closed by less code). On the other side, the reviewer should aim
for providing the feedback reasonably quickly and a time frame should clearly be
communicated from both sides.

Both parties should keep in mind the broad effects of code reviews, particularly
the learning aspects, and act to their best effect. This implies that reviewers
are not assigned due to any hierarchy, neither in title nor in (presumed)
qualification. Even if the reviewer might know less about the language or
project at hand, they can still make valueable points, spark discussions and at
the very least learn themselves. In the worst case, there can be a further
review afterwards.

Feedback is usually most effective if the reviewer can be provided with a clear
set of questions about the code and coder and reviewer are encouraged to clearly
communicate about open questions and particular focus during the review.

## The Code to be Reviewed

It is in the coder's responsibility that
  - the reviewer knows how to run and work with the code (this is best done
    in form of a documentation or README and, if so, this becomes part of the
    review)
  - has a reasonable size as to not be a burden for the reviewer
  - the code passes all automated tests
  - the code passes all pertinent linters
  - the code is reasonably formatted (with an autoformatting tool if
    pertinent)
  - the code conforms with all pertinent style guides
  - that any deviation from the above is clearly communicated to the reviewer
    (with a reseasonable argument at best)

## How to Review and Provide Feedback

The reviewer can reject the code without any further consideration if the code
to be reviewed does not meet the above criteria unless communicated by the coder
in advance. Therefore every review should start with running all automated
tests, linters, formatters etc.

The review should then consider in order of priority:
  - Positive aspects of the code
  - No bikeshedding (i.e., no pondering on about small and/or subjective aspects
    of minor importance like variable names, distribution of code across files,
    etc. as long as they don't interfere with understanding severely)
  - Functional correctness as far as possible (it might be hard to assess that
    without a deeper understanding of the project)
  - Structural aspects
  - Readability (this includes severe cases of bad variable names, etc., beyond
    bikeshedding)
  - Anything else unclear to the reviewer
  - Performance aspects (if necessary and unambiguously assessible)

The reviewer should keep in mind the broad effects of code reviews and
therefore:
  - always maintain a positive communication about the code and start with
    positive aspects
  - provide short explanations for their comments
  - ask about anything unclear even if it is only for their own learning and
    does not imply any changes to the code