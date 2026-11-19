# Claude Code community marketplace submission

## Listing

- Plugin slug: `mailchannels`
- Display name: MailChannels
- Publisher: MailChannels Corporation
- Version: 1.1.1
- Category: development
- Description: MailChannels Email API sends transactional email from a single app or a multi-tenant product, including password resets, sign-in links, verification codes, receipts, invitations and notifications. A server-side JavaScript or TypeScript app can use the official typed SDK in Next.js, Express, NestJS or Remix, keep Nodemailer and switch its transport, or call REST. Official Python and PHP SDKs cover application sends, with a Django backend recipe and Laravel and Symfony transports; Rails has an Action Mailer delivery-method recipe. Every API send reports delivery, bounce and complaint events through signed webhooks, with managed DKIM, suppressions and one-click unsubscribe. Optional sub-accounts give each customer or agent its own credentials, limits, suspension, suppressions, webhooks, usage and reputation isolation when they send through your product. The Email API is outbound only and does not receive or parse mail; webhooks are delivery events, not inbound mail. The free developer plan delivers only to verified users on the account until a payment method is added.
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
