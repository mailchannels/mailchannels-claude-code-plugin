# MailChannels skills and plugins

This distribution packages the same six MailChannels Agent Skills for Codex and
Claude Code. It is skills-only: it does not run an MCP server, execute hooks, or
collect credentials.

## Structure

```text
.agents/plugins/marketplace.json       Codex repository marketplace
.claude-plugin/marketplace.json        Claude Code marketplace
plugins/mailchannels/
  .codex-plugin/plugin.json            Codex plugin manifest
  .claude-plugin/plugin.json           Claude Code plugin manifest
  skills/                               Shared cross-host skills
submission/                             Listing copy and review cases
```

## Local Codex installation

Register this repository marketplace and install the plugin:

```bash
codex plugin marketplace add /absolute/path/to/skills-and-plugins
codex plugin add mailchannels@mailchannels
```

Start a new Codex task after installation so the six skills are loaded.

## Local Claude Code installation

From the directory containing this repository:

```bash
claude plugin marketplace add ./skills-and-plugins
claude plugin install mailchannels@mailchannels
```

Run `/reload-plugins` in an active Claude Code session. Explicit skill names are
namespaced, for example `/mailchannels:mailchannels-js`.

## Public Claude Code installation

Add the public MailChannels marketplace and install the plugin:

```bash
claude plugin marketplace add mailchannels/mailchannels-claude-code-plugin
claude plugin install mailchannels@mailchannels
```

For a one-session development test:

```bash
claude --plugin-dir ./skills-and-plugins/plugins/mailchannels
```

## Validate

From this directory:

```bash
python3 /path/to/skill-creator/scripts/quick_validate.py plugins/mailchannels/skills/mailchannels-email-api
python3 /path/to/plugin-creator/scripts/validate_plugin.py plugins/mailchannels
claude plugin validate . --strict
```

Run the skill validator for all six skill directories. Also compile or test the
generated JavaScript, Python, and PHP examples against the released SDK version
before publishing.

## Publish

- Submit the plugin bundle and materials under `submission/openai/` to the
  OpenAI universal plugin directory.
- Host this repository publicly and submit the source URL with the materials
  under `submission/anthropic/` to the Claude Code community marketplace.

Tag the reviewed source commit as `v1.0.1`. Do not change the public
`mailchannels` slug after release.

## License and service terms

The skills are MIT-licensed. Use of MailChannels services remains subject to
the [MailChannels Terms of Service](https://www.mailchannels.com/terms-of-service/).
