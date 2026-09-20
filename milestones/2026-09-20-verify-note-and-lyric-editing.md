# verify note and lyric editing

**Date:** 2026-09-20  
**Engine version:** v1.1.0  
**Category:** capability

## What changed

The ACE Experimental Engine verified two narrow agent-controlled musical-content operations in ACE Studio 2.1.8 through CLI 0.17.0: one existing note pitch mutation and one existing Sing-note lyric mutation. Each change was independently read back and exactly restored. These fixture-bound tests do not establish universal MIDI, lyric, vocal or MCP mutation support.

## Verified findings

- One existing note was moved from C4 to C#4, read back and restored to C4 with the same note identity.
- The note's position, duration, velocity and note count remained unchanged during the pitch canary.
- One existing English Sing-note lyric was changed from la to da, independently read back and restored to la with the same note identity.
- The lyric canary retained language, pitch, position, duration and note count.
- Note-content, pronunciation, vocal-expression and complete readable-state fingerprints returned exactly to baseline where applicable.
- Transport, loop, selection, caret, track identity and clip identity remained unchanged in both canaries.
- Dirty state and exactly two attributed history entries changed as expected in each canary.
- No save, playback, generation, render, export, plugin operation, preset operation or MCP mutation occurred.
- The evidence is operation-, fixture-, interface- and version-bound and is not a general editing claim.

## Why it matters

This demonstrates bounded agent control over both note geometry content and sung lyric content while preserving note identity and restoring the original project state exactly at every readable layer.

## Next step

Test one guarded existing-note duration resize and exact restoration on a separately prepared GenericMidi fixture. General MIDI, lyric, vocal and MCP mutation support remain unverified.
