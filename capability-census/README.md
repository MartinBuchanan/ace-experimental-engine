# Capability census

This table will record public capability results after the structured census begins. No capability is marked Verified merely because documentation describes it or an interface exposes it.

**Documented ≠ Exposed ≠ Tested ≠ Verified**

| Capability | CLI access | MCP access | Documented | Exposed | Tested | Verified | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
<!-- capability-results:start -->
| Current interface discovery | Yes | Yes | Yes | Yes | Yes | Yes | Live enumeration established the current version and aggregate CLI/MCP surface. |
| Existing Sing-note lyric mutation | Yes | Yes | Yes | Yes | Yes | Yes | One UUID-targeted la to da mutation and exact la restoration were verified through CLI; pronunciation and expression state were reconciled. |
| Existing-clip position mutation | Yes | Yes | Yes | Yes | Yes | Yes | One UUID-targeted Sing clip moved from tick 0 to tick 480 and exactly back to tick 0 through CLI; MCP mutation was not tested. |
| Existing-note pitch mutation | Yes | Yes | Yes | Yes | Yes | Yes | One UUID-targeted C4 to C#4 mutation and exact C4 restoration were verified through CLI; MCP mutation was not tested. |
| Existing-track rename mutation | Yes | Yes | Yes | Yes | Yes | Yes | One UUID-targeted Sing track was renamed to a unique temporary name and exactly restored through CLI; MCP mutation was not tested. |
| General arrangement and track control | Yes | Yes | Yes | Yes | No | No | Other clip types, occupied destinations, multi-clip arrangements, track creation, deletion, reorder, routing, persistence and other fixtures remain unverified. |
| General MIDI, lyric and vocal editing | Yes | Yes | Yes | Yes | No | No | Multiple notes, other edits, languages, phoneme controls, persistence and other fixtures remain outside the verified result. |
| MCP mutation parity | Yes | Yes | Yes | Yes | No | No | The relevant MCP operation families are exposed, but neither clip movement nor track rename was dispatched through MCP. |
| Read-only operational capabilities | Yes | Yes | Yes | Yes | Yes | No | 26 normalized capabilities were tested; 8 were conservatively verified individually. |
| State-changing capabilities | Yes | Yes | Yes | Yes | No | No | Other state-changing operations remain outside this verified result. |
| Third-party VST effect parameter control | Yes | Yes | Yes | Yes | Yes | Yes | One SSL effect parameter was mutated and exactly restored through CLI; MCP mutation was not tested. |
<!-- capability-results:end -->

No census execution has been performed as part of the publication-workflow milestone.
