# XCGS v1 — Executive Summary (English)

> **Status:** Release-ready. To be published together with the XCGS v1 white paper (Chinese full text: xcgs-runtime-governance-v1.md). Human push approval required per release gate.
> **Purpose:** One-page front face for the XCGS white paper when released to international audiences. Chinese full text = 02 file; this summary stands alone.
> **Author:** Krites@SynomosAI ｜ **Copyright:** SynomosAI · CC BY 4.0

---

## XCGS: A Runtime Governance Framework for Agentic AI

### The Gap

ISO/IEC 42001, the NIST AI RMF, and the EU AI Act share a common foundation: they assume that an AI system's behavior is known at deployment, can be documented, and can be reviewed by a human. Agentic AI breaks this assumption. Agents act at machine speed across dynamic environments, chain across multiple delegations, and make tool calls whose per-step legitimacy is not captured by any identity or authorization layer.

The industry has named this the **missing layer**: action governance — the runtime evaluation of whether *this specific action* should proceed, independent of *who* is calling it. As of 2026, no international standard fills it. Singapore's IMDA published the first agentic-specific governance framework in January 2026; the IETF has multiple competing proposals but no RFC; NIST opened an RFI on agent security in January 2026 acknowledging the structural gap.

### What XCGS Is

XCGS (Cross-cutting Control & Governance System) is a **runtime governance layer** designed to sit above existing management systems (ISO 42001 AIMS, NIST AI RMF processes) and below the application layer. It does not replace them; it adds the execution-time controls they lack.

The framework has three core contributions:

**1. A five-layer runtime architecture.**
- L1 Identity anchoring: dual binding to China's GB/Z 185 Agent Identity Code (AIC) and international DID/Verifiable Credential paths.
- L2 Permission governance: zero-standing-privilege, just-in-time task-scoped authorization, machine-readable action boundary declarations.
- L3 Delegation governance: delegation-chain depth caps, per-hop authorization proofs, chain accountability.
- L4 Action governance: per-tool-call intent verification × boundary check × context policy evaluation — independent of the identity layer.
- L5 Audit & traceability: full-chain replayable logs (identity → intent → action → outcome).

**2. An Autonomy Level (AL) axis — the theoretical core.**
Four tiers from AL0 (controlled execution, no autonomy) through AL3 (cross-agent collaboration, no human in loop), with runtime governance requirements scaling by tier. The AL axis maps onto FDA's proposed informs/recommends/acts distinction for medical AI, making XCGS and the regulatory framework mutual mirrors — evidence that the theory generalizes.

**3. A control catalog.**
Version 1 specifies 12 controls (RT-01 through RT-12), including action boundary declarations, zero-standing-privilege, delegation depth limits, prompt-injection isolation belts, cascade circuit-breakers, behavior-drift sentinels, and cross-domain mutual recognition (AIC ↔ DID). The full version targets 38+ controls.

### Differentiation from IMDA

IMDA's framework identifies four agentic risk classes. XCGS is complementary, not duplicative: it drills from risk classes down to a **control catalog**, introduces the **AL axis** for autonomy classification, adds a **delegation-chain accountability model**, elevates action governance to an **independent layer**, and **dual-anchors** identity to both Chinese (GB/Z 185) and international (DID/VC) systems for cross-border interoperability.

### Honest Boundaries

XCGS v1 is a theoretical framework with partially executable controls. It has not undergone third-party conformity assessment and does not constitute certification basis. GB/Z 185 is a guiding technical document (non-mandatory). The framework's companion API and authorization-code mechanisms are roadmap items, not yet live; the ambassador mechanism has completed its first issuance batch under the AI Passport Specification (eight voice ambassadors, verifiable via the anchor chain in the ai-passport-spec repository), though their public content is not yet published. Integration paths with existing ISO 42001 certification systems remain to be validated — XCGS positions itself as a *runtime supplement*, not a replacement for AIMS.

### Roadmap

- **Step 1 — Expert (2026 Q4):** Publish v1; demonstrate with own agents registered under GB/Z 185 as first reference case.
- **Step 2 — Police (2027 H1):** Run RT-01–RT-09 controls in live business workflows; publish implementation case studies.
- **Step 3 — Standard (2027 H2+):** Submit runtime governance provisions to national AI standards bodies and the AIP open-source community; propagate English version via international forums.

---

*© 2026 SynomosAI ｜ Author: Krites@SynomosAI ｜ CC BY 4.0. This is a framework summary, not legal advice.*
