# Changelog

Concise public changes are listed newest first. Detailed context belongs in the linked milestone records.

<!-- milestone-entries -->

## 2026-09-20 — ACE Studio 2.1.8 CLI-controlled instrument and vocal WAV acquisition demonstrated

- ACE Studio 2.1.8 with CLI 0.17.0 produced valid non-silent instrument and vocal WAV output in two bounded tests. Important timing limitation: both tested 44.1 kHz exports contained exactly 824 frames beyond their nominal requested durations, equivalent to 18.684807 ms. The cause remains unresolved. This is a file-length excess, not an established alignment offset, and does not justify trimming. Sample-accurate export is not claimed. The original instrument canary remains STOPPED under its frozen one-frame duration criterion; this milestone demonstrates acquisition, not full canary acceptance.

## 2026-09-20 — ACE Studio 2.1.8 transport seek, play and stop verified

- The ACE Experimental Engine verified three narrow transport operations in ACE Studio 2.1.8 through CLI 0.17.0: one stopped seek with exact restoration, one playback start on an isolated instrument fixture with normal playing state and advancing position, and one Stop with stable stopped readback. These findings do not establish complete transport support.

## 2026-09-20 — ACE Studio 2.1.8 clip arrangement and track structure control verified

- The ACE Experimental Engine verified two narrow structural operations in ACE Studio 2.1.8 through CLI 0.17.0: moving one existing clip by one quarter note and restoring it, and renaming one existing track and restoring it. Both tests retained stable object identity and reconciled the surrounding readable state; they do not establish general arrangement, track or MCP mutation control.

## 2026-09-20 — verify note and lyric editing

- The ACE Experimental Engine verified two narrow agent-controlled musical-content operations in ACE Studio 2.1.8 through CLI 0.17.0: one existing note pitch mutation and one existing Sing-note lyric mutation. Each change was independently read back and exactly restored. These fixture-bound tests do not establish universal MIDI, lyric, vocal or MCP mutation support.

## 2026-09-20 — ACE Studio 2.1.8 third-party VST parameter control verified

- The ACE Experimental Engine verified agent-controlled parameter mutation and restoration for one third-party VST effect under ACE Studio 2.1.8 using CLI 0.17.0. This is a narrow plugin- and operation-specific result, not a general VST compatibility claim.

## 2026-09-19 — ACE Studio 2.1.8 live CLI/MCP surface mapped

- The ACE Experimental Engine completed a live read-only census of the current ACE Studio 2.1.8 agent interface. The current CLI/MCP surface was established directly rather than inherited from prior-version assumptions.

## 2026-09-19 — ACE Experimental Engine enters CLI/MCP reassessment phase

- ACE Studio's expanded official CLI/MCP interface may replace or simplify parts of the original custom control layer. The project is beginning a structured capability reassessment while retaining earlier validation as useful evidence.
