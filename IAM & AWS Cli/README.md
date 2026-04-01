# AWS IAM and CLI Hands-on

Tested AWS CLI on both Windows (local) and Linux (CloudShell)

---

## 1. AWS CLI Installation

- Method: MSI Installer (Windows)

- Verification Command:
  aws --version

- Output:
  aws-cli/2.34.21 Python/3.14.3 Windows/10 exe/AMD64

- Status:
  AWS CLI installed successfully

---

## 2. AWS CLI Configuration

- Command:
  aws configure

- Inputs:
  AWS Access Key ID: <access-key>
  AWS Secret Access Key: <secret-key>
  Default Region: <your-region>
  Default Output Format: json

- Status:
  CLI configured successfully

---

## 3. IAM CLI Test - List Users

- Command:
  aws iam list-users

- Output:
  Retrieved IAM users successfully

- Users Found:
  1. lavanya-admin
     - ARN: arn:aws:iam::<account-id>:user/lavanya-admin
     - Created On: 2026-04-01

  2. lavanya-ops
     - ARN: arn:aws:iam::<account-id>:user/lavanya-ops
     - Created On: 2026-04-01
     - Password Last Used: 2026-04-01

- Status:
  CLI configured correctly and IAM access verified

---

## 4. CloudShell CLI Verification (Linux Environment)

- Environment:
  AWS CloudShell (Linux-based terminal)

- Command:
  aws --version

- Output:
  aws-cli/2.34.16 Python/3.14.3 Linux CloudShell

- Command:
  aws iam list-users

- Status:
  CloudShell working correctly and IAM access verified

---

## 5. IAM Security Tools (Audit and Monitoring)

### Credential Report

- Description:
  Account-level report showing all IAM users and credential status

- Actions Performed:
  - Generated credential report (CSV)
  - Reviewed password usage, MFA status, access key status, and last used timestamps

- Insight:
  Helps identify inactive users and security gaps

---

### Access Advisor

- Description:
  Shows which AWS services a user accessed and when

- Actions Performed:
  - Checked Access Advisor for IAM users
  - Reviewed last accessed services

- Insight:
  Helps enforce least privilege by removing unused permissions

---

## 6. IAM Concepts Covered

- IAM Users (one user equals one person)
- IAM Groups (permission management)
- IAM Policies (JSON-based permissions)
- Inline and Managed Policies
- IAM Roles (used by AWS services)
- Principle of Least Privilege

---

## 7. Security Best Practices Applied

- Avoided use of root account
- Created IAM users and groups
- Used secure CLI access with access keys
- Did not expose access keys in documentation
- Masked account ID in outputs
- Reviewed permissions using Access Advisor

---

## 8. Key Learnings

- IAM is a global service
- Permissions are controlled via policies
- CLI provides programmatic access to AWS
- Same IAM permissions apply across Console, CLI, and SDK
- Security auditing is important in IAM

---

## 9. Status

- IAM setup completed
- CLI configured and tested
- Cross-platform validation done (Windows and Linux)
- Security auditing performed

---

## Notes

- All sensitive data (access keys, account ID) are masked
- This repository is for learning and demonstration purposes only
