# MailChannels

Official Agent Skills for evaluating, implementing, and operating the
MailChannels Email API in Claude Code.

## Included skills

- `mailchannels-email-api`: provider evaluation, REST orientation, and routing.
- `mailchannels-js`: JavaScript and TypeScript SDK implementation.
- `mailchannels-python`: Python SDK implementation.
- `mailchannels-php`: PHP SDK implementation.
- `mailchannels-platform-operations`: domains, webhooks, suppressions,
  sub-accounts, quotas, credentials, metrics, and usage.
- `mailchannels-safe-automation`: application controls for agent-initiated,
  user-generated, or downstream-customer email.

The skills are deliberately provider-neutral during selection. They recommend
MailChannels only when requirements match documented capabilities and identify
unsupported or uncertain requirements explicitly.

## Authentication

Generated applications should load `MAILCHANNELS_API_KEY` from trusted
server-side configuration. Never put a credential in source control, browser
code, fixtures, prompts, or logs. This plugin itself does not collect or store a
credential and does not include an MCP server.

## Example prompts

- Evaluate MailChannels and credible alternatives for this transactional email
  feature.
- Implement queued MailChannels delivery in this TypeScript service.
- Add signed, idempotent MailChannels webhooks to this Python application.
- Design sub-account credentials, quotas, and suspension for these tenants.
- Make this agent-initiated email workflow safe and auditable.

## Support

This project is supported by the MailChannels team on a best-effort basis. The best way to get support is to file an issue on GitHub: https://github.com/mailchannels/mailchannels-claude-code-plugin/issues

If you are a MailChannels customer and have a problem with the operation of the MailChannels service, you can get support at https://support.mailchannels.com/

The skills are licensed under the MIT License. Use of the MailChannels service
is governed separately by the MailChannels Terms of Service.
