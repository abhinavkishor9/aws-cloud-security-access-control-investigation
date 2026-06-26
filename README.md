# aws-cloud-security-access-control-investigation

## Overview

This project demonstrates a cloud security investigation performed in an AWS Skill Builder sandbox from the perspective of a SOC Analyst.

Rather than identifying an active attack, the investigation validates that AWS security controls—including IAM permissions, Service Control Policies (SCPs), and least-privilege access—are functioning as intended.

The project shows how security analysts differentiate between intentional security restrictions and indicators of compromise.

---

## Investigation Scenario

A cloud administrator reports that multiple AWS security services cannot be accessed.

As a SOC Analyst, the objective is to determine whether the issue is caused by:

- AWS service failures
- Unauthorized activity
- Misconfiguration
- Correctly enforced security controls

---

## Services Investigated

- AWS CloudTrail
- Amazon GuardDuty
- AWS Security Hub
- Amazon Inspector
- Amazon Macie
- IAM Access Analyzer
- Amazon S3 Security Controls
- Security Groups

---

## Investigation Workflow

1. Review CloudTrail event history.
2. Validate GuardDuty access.
3. Check Security Hub status.
4. Review Amazon Inspector permissions.
5. Investigate Amazon Macie.
6. Verify IAM Access Analyzer.
7. Review S3 bucket security settings.
8. Examine Security Group rules.
9. Correlate all permission errors.
10. Determine root cause.

---

## Key Findings

- CloudTrail access blocked by Service Control Policy (SCP)
- GuardDuty access restricted
- Security Hub unavailable due to IAM permissions
- Inspector activation restricted
- Macie explicitly denied by IAM policy
- IAM Access Analyzer inaccessible
- S3 security settings protected
- Security Group rules intentionally permissive for training purposes

---

## Root Cause

The investigation confirmed that all observed access issues resulted from intentionally enforced AWS security controls rather than malicious activity.

Security mechanisms observed include:

- Least-Privilege IAM
- Service Control Policies (SCPs)
- Identity-based IAM policies
- Managed AWS Skill Builder sandbox restrictions

---

## SOC Analyst Conclusion

**Incident Severity:** Informational

**Status:** Closed – No Security Incident

The AWS environment is operating as designed. Permission errors observed throughout the investigation are expected behavior within a managed AWS sandbox and demonstrate effective enforcement of cloud security controls.

---

## Skills Demonstrated

- Cloud Security Investigation
- AWS IAM
- Service Control Policies (SCP)
- AWS Security Services
- Amazon S3 Security
- Security Validation
- Least Privilege
- SOC Investigation Workflow
- Root Cause Analysis
- Documentation

---
