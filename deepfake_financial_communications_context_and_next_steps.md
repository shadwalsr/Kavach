# Amazon AI Cyber Security Hackathon — Track 03
## Deepfake Detection for Financial Communications
### Research Context, Current Position, Gaps, and What To Do Next

> **Purpose of this file**
>
> This is the working handoff document for continuing the project from the current research stage into the actual Round 1 submission and prototype definition.
>
> It consolidates the available project context, the research themes already covered, the official Round 1 requirements, the major technical conclusions, the gaps that still need to be resolved, and the recommended execution sequence from **Problem Statement 3 research → product definition → architecture → validation → pitch deck → 48-hour MVP plan**.
>
> This document is a synthesis/working plan. It is **not a replacement for the full research files**. The underlying research remains the source of detailed papers, incidents, vendors, benchmarks, references, and technical annexes.

---

# 1. PROJECT CONTEXT

## 1.1 Competition

**Amazon AI Cyber Security Hackathon — Round 1**

Goal stated in the participant brief:

> Build the pitch deck and architecture for a final product that makes India’s digital financial ecosystem safer from AI-enabled threats.

The selected track is:

## Track 03 — Deepfake Detection for Financial Communications

The official problem statement asks teams to:

> Help people and institutions verify financial communications, detect manipulation, and create an actionable path for review, reporting, or response.

The key implication is important:

**The project should not be presented as “just a deepfake classifier.”**

The research already points toward a broader architecture:

**financial communication verification + media forensics + provenance + identity + authorization + contextual risk + human review + evidence preservation**

That framing should become the central product thesis.

---

# 2. CURRENT PROJECT POSITION

The current project has completed a broad research phase and has covered material up to the third problem-statement/track context.

The research is currently strongest on:

- Deepfake threat taxonomy
- Financial attack chains
- India/global examples
- Audio/video/image/document detection
- Multimodal detection
- C2PA and content provenance
- Watermarking
- Document forensics
- Identity versus authorization
- Contextual financial risk
- Research papers and benchmark datasets
- Competitor/vendor landscape
- Research gaps
- Adversarial limitations
- Regulatory/evidentiary considerations
- Zero-trust architecture
- Evidence vault / forensic preservation
- Enterprise integration concepts
- Market/adoption research
- Future technology roadmap

The project is therefore **not research-poor**.

The main problem now is the opposite:

> **There is too much breadth and not yet enough product focus.**

The project must now shift from:

**“Here is everything we know about deepfakes in finance.”**

to:

**“Here is one specific financial communication problem, here is the user, here is our product, here is exactly how it verifies the communication, here is what happens when the evidence is weak, and here is what we can actually build and demonstrate.”**

---

# 3. SOURCE MATERIAL AVAILABLE

The current working corpus includes:

1. `final_deepfake_content.md`
   - Main large research monograph
   - Expanded literature review
   - Incident research
   - technical annexes
   - competitor/market research
   - architecture
   - datasets
   - regulations/evidentiary discussion
   - research gaps
   - future roadmap
   - bibliography/reference material

2. `main deepfake finance research.md`
   - More compact research version
   - Detection technologies
   - API/SDK landscape
   - datasets
   - financial deployments
   - competitor matrix
   - research gaps
   - unresolved technical problems
   - zero-trust/financial verification architecture

3. `Deepfake_Content.md`
   - Earlier/condensed research synthesis
   - verification/evidence rules
   - attack-chain framing
   - 14 fundamental verification questions
   - coverage targets
   - systematic literature-review requirements
   - evidence hierarchy
   - source verification rules

4. `6ab571dd46c0a_round-1-participant-brief.pdf`
   - Official Amazon AI Cyber Security Hackathon Round 1 participant brief
   - Submission structure
   - Evaluation rubric
   - track definitions
   - safety requirements
   - deck/architecture limits
   - final submission checklist

---

# 4. OFFICIAL ROUND 1 REQUIREMENTS

## 4.1 Submission format

One PDF containing:

### A. Pitch deck
- Maximum **10 slides**
- Optional appendix is allowed

### B. Architectural overview
- Maximum **3 pages/slides**

Reviewers score the submitted PDF itself; the idea must be understandable without a live presentation or external link.

---

## 4.2 Pitch deck must cover

1. Team, selected challenge statement, one-sentence solution
2. User, threat scenario, and harm
3. Current journey, product flow, and differentiation
4. Core detection / decision-making approach
5. Data, evidence, validation plan, and key assumptions
6. Privacy, security, safety, and misuse safeguards
7. Deployment pathway and 48-hour prototype plan

---

## 4.3 Architecture must cover

- One legible end-to-end system diagram
- Inputs and data sources
- Consent and provenance
- Components/models/rules
- Storage
- Interfaces
- Outputs
- Detection/decision flow
- Alerts
- Escalation
- Human review
- Notifications
- Reporting
- Evidence path
- Security/privacy mitigations
- Adversarial-risk mitigations
- Performance assumptions
- Validation approach

---

## 4.4 Data restrictions

Use only:

- synthetic data
- public data
- consented data
- properly authorized data

Do **not** include confidential bank, customer, or platform data.

Disclose:

- AI-generated content
- datasets
- models
- third-party assets

in an appendix or slide note.

---

# 5. OFFICIAL EVALUATION RUBRIC

| Criterion | Weight | What must be demonstrated |
|---|---:|---|
| Problem fit and user understanding | 20 | Specific India-relevant threat, clear primary user, credible journey, sharply bounded problem |
| Technical architecture and detection logic | 20 | Legible end-to-end design, defensible verification/detection logic, clear inputs/outputs, realistic boundaries |
| Solution value and differentiation | 15 | Clear before/after workflow and meaningful user value beyond a generic AI detector |
| Feasibility and finale execution plan | 15 | Narrow demonstrable MVP, assumptions/dependencies, proof of progress in 48 hours |
| Safety, privacy, and responsible AI | 15 | Safeguards, escalation path, false-positive/bias/misuse/adversarial considerations |
| Adoption, integration, and scale | 10 | Practical integration path, operating owner, rollout sequence, latency/operational friction |
| Communication quality | 5 | Clear, concise, legible submission and architecture |

### Strategic consequence

The research already supports many of these categories.

The biggest scoring risk is no longer “insufficient technical research.”

The biggest scoring risks are:

- scope too broad
- unclear primary user
- no crisp product flow
- unclear final decision logic
- weak action/escalation definition
- no convincing 48-hour MVP
- insufficient concrete validation plan
- differentiation not stated simply enough
- architecture too ambitious for prototype reality

---

# 6. CENTRAL RESEARCH CONCLUSION

The strongest cross-cutting conclusion from the research is:

> **A deepfake detector alone cannot establish whether a financial communication is legitimate or whether a resulting financial action is authorized.**

A media detector can estimate synthetic/manipulated-media likelihood.

It does **not** by itself answer:

1. Is this actually the claimed person?
2. Is the media genuine?
3. Was the media AI-generated?
4. Was provenance stripped?
5. Was the media recaptured through the analog hole?
6. Is the communication consistent with trusted financial records?
7. Is the sender authorized to issue the instruction?
8. Is the communication channel legitimate?
9. Is the message context part of a social-engineering workflow?
10. Has the communication been altered after creation?
11. Can the system explain the anomaly?
12. Can evidence be preserved for audit/investigation?
13. Can the system avoid creating a biometric honeypot?
14. Can verification operate with acceptable friction and latency?

Therefore:

## Product thesis

**Verify the communication and the requested action, not merely the face/voice.**

This should become the core narrative.

---

# 7. THREAT MODEL ALREADY DEVELOPED

The research contains a **9-stage financial deepfake attack chain**.

## Stage 1 — Reconnaissance
Attackers collect:

- executive audio/video
- corporate hierarchy
- treasury approval chains
- assistants and workflows
- normal communication patterns

### Detection opportunity
Communication/channel anomalies, identity graph inconsistencies, unusual collection/signals.

---

## Stage 2 — Identity acquisition

Attackers obtain:

- voice samples
- facial references
- signatures
- corporate templates
- contextual language

### Detection opportunity
Identity provenance, protected reference material, suspicious reuse of public media.

---

## Stage 3 — Synthetic generation

Potential manipulation:

- voice cloning
- voice conversion
- facial reenactment
- lip-sync
- synthetic avatars
- AI-generated documents
- LLM-crafted scripts

### Detection opportunity
Audio/video/document/text forensics and cross-modal consistency.

---

## Stage 4 — Channel injection

Possible delivery channels:

- virtual cameras
- WebRTC injection
- SIP/RTP routing
- compromised messaging accounts
- synthetic PDFs/images
- direct messaging

### Detection opportunity
Channel integrity, endpoint/device signals, provenance, account consistency, transport/context metadata.

---

## Stage 5 — Social engineering

Typical lures include:

- urgent transfer
- acquisition
- regulatory demand
- account recovery
- payroll
- legal threat
- executive emergency

### Detection opportunity
Semantic/contextual anomaly analysis and workflow-risk analysis.

---

## Stage 6 — Live interaction / session hijacking

Attackers may create:

- real-time synthetic avatars
- conversational synthetic audio
- mid-session media injection

### Detection opportunity
Continuous, not one-time, verification.

---

## Stage 7 — Financial action

Potential impact:

- wire transfer
- UPI transfer
- account takeover
- credential capture
- portfolio liquidation
- trading reaction

### Detection opportunity
Authorization and transaction-risk controls.

---

## Stage 8 — Rapid monetization

Potential movement through:

- instant-payment rails
- mule accounts
- crypto conversion
- cross-border movement

### Detection opportunity
Fraud-risk engines, beneficiary risk, transaction anomalies.

---

## Stage 9 — Forensic evasion

Attackers may:

- delete logs
- strip metadata
- recompress media
- re-record screens
- move to less-monitored channels

### Detection opportunity
Hashing, provenance checks, screen-recapture detection, immutable evidence capture, multi-signal fallback.

---

# 8. RESEARCH COVERAGE ALREADY ACHIEVED

## 8.1 Media modalities

Research covers:

- video
- audio
- images
- documents
- text
- multimodal combinations

The key finding:

> **No single modality is sufficient across the full attack surface.**

---

# 9. VISUAL DEEPFAKE RESEARCH

The research covers several major lines of visual forensics.

## Spatial / visual artifacts

Examples:

- blending boundaries
- upsampling artifacts
- facial edge inconsistencies
- illumination/color mismatches

Representative research:

- Face X-Ray
- related face-forgery localization approaches

### Strength
Useful for certain face-swap/manipulation families.

### Weakness
Can degrade heavily under compression and is less useful against full-frame synthetic/diffusion content where blending boundaries may not exist.

---

## Frequency-domain forensics

Representative research:

- F3-Net

Idea:

- extract high-frequency/frequency-domain traces associated with synthetic generation

### Strength
Strong benchmark performance on suitable data.

### Weakness
Compression and channel transformations can destroy high-frequency clues.

### Financial lesson
A detector trained on pristine media cannot automatically be trusted on WhatsApp/social-media/telephony-reencoded content.

---

## Temporal/semantic visual analysis

Representative research:

- LipForensics

Uses semantic temporal mouth/face dynamics rather than only low-level pixels.

### Strength
More robust to certain resolution/compression changes.

### Weakness
Can fail as generation technology becomes more physically/semantically accurate.

---

## Self-supervised/generalization approaches

Representative research:

- SBI (Self-Blended Images)

Idea:

- generate diverse self-blended training examples rather than rely entirely on fixed fake datasets

### Strength
Improves generalization to some unseen manipulations.

### Weakness
Does not solve all modern foundation-model/deep-synthesis cases.

---

# 10. AUDIO DEEPFAKE RESEARCH

## Classical anti-spoofing

Representative approach:

- LFCC + LCNN

Looks at:

- spectral characteristics
- phase/magnitude patterns
- vocoder artifacts

### Weakness
Can degrade substantially under telephony/channel compression and unseen generation methods.

---

## End-to-end raw waveform approaches

Representative:

- RawNet2

Motivation:

- learn representations directly from waveform

### Lesson
Useful for flexible audio anti-spoofing but still subject to channel and distribution shift.

---

## Graph/spectro-temporal approaches

Representative:

- AASIST

Uses spectro-temporal representations and graph attention.

### Lesson
Strong academic benchmark performance does not guarantee comparable real-world performance under VoIP/telephony/noise conditions.

---

## Newer/self-supervised audio direction

Research references modern foundation/self-supervised representations such as:

- WavLM
- wav2vec 2.0
- newer spoofing systems and challenge results

### Core financial lesson

The audio signal must be evaluated in its **real communication channel**, not only in clean benchmark conditions.

---

# 11. IMAGE / DIFFUSION RESEARCH

Research covers diffusion-era generation and forensic approaches such as:

- DIRE
- De-Diffusion
- diffusion-related forensic methods

### Strategic lesson

Older artifact assumptions are becoming weaker.

Therefore the system should not rely on a single fixed “fake signature.”

The architecture should be:

- ensemble-based
- open-set aware
- updateable
- provenance-aware
- context-aware

---

# 12. MULTIMODAL RESEARCH

The research contains multimodal directions covering:

- audio
- video
- text
- synchronization
- phoneme/viseme alignment
- cross-modal inconsistencies

### Why this matters

An attacker may generate each modality separately but still fail to keep them perfectly synchronized or contextually consistent.

Potential signals:

- lip movement vs speech timing
- wording vs known communication style
- visual timing vs audio timing
- document wording vs metadata
- stated identity vs channel/account identity

### Product implication

The system should combine several weak/medium signals instead of relying on one “magic” detector.

---

# 13. DOCUMENT FORENSICS

The research explicitly includes document-level checks.

Potential signals include:

- PDF structural anomalies
- incremental updates
- font subsets
- object-stream inconsistencies
- OCR/visual mismatch
- metadata inconsistencies
- suspicious signing/provenance
- layout/template anomalies

A simple example explored in the research is checking for multiple `%%EOF` markers as one possible clue for incremental revisions.

### Important caveat

A structural anomaly is **evidence of suspicion**, not definitive proof of fraud.

This distinction must remain visible in the product.

---

# 14. PROVENANCE AND CONTENT AUTHENTICITY

## C2PA / Content Credentials

The research treats C2PA as a useful provenance mechanism.

Potential uses:

- verify signed content
- establish creator/source chain
- inspect content history
- connect content to a trusted signer/certificate

### Critical limitation

**Presence of provenance is useful evidence.**

**Absence of provenance is not proof of forgery.**

**Valid provenance does not prove that the underlying financial claim is truthful.**

Therefore:

> provenance = authenticity signal, not truth guarantee.

---

# 15. WATERMARKING

The research also covers invisible watermarking.

Potential use:

- authorized institutions publish signed/watermarked media
- later systems verify whether the artifact carries expected authenticity material

Potential technologies discussed include:

- vendor/industry watermarking
- latent/invisible watermark techniques
- content authenticity systems

### Limitations

Must be tested against:

- compression
- cropping
- filtering
- screen recapture
- re-encoding

### Product implication

Watermarking is best treated as a **high-value authenticity signal**, not as the only defense.

---

# 16. IDENTITY VS AUTHORIZATION

This is one of the most important conceptual findings.

## Problem

Even if the communication really comes from the executive:

- the executive may not be authorized to approve the transaction
- the message may attempt to bypass segregation-of-duties
- the requested beneficiary may be new
- the amount may exceed expected authority
- an emergency claim may conflict with corporate policy

Therefore:

> **Authenticating a person is not equivalent to authenticating the financial action.**

This distinction is an excellent differentiator for the proposed product.

---

# 17. ZERO-TRUST ARCHITECTURE RESEARCH

The research contains a reference architecture similar to:

```text
Trusted Capture
      ↓
Hardware / Device Attestation
      ↓
C2PA / Content Credentials
      ↓
Encrypted Transport
      ↓
Continuous Session Verification
      ↓
Multimodal Forensics
(video / audio / image / document / text)
      ↓
Identity Verification
      ↓
Authorization Verification
      ↓
Contextual Financial Risk Engine
      ↓
Decision Engine
      ↓
Human Review / Step-Up / Hold / Allow
      ↓
Immutable Evidence Vault
```

This is a strong target architecture.

However:

## It is too broad for a 48-hour prototype if implemented literally.

The Round 1 submission can present the broader target architecture while the 48-hour MVP implements only a narrow subset.

---

# 18. FINANCIAL CONTEXT SIGNALS

The research supports using contextual risk signals such as:

- beneficiary risk
- transaction amount
- abnormality relative to user/entity history
- device reputation
- geography
- communication pattern
- authorization-chain mismatch
- unusual timing
- unexpected channel
- request urgency
- mismatch with trusted financial records

### Core principle

A media-verification alert becomes much more valuable when it is connected to the **financial consequence**.

Example:

> “Synthetic-media suspicion detected” is weaker than:

> “Synthetic-media suspicion + new beneficiary + unusual amount + bypass of normal approval path.”

The latter produces an actionable risk signal.

---

# 19. RESEARCH LIMITATIONS / UNSOLVED PROBLEMS

The research identifies multiple unresolved areas.

A few especially relevant to the final product:

## 19.1 Open-set generalization

Detectors can perform extremely well on known benchmarks but degrade when faced with unseen generation techniques.

### Product response
Use multiple detectors and do not claim certainty beyond validation.

---

## 19.2 Analog hole / screen recapture

Screen capture and re-recording can:

- remove metadata
- distort frequency traces
- weaken forensic artifacts

### Product response
Add screen-recapture/channel-aware analysis and treat provenance failure as a reason to fall back to forensic/context signals.

---

## 19.3 Compression robustness

Financial communications may pass through:

- WhatsApp
- social platforms
- telephony
- video conferencing codecs
- screenshots
- resaving/re-encoding

### Product response
Validate under realistic transformations.

---

## 19.4 Cross-lingual and Hinglish performance

English-centric datasets/models can fail to represent Indian communication realities.

### Product response
Evaluate Indian-language and Hinglish cases wherever the chosen model supports them, and explicitly state this as a limitation if the MVP cannot cover it.

---

## 19.5 Real-time latency

Multimodal models can be expensive.

### Product response
Use tiered verification:

**cheap first-pass → deeper asynchronous analysis only when needed**

---

## 19.6 Biometric privacy

Raw face and voice data create privacy/security risks.

### Product response
- minimize storage
- process only required windows
- hash/store evidence references where practical
- encrypt sensitive artifacts
- strict access control
- defined retention
- consent/authorization boundaries

---

# 20. REPRESENTATIVE RESEARCH PAPERS ALREADY COVERED

The research corpus includes, among others:

### Visual/video

- MesoNet
- Head Pose inconsistency approaches
- F3-Net
- LipForensics
- Face X-Ray
- SBI / Self-Blended Images

### Audio

- LFCC-LCNN / ASVspoof baselines
- RawNet2
- AASIST
- SpecXNet
- newer self-supervised anti-spoofing directions

### Diffusion/image

- DIRE
- De-Diffusion
- related diffusion-generation detection research

### Multimodal

- multimodal A/V/text approaches
- audiovisual synchronization
- cross-modal consistency
- modern multimodal deepfake surveys

### Benchmarks / datasets

- FaceForensics++
- Celeb-DF
- ASVspoof
- ASVspoof 5
- DeepMoiréFake (screen recapture focus)
- AV-Deepfake1M++
- other research datasets discussed in the corpus
- India-focused speech/multimodal data references where available

### Important research-management rule

The research corpus itself explicitly recommends:

- verify titles
- verify authors
- verify venue
- verify DOI
- verify reported metrics
- verify patents/statuses
- separate vendor claims from independent evidence
- separate confirmed incidents from disputed/reported incidents
- distinguish benchmark performance from real-world performance
- mark evidence status
- record last-verified dates for fast-changing claims

Do not copy every metric from the monograph into the deck without checking its evidence status.

---

# 21. RESEARCH DATASETS — WHAT THEY TELL US

The research has repeatedly surfaced the same problem:

> Laboratory benchmark performance can overestimate real-world financial communication performance.

Important perturbations to simulate:

- compression
- telephony
- VoIP
- screen recapture
- cropping
- resizing
- noise
- recompression
- cross-generator / zero-shot cases
- multilingual/accent conditions
- asynchronous media
- mixed real/fake modalities

### Key evaluation principle

A detector should be tested on:

**clean + transformed + adversarial + unseen-generator + channel-realistic samples.**

---

# 22. COMPETITOR / MARKET RESEARCH ALREADY COVERED

The research includes commercial tools/providers across categories such as:

- deepfake detection APIs
- identity verification / liveness platforms
- audio anti-spoofing
- fraud orchestration
- enterprise media verification
- provenance/content credentials
- browser/OSINT investigation
- document forensics
- forensic suites
- enterprise SIEM/SOC integration

Representative technologies/providers discussed include examples such as:

- Resemble Detect
- Reality Defender
- Sumsub
- Pindrop
- C2PA tooling
- enterprise fraud/case-management integrations

### What the competitor research should NOT become

Do not put a giant 20–30 column matrix into the main deck.

Use the large matrix as supporting research.

For the deck, reduce it to **4–6 strategically relevant capabilities**.

---

# 23. WHAT THE DIFFERENTIATION SHOULD BE

Do **not** lead with:

> “Our model detects deepfakes better.”

That is difficult to defend in a short hackathon and invites benchmark comparison.

A stronger positioning is:

> **We connect media authenticity to financial authorization and actionable evidence.**

Possible differentiation dimensions:

| Capability | Generic deepfake detector | Proposed architecture |
|---|---|---|
| Media forensics | Yes | Yes |
| Provenance | Sometimes | Yes |
| Identity consistency | Partial | Yes |
| Authorization verification | Usually no | Yes |
| Financial context | Usually no | Yes |
| Explainable risk reasons | Limited | Core feature |
| Human escalation | Not always | Explicit |
| Evidence package | Often limited | Core feature |
| Cross-modal verification | Variable | Core |
| Safe response workflow | Often outside scope | Built into product |

---

# 24. THE MAIN PRODUCT GAP RIGHT NOW

## The research describes an architecture.

## The submission needs a product.

That product needs an explicit loop:

```text
INPUT
  ↓
VERIFY SOURCE / PROVENANCE
  ↓
ANALYZE MEDIA / DOCUMENT
  ↓
CHECK IDENTITY & CHANNEL
  ↓
CHECK FINANCIAL CONTEXT / AUTHORIZATION
  ↓
FUSE SIGNALS
  ↓
RISK DECISION
  ↓
ACTION
  ↓
EVIDENCE RECORD
```

The system should answer:

> **What does the user actually do with the result?**

That answer is currently not sharp enough.

---

# 25. RECOMMENDED PRODUCT DEFINITION

A strong initial product definition is:

## Primary user

**Bank / fintech fraud-risk analyst or financial security analyst**

Why start here?

- Clear business owner
- High-value financial decisions
- Easier human-in-the-loop design
- Easier evidence/escalation model
- Fits enterprise deployment
- Avoids trying to solve every consumer communication problem at once

---

## Communication under inspection

A suspicious financial communication containing one or more of:

- audio
- video
- image
- document

Example:

- executive transfer request
- payment approval
- beneficiary-change request
- urgent treasury instruction
- suspicious financial PDF/voice/video

---

## Harm

Potential harms include:

- unauthorized transfer
- account takeover
- fraudulent payment approval
- exposure of sensitive financial information
- market reaction / reputational impact
- circumvention of approval workflow

---

## Product output

Do NOT output only:

> “Fake — 94%”

Instead produce:

### Verification result

- **LOW RISK**
- **SUSPICIOUS**
- **HIGH RISK**
- **CRITICAL / HUMAN REVIEW**

with supporting reasons.

Example reasons:

- provenance unavailable
- suspicious audio characteristics
- lip-sync inconsistency
- document structural anomaly
- sender/channel inconsistency
- authorization mismatch
- unusual beneficiary
- unusual transaction context
- urgency/social-engineering indicators

---

# 26. RECOMMENDED USER JOURNEY

## Before

A financial employee receives an urgent communication.

Current behavior may be:

1. recognize sender/voice
2. trust communication
3. respond immediately
4. execute or approve transaction
5. discover fraud later

---

## With proposed product

1. Communication is forwarded/uploaded/ingested.
2. Provenance is checked.
3. Media/document is analyzed.
4. Identity/channel signals are checked.
5. Financial-context checks run.
6. Signals are fused.
7. User receives an explanation-oriented result.
8. High-risk cases trigger step-up or human review.
9. Evidence is preserved.
10. Analyst can report/escalate through the case workflow.

This should be shown visually in the deck.

---

# 27. RECOMMENDED DETECTION PIPELINE FOR THE MVP

The MVP should implement **only the pieces that can realistically be demonstrated.**

## Layer 1 — Input normalization

Accept:

- video
- audio
- image/PDF

Optional text extraction:

- OCR
- transcript

Generate:

- file hash
- metadata
- basic media properties

---

## Layer 2 — Provenance

Check:

- C2PA/content credentials if present
- metadata consistency
- signature/provenance status

Output:

```text
PROVENANCE_STATUS
= VALID / MISSING / INVALID / UNKNOWN
```

---

## Layer 3 — Media forensics

### Audio
Use one available anti-spoofing route.

Possible model family:

- pretrained audio deepfake / anti-spoofing model
- SSL-based audio representation
- AASIST-style baseline if implementation time permits

### Video
Use one practical video/deepfake model.

Possible families:

- frame-based deepfake classifier
- temporal model
- lip-sync/semantic consistency model

### Image
Use a practical image/deepfake classifier.

### Document
Use:

- metadata/structure checks
- OCR consistency
- visual/layout anomaly checks
- suspicious incremental revisions

---

## Layer 4 — Cross-modal checks

Examples:

- speech vs lip movement
- transcript vs stated action
- media identity vs claimed sender
- document sender vs email/message metadata

Not every check needs to be AI-based.

Rules are acceptable and useful.

---

## Layer 5 — Contextual financial risk

For MVP, simulate safe/public/synthetic fields:

- amount
- beneficiary novelty
- urgency
- authorization-chain match
- channel
- device/session trust
- historical baseline

Do not use real confidential customer data.

---

## Layer 6 — Risk fusion

A conceptual model:

```text
Final Risk
  =
  media-forensics evidence
  +
  provenance evidence
  +
  identity/channel consistency
  +
  authorization consistency
  +
  financial-context risk
  +
  communication/social-engineering anomalies
```

### Important

Do not invent arbitrary production weights and present them as scientifically validated.

For the submission:

- define the factors
- use transparent scoring in the prototype
- state that weights/thresholds will be calibrated against the validation set

---

# 28. RECOMMENDED DECISION LOGIC

A safe decision policy:

```text
LOW RISK
→ allow / continue normal workflow

MODERATE / SUSPICIOUS
→ step-up verification
→ trusted-channel confirmation

HIGH RISK
→ analyst review
→ do not rely on detector score alone

CRITICAL
→ hold or pause high-impact action
→ require authorized human confirmation
```

The system should avoid:

- automatic accusations
- irreversible blocking based on one weak signal
- “fake” labels without explanation
- silent decisions with no evidence trail

---

# 29. HUMAN-IN-THE-LOOP IS NOT OPTIONAL

The official brief emphasizes safe escalation.

The proposed product should explicitly define:

## Who acts?

**Primary actor:** fraud/security analyst

## What can they do?

- review evidence
- request out-of-band verification
- escalate to authorized business owner
- report the communication
- preserve evidence
- recommend/authorize action according to existing bank controls

## What the detector cannot do alone

It should not independently:

- accuse the sender
- terminate an account
- freeze a customer permanently
- authorize a financial transaction

The exact high-impact controls should remain under authorized human/enterprise policy.

---

# 30. EXPLAINABILITY / EVIDENCE UX

This is one of the strongest potential differentiators.

Do not show only:

> Deepfake probability = 0.91

Instead show:

### Verification Summary

**Status: HIGH RISK**

### Why

- C2PA provenance: missing
- Audio anti-spoofing: elevated anomaly
- Face/lip temporal consistency: mismatch
- Sender/channel: inconsistent with trusted profile
- Financial action: unusual amount
- Beneficiary: new
- Authorization chain: mismatch

### Recommended action

**Request out-of-band confirmation before payment approval.**

---

# 31. EVIDENCE VAULT / CASE RECORD

Every suspicious case can generate a structured evidence record:

```text
Case ID
Original file hash
Capture / ingestion timestamp
Source/channel metadata
Provenance result
Detector results
Model versions
Rules triggered
Extracted frames/audio/transcript references
Risk decision
Reviewer actions
Final disposition
```

### Why this matters

The evidence path:

- supports human investigation
- supports auditability
- preserves reproducibility
- allows later incident review
- reduces “black box detector” criticism

Again:

**Evidence ≠ proof of fraud.**

It is evidence supporting a risk decision.

---

# 32. PRIVACY / SECURITY DESIGN

The architecture should visibly answer:

## What data is needed?

Only data required to verify the communication.

## Why is each input needed?

Map each input to a specific decision signal.

## What is not collected?

Do not collect unrelated messages, unnecessary biometric histories, or confidential data.

## Where does processing happen?

Prefer:

- secure processing boundary
- minimal transfer
- encrypted transport
- strict access control

## How long is raw evidence retained?

Define a policy.

For the prototype:

- short-lived local processing where possible
- explicit case export only when needed

## Who sees evidence?

Only authenticated/authorized reviewers.

## Evidence security

Use:

- encryption
- immutable or append-only storage model where feasible
- access logging
- case-based authorization

---

# 33. ADVERSARIAL / MISUSE MITIGATIONS

The submission must show awareness that attackers will adapt.

Threats include:

- generator evolution
- adversarial perturbations
- recompression
- screen recapture
- metadata stripping
- model-specific evasion
- replay attacks
- unauthorized access to evidence
- abuse of verification outputs

Possible mitigations:

- ensemble detection
- fallback signals
- open-set monitoring
- provenance + forensic combination
- continuous verification for live sessions
- rate limiting
- evidence access control
- model/version tracking
- uncertainty-aware decisions
- periodic recalibration

---

# 34. VALIDATION PLAN — CURRENTLY MISSING AS A CONCRETE EXPERIMENT

This is one of the most important next steps.

## Build a small controlled evaluation set

Example prototype set:

- genuine communications
- AI-generated media
- manipulated media
- recompressed media
- screen-recorded media
- provenance-stripped media
- mixed-modality cases

A simple starting design could be around:

- 20 genuine
- 20 AI-generated
- 20 manipulated
- 10 recompressed
- 10 screen-recorded
- 10 provenance-stripped

= **90 test cases**

This is a suggested prototype design, not a benchmark claim.

Add Indian-language / Hinglish cases where practical.

---

# 35. VALIDATION METRICS

Report:

- precision
- recall
- F1
- false-positive rate
- false-negative rate
- confusion matrix
- latency
- throughput

Also measure robustness under:

- compression
- resizing
- noise
- screen recapture
- metadata stripping
- unseen generation family

For a hackathon, even a small but honest evaluation is stronger than quoting benchmark results without testing the actual pipeline.

---

# 36. KEY ASSUMPTIONS TO STATE

The submission should explicitly identify assumptions.

Examples:

1. Input communication is accessible to the verification service.
2. Trusted identity references are available through an authorized source.
3. Financial-context fields are available only in a controlled enterprise integration.
4. High-impact actions remain subject to existing bank controls.
5. The detector is advisory/risk-scoring, not a standalone truth oracle.
6. Benchmark accuracy does not equal production accuracy.
7. The MVP prioritizes explainability and workflow safety over broad modality coverage.
8. Public/synthetic/authorized data is sufficient for the prototype demonstration.

---

# 37. INTEGRATION PATH

The strongest enterprise positioning is not:

> “Replace the bank fraud engine.”

Instead:

> **Add a communication-verification risk layer before high-impact financial actions.**

Example:

```text
WhatsApp / Email / Teams / Video / Document
                    ↓
          Verification Gateway
                    ↓
       Deepfake + Provenance Engine
                    ↓
       Identity / Authorization Layer
                    ↓
        Financial Risk Engine
                    ↓
      Existing Bank Fraud Platform
                    ↓
   Analyst Queue / Step-Up / Action
```

### Integration interfaces

Potential interfaces:

- REST API
- SDK
- analyst dashboard
- event/webhook
- SIEM/case-management connector
- browser/desktop capture or upload interface

For the MVP, a simple web dashboard + API is enough.

---

# 38. ADOPTION / OPERATING OWNER

Possible initial buyers/users:

### Primary

- bank fraud-risk teams
- financial security teams
- fintech trust & safety teams

### Secondary

- treasury security
- enterprise SOCs
- brokerages / market-integrity teams
- compliance/investigation teams

### Operating owner

Best initial owner:

**Fraud / Financial Crime / Security Operations**

---

# 39. DEPLOYMENT MODEL

Possible product forms:

### API
Other systems submit media and receive structured verification.

### Analyst dashboard
Human reviewers see evidence and recommended next steps.

### Enterprise gateway
Interposes before selected high-risk actions or communication workflows.

### Future
- browser extension
- mobile SDK
- meeting plug-in
- communications gateway
- signed-content infrastructure

For the 48-hour prototype:

**Web app + API + synthetic sample dataset** is the most realistic.

---

# 40. RECOMMENDED MVP SCOPE

## MVP should prove four things

### 1. Can we ingest the communication?

Input:

- video/audio/image/PDF

### 2. Can we generate multiple verification signals?

Examples:

- provenance
- media forensic score
- document anomaly
- cross-modal check

### 3. Can we fuse those signals into an actionable risk level?

Output:

- low
- suspicious
- high/critical

### 4. Can we show what the analyst should do next?

Example:

> “Do not rely on this communication for payment authorization. Perform trusted-channel verification.”

and preserve the evidence record.

---

# 41. WHAT NOT TO BUILD IN 48 HOURS

Avoid attempting:

- a new foundation model from scratch
- full bank-core integration
- production-grade real-time Zoom interception
- universal multilingual coverage
- all possible media modalities at research depth
- hardware attestation infrastructure
- complete cryptographic payment authorization
- a full compliance platform
- perfect real-world detector accuracy

Those can remain **future architecture / roadmap** elements.

---

# 42. PROPOSED 48-HOUR BUILD PLAN

## Hour 0–6 — Foundation

Deliver:

- repo/environment
- project skeleton
- dataset/sample cases
- ingestion UI
- case schema
- hashing

---

## Hour 6–16 — Verification engines

Implement selected:

- provenance check
- audio detector OR video detector as primary modality
- document/metadata forensics
- optional cross-modal check

Do not chase too many models.

---

## Hour 16–24 — Risk fusion

Implement:

- signal normalization
- transparent risk score
- thresholds
- reason codes
- decision levels

Example:

```text
LOW
SUSPICIOUS
HIGH
CRITICAL
```

---

## Hour 24–32 — Analyst workflow

Implement dashboard showing:

- submitted communication
- detected modality
- scores
- evidence reasons
- provenance
- risk decision
- recommended next action
- case ID

---

## Hour 32–40 — Safety / adversarial tests

Test:

- clean real media
- generated media
- recompressed media
- screen capture
- metadata stripping
- false positives

---

## Hour 40–48 — Integration + demo

Finalize:

- end-to-end demo
- evaluation chart
- architecture diagram
- screenshots
- deployment narrative
- known limitations
- appendix disclosures
- final PDF

---

# 43. WHAT THE 10-SLIDE PITCH DECK SHOULD PROBABLY LOOK LIKE

## Slide 1 — Problem + Solution

- Track 03
- team
- one-sentence product
- one-line value proposition

Suggested headline:

> **Verify the financial communication before it becomes a financial loss.**

---

## Slide 2 — Threat Scenario

Show one concrete scenario:

**CEO / finance executive → deepfake communication → urgent payment request → unauthorized transfer**

Include:

- user
- harmful moment
- attacker
- consequence

---

## Slide 3 — Existing Journey vs New Journey

### Today

Receive → Trust → Act → Discover fraud

### Proposed

Receive → Verify → Explain → Step-up/review → Act safely → Preserve evidence

---

## Slide 4 — Product Flow

Visual pipeline:

```text
Input
→ Provenance
→ Media Forensics
→ Identity/Channel
→ Financial Context
→ Risk Fusion
→ Action
→ Evidence
```

---

## Slide 5 — Detection / Decision Engine

Explain the actual signals.

Avoid equations that cannot be defended.

Focus on:

- multimodal evidence
- provenance
- context
- authorization
- uncertainty

---

## Slide 6 — Example Analyst Output

Mock UI.

Show:

- risk level
- evidence reasons
- action recommendation
- case/evidence record

This can become the strongest slide.

---

## Slide 7 — Validation

Show:

- dataset composition
- test conditions
- metrics
- target thresholds
- robustness tests

---

## Slide 8 — Privacy / Safety / Misuse

Show:

- minimum necessary data
- encryption
- access control
- retention
- no automatic accusation
- human review
- adversarial resilience

---

## Slide 9 — Integration / Adoption

Show:

- bank/fraud engine
- verification gateway
- analyst workflow
- API
- deployment sequence

---

## Slide 10 — 48-Hour MVP + Roadmap

Left:

**What we can build in 48h**

Right:

**Production pathway**

This makes feasibility explicit.

---

# 44. ARCHITECTURAL OVERVIEW — 3 PAGE/SLIDE PLAN

## Architecture Page 1 — End-to-End System

Large central diagram:

```text
Communication Sources
(email / messaging / video / document)
             ↓
         Ingestion
             ↓
   Provenance / Metadata
             ↓
    Multimodal Forensics
             ↓
 Identity + Channel Checks
             ↓
 Authorization + Context
             ↓
       Risk Fusion
             ↓
 Allow / Step-Up / Review / Hold
             ↓
       Evidence Vault
```

---

## Architecture Page 2 — Components + Data Boundaries

Show:

- APIs
- model layer
- rules
- storage
- model registry/versioning
- secure processing boundary
- identity references
- financial-context interface
- analyst interface

Make data movement obvious.

---

## Architecture Page 3 — Safety + Operations

Show:

- human review
- evidence package
- alerts
- case management
- audit trail
- adversarial mitigation
- access controls
- latency strategy
- validation loop

---

# 45. THE MOST IMPORTANT RESEARCH-TO-PRODUCT BRIDGE

Create this table for the internal team and eventually compress it into the deck:

| Research finding | Product problem | Product response |
|---|---|---|
| Known-generator overfitting | Zero-day generators bypass detectors | Ensemble/open-set approach + uncertainty |
| Compression destroys artifacts | Messaging/telecom weakens signals | Channel-aware validation + multi-signal fallback |
| Provenance can disappear | Missing credentials cannot prove fraud | Use provenance when available; forensic fallback |
| Screen recapture erases metadata | Analog hole | Screen-recapture/channel checks |
| Genuine person ≠ authorized action | Identity alone is insufficient | Authorization/financial-context verification |
| Live injection can occur mid-session | One-time check can be bypassed | Continuous/session-aware verification |
| Detector score is not proof | Analysts need reasons | Explanation layer + evidence package |
| Centralized biometrics create risk | Sensitive data exposure | Data minimization + secure evidence handling |
| Multimodal models can be slow | Real-time friction | Tiered/async verification |
| Attackers adapt | Static detector becomes obsolete | Versioning, monitoring, update loop |

This table is the bridge from research to the final product narrative.

---

# 46. MAJOR GAPS THAT MUST BE CLOSED NEXT

## GAP 1 — Sharp problem statement

Current research is too broad.

Need one final sentence covering:

- primary user
- communication
- moment
- threat
- harm
- output

### Recommended starting frame

> **For Indian banks and fintechs, verify suspicious audio/video/document financial communications before high-impact actions by combining provenance, multimodal forensics, identity/channel checks, and financial authorization context, then route uncertain or high-risk cases to human review with an evidence package.**

This is a working formulation and should be refined with the team.

---

## GAP 2 — Final product name / product identity

The system needs a memorable name.

Do not spend excessive time on branding.

Priority is product clarity.

---

## GAP 3 — Exact MVP modality

Choose the modality that will be strongest and most demonstrable.

Recommended:

**Primary: video + audio**

Secondary:

**document/provenance**

But if implementation resources are limited, build one strong end-to-end path instead of three weak ones.

---

## GAP 4 — Exact model/tool stack

Decide:

- which open-source model
- which API, if any
- compute required
- expected latency
- license
- installation complexity
- fallback if model fails

This is a major immediate task.

---

## GAP 5 — Risk score and thresholds

Need:

- factors
- normalization
- thresholds
- action mapping
- calibration plan

Do not claim the score is scientifically calibrated until validated.

---

## GAP 6 — User interface

Need at least one screen showing:

- result
- explanation
- evidence
- action

---

## GAP 7 — Validation set

Need actual cases and test transformations.

---

## GAP 8 — 48-hour plan

Need ownership and deliverables.

---

## GAP 9 — Integration details

Need one concrete insertion point in a bank/fintech workflow.

---

## GAP 10 — Differentiation

Reduce to one sentence:

> **Not just “is this media fake?” but “can this financial communication be trusted for this action, and what evidence should the reviewer see?”**

---

# 47. EVIDENCE / CLAIM MANAGEMENT

The research files explicitly propose an evidence hierarchy.

Use this standard:

## Highest confidence

1. Primary statutory/regulatory text
2. Peer-reviewed academic literature
3. Official government / standards / institutional documentation
4. Verified cybersecurity incident reporting
5. Vendor technical documentation
6. Reputable secondary reporting
7. Market-research estimates
8. Unverified / representative claims

---

## Claim status labels

Use:

- **Verified**
- **Independently corroborated**
- **Vendor-reported**
- **Reported but not independently verified**
- **Representative / illustrative**
- **Unsupported and excluded**

### Critical rule

Do not turn uncertain research into definitive pitch-deck claims.

Especially verify:

- exact benchmark metrics
- exact incident losses
- vendor capabilities
- current pricing
- patent claims
- regulatory interpretations
- market-size numbers
- recent deployments

---

# 48. WHAT SHOULD GO IN THE MAIN DECK VS APPENDIX

## Main deck

Only include what directly proves:

- problem
- user
- threat
- product
- detection logic
- differentiation
- evidence
- safety
- adoption
- feasibility

---

## Appendix

Move detailed research here:

- literature table
- model-by-model metrics
- large competitor matrix
- long incident timeline
- datasets
- regulatory detail
- patents
- source-quality audit
- technical benchmarks
- future architecture
- roadmap

The large research corpus is valuable.

The deck should **compress it**, not reproduce it.

---

# 49. STRATEGIC NARRATIVE FOR THE ENTIRE PROJECT

A clean narrative is:

## 1. Deepfakes are now a financial communication risk

AI can impersonate trusted people and produce convincing multimedia.

## 2. Financial decisions depend on context, not appearance alone

The key question is not merely:

> “Does this face/voice look real?”

It is:

> “Should this communication be trusted for this financial action?”

## 3. Existing detectors are narrow

They can fail under:

- unseen generators
- compression
- screen recapture
- telephony
- adversarial transformations

## 4. Therefore use layered verification

Combine:

- provenance
- forensic signals
- identity/channel signals
- authorization
- financial context

## 5. Do not over-automate high-impact decisions

Route uncertainty to people.

## 6. Preserve evidence

Every decision should be explainable and auditable.

## 7. Build the narrow version first

48-hour MVP:

**communication → verify → explain → escalate → evidence**

---

# 50. RECOMMENDED FINAL POSITIONING

A strong positioning statement to work from:

> **A financial communication verification gateway that combines deepfake forensics, content provenance, identity/channel checks, and transaction-context risk to detect suspicious communications before they trigger high-impact financial actions — with human escalation and an evidence trail instead of blind auto-blocking.**

This should be treated as the current working positioning, not a final locked marketing line.

---

# 51. TEAM WORK SPLIT FROM HERE

A practical 4-person split:

## Person 1 — Product / Pitch

Own:

- problem statement
- user journey
- story
- differentiation
- slides

## Person 2 — ML / Detection

Own:

- model selection
- inference
- modality pipeline
- evaluation

## Person 3 — Backend / Risk

Own:

- ingestion API
- provenance
- risk engine
- case/evidence schema
- integration

## Person 4 — Security / Validation / UX

Own:

- threat model
- privacy
- adversarial tests
- dashboard
- validation
- evidence presentation

If the team has fewer members, combine responsibilities.

---

# 52. EXACT NEXT TASK SEQUENCE

Do these in order.

## NEXT 1 — Lock the problem

Write one final bounded problem statement.

Must identify:

- user
- communication
- harmful moment
- attacker
- harm
- desired output

**Do not continue broad research before this is locked.**

---

## NEXT 2 — Lock the product

Define:

- input
- processing
- risk output
- action
- evidence

Produce one simple flow diagram.

---

## NEXT 3 — Lock MVP scope

Choose:

- primary modality
- one secondary modality/provenance
- exact model/tool stack
- expected prototype output

---

## NEXT 4 — Build the decision matrix

Example:

| Signal | Normal | Suspicious | High Risk |
|---|---|---|---|
| Provenance | valid | missing | invalid |
| Media forensics | low anomaly | elevated | high |
| Identity/channel | consistent | uncertain | inconsistent |
| Authorization | valid | unclear | mismatch |
| Financial context | normal | unusual | highly anomalous |

Then map to:

**allow / step-up / review / hold**

---

## NEXT 5 — Build validation dataset

Use:

- public
- synthetic
- consented
- authorized material

Add transformations.

---

## NEXT 6 — Build the analyst UX

At minimum one case page.

---

## NEXT 7 — Build architecture diagram

Keep it aligned to what will actually be demonstrated.

---

## NEXT 8 — Build 48-hour execution plan

Turn the timeline above into owner + deliverable.

---

## NEXT 9 — Build pitch deck

Only after product and architecture are locked.

---

## NEXT 10 — Final claim/source audit

Before submission:

- verify every number
- verify every external claim
- disclose third-party models/assets
- mark limitations
- confirm data provenance
- ensure no confidential data is included

---

# 53. INTERNAL DEFINITION OF DONE

The project is ready for Round 1 when a reviewer can answer all of these in under one minute:

### Problem
- Who is the primary user?
- What exact communication is being verified?
- What is the harmful moment?
- What does the attacker do?
- What financial harm occurs?

### Product
- What do I upload/forward?
- What happens next?
- What output do I receive?
- What should I do with that output?

### Technical
- What signals are analyzed?
- How are they fused?
- What happens when signals conflict?
- What is the role of provenance?
- What is the role of authorization?

### Safety
- What data is collected?
- What happens on false positives?
- Who can make the final high-impact decision?
- How is evidence protected?

### Feasibility
- What can be demonstrated in 48 hours?
- What is mocked/simulated?
- What is real?
- What remains future work?

### Adoption
- Where does this plug into a bank/fintech?
- Who owns the workflow?
- How does the system scale?

If these answers are not obvious, keep refining.

---

# 54. DO NOT LOSE THESE CORE PRINCIPLES

1. **Deepfake probability is not truth.**
2. **Identity is not authorization.**
3. **Provenance is evidence, not truth.**
4. **One detector is not enough.**
5. **Benchmarks are not production proof.**
6. **Human escalation matters for high-impact financial actions.**
7. **Explainability must be actionable, not merely a score.**
8. **Evidence preservation is part of the product.**
9. **Privacy must be designed into the architecture.**
10. **The hackathon rewards a product that is buildable, not an unlimited research platform.**

---

# 55. FINAL PROJECT THESIS

The project should ultimately be understood as:

> **A layered financial communication trust system.**

Not:

> a single AI model that guesses whether a video is fake.

The most defensible architecture is:

```text
              FINANCIAL COMMUNICATION
                       │
          ┌────────────┴────────────┐
          ↓                         ↓
     PROVENANCE                MEDIA FORENSICS
   C2PA / Metadata           Audio / Video / Image
          │                         │
          └────────────┬────────────┘
                       ↓
             IDENTITY / CHANNEL
                       ↓
            AUTHORIZATION CHECK
                       ↓
           FINANCIAL CONTEXT
                       ↓
                RISK FUSION
                       ↓
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
      ALLOW        STEP-UP          REVIEW/HOLD
        │              │              │
        └──────────────┴──────────────┘
                       ↓
                 EVIDENCE VAULT
                       ↓
             AUDIT / REPORT / RESPONSE
```

---

# 56. IMMEDIATE WORKING CHECKLIST

## Product

- [ ] Final problem statement
- [ ] Primary user
- [ ] Threat scenario
- [ ] Harm
- [ ] One-sentence solution
- [ ] Product name
- [ ] Product flow
- [ ] Output states
- [ ] Recommended actions

## Technical

- [ ] Primary modality
- [ ] Model selection
- [ ] Provenance implementation
- [ ] Identity/channel logic
- [ ] Financial-context inputs
- [ ] Risk-fusion logic
- [ ] Thresholds
- [ ] Evidence schema
- [ ] API/dashboard

## Validation

- [ ] Genuine set
- [ ] Fake set
- [ ] Manipulated set
- [ ] Recompression set
- [ ] Screen-recapture set
- [ ] Provenance-stripped set
- [ ] Metrics
- [ ] Latency
- [ ] Robustness tests

## Safety

- [ ] Data minimization
- [ ] Encryption
- [ ] Access control
- [ ] Retention
- [ ] Human review
- [ ] False-positive handling
- [ ] False-negative handling
- [ ] Adversarial mitigation
- [ ] Third-party/model disclosure

## Submission

- [ ] 10-slide pitch deck
- [ ] 3-page architecture
- [ ] Appendix/source notes
- [ ] All claims verified
- [ ] No confidential data
- [ ] 48-hour plan
- [ ] Clear MVP boundary

---

# 57. CURRENT STATUS SUMMARY

| Area | Status | Assessment |
|---|---|---|
| Threat research | Strong | Broad and detailed |
| India relevance | Strong | Good foundation |
| Academic literature | Strong | Large corpus; claim verification still needed |
| Dataset research | Strong | Good breadth |
| Detection research | Very strong | More than sufficient for Round 1 |
| Multimodal research | Strong | Good basis for layered architecture |
| Provenance | Strong | C2PA/watermarking covered |
| Document forensics | Strong | Useful differentiator |
| Identity/authorization distinction | Very strong | Key product insight |
| Competitor research | Strong | Needs compression for deck |
| Market/adoption research | Strong | Needs concrete buyer/integration story |
| Architecture concept | Strong | Too broad for literal MVP |
| Problem definition | **Needs work** | Must be sharply bounded |
| Product definition | **Needs work** | Must convert architecture into a workflow |
| Exact model stack | **Needs work** | Must be locked |
| Decision/risk engine | **Needs work** | Must be explicit |
| User journey | **Needs work** | Must be visually shown |
| Explainability UI | **Needs work** | Must be demonstrated |
| Human escalation | Partially defined | Needs productization |
| Validation experiment | **Needs work** | Must be concrete |
| 48-hour MVP | **Needs work** | Must be realistic |
| Integration pathway | Partially defined | Needs one concrete deployment point |
| Differentiation | Partially defined | Must be one clear sentence |
| Privacy/safety | Strong research basis | Needs implementation-level specifics |
| Final claim audit | Required | Must happen before submission |

---

# 58. BOTTOM LINE

## What has already been done

A large amount of deep research has already been completed.

## What is missing

The missing work is mostly **decision-making and productization**, not more background research.

## What to do next

Move immediately in this direction:

```text
PS3 RESEARCH
    ↓
SHARPLY BOUND PROBLEM
    ↓
ONE PRIMARY USER
    ↓
ONE CONCRETE FINANCIAL WORKFLOW
    ↓
PRODUCT FLOW
    ↓
MVP MODEL STACK
    ↓
RISK / DECISION ENGINE
    ↓
ANALYST UI + EVIDENCE
    ↓
VALIDATION
    ↓
ARCHITECTURE
    ↓
10-SLIDE PITCH
    ↓
48-HOUR EXECUTION PLAN
```

### Most important strategic shift

**Stop expanding the universe of deepfake research unless a missing claim is directly needed for the final product.**

The team is now at the stage where the project must become:

> **specific + explainable + safe + technically credible + demonstrable in 48 hours.**

That is the next phase.