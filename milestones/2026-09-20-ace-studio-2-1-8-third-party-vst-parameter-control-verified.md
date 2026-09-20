# ACE Studio 2.1.8 third-party VST parameter control verified

**Date:** 2026-09-20  
**Engine version:** v1.1.0  
**Category:** capability

## What changed

The ACE Experimental Engine verified agent-controlled parameter mutation and restoration for one third-party VST effect under ACE Studio 2.1.8 using CLI 0.17.0. This is a narrow plugin- and operation-specific result, not a general VST compatibility claim.

## Verified findings

- The original Input Trim value was read before mutation.
- One bounded Input Trim change was applied and read back successfully.
- The exact original value was restored and read back successfully.
- The complete eight-parameter plugin fingerprint returned to its baseline value.
- Transport, selection, loop, caret, track identity, plugin identity, enable and bypass state, and final parameter state were unchanged.
- Project dirty state and two attributed undo entries changed as expected.
- No save, playback, generation, render, export, preset operation or additional mutation occurred.
- Documented, Exposed, Tested and Verified remain distinct evidence states; MCP mutation was not tested.

## Why it matters

This proves one controlled third-party effect parameter can be changed, independently read back and restored through the supported CLI while preserving surrounding project state.

## Next step

Test the same bounded mutation and restoration method on one existing third-party VST instrument. General VST control remains unverified.
