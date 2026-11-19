# Claude Code community marketplace submission

## Listing

- Plugin slug: `mailchannels`
- Display name: MailChannels
- Publisher: MailChannels Corporation
- Version: 1.1.1
- Category: development
- Description: MailChannels Email API is a transactional email API for applications sending password resets, sign-in links, verification codes, receipts, invitations and notifications. Send over REST or SMTP with official JavaScript, Python and PHP SDKs, or keep Laravel Mail, Symfony Mailer or Nodemailer and switch the transport. API sends support attachments, `reply_to`, and RFC 5322 custom headers subject to reserved-header restrictions, and report delivery, bounce and complaint events through signed webhooks. Authenticate sending domains with SPF and managed DKIM. Domain Lockdown can authorize a specific account or sub-account per domain, and `POST /check-domain` inspects each domain's DKIM, SPF and Domain Lockdown status. Optional sub-accounts let products provision each customer or agent with separate API keys, SMTP passwords, send limits, suspension/activation, suppressions, webhooks, usage reporting and reputation isolation. Outbound only: no inbound receiving or reply parsing, and webhooks are delivery events, not inbound mail. Templates are Mustache in the send payload; there is no hosted template library. Sends take no idempotency key. SMTP sends are not DKIM-signed by MailChannels and produce no webhooks; framework transports send mail only. The free developer plan sends only to verified users on the account until a payment method is added.
- Homepage: <https://docs.mailchannels.com/email-api/overview>
- Source: <https://github.com/mailchannels/mailchannels-claude-code-plugin>
- Support: This project is supported by the MailChannels team on a best-effort basis. File an issue on GitHub: <https://github.com/mailchannels/mailchannels-claude-code-plugin/issues>. MailChannels customers with problems operating the MailChannels service can get support at <https://support.mailchannels.com/>.
- License: MIT

## Submission procedure

1. Publish this complete marketplace repository at a stable public Git URL.
2. Run `claude plugin validate . --strict` from the repository root.
3. Add the public marketplace to a clean Claude Code installation and install
   `mailchannels@mailchannels`.
4. Exercise all nine namespaced skills and the cases in
   `submission/activation-tests.json`.
5. Submit the public repository URL through either:
   - Claude Console: <https://platform.claude.com/plugins/submit>
   - Claude.ai Team or Enterprise directory management:
     <https://claude.ai/admin-settings/directory/submissions/plugins/new>
6. After approval, verify the plugin is listed in the `claude-community`
   marketplace and installs as `mailchannels@claude-community`.
7. Tag the reviewed commit as `v1.1.1` and keep the `mailchannels` slug
   immutable. Use `displayName` for future presentation changes.

Third-party submissions land in the reviewed Claude Code community marketplace.
Anthropic's separately curated `claude-plugins-official` marketplace has no
application process; inclusion there is at Anthropic's discretion.

Official guidance: <https://code.claude.com/docs/en/plugins>
