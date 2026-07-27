# MailChannels for Claude Code

Official Agent Skills for evaluating, implementing, and operating the
MailChannels Email API with Claude Code.

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

## License and service terms

The skills are MIT-licensed. Use of MailChannels services remains subject to
the [MailChannels Terms of Service](https://www.mailchannels.com/terms-of-service/).
