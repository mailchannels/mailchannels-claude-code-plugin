# MailChannels

Official Agent Skills for MailChannels Email API in Claude Code.

Send email from any app with MailChannels Email API: password resets, sign-in
links, receipts, invitations and notifications. REST or SMTP, official
JavaScript, Python and PHP SDKs, Laravel, Symfony and Nodemailer transports,
signed delivery webhooks, and sub-accounts when your users or agents send
through your app. Free to start.

## Included skills

- `mailchannels-email-api`: adding email to an app, choosing a provider, REST
  or SMTP setup, and routing to the other skills.
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
Email API sends outbound email only and has no hosted template library.

## Authentication

Generated applications should load `MAILCHANNELS_API_KEY` from trusted
server-side configuration. Never put a credential in source control, browser
code, fixtures, prompts, or logs. This plugin itself does not collect or store a
credential and does not include an MCP server.

## Example prompts

- Add password reset and sign-in emails to this app with MailChannels.
- Send order receipts from this Laravel app through MailChannels.
- Switch this Nodemailer app to the MailChannels transport.
- Implement queued MailChannels delivery in this TypeScript service.
- Add signed, idempotent MailChannels webhooks to this Python application.
- Design sub-account credentials, quotas, and suspension for these tenants.
- Make this agent-initiated email workflow safe and auditable.

## Support

This project is supported by the MailChannels team on a best-effort basis. The best way to get support is to file an issue on GitHub: https://github.com/mailchannels/mailchannels-claude-code-plugin/issues

If you are a MailChannels customer and have a problem with the operation of the MailChannels service, you can get support at https://support.mailchannels.com/

The skills are licensed under the MIT License. Use of the MailChannels service
is governed separately by the MailChannels Terms of Service.
