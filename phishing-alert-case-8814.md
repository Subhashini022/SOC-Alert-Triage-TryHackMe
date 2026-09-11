# Phishing Alert Investigation – Case 8814

## Alert Details

**Alert:** Inbound Email Containing Suspicious External Link

**Incident Classification:** False Positive

**Time of Activity:** September 2, 2026 at 12:25

---

## Related Entities

| Entity | Details |
|---|---|
| Subject | Action Required: Finalize Your Onboarding Profile |
| Sender | onboarding@hrconnex.thm |
| Recipient | j.garcia@thetrydaily.thm |
| Attachment | None |

---

## Investigation

The alert was triggered because the email contained an external URL.

During the investigation, the URL was checked and found to be clean. The email content was related to the employee onboarding process, and the recipient was instructed to complete the onboarding process through the provided link.

No suspicious attachment was present.

---

## Reason for False Positive

The alert was classified as a **False Positive** because the URL was determined to be clean and the email was related to a legitimate HR onboarding process.

There were no additional indicators suggesting malicious activity.

---

## Verdict

**False Positive**

---

## Key Learning

This investigation helped me understand that an alert containing a suspicious external link does not automatically mean that the email is malicious.

A SOC analyst should investigate the URL, email context, sender, recipient, and other available indicators before making a final classification.

---

## SOC Investigation Process

1. Review the alert.
2. Examine the email subject and sender.
3. Check the external URL.
4. Look for suspicious attachments or other indicators.
5. Understand the context of the email.
6. Determine whether the activity is malicious or legitimate.
7. Classify the alert as True Positive or False Positive.
8. Document the reason for the decision.
