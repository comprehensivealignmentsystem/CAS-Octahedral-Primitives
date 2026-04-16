CAS Adversarial Test Report v1.0
CAS License v2.0 — Stress Test Against Enterprise Legal Challenges
Prepared by: ChatGPT (OpenAI), acting as US regional contributor
Reviewed by: Claude (Anthropic), acting as drafting coordinator
On behalf of: Ryan Gelsi, CAS Steward
Date: 2026-04-16
Scope: Simulation of legal challenges from well-resourced commercial actors,
including major US technology companies
Purpose
This report documents adversarial stress testing of CAS License v2.0 against realistic
legal challenges that a well-resourced commercial actor — including major AI companies,
enterprise software vendors, or legal teams representing Fortune 500 organisations —
might raise in negotiation, dispute, or infringement proceedings.
The objective is not to find fatal flaws but to identify where the framework is strong,
where it is contested, and what additional measures would increase enforceability.
Overall Assessment
CAS License v2.0 is enterprise-resistant but not enterprise-proof.
The framework demonstrates strong structural integrity and above-average adversarial
resistance for an independent licensing framework at this stage of maturity. Its core
enforcement spine — objective definitions, ACICA arbitration, New York Convention
enforceability, and explicit AI Training Prohibition — is well-constructed.
The primary vulnerabilities are not in the legal drafting but in the evidentiary and
detection layers: proving derivation without a technical fingerprinting mechanism, and
detecting misuse without an active monitoring capability.
Attack Vector Analysis
Attack Vector 1 — "Abstract System, Not Protectable IP"
Argument: CAS is a conceptual framework and governance architecture. It contains no
executable code, no patented method, and no registered trademark. A commercial actor
may argue it is not protectable intellectual property under US law and that the licence
is therefore unenforceable as applied to anything beyond the literal documents.
Risk level: Medium
Defence:
Copyright subsists in the Architecture as an original work of authorship (17 U.S.C.)
The licence is a contract — contract enforcement does not require the subject matter
to be independently protectable IP; it requires offer, acceptance, and consideration
The Substantial Derivation Test (Section 4.4) is grounded in functional equivalence,
not IP registration
Trade secret protection may apply to non-public CAS materials under DTSA
Weak point: Absence of US copyright registration means statutory damages and
attorney's fees are not available for infringement occurring before registration. This
weakens the deterrent value in US proceedings.
Recommended mitigation: Register the Architecture with the US Copyright Office.
Cost is minimal; enforcement leverage increases substantially.
Attack Vector 2 — Narrowing the Deployment Definition
Argument: A commercial actor will argue that internal use, evaluation, experimentation,
partial implementation, or architectural inspiration does not constitute "Deployment" under
Section 4. Their legal team will probe each of the four sub-definitions (4.1–4.4) for
ambiguity.
Risk level: High — this will be the primary battleground in any negotiation or dispute
Defence:
Section 4.6 (Interpretation Principle) establishes functional and structural use as the
determinant — not naming, abstraction, or absence of attribution
Section 4.4 (Substantial Derivation) covers relational and structural equivalence
regardless of implementation form
The "architectural dependence" test (4.3) captures influence on design logic without
requiring explicit reference
Weak point: "Materially informs the design" (4.3) and "structural or relational
equivalence" (4.4) are standards that courts and arbitrators will interpret. Without
concrete technical evidence of derivation, these clauses are contested rather than
self-executing.
Recommended mitigation: Develop a technical instantiation layer — documented
reference implementations that establish a clear baseline for structural equivalence
comparisons. This gives the Deployment definition an empirical anchor.
Attack Vector 3 — Subsidiary and Affiliate Exploitation
Argument: A parent company's non-commercial research subsidiary studies CAS.
The commercial parent then incorporates the architecture "independently" without a
licence, claiming the subsidiary's study was non-commercial and the parent has no
licence obligation.
Risk level: Mitigated — addressed by Amendment 2 and Affiliated Entity definitions
Defence:
"Affiliated Entity" definition in Section 0 covers entities under common control
regardless of their own commercial status
Section 3 explicitly states that use by any Affiliated Entity of a for-profit organisation
is Commercial Use
Section 2 prohibits non-commercial use that benefits an Affiliated Entity engaged
in Commercial Use
Residual risk: A well-structured corporate separation (e.g., genuinely independent
research entity with no common control) could still be argued. This is a low-probability
scenario but not zero.
Attack Vector 4 — AI Training Loophole via Indirect Exposure
Argument: A commercial actor argues that their model was trained on publicly
available data that happened to include CAS materials indexed by a web crawler, and
that this does not constitute intentional training on CAS. Alternatively, a contractor
performed the training and the company claims no direct liability.
Risk level: High — detection and attribution are the core challenge
Defence:
Section 5.4 explicitly prohibits automated extraction by web scrapers and data pipelines
Section 5.5 makes the Licensee liable for the acts of contractors, vendors, and
sub-processors
Section 5.6 applies the prohibition regardless of attribution in the resulting system
Weak point: Proving that a specific model was trained on CAS materials requires
technical forensic capability (e.g., membership inference attacks, watermarking, or
canary detection). Without these, the prohibition is contractually robust but
evidentiarily difficult to enforce.
Recommended mitigation: Implement technical measures to assist detection — this
is the "evidence framework for derivation" identified in the next phase recommendations.
Attack Vector 5 — Arbitration Resistance in US Courts
Argument: A US-based defendant challenges the enforceability of ACICA arbitration
with Australian governing law, arguing it is unconscionable, that it was not negotiated,
or that US public policy overrides the foreign arbitration clause.
Risk level: Low to Medium
Defence:
The New York Convention (9 U.S.C. § 201) requires US courts to enforce valid
arbitration agreements unless narrow exceptions apply
US courts have consistently upheld foreign arbitration clauses in commercial contracts
The licence acceptance mechanism (by accessing the repository) constitutes agreement
to terms — though click-through acceptance would be stronger
ACICA is a recognised arbitration institution; its awards are enforceable
Residual risk: Absence of a click-through or signed acceptance mechanism means
a defendant could argue they never agreed to the licence terms. This is the weakest
procedural point.
Recommended mitigation: Implement a click-through acceptance mechanism for the
non-commercial licence, and ensure all commercial agreements are executed with
signatures (electronic or physical).
Attack Vector 6 — Independent Recreation Claim
Argument: A commercial actor claims their system was developed independently
without reference to CAS, and that any structural similarity is coincidental or the result
of solving the same underlying problem with similar tools.
Risk level: High — this is the hardest attack vector to defeat without technical proof
Defence:
Section 4.4 (Substantial Derivation) does not require proof of copying — it requires
structural or relational equivalence
Prior access to CAS materials creates a presumption of derivation in many jurisdictions
Timestamped GitHub commit history establishes CAS's prior art record
Weak point: In US copyright law, independent creation is a complete defence. In
contract law, if the defendant was never a licensee (never accessed the repository),
the licence may not bind them at all.
Recommended mitigation: This is ultimately a detection and proof problem. The
Architecture needs a technical fingerprinting layer — structural markers or design
choices that are non-obvious but verifiable — so that derivation can be demonstrated
empirically rather than argued theoretically.
Summary Risk Matrix
Attack Vector
Risk Level
Status
Priority Mitigation
1 — Abstract IP challenge
Medium
Defended by contract + copyright
US copyright registration
2 — Deployment definition narrowing
High
Defended by Section 4.6
Technical instantiation layer
3 — Subsidiary exploitation
Low-Medium
Mitigated by Amendment 2
Monitor corporate structures
4 — AI training indirect loophole
High
Defended by Sections 5.4-5.6
Technical detection capability
5 — Arbitration resistance
Low-Medium
Defended by NY Convention
Click-through acceptance
6 — Independent recreation
High
Defended by prior art record
Technical fingerprinting
Recommended Next Phase
Phase 1 — Immediate (before first commercial outreach)
US copyright registration of the Architecture
Click-through acceptance mechanism for repository access
Phase 2 — Short term (within 3 months)
Technical instantiation layer: documented reference implementations establishing
structural equivalence baseline
Evidence framework: design choices and structural markers that are non-obvious
and verifiable as CAS-derived
Phase 3 — Medium term (with first commercial licensee)
Active monitoring: automated detection of CAS structural patterns in publicly
available AI system architectures
Audit trail: documented record of all entities known to have accessed CAS materials
Field
Detail
Document
CAS Adversarial Test Report v1.0
Version
1.0
Date
2026-04-16
Prepared by
ChatGPT (OpenAI) — US regional contributor
Reviewed by
Claude (Anthropic) — drafting coordinator
Steward
Ryan Gelsi
Base License
CAS License v2.0
Status
Advisory — subject to steward review and approval
