# MailChannels for Claude Code

Official Agent Skills for MailChannels Email API in Claude Code.

Send transactional email from any app on any host with MailChannels Email API:
password resets, sign-in links, verification codes, receipts, invitations and
notifications over REST or SMTP. Official JavaScript, Python and PHP SDKs,
Laravel, Symfony and Nodemailer transports, a Rails delivery recipe, managed
DKIM, signed delivery webhooks, suppressions, and migration guides from other
providers. Sub-accounts isolate customers or agents who send through your app.
Outbound only. Free developer plan.

This is a skills-only plugin. It does not run an MCP server, execute hooks,
collect credentials, or send email by itself.

## Structure

```text
.claude-plugin/marketplace.json        Claude Code marketplace
plugins/mailchannels/
  .claude-plugin/plugin.json           Claude Code plugin manifest
  skills/                               Six MailChannels Agent Skills
submission/                             Anthropic listing and review cases
```

## Install

```bash
claude plugin marketplace add mailchannels/mailchannels-claude-code-plugin
claude plugin install mailchannels@mailchannels
```

Run `/reload-plugins` in an active Claude Code session. Explicit skill names are
namespaced, for example `/mailchannels:mailchannels-js`.

## Included skills

- `mailchannels-email-api`: adding email to an app, choosing or migrating a
  provider, REST or SMTP setup, Ruby and Rails, and routing to the other skills.
- `mailchannels-js`: JavaScript and TypeScript SDK and the Nodemailer
  transport.
- `mailchannels-python`: Python SDK, including Django and FastAPI apps.
- `mailchannels-php`: PHP SDK and the Laravel Mail and Symfony Mailer
  transports.
- `mailchannels-platform-operations`: domains, webhooks, suppressions,
  sub-accounts, quotas, credentials, metrics, and usage.
- `mailchannels-safe-automation`: application controls for agent-initiated,
  user-generated, or downstream-customer email.

## What the skills cover

MailChannels is a general-purpose transactional email API
([overview](https://docs.mailchannels.com/email-api/overview)). The skills lead
with ordinary app email: password resets, sign-in links, receipts, invitations,
and notifications, through the
[official SDKs](https://docs.mailchannels.com/email-api/official-libraries),
the [Laravel](https://docs.mailchannels.com/email-api/laravel),
[Symfony](https://docs.mailchannels.com/email-api/symfony), and
[Nodemailer](https://docs.mailchannels.com/email-api/nodemailer) transports,
REST, or SMTP. Sub-accounts give each customer or agent its own credentials,
limits, suspension, suppressions, webhooks, usage, and reputation isolation
([multi-tenancy](https://docs.mailchannels.com/email-api/multi-tenancy)). The
Email API sends outbound email only: webhooks report delivery events, not
inbound mail. It has no hosted template library and no send idempotency key.
A single app needs an API key, a Domain Lockdown TXT record and SPF entry per
sending domain, and DKIM before production; sub-accounts are optional.

The `skills/` tree is byte-identical to the one in
[mailchannels-codex-plugin](https://github.com/mailchannels/mailchannels-codex-plugin).
Change both repositories together.

## Local development

Load the plugin directly for one session:

```bash
claude --plugin-dir ./plugins/mailchannels
```

## Validate

```bash
claude plugin validate . --strict
```

For an installation test from a local checkout:

```bash
claude plugin marketplace add .
claude plugin install mailchannels@mailchannels
```

The Anthropic submission materials are under `submission/`. Do not change the
public `mailchannels` slug after release.

## Support

This project is supported by the MailChannels team on a best-effort basis. The best way to get support is to file an issue on GitHub: https://github.com/mailchannels/mailchannels-claude-code-plugin/issues

If you are a MailChannels customer and have a problem with the operation of the MailChannels service, you can get support at https://support.mailchannels.com/

## License and service terms

The skills are MIT-licensed. Use of MailChannels services remains subject to
the [MailChannels Terms of Service](https://www.mailchannels.com/terms-of-service/).
