# Capability census

This table will record public capability results after the structured census begins. No capability is marked Verified merely because documentation describes it or an interface exposes it.

**Documented ≠ Exposed ≠ Tested ≠ Verified**

| Capability | CLI access | MCP access | Documented | Exposed | Tested | Verified | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
<!-- capability-results:start -->
| Current interface discovery | Yes | Yes | Yes | Yes | Yes | Yes | Live enumeration established the current version and aggregate CLI/MCP surface. |
| Read-only operational capabilities | Yes | Yes | Yes | Yes | Yes | No | 26 normalized capabilities were tested; 8 were conservatively verified individually. |
| State-changing capabilities | Yes | Yes | Yes | Yes | No | No | Exposed by the current interface but not mutation-tested during Phase 2. |
<!-- capability-results:end -->

No census execution has been performed as part of the publication-workflow milestone.
