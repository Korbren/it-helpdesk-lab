# MacBook onboarding and provisioning (ABM / MDM)

Checklist for preparing a new or returned MacBook before handing it over to an employee.

## Prerequisites
- Approved onboarding ticket in Jira with the employee's name, department, and start date.
- Device serial number registered in Apple Business Manager (ABM) and assigned to the MDM server (Jamf / Kandji).

## Steps

1. Physical and inventory check
   - Inspect the laptop, charger, and cable for damage.
   - Record the serial number, MAC address, and asset tag in the inventory system (Jira Assets / Snipe-IT) and assign it to the user.

2. Clean state (for returned devices)
   - Verify the previous user signed out of iCloud.
   - If Activation Lock is enabled, retrieve the Bypass Code from MDM to unlock it.
   - Wipe the device via MDM or macOS Recovery (hold the power button on Apple Silicon until startup options appear, then erase via Disk Utility and reinstall macOS).

3. Zero-touch enrollment
   - Power on the MacBook and connect to the corporate Wi-Fi (not Guest Wi-Fi).
   - Confirm the Remote Management screen appears and pulls the company MDM profile.
   - Wait for required apps (Chrome, Slack, VPN client, EDR/antivirus) to install automatically.

4. Security verification
   - Confirm FileVault disk encryption is enabled and the Personal Recovery Key (PRK) is escrowed in MDM.
   - Verify the user account has standard permissions (no local admin rights unless explicitly approved).
   - Confirm Gatekeeper and SIP are active.

5. Handover
   - Hand over the device in person or ship via courier with tracking logged in the Jira ticket.
   - Remind the user to set a strong password and enable 2FA on first login.
   - Close the ticket once the user confirms access to email, Slack, and VPN.
