---
name: email-account-audit
description: Review every MailSprout email account across all domains, flag unused, nearly full or forgotten accounts, and tidy up with the owner's approval. Use for an email cleanup, storage check, or "who still has an address" review.
---

# Audit email accounts

Use the MailSprout connector's tools.

1. Call `audit_accounts`. It returns every account on every domain with storage used and flags for stale and oversized accounts.
2. Call `list_aliases` so forwards are part of the picture.
3. Present one table per domain: address, storage used, flag, and whether a forward points to or from it. Put flagged accounts first.
4. Summarize in plain words:
   - Accounts that look unused (stale flag). Ask whether each person still needs one.
   - Accounts close to the storage limit. Suggest the person clears old mail with large attachments.
   - Forwards that point to addresses that no longer exist.
5. Change nothing on your own. For any account the owner wants gone, follow the removal order in the add-or-remove-teammate skill: decide where future mail goes, give them a chance to copy old messages, delete only after an explicit yes, then forward the address.

Storage on MailSprout is shared across the whole plan, so the useful number is the plan total in the dashboard; individual accounts have no separate cap to raise.
