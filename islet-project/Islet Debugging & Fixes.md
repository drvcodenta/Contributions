## Overview
The Islet Project is a cybersecurity-focused initiative that involves creating virtual machines inside ARM devices. Contributing to this project required deep technical expertise, particularly in debugging and resolving system-specific errors related to virtual environments and package management.

## Contribution Details
### Fix: Resolve `pip install toml` Error with Virtual Python Env ([#415](https://github.com/islet-project/islet/pull/415))
**Issue Faced:**
- While setting up Islet on **Ubuntu 24.04**, the `./scripts/init.sh` script failed due to an **externally-managed-environment error**.
- This error arose because Ubuntu 24.04 prevents conflicts between system and user-managed Python packages.

**Solution Implemented:**
- Created a **temporary Python virtual environment** for installing the `toml` package, ensuring that the script runs smoothly.
- Updated `.gitignore` to exclude the `venv` folder to prevent tracking unnecessary virtual environment files.
- Opened the fix for review and discussion, considering whether using a virtual environment for a single dependency was the best approach.

**Outcome:**
- The solution worked successfully across multiple Ubuntu versions, including **Ubuntu 22.04**.
- Maintainers approved and merged the fix on **January 3, 2025**.
- 8 CI checks passed, and the fix was accepted without conflicts.

### Additional Debugging Efforts
During initial testing on **WSL**, the system consistently crashed, preventing progress. To mitigate this:
- Switched to **VMware** and installed Ubuntu.
- Encountered further errors while running the **FVP creation script**.
- Initially assumed it was an OS-related error, but after thorough debugging, identified that the root cause was within the **project code** itself.
- Proposed and implemented a fix that resolved the issue across different system environments.

## Issue Reference
- Detailed discussion and debugging process documented in [Issue #398](https://github.com/islet-project/islet/issues/398)

## Maintainers' Response
- The maintainers appreciated the contribution.
- The fixes were tested successfully on different Ubuntu versions.
- The proposed solutions were merged into the main branch and resolved major setup issues for new contributors.

## Conclusion
Contributing to the Islet Project was a technically challenging task requiring advanced debugging skills, understanding of virtual environments, and experience with system-specific errors. The resolution of these issues improved the project's compatibility across multiple operating systems, making the setup process smoother for future contributors.

