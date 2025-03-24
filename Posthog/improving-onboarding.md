# Improving Onboarding Experience  
**Time Spent:** ~1 month  
**Issue Link:** [GitHub Issue](https://github.com/PostHog/posthog/issues/29387)  

# PostHog Contributions

## Installation Steps

1. I think the installation of Docker using `apt` causes the crash of the VM, but I don’t know the real cause of the issue.
2. It was working the first time without this error, but it started right after that.
3. I installed `open-vm-tools` and `open-vm-tools-desktop` before running `sudo apt upgrade`, which might have caused the system to fail.
4. To confirm if there is any issue with the `apt` installation of Docker, I tried installing it using `apt` and restarted the system—it worked. This suggests that the issue might have been caused by installing `open-vm-tools` before updating the system.
5. Cloned the repository and restarted it—it worked.
6. Restarted after `flox` installation—it worked.
7. Restarted after `homebrew` installation—it worked.
8. Ran `brew install` and restarted again—it worked.
9. Ran `flox activate`—testing now.

## Contributions and Learnings

### Improving the Onboarding Experience

- **Issue worked on:** [Improving onboarding experience for new contributors](https://github.com/PostHog/posthog/issues/29387).
- **Key Fixes:**
  - Identified and documented issues in the onboarding process.
  - Proposed and implemented improvements for smoother setup.
  - Provided feedback for better documentation and contributor experience.

### Challenges Faced & Solutions

- **Environment Setup Issues:**

  - Faced multiple VM crashes due to unexpected package conflicts.
  - Identified root cause related to package installation order.
  - Documented step-by-step debugging and resolution approach.

- **GitHub Codespaces Access:**

  - Requested maintainer access for Codespaces to ease onboarding.
  - Explored alternative local setups when access was unavailable.

## Future Contributions

I plan to continue contributing to PostHog and improving the developer experience by:.

- Addressing more open issues related to frontend and backend improvements.
- However, I would require organizational contributor access for Codespaces to ensure a smooth workflow.

---
