**Time Spent:** ~1 month  

**Issue Link:** [GitHub Issue](https://github.com/openvinotoolkit/openvino/issues/20210##issuecomment-1884629007)  
#### **Context:**
The task aimed to automate the movement of issues between columns in the OpenVINO GitHub Project Board. While default GitHub workflows automated some transitions (e.g., moving issues labeled "good first issue" to the **Contributors needed** column and closed issues to the **Closed** column), the **Assigned** and **In review** columns required custom automation.

#### **Objective:**
- Move issues from **Contributors needed** to **Assigned** when a contributor is assigned.
- Revert issues back to **Contributors needed** if the contributor is unassigned.

---

#### **Approach and Challenges:**

1. **First Attempt:**
- Used the **alex-page/github-project-automation-plus** GitHub Action from the official GitHub Docs.
- Steps taken:
  - Created a new project with separate columns.
  - Renamed the project and columns.
  - Switched the project visibility.
  - Rotated and modified the secret keys with different scopes to ensure proper access.
- **Outcome:**
  - Despite multiple adjustments, the action failed to detect the linked project.

2. **Second Attempt:**
- Created a custom workflow with the following steps:
  - Triggered on issue assignment and unassignment.
  - Fetched the assigned user.
  - Retrieved project information.
  - Attempted to move the issue to the appropriate column.
- **Challenges:**
  - The workflow successfully detected the assigned user.
  - However, it consistently failed to retrieve project information, returning a **null Project ID**.
  - This prevented the workflow from proceeding with moving the card, despite having correct syntax.

---

#### **Key Learnings and Conclusion:**
- The automation failed due to **project linkage and token access issues**, causing the Project ID to return null.
- Despite multiple strategies, the workflow couldn't access the project data, preventing further automation steps.
- The core challenge was GitHub's project authorization and API access constraints, which required further investigation or potential GitHub support intervention.

