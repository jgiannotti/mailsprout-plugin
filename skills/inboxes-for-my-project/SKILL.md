---
name: inboxes-for-my-project
description: Give a website or app you are building real email inboxes on its own domain (hello@, support@, you@) with MailSprout, and wire the addresses into the project. Use when a project has a custom domain and needs contact addresses.
---

# Real inboxes for a project's domain

For a project that has its own domain and needs addresses people can write to and reply from. Use the MailSprout connector's tools.

## 1. Find the domain

Work out the project's domain from what the user said, or from the project itself (deployment config, `package.json` homepage, site metadata, the README). Confirm it with the user.

Call `list_domains`. If the domain is not there or not verified, explain that it is added once in the MailSprout dashboard at https://mailsprout.io/dashboard, where a setup wizard detects where the domain's DNS is hosted and shows the records to add. Continue when they are done.

## 2. Pick the addresses

Suggest a small set and let the user choose, for example:

- `hello@` for general contact
- `support@` for customers
- the founder's own address

Ask whether any should be a forward to an inbox they already use rather than a separate inbox. Read the final list back before creating anything.

## 3. Create them

Use `create_accounts_bulk` for inboxes and `create_alias` for forwards. Show each password once and tell the user to save it. Call `generate_setup_link` for each inbox so they can add it to Apple Mail in one tap.

## 4. Wire them into the project (only if asked)

If the user wants it, update the project's contact details: footer, contact page, `mailto:` links, README, structured data. Never write passwords into the project, its environment files, or version control.

## Keep it to people-to-people email

These are inboxes for people. Don't configure them as the app's automated sender for sign-up confirmations, password resets, notifications or newsletters: MailSprout is for person-to-person email and limits sending per account. If the project needs automated email, say that it calls for a transactional email service and leave that choice to the user.
