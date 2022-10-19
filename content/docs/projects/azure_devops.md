---
# Page title as it appears in the navigation menu
title: "Azure DevOps"
# Adjust the weight to reorder menu items (lower numbers appear first)
weight: 1
# Uncomment to hide nested pages in a collapsed menu
# bookCollapseSection = true
# Uncomment to hide this page from the navigation menu
# bookHidden = false
# Uncomment to exlude this page from the search
# bookSearchExclude = true
---

# Azure DevOps

## Current Process

- We use the boards/work items functionality of Azure DevOps to track tasks and progress on projects. These are structured in a relatively prescriptive way

  - Each project is created as a “team” and “area path” in Azure DevOps language.

  - Overarching areas of work within projects are created as Epics. Many/most projects have a single Epic.

  - Goals within an area are created as Features. Features must be parented to Epics. (DevOps does not enforce this, but floating work items get lost.)

  - Specific pieces of work to do towards a particular goal are created as Development Tasks or Admin Tasks. Meetings that will enable progress towards a goal are created as Meetings. These must all be parented to a Feature.

- Because Azure DevOps was designed for teams working on a single product, the web-based views work very poorly for our team meetings where we review progress on multiple projects. Instead, we use a client written in Emacs Lisp that pulls down all work items in projects of interest and displays them in a tree view.

  - This is available from https://github.com/edbennett/azdev-mode/

  - The team ordering list is defined in azdev_config.el in Record.

  - Work items can be created (M-x azdev/add-item), be deleted (M-x azdev/remove-item), have their title changed (M-x azdev/set-work-item-title), and have their status updated (Tab) from the client. Certain work item statuses are not available currently (e.g. “Parked”); these must be set on the web instead.

  - Only work items with parents can be created in the client; new Epics must be created on the web.

  - If you need help setting up the Emacs client, then talk to someone who already has it working

- Currently support items and other smaller pieces of work not attached to projects are not tracked in DevOps.

- Work items can be assigned to specific team members; this is not currently done consistently however.

- Some aspects of the setup are no longer relevant:

  - Previously we recorded time spent on each work-item; we do not currently do this.

  - Previously meetings had associated “meeting attendances” associated with specific people; we do not currently record these.

## Proposed Changes 

- If any has capacity they can write a Vim client