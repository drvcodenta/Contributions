### 🛠️ **Open Source Contributions – OWASP BLT**
**Duration:** 2 months  
**Role:** Contributor (UI/UX Improvements, Docker Optimization, Bug Fixes, Documentation, and Automation)  
**Tech Stack:** Python (Django), PostgreSQL, Docker, Git, Sentry, RapidAPI  

#### **Key Contributions:**
1. **Docker Optimization:**
   - **Reduced Image Size by 50%:** Refactored the Docker setup by creating a multi-stage Dockerfile, reducing the image size from **2.04 GB** to **~900 MB**.
   - **Security Enhancements:** Minimized **vulnerabilities from 290+ to around 80** by streamlining dependencies and applying security best practices.
   - **PRs:**
     - [#3072](https://github.com/OWASP-BLT/BLT/pull/3072) – Reduced container size and eliminated vulnerabilities.
     - [#3049](https://github.com/OWASP-BLT/BLT/pull/3049) – Updated Docker setup documentation for new contributors.

2. **Trademark Search Automation:**
   - **Django Management Command:** Implemented a command to periodically search for trademarks using **RapidAPI (USPTO API)**.
   - **Efficient Execution Flow:** Added rate-limiting logic to avoid API overuse by:
     - Performing **hourly trademark checks** for companies that haven't been searched in a week.
     - Sending **email alerts** if new trademarks are found.
   - **Database Synchronization:** Added fields to track the last trademark search date and trademark count, ensuring consistent updates.
   - **PR:**
     - [#3116](https://github.com/OWASP-BLT/BLT/pull/3116) – Trademark search automation with DB updates and email alerts.

3. **CI/CD and Documentation:**
   - **Enhanced Setup Guide:** Improved project documentation by creating a **"How to Set Up the Project"** guide with detailed Docker configuration instructions.
   - **Streamlined PostgreSQL Configuration:** Standardized environment variable management for smooth local development.
   - **PR:**
     - [#2967](https://github.com/OWASP-BLT/BLT/pull/2967) – Docker setup guide.

4. **Bug Fixes & Maintenance:**
   - **Resolved MacOS Compatibility Issues:** Identified and fixed environment inconsistencies in Docker dev containers that caused build failures on MacOS due to incorrect remote user configurations.
   - **Handled Sentry Failures Gracefully:** Fixed issues where the application repeatedly attempted to connect to **Sentry** (even when commented out), causing unnecessary container crashes.
   - **PR:**
     - [#3080](https://github.com/OWASP-BLT/BLT/pull/3080) – Sentry bug fix and improved error handling.

## 🛠️ **Pull Requests**
1. [#3116](https://github.com/OWASP-BLT/BLT/pull/3116) - Improved Docker setup, optimized build process.
2. [#3086](https://github.com/OWASP-BLT/BLT/pull/3086) - Fixed responsiveness issues in the leaderboard section.
3. [#3072](https://github.com/OWASP-BLT/BLT/pull/3072) - Redesigned BugHunt Create page for better UX and added validation handling.
4. [#3049](https://github.com/OWASP-BLT/BLT/pull/3049) - Improved styling on the About Us and Terms page.
5. [#2823](https://github.com/OWASP-BLT/BLT/pull/2823) - Fixed issue with leaderboard overflow and made it scrollable on larger viewports.
6. [#2967](https://github.com/OWASP-BLT/BLT/pull/2967) - Fixed Docker build issues and improved PostgreSQL connectivity.
7. [#2944](https://github.com/OWASP-BLT/BLT/pull/2944) - Redesigned BugHunt Create page for improved UX.
8. [#2930](https://github.com/OWASP-BLT/BLT/pull/2930) - Added consistent styling on About Us and Terms page based on Figma design.
9. [#2925](https://github.com/OWASP-BLT/BLT/pull/2925) - Separated sponsorship and donation pages.
10. [#2922](https://github.com/OWASP-BLT/BLT/pull/2922) - Fixed Docker environment configuration issues.
11. [#2875](https://github.com/OWASP-BLT/BLT/pull/2875) - Improved the Bacon page UI.
12. [#2874](https://github.com/OWASP-BLT/BLT/pull/2874) - Improved responsiveness of issue cards.
13. [#2872](https://github.com/OWASP-BLT/BLT/pull/2872) - Fixed responsive issues in the bug card.
14. [#2823](https://github.com/OWASP-BLT/BLT/pull/2823) - Fixed leaderboard responsiveness issues.
