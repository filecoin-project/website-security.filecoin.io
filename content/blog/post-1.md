---
title: "Response & Disclosure Process"
date: 2020-03-14T15:40:24+06:00
image : "images/2020-three-quarters-1.png"
# meta description
description: "We have a Coordinated Disclosure policy"
# save as draft
draft: false
---

We have a **Coordinated Disclosure** policy.

A researcher can share details of a vulnerability after a fix has been applied and our security team has provided permission to disclose.

We will make a best effort to address and patch if possible vulnerabilities within 90 days from submission.

Please keep security vulnerabilities private until we've had a chance to address them.


#### Response Process

1. A security researcher reports a vulnerability via email to security@filecoin.org or Keybase.
2. Our security team will designate a Response Manager in charge of a particular report based on expertise and availability.
  1. They will acknowledge receipt of the report in a quick response to the researcher.
3. The Response Manager will evaluate the vulnerability and assign an initial OWASP Severity estimate. They may optionally also contact the researcher using a secure private channel for more information.
4. Based on the vulnerability’s potential OWASP Severity additional security team members will be alerted for additional review and to develop a patch.
  2. Response Manager designates a private git branch for the patch + proposed OWASP score
  3. Reviewed by security team
  4. Response Manager drafts vulnerability announcement for the community
      1. Severity - Systems impacted - Solutions / patches
  5. Security team discusses a release target + date for the announcement + patch
  6. Response Manager communicates with the researcher who submitted the vulnerability:
      1. Proposed patch + release date
      2. Whether the researcher would like public credit for reporting the bug (anonymous reporting is also supported)
      3. Reporter’s bounty distribution address
  7. The security team will make a best effort to complete the above process within 90 days.
5. Community notifications and patches
  8. For High or Critical Severity issues, the security team will notify the Filecoin community that a security release is imminent. Notifications can include Filecoin Community Slack announcements, tweets, emails to ecosystem collaborators. 
      1. 24 hours following this notification, the fixes are applied publicly and new releases are issued.
  9. Medium to High Severity issues may result in a minor release including the patch.
  10. Low severity issues can be addressed in the next regular release.