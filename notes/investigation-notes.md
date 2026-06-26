# Investigation Notes

## Objective

Determine whether inaccessible AWS security services indicate malicious activity or correctly enforced cloud security controls.

---

## Evidence Collected

### CloudTrail

Observation

- Event History inaccessible
- LookupEvents denied

Finding

- Explicit deny via Service Control Policy (SCP)

Conclusion

CloudTrail audit logs are protected by organizational policy.

---

### GuardDuty

Observation

Permission warning displayed.

Conclusion

Service access intentionally restricted.

---

### Security Hub

Observation

Failed to fetch enablement status.

Conclusion

Insufficient IAM permissions.

---

### Amazon Inspector

Observation

Unable to determine account status.

Missing Permission

inspector2:BatchGetAccountStatus

Conclusion

Least privilege successfully enforced.

---

### Amazon Macie

Observation

Explicit deny.

Permission

macie2:GetMacieSession

Conclusion

Identity-based IAM policy blocks access.

---

### IAM Access Analyzer

Observation

ListAnalyzers permission denied.

Conclusion

Restricted analyst permissions.

---

### Amazon S3

Observed

- Bucket Versioning inaccessible
- Block Public Access protected
- Object Ownership protected

Conclusion

Critical storage security settings cannot be modified by the analyst role.

---

### Security Groups

Observed

Inbound

Allow All Traffic

Outbound

Allow All Traffic

Conclusion

Expected configuration within a temporary AWS lab environment.

---

## Overall Assessment

No evidence of:

- Credential compromise
- Privilege escalation
- Misconfiguration
- Suspicious activity

Observed behavior aligns with enterprise cloud security best practices using least privilege and organizational access controls.
