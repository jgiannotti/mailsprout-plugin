# MailSprout for Claude

Create and manage email accounts on every domain you own by asking Claude. This plugin connects Claude to [MailSprout](https://mailsprout.io), email hosting where one flat monthly price covers unlimited email accounts on all your domains, and adds skills for the jobs people do most.

## What's included

**Connector:** the MailSprout MCP server at `https://mailsprout.io/mcp`. You sign in with your MailSprout account when you connect (OAuth). Its tools list domains, list and audit accounts, create one account or many, reset passwords, set up forwarding, create one-tap iPhone and Mac setup links, and delete accounts.

**Skills:**

| Skill | Use it to |
|---|---|
| `set-up-domain-email` | Create the first accounts on a domain and get everyone connected |
| `add-or-remove-teammate` | Add a new hire, or offboard someone without losing their incoming mail |
| `email-account-audit` | Find unused or nearly full accounts and tidy up with your approval |
| `inboxes-for-my-project` | Give a site or app you're building real inboxes on its domain |

## Requirements

- A MailSprout plan (from $15/month) with at least one domain added and verified in the [dashboard](https://mailsprout.io/dashboard). Domains are added there; the connector manages accounts on them.

## What it runs and sends

- No local code, hooks or scripts. The plugin is the connector reference above plus instruction files.
- All requests go only to `mailsprout.io` over HTTPS, using the access you grant when you sign in.
- The connector manages accounts. It cannot read the messages inside them.
- Passwords for new or reset accounts are shown once in the conversation. Save them somewhere safe.

## Privacy and support

- Privacy policy: https://mailsprout.io/privacy
- Docs: https://mailsprout.io/claude
- Support: support@mailsprout.io

MailSprout is for person-to-person business email, not newsletters or marketing sends.

MailSprout is an independent product and is not affiliated with Anthropic.
