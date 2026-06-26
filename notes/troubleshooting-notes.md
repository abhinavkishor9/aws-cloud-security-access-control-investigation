# Troubleshooting Notes

## Issue 1

CloudTrail Event History inaccessible.

Reason

Service Control Policy (SCP) explicitly denies:

cloudtrail:LookupEvents

Resolution

Expected behavior within the AWS Skill Builder sandbox.

---

## Issue 2

GuardDuty shows Permission Warning.

Reason

Insufficient IAM permissions.

Resolution

No action required.

---

## Issue 3

Security Hub cannot determine enablement status.

Reason

Restricted IAM role.

Resolution

Expected sandbox limitation.

---

## Issue 4

Amazon Inspector cannot activate.

Missing Permission

inspector2:BatchGetAccountStatus

Resolution

Requires elevated privileges.

---

## Issue 5

Macie access denied.

Reason

Explicit deny through identity-based IAM policy.

Resolution

Working as designed.

---

## Issue 6

IAM Access Analyzer inaccessible.

Reason

Missing:

access-analyzer:ListAnalyzers

Resolution

Expected least-privilege enforcement.

---

## Issue 7

Unable to view S3 security settings.

Affected Settings

- Bucket Versioning
- Object Ownership
- Block Public Access

Reason

Restricted IAM permissions.

Resolution

Expected security restriction.

---

## Lessons Learned

Permission errors are not always indicators of security incidents.

SOC analysts should verify:

- IAM policies
- Service Control Policies
- Resource policies
- Organizational restrictions

before concluding that a cloud environment has been compromised.

This investigation demonstrates how properly configured cloud security controls can intentionally restrict analyst access while maintaining a secure AWS environment.
