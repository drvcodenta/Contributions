## Overview
Open-source IT and security project for teams to monitor security flaws in the devices of the IT Teams

### Why do I love this project?
I came across many projects during my open-source journey.
The most important thing that acted as a fuel for me being engaged in the community was people.
Whatever projects I had been able to contribute to had great people and great communication.
There were many projects where the reply never even came, even after months.

This is the exact reason why Fleet stood out. The people here — especially Scott — are incredibly supportive. Replies come within days (sometimes even in seconds 🙌😭).


## Contribution Details
### Feature: Surface `team_id` and `team_name` in Activity Feed ([#28394](https://github.com/fleetdm/fleet/pull/28394))

**Problem Identified:**
- The Fleet activity feed lacked visibility into which **team** a query or policy was associated with.
- This created confusion in multi-team setups where policies and queries could be global or team-scoped, but activity logs didn’t reflect that.

**Solution Implemented:**
- Extended the backend to include `team_id` and `team_name` fields in activity logs for policy/query create, edit, and delete events.
- Handled edge cases like the “No Team” scenario by using a sentinel `team_id = -1` and properly formatting the output.
- Updated the frontend (`GlobalActivityItem.tsx`) to conditionally display team context in a human-readable format.
- Made the solution backward-compatible by adding `omitempty` to the new fields to prevent nulls from breaking legacy clients.

**Outcome:**
- The feature was tested thoroughly and iterated over 18 commits.
- All frontend copy was verified with design reviewers.
- After feedback and testing, the pull request was finalized and accepted.
- Improves auditability and clarity for teams using Fleet Enterprise features.

---

### Fix: Software URLs Missing in GitOps Export ([#30177](https://github.com/fleetdm/fleet/pull/30177))

**Issue Faced:**
- When exporting software using `fleetctl generate-gitops`, Fleet-maintained applications with defined URLs did not include those URLs in the output YAML.

**Solution Implemented:**
- Implemented logic to correctly include the `url` field from the `software_installers` metadata when present.
- Added tests to validate that URLs are exported correctly when software contains installer metadata with a defined URL.

**Outcome:**
- The fix resolved a long-standing gap in GitOps export behavior.
- All test cases passed and the PR was merged into Fleet’s main branch.
- Makes software metadata more complete and reliable in enterprise environments.

---

## Issue Reference

- Identified and documented the root cause for missing software URLs in GitOps export: [Issue #30282](https://github.com/fleetdm/fleet/issues/30282)
- Tracked and fixed the original behavior discussed in [Issue #29617](https://github.com/fleetdm/fleet/issues/29617)
- Website request: Fleet Docs powered AI Chatbot in [Issue #31074](https://github.com/fleetdm/fleet/issues/31074)

---

## Maintainers' Response

- Multiple maintainers reviewed the changes and gave detailed feedback, which was incorporated to handle edge cases and maintain backward compatibility.
- Contributions were acknowledged and merged into the main branch as part of the upcoming release cycles.

---

i am planning to continue contributing in this project...
