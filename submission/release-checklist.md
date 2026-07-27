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
- [ ] The Claude manifest and marketplace catalog report `1.0.2`.
- [ ] No evaluation-only metadata, simulation-only claims, dated prerelease
      suffixes, copied third-party content, or secret material appears in the
      package.
- [ ] Every relative reference resolves from the installed plugin cache.

## Behavior

- [ ] Positive and negative activation cases pass in Claude Code.
- [ ] JavaScript, Python, and PHP examples pass against current released SDKs.
- [ ] Tests use mocks or the simulator and send no live mail.
- [ ] Provider comparisons remain neutral.
- [ ] Unsupported inbound email and hosted template management are identified.
- [ ] Sub-account guidance does not impose a minimum monthly-send plan or claim
      reputation isolation or daily provider limits.

## Release

- [ ] A clean user can add the Claude marketplace and install the plugin.
- [ ] The reviewed commit is tagged `v1.0.2`.
- [ ] Submission bundles, validator output, test evidence, approvals, and commit
      SHA are archived.
