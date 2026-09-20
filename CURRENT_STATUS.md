# Current status

Last updated: 2026-09-20

## Released capability

A validated private development baseline supports controlled, evidence-preserving experimentation, and the ACE Studio 2.1.8 CLI/MCP surface has been mapped read-only.

## Current reassessment work

Verified current-version CLI 0.17.0 control now includes bounded round trips for third-party VST parameters, existing-note pitch, existing Sing-note lyric content, one clip arrangement position, and one track rename. Each result is limited to its named fixture and operation; MCP mutation was not tested.

## Planned work

The next bounded structural test is one stopped-transport position seek and exact restoration without playback. Broader arrangement, track, transport and MCP mutation support remain unverified.

## Evidence language

Documented, Exposed, Tested and Verified are distinct evidence levels. Documentation or interface exposure alone does not establish verification.

Historical changes are recorded in [CHANGELOG.md](CHANGELOG.md) and [MILESTONES.md](MILESTONES.md).
