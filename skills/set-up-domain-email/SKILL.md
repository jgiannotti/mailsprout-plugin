---
name: set-up-domain-email
description: Set up the first email accounts on a domain hosted with MailSprout and get every person connected on their phone or computer. Use when someone wants email addresses created for a business, a new domain, or a list of people.
---

# Set up email accounts on a domain

Use the MailSprout connector's tools. MailSprout manages accounts; it cannot read anyone's mail.

## 1. Confirm the domain is ready

Call `list_domains`.

- If the domain is listed and verified, continue.
- If it is missing or not verified yet, stop and explain: domains are added and verified in the MailSprout dashboard at https://mailsprout.io/dashboard, where a setup wizard shows the exact records to add at their domain registrar. Account creation only works on verified domains. Offer to continue once they have finished that step.

## 2. Agree the list of addresses

Collect the addresses before creating anything. Ask only for what is missing:

- The part before the @ for each person or role (for example `sarah`, `billing`, `hello`).
- Whether any address should forward somewhere instead of being its own inbox (for example `info@` forwarding to the owner). Those become forwards in step 4, not accounts.

Read the final list back and get a yes before creating.

## 3. Create the accounts

- One account: `create_account`.
- Two or more: `create_accounts_bulk` (up to 25 per call; split longer lists).

Each result includes a password that is shown once. Present every address with its password in a table and tell the user to save them now, for example in their password manager. Do not repeat passwords later in the conversation unless asked.

## 4. Add forwards

For each forward agreed in step 2, call `create_alias` with the source address and the destination.

## 5. Get people connected

For each account, call `generate_setup_link` and share the link with a one-line note: opening it on an iPhone, iPad or Mac installs the account in Apple Mail in one tap. For Outlook, Gmail and other apps, point them to the account page in the MailSprout dashboard, which lists the settings.

## 6. Wrap up

Summarize what now exists: accounts, forwards, and who still needs to open their setup link. Every MailSprout plan is one flat price for unlimited accounts, so creating accounts does not change the bill.
