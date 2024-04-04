---
title: "Responsible Disclosure"
date: 2020-03-14T15:40:24+06:00
image : "/images/2020-three-quarters-3.jpg"
---

## Coordinated Disclosure Policy

When working with us according to this policy, you can expect us to:
- Work with you to understand and validate your report, including a timely initial response to the submission
- Work to remediate discovered vulnerabilities in a timely manner
- Recognize your contribution to improving Filecoin security if you are the first to report a unique vulnerability, and your report triggers a code or configuration change

#### Disclosure channels

We’ve created two main channels for reporting:

- Send an email to [security@filecoin.org](mailto:security@filecoin.org). This email is monitored everyday. Please use our [PGP](https://github.com/filecoin-project/community/blob/master/public.key) key to encrypt sensitive information.
- Report a bug on [Immunefi](https://immunefi.com/bounty/filecoin/).

Please do not file a public issue or discuss the vulnerability in public places like Slack, Twitter, etc.

#### Process overview

1. A security researcher reports a vulnerability via email to security@filecoin.org or Keybase.
1. Our security team will designate a Response Manager in charge of a particular report based on expertise and availability. They will acknowledge receipt of the report in a quick response to the researcher.
1. The Response Manager will evaluate the vulnerability and assign an initial OWASP Severity estimate. They may optionally also contact the researcher using a secure private channel for more information.
1. Based on the vulnerability’s potential OWASP Severity additional security team members will be alerted for additional review and to develop a patch.
    1. Response Manager designates a private git branch for the patch + proposed OWASP score
    1. Reviewed by security team
    1. Response Manager drafts vulnerability announcement for the community
        1. Severity - Systems impacted - Solutions / patches
    1. Security team discusses a release target + date for the announcement + patch
    1. Response Manager communicates with the researcher who submitted the vulnerability:
        1. Proposed patch + release date
        1. Whether the researcher would like public credit for reporting the bug (anonymous reporting is also supported)
        1. Reporter’s bounty distribution address
    1. The security team will make a best effort to complete the above process within 90 days.
1. Community notifications and patches
    1. For High or Critical Severity issues, the security team will notify the Filecoin community that a security release is imminent. Notifications can include Filecoin Community Slack announcements, tweets, emails to ecosystem collaborators. 
        1. 24 hours following this notification, the fixes are applied publicly and new releases are issued.
    1. Medium to High Severity issues may result in a minor release including the patch.
    1. Low severity issues can be addressed in the next regular release.

#### Safe harbor

We consider security research conducted in alignment with our Disclosure Policy to be protected by Safe Harbor:

- Authorized in view of any applicable anti-hacking laws, and we will not initiate or support legal action against you for accidental, good faith violations of this policy
- Authorized in view of relevant anti-circumvention laws, and we will not bring a claim against you for circumvention of technology controls
- Exempt from restrictions in our Acceptable Usage Policy that would interfere with conducting security research, and we waive those restrictions on a limited basis
- Lawful, helpful to the overall security of the Internet, and conducted in good faith

You are expected to comply with all applicable laws. If legal action is initiated by a third party against you and you have complied with this policy, we will take steps to make it known that your actions were conducted in compliance with this policy.</p>

If at any time you have concerns or are uncertain whether your security research is consistent with this policy, please submit a report through one of our Official Channels before going any further.

<small>These are based on recommendations from [disclose.io](https://disclose.io) to accelerate adoption of vulnerability disclosure best practices.</small>