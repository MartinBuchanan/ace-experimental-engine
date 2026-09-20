# ACE Studio 2.1.8 CLI-controlled instrument and vocal WAV acquisition demonstrated

**Date:** 2026-09-20  
**Engine version:** v1.1.0  
**Category:** capability

## What changed

ACE Studio 2.1.8 with CLI 0.17.0 produced valid non-silent instrument and vocal WAV output in two bounded tests. Important timing limitation: both tested 44.1 kHz exports contained exactly 824 frames beyond their nominal requested durations, equivalent to 18.684807 ms. The cause remains unresolved. This is a file-length excess, not an established alignment offset, and does not justify trimming. Sample-accurate export is not claimed. The original instrument canary remains STOPPED under its frozen one-frame duration criterion; this milestone demonstrates acquisition, not full canary acceptance.

## Verified findings

- One bounded synthesis-free instrument export job succeeded and produced valid non-silent master WAV output at 44.1 kHz, 16-bit stereo; its original duration-acceptance result remains STOPPED.
- A separate bounded Sing/vocal export produced valid non-silent master WAV output at 44.1 kHz, 16-bit stereo.
- The vocal export used no separate Play or explicit synthesis command. Observed synthesis activity and target-derived changes evidence synthesis during the export workflow, not fresh uncached computation.
- Authored project state remained preserved in both bounded tests; derived synthesis state was evaluated separately.
- Asynchronous CLI-controlled output jobs reached authoritative success in both cases. Job success alone does not establish timing acceptance.
- Instrument output contained 44,924 versus nominal 44,100 frames; vocal output contained 22,874 versus nominal 22,050 frames. Each excess was exactly 824 frames.
- The instrument region beyond nominal length contained continuing signal; the vocal region was silent. Their shared length does not establish a common cause, intentional tail, alignment offset or safe cropping rule.
- These findings do not establish universal export support, exact render timing, all scopes/rates/formats, standalone vocal synthesis, MCP execution parity or a complete reconstruction engine.

## Why it matters

These bounded results demonstrate agent-controlled acquisition of instrument and vocal audio with authored-state preservation. The shared 824-frame length excess remains unresolved; alignment and sample-accurate boundaries are not established, and no trimming or compensation rule follows.

## Next step

Run one separately bounded 48 kHz instrument timing discriminator, then pause capability proving before a separate Retain / Adapt / Replace / Retire architecture assessment. No automatic timing compensation is authorized.
