# Requirement: Account lockout after failed logins

## Background
Automated tools are guessing passwords on our login page. We want to slow this down.

## What we want
- After 5 consecutive failed login attempts on an account, lock that account for 15 minutes.
- A successful login resets the failed-attempt count to zero.
- While an account is locked, login must be rejected even if the password is correct.
- The error message shown to the user must not reveal whether the account exists or is locked.
- Support staff must be able to unlock an account manually.
- Lockout applies per account, not per IP address.

## Out of scope
- Password reset flow.
- Multi-factor authentication.
