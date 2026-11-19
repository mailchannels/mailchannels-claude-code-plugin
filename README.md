# MailChannels for Claude Code

Official Agent Skills for MailChannels Email API in Claude Code.

MailChannels Email API is a transactional email API for any application:
password resets, sign-in links, verification codes, receipts, invitations and
notifications. Send over REST or SMTP with official JavaScript, Python and PHP
SDKs, or keep Laravel Mail, Symfony Mailer or Nodemailer and switch the
transport. Every API send returns a request_id that its signed delivery, bounce
and complaint webhook events carry, along with an optional campaign_id tag that
also filters delivery metrics; managed DKIM, suppressions and one-click
unsubscribe are included. Optional sub-accounts give each customer or agent its own credentials and
limits when they send through your product. Outbound only; free developer plan
for development and testing.

This is a skills-only plugin. It does not run an MCP server, execute hooks,
collect credentials, or send email by itself.

## Structure

```text
.claude-plugin/marketplace.json        Claude Code marketplace
plugins/mailchannels/
  .claude-plugin/plugin.json           Claude Code plugin manifest
  skills/                               Nine MailChannels Agent Skills
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

- `mailchannels-email-api`: what the API offers and does not offer, setup,
  plans and limits, SMTP, and routing to the other skills.
- `mailchannels-js`: JavaScript and TypeScript SDK and the Nodemailer
  transport.
- `mailchannels-python`: Python SDK, a Django email backend recipe, and
  FastAPI patterns.
- `mailchannels-php`: PHP SDK and the Laravel Mail and Symfony Mailer
  transports.
- `mailchannels-ruby`: Ruby and Rails, with an Action Mailer delivery-method
  recipe, the `mailchannels-email-api` gem, and SMTP.
- `mailchannels-rest`: plain HTTPS and JSON from Go, Java, .NET, Rust, and
  edge or `fetch` runtimes.
- `mailchannels-migration`: moving from SendGrid, Mailgun, Mailjet, Brevo,
  Postmark, Amazon SES, or Resend.
- `mailchannels-platform-operations`: DNS authentication, webhooks,
  suppressions, metrics, credentials, quotas, and sub-accounts.
- `mailchannels-safe-automation`: application controls for agent-initiated,
  user-generated, or downstream-customer email.

## What the skills cover

MailChannels is a general-purpose transactional email API
([overview](https://docs.mailchannels.com/email-api/overview)). The skills lead
with ordinary app email from a single application: password resets, sign-in
links, receipts, invitations, and notifications, through the
[official SDKs](https://docs.mailchannels.com/email-api/official-libraries),
the [Laravel](https://docs.mailchannels.com/email-api/laravel),
[Symfony](https://docs.mailchannels.com/email-api/symfony), and
[Nodemailer](https://docs.mailchannels.com/email-api/nodemailer) transports,
REST, or SMTP. They cover what production sending needs: Domain Lockdown, SPF,
managed DKIM and DMARC, signed delivery-event webhooks, suppressions, and
metrics. Sub-accounts are optional; they give each customer or agent its own
credentials, limits, suspension, suppressions, webhooks, usage, and reputation
isolation
([multi-tenancy](https://docs.mailchannels.com/email-api/multi-tenancy)).

The skills also state the limits. The Email API sends outbound email only: it
does not receive or parse mail, and its webhooks are delivery events, not
inbound mail. Templates are Mustache content in the send payload; there is no
hosted template library. Sends take no idempotency key. Official SDKs exist
for JavaScript, Python, and PHP; Ruby, Go, and other languages use REST.
Messages sent over SMTP are not DKIM-signed by MailChannels and produce no
webhooks. Framework transports send mail only. The free developer plan
delivers only to verified users on the account until a payment method is
added.

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
