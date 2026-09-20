# ACE Studio 2.1.8 transport seek, play and stop verified

**Date:** 2026-09-20  
**Engine version:** v1.1.0  
**Category:** capability

## What changed

The ACE Experimental Engine verified three narrow transport operations in ACE Studio 2.1.8 through CLI 0.17.0: one stopped seek with exact restoration, one playback start on an isolated instrument fixture with normal playing state and advancing position, and one Stop with stable stopped readback. These findings do not establish complete transport support.

## Verified findings

- One stopped seek moved the playhead from tick 0 to tick 480 and restored it exactly to tick 0.
- One Play command on a soloed instrument-plugin fixture produced normal playing state and independently observed playhead movement.
- One Stop command after proven playback returned transport to stopped state, with two stable readbacks at the same position.
- One stopped seek then restored the original playhead position exactly to zero.
- Project content, track and clip arrangement, mute and solo state, instrument-plugin parameters, authored vocal content and derived pronunciation state remained unchanged.
- Vocal synthesis was isolated from the successful playback test and synthesis remained idle.
- An earlier vocal-fixture playback attempt was interrupted by synthesis and was therefore not counted as verified playback.
- The evidence is operation-, fixture-, isolation-, interface- and version-bound; Pause, loop, scrub, recording, other playback topologies and MCP mutation remain unverified.

## Why it matters

This establishes bounded agent control over seek, playback start and playback stop while preserving the tested project and sound-source state and separating normal playback from synthesis-interrupted behavior.

## Next step

Assess persistence and reopen behavior under a separately bounded protocol. Pause, loop, scrub, recording, other playback topologies and MCP mutation remain unverified.
