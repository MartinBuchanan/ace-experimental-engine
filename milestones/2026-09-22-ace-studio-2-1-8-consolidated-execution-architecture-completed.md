# ACE Studio 2.1.8 consolidated execution architecture completed

**Date:** 2026-09-22  
**Engine version:** v1.2.0-rc  
**Category:** infrastructure

## What changed

The ACE Experimental Engine completed and privately cut over a consolidated, fail-closed CLI execution architecture for the bounded ACE Studio 2.1.8 operation set proven across migration Stages 1 through 12.

## Verified findings

- Bounded reads and guarded edit/readback/restoration operations share one normalized execution boundary.
- Transport seek and Play/Stop, existing-path persistence, WAV acquisition and asynchronous job observation are integrated.
- One end-to-end workflow linked a bounded edit, export job, independently verified WAV, audio analysis, structured provenance and exact source restoration.
- State-changing operations select one CLI route and do not shadow-dispatch or fall back to another backend.
- Historical exact-version evidence remains distinct and unsupported future versions fail closed.
- The private v1.2.0 candidate passed baseline-relative certification with zero regressions against its committed Stage 12 baseline and four improvements.
- Tested 44.1 kHz exports measured 824 frames beyond nominal; the cause remains unresolved and no compensation is applied.

## Why it matters

One explicit authority and evidence boundary reduces ambiguous execution while preserving operation-specific safety, provenance and restoration guarantees.

## Next step

Perform the separately authorized v1.2.0 publication process; calibrate export timing before any sample-aligned claim and migrate creation operations only with their own evidence.
