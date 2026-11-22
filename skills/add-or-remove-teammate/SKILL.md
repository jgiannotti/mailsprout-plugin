---
name: add-or-remove-teammate
description: Give a new hire a MailSprout email account, or offboard someone who is leaving while keeping their incoming mail. Use when someone joins or leaves a team, or when an employee's address needs to be redirected.
---

# Add or remove a teammate

Use the MailSprout connector's tools.

## Adding someone

1. Call `list_domains` and confirm which domain the address belongs on. If there are several, ask.
2. Agree the address (for example `jamie@` or `jamie.lee@`). Call `list_accounts` for that domain first so you don't propose an address that already exists.
3. Call `create_account`. Show the password once and tell the user to pass it on securely.
4. Call `generate_setup_link` for the new account and share it: on an iPhone, iPad or Mac it installs the account in one tap.
5. If the new person should also receive a shared address (for example `support@`), ask whether to set up a forward with `create_alias`.

## Removing someone

Deleting an account deletes its stored mail and cannot be undone, so take it in this order and confirm at each step:

1. Call `list_accounts` and confirm the exact address.
2. Ask where their future mail should go (usually the owner or a manager). Right after deleting, you will forward the address there so customers who still write to it are not lost.
3. Ask whether anyone needs to keep the old messages. If yes, they should copy them out with the person's mail app before you continue. Stop here until they confirm.
4. Call `delete_account` only after an explicit yes.
5. Call `create_alias` to forward the old address to the destination from step 2.

## Locked out or suspicious activity

If the person is staying but their password may be compromised, use `reset_account_password` instead of deleting. Their phone and computer stop syncing until they sign in again, so share the new password and a fresh `generate_setup_link` so they can reconnect in one tap.
