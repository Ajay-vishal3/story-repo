# DEMO-1: Account lockout after failed logins

## Background
Users sometimes have their accounts guessed at by automated scripts. We want to slow
this down without making life hard for genuine users.

## Requirement
- After 5 consecutive failed login attempts, the account is locked for 15 minutes.
- A successful login resets the failed-attempt count to zero.
- While locked, even a correct password is rejected.
- The error message shown to the user must not reveal whether the account exists or is locked.
- Support staff should be able to unlock an account manually.

## Out of scope
- Password reset flow
- Multi-factor authentication

## Notes
- Locking is per account, not per IP address.
