# Phishing incident response (L1 Helpdesk)

Immediate containment and escalation steps when an employee reports clicking a suspicious link or entering credentials on a phishing page.

## Scope
Helpdesk L1 handles account containment and basic evidence collection. The SOC / Security team handles threat investigation, email purging, and root-cause analysis.

## Steps

1. Verify the report
   - Confirm with the user what happened: did they only open the email, click a link, enter their password, or download/run a file?

2. Account containment (if credentials were entered)
   - In Google Workspace Admin Console, immediately revoke all active sessions (Sign out).
   - Force a password reset.
   - Check 2-Step Verification settings to ensure the attacker did not enroll a new device or generate backup codes.

3. Endpoint containment (if a file was downloaded or executed)
   - Instruct the user to disconnect from Wi-Fi and unplug Ethernet immediately.
   - Do not turn off the machine unless instructed by SOC (to preserve volatile memory if needed).
   - Check the EDR/antivirus console for alerts on that host.

4. Collect evidence
   - Tell the user not to delete the phishing email.
   - Collect the sender address, subject line, timestamp, and the suspicious URL (or ask the user to export/forward the email as an `.eml` attachment).

5. Escalate to SOC
   - Open a high-priority security ticket or alert the SOC channel immediately.
   - Include: affected username, host/asset tag, exact time of the click, actions already taken by Helpdesk, and the collected email details.
   - Wait for SOC clearance before restoring full access or reissuing the workstation.
