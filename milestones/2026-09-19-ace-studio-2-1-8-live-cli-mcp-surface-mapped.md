# ACE Studio 2.1.8 live CLI/MCP surface mapped

**Date:** 2026-09-19  
**Engine version:** v1.1.0  
**Category:** capability

## What changed

The ACE Experimental Engine completed a live read-only census of the current ACE Studio 2.1.8 agent interface. The current CLI/MCP surface was established directly rather than inherited from prior-version assumptions.

## Verified findings

- The census tested 26 normalized capabilities and conservatively verified 8.
- The official ACE agent skills currently provide guidance rather than additional executable behavior.
- No ACE mutation occurred during the Phase 2 census.
- Documented, Exposed, Tested and Verified remain separate evidence states.
- Prior-version evidence remains bound to the version on which it was collected.

## Why it matters

The current interface is materially broader than the historical baseline, so future architecture decisions can be based on observed current-version capabilities instead of assumptions.

## Next step

Begin controlled reversible mutation verification, starting with one bounded plugin-parameter change and exact restoration. No Retain, Adapt, Replace or Retire assessment has yet been made.
