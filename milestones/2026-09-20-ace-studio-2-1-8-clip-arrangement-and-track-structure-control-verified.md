# ACE Studio 2.1.8 clip arrangement and track structure control verified

**Date:** 2026-09-20  
**Engine version:** v1.1.0  
**Category:** capability

## What changed

The ACE Experimental Engine verified two narrow structural operations in ACE Studio 2.1.8 through CLI 0.17.0: moving one existing clip by one quarter note and restoring it, and renaming one existing track and restoring it. Both tests retained stable object identity and reconciled the surrounding readable state; they do not establish general arrangement, track or MCP mutation control.

## Verified findings

- One existing Sing clip was moved from tick 0 to tick 480, independently read back and restored to tick 0 with the same clip UUID.
- The moved clip retained its 7,680-tick duration, internal note identity and content, lyric, pronunciation and vocal-expression state.
- Target-track and project-wide arrangement fingerprints returned exactly to baseline after clip restoration.
- One existing Sing track was renamed to a unique temporary name, independently read back and restored to its original name with the same track UUID.
- Track order, child membership, mixer, color, input, content and mounted-plugin state remained unchanged during the rename round trip.
- Dirty state and exactly two operation-attributed history entries changed as expected in each independent canary.
- No save, playback, transport mutation, generation, render, export or MCP mutation occurred.
- The evidence is operation-, fixture-, interface- and version-bound and is not a general arrangement or project-structure claim.

## Why it matters

This establishes bounded agent control over one arrangement position and one project-structure label while preserving stable identities and restoring every tested readable structural fingerprint.

## Next step

Test one stopped-transport position seek and exact restoration without playback. General transport, arrangement, track and MCP mutation control remain unverified.
