---
# Page title as it appears in the navigation menu
title: "Team Meeting"
# Adjust weight to reorder menu items (lower numbers appear first)
weight: 1
# Uncomment to hide nested pages in a collapsed menu
# bookCollapseSection = true
# Uncomment to hide this page from the navigation menu
# bookHidden = false
# Uncomment to exclude this page from the search
# bookSearchExclude = true
---

# Team Meeting

The team has a Weekly Team Meeting, typically scheduled for Mondays
(sometimes shifted due to unavailability or bank holidays).
The team meeting is conducted via Zoom and is allocated a 1 hour time slot, typically 10:00am to 11:00am, though a target time to finish the meeting is 30 to 45 minutes. The aims of the weekly team meeting are:

- Ensure RSE team members are up to date on project progress,
- Facilitate coordination between team members working on the same project,
- Discuss interactions with the wider Swansea University research community via support and job efficiency monitoring,
- Coordinate team-wide responsibilities such as delivering teaching and writing administrative reports.

On days where a weekly team meeting is scheduled, the daily Standup for that day is cancelled. A rotating chair is appointed for these meetings, and the chair is responsible for the introduction of topics for discussion and ensuring the meeting keeps to time.

Order of discussion:

- Calendar
  - Discuss events for the coming week, with some brief mentions of activities in the previous and next week.
  - Typically use screen share of Google calendar, though the choice of calender app is not prescribed.
  - Estimated time: 3-5 minutes.
- Projects
  - Provide updates on the project listing, commenting on status of work items, keep up to date on collaborative projects.
  - Project listings displayed using [Azure DevOps Emacs client][azdev].
  - Estimated time: 20-30 minutes.
- Support
  - Briefly summarize support provided by the team to users.
  - Estimated time: 3-5 minutes.
- Efficiency Monitoring
  - Evaluation of user efficiencies on the Sunbird cluster, noting idle node hours and job efficiencies as main indicators.
  - Usage metrics are displayed on a Grafana dashboard, which can be displayed in a web browser provided the browser is configured to utilise a SSH tunnel to Sunbird as a proxy.
    - The browser must be configured for manual proxy settings, using the SOCKS v5 protocol, and setting the SOCKS host to localhost on port 8888.
    - To activate the SSH tunnel to Sunbird, in a terminal use the command `ssh -D8888 [username]@sunbird.swansea.ac.uk`, replacing `[username]` with a Sunbird account name.
    - As this will prevent the configured browser from connecting to the internet while the SSH tunnel is active, it is recommended that configuration is performed for a secondary web browser, not a browser used in general day-to-day browsing.
  - Consider contacting users for support if efficiency drops below 70% with >50 node hours wasted (rough metrics, varies case by case).
  - Prioritise any projects with <40% efficiency, as these may appear in Cardiff’s utilisation data and be flagged for further action.
  - Estimated time: 5-7 minutes.
- Any Other Business (AOB)
  - Raise miscellaneous items not covered in previous sections.
  - Estimated time: 3-5 minutes.
- (Optional) Follow-up meetings
  - If time remains in the hour allocation and some team members wish to discuss other specific items like technical solutions or coordinating other actions, those who wish to can stay on the Zoom call.

[azdev]: {{< relref "/docs/projects/azure_devops" >}}
