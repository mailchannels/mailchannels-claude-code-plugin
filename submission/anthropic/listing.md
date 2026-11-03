# Claude Code community marketplace submission

## Listing

- Plugin slug: `mailchannels`
- Display name: MailChannels
- Publisher: MailChannels Corporation
- Version: 1.0.2
- Category: development
- Description: Send email with MailChannels
- Homepage: <https://docs.mailchannels.net/email-api>
- Source: <https://github.com/mailchannels/mailchannels-claude-code-plugin>
- Support: This project is supported by the MailChannels team on a best-effort basis. File an issue on GitHub: <https://github.com/mailchannels/mailchannels-claude-code-plugin/issues>. MailChannels customers with problems operating the MailChannels service can get support at <https://support.mailchannels.com/>.
- License: MIT

## Submission procedure

1. Publish this complete marketplace repository at a stable public Git URL.
2. Run `claude plugin validate . --strict` from the repository root.
3. Add the public marketplace to a clean Claude Code installation and install
   `mailchannels@mailchannels`.
4. Exercise all six namespaced skills and the cases in
   `submission/activation-tests.json`.
5. Submit the public repository URL through either:
   - Claude Console: <https://platform.claude.com/plugins/submit>
   - Claude.ai Team or Enterprise directory management:
     <https://claude.ai/admin-settings/directory/submissions/plugins/new>
6. After approval, verify the plugin is listed in the `claude-community`
   marketplace and installs as `mailchannels@claude-community`.
7. Tag the reviewed commit as `v1.0.2` and keep the `mailchannels` slug
   immutable. Use `displayName` for future presentation changes.

Third-party submissions land in the reviewed Claude Code community marketplace.
Anthropic's separately curated `claude-plugins-official` marketplace has no
application process; inclusion there is at Anthropic's discretion.

Official guidance: <https://code.claude.com/docs/en/plugins>
