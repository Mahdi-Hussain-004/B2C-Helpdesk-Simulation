# Automation Engine Logic

Below is the Boolean logic configured in Spiceworks to automate triage and enforce SLAs.

### Rule 1: Auto-Escalate Billing Issues
* **Logic:** IF `Description` CONTAINS `refund` OR `charged twice`
* **Action:** SET Category TO `Billing & Subscriptions` AND SET Priority TO `High`

### Rule 2: Critical - Legal & Risk
* **Logic:** IF `Description` CONTAINS `lawyer` OR `sue` OR `illegal`
* **Action:** SET Category TO `Trust & Safety` AND SET Priority TO `Critical`

### Rule 3: Auto-Triage App Bugs
* **Logic:** IF `Summary` CONTAINS `crash` OR `glitch` OR `black screen`
* **Action:** SET Category TO `App Performance & Bug Reports` AND SET Priority TO `Normal`

### Rule 4: VIP Fast-Track
* **Logic:** IF `Created By` CONTAINS `@vip-agency.com` OR `Description` CONTAINS `Verified Creator`
* **Action:** SET Category TO `Creator / VIP Support` AND SET Priority TO `High`