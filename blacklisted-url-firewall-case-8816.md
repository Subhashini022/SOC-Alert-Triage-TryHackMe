# Blacklisted URL Investigation – Case 8816

## Alert Details

**Alert:** Blacklisted External URL Blocked by Firewall

**Incident Classification:** True Positive

**Time of Activity:** September 2, 2026 at 07:57:33

---

## Affected Entities

- User/employee endpoint that attempted to access the URL
- Source IP address
- Destination URL/domain blocked by the firewall

---

## Investigation

The alert was generated when an endpoint attempted to access an external URL that was identified as suspicious/blacklisted.

The firewall detected the connection attempt and successfully blocked the connection.

The URL was analyzed and confirmed to be suspicious, supporting the classification of this alert as a True Positive.

---

## Reason for True Positive

The alert was classified as a **True Positive** because the destination URL was confirmed to be suspicious/blacklisted and the firewall blocked the attempted connection.

This indicates that the security control detected and prevented access to a potentially malicious destination.

---

## Escalation Reason

The alert was escalated because the URL was confirmed as suspicious and an endpoint attempted to access it.

Further investigation is required to determine:

- Why the endpoint attempted to access the URL
- Whether the user intentionally or unintentionally accessed it
- Whether there were any other related connection attempts
- Whether the endpoint shows any signs of compromise

---

## Recommended Remediation

- Confirm that the firewall successfully blocked the connection.
- Keep the malicious URL/domain on the blocklist.
- Review related firewall and network logs.
- Review the affected endpoint for signs of compromise.
- Review related user activity.
- Search for additional attempts to access the same destination.
- Continue monitoring the endpoint and network traffic.

---

## Attack Indicator

**Firewall**

---

## Verdict

**True Positive**

---

## Key Learning

This investigation helped me understand how a SOC analyst can use firewall alerts to identify and respond to attempts to access suspicious external destinations.

I also learned that a blocked connection does not necessarily mean the investigation is complete. The affected endpoint and related activity should still be reviewed to determine whether there is any additional suspicious behavior.

---

## SOC Investigation Process

1. Review the firewall alert.
2. Identify the affected endpoint and network entities.
3. Analyze the destination URL/domain.
4. Determine whether the destination is suspicious or legitimate.
5. Confirm whether the firewall blocked the connection.
6. Classify the alert as a True Positive or False Positive.
7. Escalate when further investigation is required.
8. Review related logs and endpoint activity.
9. Document remediation and monitoring actions.
