# Release checklist

## Product and legal

- [ ] A MailChannels product owner has approved every capability and plan claim.
- [ ] Security has approved credential, webhook, retry, logging, and automation
      guidance.
- [ ] Legal has approved the MIT license, marks, privacy URL, terms URL, and
      marketplace copy.
- [ ] The public repository URL and company-approved release regions are set.

## Package

- [ ] All six skill validators pass.
- [ ] `claude plugin validate . --strict` passes.
- [ ] The Claude manifest and marketplace catalog report `1.1.0`.
- [ ] No evaluation-only metadata, simulation-only claims, dated prerelease
      suffixes, copied third-party content, or secret material appears in the
      package.
- [ ] Every relative reference resolves from the installed plugin cache.

## Behavior

- [ ] Positive and negative activation cases pass in Claude Code.
- [ ] JavaScript, Python, and PHP examples pass against current released SDKs.
- [ ] Tests use mocks or the simulator and send no live mail.
- [ ] Provider comparisons remain neutral.
- [ ] The `Scope` section states the documented limits as facts: outbound
      email only and no hosted template library.
- [ ] Sub-account guidance matches the documented wording on
      <https://docs.mailchannels.com/email-api/multi-tenancy>: per-sub-account
      API keys and SMTP passwords, limits (`-1` inherits the parent's), suspend
      and activate, suppressions, webhooks, usage, and reputation isolation.
- [ ] `plugins/mailchannels/skills/` is byte-identical to the same tree in
      mailchannels-codex-plugin (`diff -r` prints nothing).

## Release

- [ ] A clean user can add the Claude marketplace and install the plugin.
- [ ] The reviewed commit is tagged `v1.1.0`.
- [ ] Submission bundles, validator output, test evidence, approvals, and commit
      SHA are archived.
