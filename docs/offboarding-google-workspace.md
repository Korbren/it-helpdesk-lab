# Employee offboarding (Google Workspace and SaaS)

Procedure for revoking corporate access and preserving company data when an employee leaves.

## Prerequisites
- Offboarding ticket from HR or the employee's manager with the exact termination date and time.
- Confirmation of who should receive the user's Google Drive files and email access.

## Steps

1. Immediate access revocation (at cutoff time)
   - Open Google Workspace Admin Console and locate the user.
   - Reset the account password to a random string.
   - Click "Sign out" / "Revoke sessions" to terminate all active web and mobile sessions.
   - Remove recovery phone/email and reset 2-Step Verification (2FA) / app-specific passwords.
   - Revoke OAuth tokens for third-party apps.

2. Account suspension (do not delete)
   - Change the user status to Suspended (or move to the Offboarded Organizational Unit).
   - Never delete the account immediately, as deletion removes all Drive files and Gmail history.

3. Data transfer
   - Transfer ownership of all Google Drive files to the designated manager.
   - If requested in the ticket, configure Email Delegation or email forwarding to the manager and set an out-of-office auto-reply.

4. Connected tools and physical access
   - Confirm Slack, Jira, and Confluence accounts are deactivated (automatically via SSO, or manually if standalone).
   - Deactivate the employee's office RFID access card.
   - Track the return of the MacBook and accessories in the asset inventory.

5. Documentation
   - Log all completed actions and timestamps in the Jira offboarding ticket before closing it.
