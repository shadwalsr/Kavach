# KAVACH — Citation, Competitive, Tool, Project, Research-Paper & Gap Intelligence

**Purpose:** This document is the **competitive/research delta and citation index** for the final KAVACH product. It is intentionally designed to sit **beside `KAVACH.md` rather than duplicate it**.

**Current product:** B2B Financial Communication & Payment Security Gateway

**Final product thesis:** KAVACH protects high-risk financial communications and actions by combining communication/channel integrity, deepfake and voice-spoof analysis, document/PDF forensics, ZIP/archive malware analysis, identity, authorization, financial context, provenance, threat intelligence and cross-artifact evidence through a Financial Communication Verification Model (FCVM), followed by policy-controlled response.

**Primary wedge:** high-value corporate payment instructions and vendor beneficiary/bank-account changes.

**Primary operating user:** fraud-risk / financial-security analyst.

**Primary innovation under active research:** the **Financial Communication Verification Model (FCVM)**, which evaluates whether a communication is trustworthy **for the financial action it is attempting to trigger**, rather than merely deciding whether an isolated artifact is fake.

**Important scope rule:** KAVACH should not claim that every component listed here is novel. Most underlying technologies already exist. The purpose of this file is to identify what already exists, where those systems are stronger, what research is closest to the FCVM idea, and exactly where KAVACH still has technical, operational, scientific, or commercial gaps.

---

# 1. How to use this file

This document has four jobs:

1. **De-duplicate the existing KAVACH research.** Items already covered extensively in `KAVACH.md` are listed in a compact baseline register instead of having their full analysis repeated.
2. **Add the external landscape that matters to the final KAVACH design.** These entries are the competitive/tool/research delta that KAVACH must understand before implementation or pitching.
3. **State plainly where another system is better than current KAVACH.** “Better” means more mature, broader, faster, more validated, more deployable, more specialized, or more operationally complete than the current KAVACH design/MVP, not that it is better at the entire KAVACH mission.
4. **Turn competitive weaknesses into a KAVACH build checklist.** Every meaningful gap should become either a build item, a dependency/integration, a validation experiment, a safety control, or an explicit non-goal.

## Evidence labels used here

- **PRIMARY:** official product documentation, official standards, official government/regulatory source, peer-reviewed paper, or original project repository.
- **SECONDARY:** reputable reporting, independent analysis, or reputable technical coverage.
- **VENDOR:** vendor-authored marketing/technical material. Useful for capability discovery; not equivalent to independent validation.
- **KAVACH-CORPUS:** information already present in the supplied KAVACH research corpus. It is included here mainly for de-duplication and navigation.
- **NEEDS-VERIFICATION:** the supplied corpus or secondary material identifies the item, but the exact claim/metric/legal interpretation should be rechecked against a primary source before presentation as fact.

**Last web-research pass:** 7 October 2026.

---

# 2. De-duplication register — already substantially covered by KAVACH

The following are already present in the KAVACH research corpus and should **not be re-researched from scratch** unless a current-product update is needed. Their detailed strengths, weaknesses, technical notes and/or bibliography entries are already in `KAVACH.md`.

| Item | Type | KAVACH treatment | Site / project link |
|---|---|---|---|
| Reality Defender | Deepfake / multimodal enterprise platform | Extensive | https://www.realitydefender.com/ |
| Pindrop / Passport | Voice anti-spoofing + identity / call intelligence | Extensive | https://www.pindrop.com/ |
| Truepic / Lens / Display | Provenance / authenticity | Extensive | https://www.truepic.com/ |
| Vastav AI / TraceX Labs | Indian deepfake detection | Extensive but validation caveats | https://vastav.ai/ |
| HyperVerge | Indian KYC / liveness / identity | Extensive | https://hyperverge.co/ |
| Signzy | Indian digital identity / onboarding | Extensive | https://www.signzy.com/ |
| IDfy | Indian identity / video KYC | Extensive | https://www.idfy.com/ |
| BioID | Face / liveness / PAD | Extensive | https://www.bioid.com/ |
| iProov | Dynamic liveness / biometric verification | Extensive | https://www.iproov.com/ |
| Sensity AI | Deepfake detection / threat intelligence | Extensive | https://sensity.ai/ |
| DeepBrain AI | Synthetic media / avatar ecosystem | Extensive | https://www.deepbrain.io/ |
| Nuance Gatekeeper | Voice biometrics / authentication | Covered in vendor matrix | https://www.microsoft.com/ |
| ValidSoft | Voice / behavioral authentication | Covered in vendor matrix | https://www.validsoft.com/ |
| DuckDuckGoose | Media / deepfake detection | Covered in vendor matrix | https://duckduckgoose.ai/ |
| ID R&D / Mitek | Voice/face biometrics and liveness | Covered in vendor matrix | https://www.miteksystems.com/ |
| Veridas | Face/voice biometrics | Covered in vendor matrix | https://veridas.com/ |
| Attestiv | Media/document authenticity and provenance | Covered in vendor matrix | https://www.attestiv.com/ |
| DeepFakeBench | Deepfake detection benchmark / framework | Extensive research coverage | https://github.com/SCLBD/DeepfakeBench |
| AASIST | Audio anti-spoofing research model | Extensive | https://github.com/mrinmoyim/AASIST |
| RawNet2 | Audio anti-spoofing model | Extensive | https://github.com/eurecom-asp/rawnet2 |
| ECAPA-TDNN | Speaker verification baseline | Extensive | https://www.isca-archive.org/interspeech_2020/desplanques20_interspeech.html |
| Whisper / WhisperX | ASR / alignment / diarization pipeline | Extensive | https://github.com/openai/whisper |
| ASVspoof 2019/2021/5 | Speech anti-spoofing benchmarks | Extensive | https://www.asvspoof.org/ |
| FaceForensics++ | Video deepfake benchmark | Extensive | https://github.com/ondyari/FaceForensics |
| Celeb-DF | Video deepfake benchmark | Extensive | https://github.com/yuezunli/celeb-deepfakeforensics |
| FakeAVCeleb | Audio-video deepfake dataset | Extensive | https://github.com/DASH-Lab/FakeAVCeleb |
| C2PA / Content Credentials | Provenance standard/ecosystem | Extensive | https://c2pa.org/ |
| Adobe Content Credentials | Provenance / content authenticity | Extensive | https://contentauthenticity.adobe.com/ |
| M2TR | Multimodal/video forensic research | Covered in research annexes | https://github.com/CHELSEA234/M2TR |
| LipForensics | Robust lip-based video forensic research | Covered in research annexes | https://github.com/ahaliassos/LipForensics |
| InVID / WeVerify | Browser media verification | Covered | https://www.invid-project.eu/ |
| Amped Authenticate | Professional image forensics | Covered | https://ampedsoftware.com/authenticate |
| ExifTool / JPEGsnoop | Metadata / image forensic utilities | Covered | https://exiftool.org/ |
| pdfid / pdf-parser | PDF triage / object extraction | Covered | https://blog.didierstevens.com/programs/pdf-tools/ |
| C2PA CLI / c2pa-rs | Provenance tooling | Covered | https://opensource.contentauthenticity.org/docs/c2patool/ |

**Do not use the presence of an item in this register as proof that every claim in KAVACH about that item is still current.** The KAVACH source itself calls for verification of metrics, product claims, legal status and fast-changing capabilities.

---

# 3. NEW / EXPANDED COMPETITIVE LANDSCAPE

The following systems are especially important because they expose capabilities KAVACH currently lacks or can only prototype.

## 3.1 Abnormal AI

**Type:** Enterprise email / messaging security; BEC/VEC/ATO detection; automated remediation.

**What it does:** Abnormal builds behavioral profiles around people, vendors and communication relationships and uses those baselines to detect business email compromise, vendor fraud, account takeover and other social-engineering attacks. Its platform has expanded beyond email into messaging and other collaboration channels and emphasizes automated triage/remediation.

**Where it is better than current KAVACH:**

- much more mature behavioral baselining for real enterprise mailboxes;
- production-scale sender-recipient relationship modelling;
- mature BEC/VEC detection and remediation;
- established enterprise deployment and customer footprint;
- operational experience with enormous volumes of benign communication.

**Where KAVACH can differ:** KAVACH is explicitly designed around a **financial action boundary** and can incorporate media/deepfake, document and malware evidence with transaction and authorization context.

**Gap exposed in KAVACH:** enterprise-grade communication behavioral modelling, large-scale relationship graphs, real-world mail telemetry, mature false-positive suppression, production mail remediation.

**Evidence:** VENDOR / PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://abnormal.ai/

---

## 3.2 Proofpoint

**Type:** Enterprise email security / BEC / executive and supplier impersonation protection.

**What it does:** Proofpoint's BEC capabilities analyze message behavior, sender-recipient relationships, authentication signals such as SPF/DKIM/DMARC, message intent and impersonation patterns, with automated quarantine/removal capabilities.

**Where it is better than current KAVACH:** deeply mature email-gateway infrastructure, BEC detection, identity/relationship analytics and enterprise remediation.

**Gap exposed in KAVACH:** KAVACH needs production-level email policy integration, message-reputation and relationship analytics, quarantine/remediation hooks, and mature mail-volume operations.

**KAVACH opportunity:** treat Proofpoint/Abnormal-like mail controls as an integration/dependency instead of rebuilding a world-class email gateway.

**Evidence:** VENDOR / PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://www.proofpoint.com/us/solutions/bec-protection

---

## 3.3 FortiMail

**Type:** Secure email gateway / BEC / impersonation / anti-phishing.

**Where it is better:** mature inbound/outbound mail gateway, enterprise filtering, policy controls, threat intelligence and existing security-fabric integration.

**Gap exposed in KAVACH:** mail-flow control, policy enforcement, attachment scanning infrastructure and enterprise deployment maturity.

**KAVACH opportunity:** ingest high-risk events from an existing mail security layer rather than attempting to replace it.

**Evidence:** VENDOR.

**Site:** https://www.fortinet.com/products/email-security

---

## 3.4 OPSWAT MetaDefender

**Type:** File/malware analysis, archive inspection, sanitization and multi-engine scanning.

**Why it matters enormously to KAVACH:** This is one of the strongest counters to the idea that KAVACH should build every ZIP capability itself.

**Capabilities relevant to KAVACH:** recursive archive inspection, many archive formats, archive-bomb detection, encrypted/password-protected archive handling, multi-engine malware scanning, content disarm/reconstruction and file-risk workflows.

**Where it is better than current KAVACH:** vastly greater maturity and breadth in archive/file security, recursive parsing, multi-engine scanning and enterprise malware workflows.

**Gap exposed in KAVACH:** KAVACH's ZIP pipeline is an architecture and orchestration design, not a mature commercial malware-analysis engine. Production deployment should likely integrate a specialist such as MetaDefender rather than reinvent archive handling and antivirus engines.

**Important product decision:** KAVACH should own the **financial-risk interpretation** of a malicious archive, not necessarily every byte-level malware capability.

**Evidence:** VENDOR / PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://www.opswat.com/products/metadefender/core

---

## 3.5 ANY.RUN

**Type:** Interactive cloud malware sandbox / behavioral analysis / C2 inspection.

**Where it is better:** actual dynamic execution analysis, process trees, network behavior, DNS/HTTP inspection, memory-oriented investigation, rapid analyst reports and API-based automation.

**Gap exposed in KAVACH:** KAVACH currently describes sandboxing as a component, but does not itself possess the mature behavioral detonation environment, analyst tooling, VM fleet, telemetry depth or threat-intelligence network of a dedicated sandbox.

**KAVACH opportunity:** use a safe malware-analysis service or a private sandbox as a downstream engine, then feed the resulting evidence into FCVM.

**Evidence:** VENDOR / PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://any.run/

---

## 3.6 CAPE Sandbox

**Type:** Open-source dynamic malware analysis framework.

**Where it is better:** deep customizable detonation, API hooking, file/network/memory analysis, unpacking and configuration extraction.

**Gap exposed:** KAVACH needs a real dynamic-analysis implementation or a well-defined external sandbox dependency for files that static inspection cannot classify confidently.

**KAVACH advantage:** FCVM can interpret a CAPE-style result in the context of a pending financial action.

**Evidence:** PRIMARY open-source project.

**Site:** https://github.com/kevoreilly/CAPEv2

---

## 3.7 BioCatch

**Type:** Behavioral biometrics / account-takeover / fraud / social-engineering detection.

**Where it is better:** continuous behavioral telemetry, user/device/session behavior, mature fraud models and financial-sector scale. Its product direction is specifically about understanding behavior in context rather than a single transaction signal.

**Gap exposed in KAVACH:** KAVACH currently has conceptual transaction-context and identity layers but not BioCatch-level behavioral telemetry, historical behavioural profiles, device/session signals, or demonstrated production fraud scale.

**KAVACH opportunity:** integrate behavioral fraud signals rather than attempt to recreate the entire behavioral-biometrics stack.

**Evidence:** VENDOR; scale and performance figures should be treated as vendor-reported until independently validated.

**Site:** https://www.biocatch.com/

---

## 3.8 Featurespace

**Type:** Adaptive behavioral analytics and payment-fraud detection.

**Where it is better:** real-time transaction scoring, adaptive behavioural analytics, link analysis, payment-network context and mature financial-fraud deployments.

**Gap exposed:** KAVACH needs stronger transaction telemetry, adaptive behaviour modelling, historical linkage and financial-fraud performance benchmarks.

**KAVACH differentiation:** the communication side, especially deepfake/document/malware evidence, can be fed into a financial-risk decision rather than keeping payment fraud and communication fraud in separate silos.

**Evidence:** VENDOR.

**Site:** https://www.featurespace.com/

---

## 3.9 Feedzai

**Type:** Payment fraud / financial crime / risk decisioning.

**Where it is better:** enormous transaction-scale infrastructure, financial-crime workflows, risk lifecycle, explainability/governance, payment context and increasingly agentic prevention capabilities.

**Gap exposed:** KAVACH lacks transaction-scale deployment maturity, broad payment-system integrations and proven financial-crime operating performance.

**KAVACH opportunity:** position itself as a **communication-evidence layer feeding financial risk**, not as a replacement for a complete payment-fraud engine.

**Evidence:** VENDOR.

**Site:** https://www.feedzai.com/

---

## 3.10 CrowdStrike Falcon

**Type:** Endpoint detection and response / threat response.

**Where it is better:** mature endpoint telemetry, host isolation, real-time response, process/file remediation, threat hunting and enterprise-scale endpoint coverage.

**Gap exposed:** KAVACH cannot credibly claim autonomous endpoint containment without an EDR connector or its own agent. “Isolate endpoint” in the architecture is an **integration dependency**, not a magically available action.

**KAVACH action:** invoke EDR API for containment and record the action as part of the financial attack case.

**Evidence:** VENDOR / PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://www.crowdstrike.com/

---

## 3.11 Microsoft Defender for Endpoint / Defender XDR

**Type:** Endpoint security, automatic attack disruption, device/user containment.

**Where it is better:** Microsoft already provides automatic device isolation, user containment/session revocation, indicator blocking and correlation into incidents. Its automatic attack disruption can take action without waiting for a human analyst in supported scenarios. citeturn189739search0turn189739search4turn189739search6

**Gap exposed in KAVACH:** endpoint isolation, user/session containment and C2 blocking must be implemented through real enterprise integrations rather than asserted abstractly.

**Important correction to KAVACH:** KAVACH should orchestrate these controls; it should not claim to replace Microsoft Defender's endpoint sensor.

**Evidence:** PRIMARY.

**Sites:**
- https://learn.microsoft.com/defender-endpoint/respond-machine-alerts
- https://learn.microsoft.com/en-us/defender-endpoint/api/isolate-machine
- https://learn.microsoft.com/en-us/defender-xdr/automatic-attack-disruption

---

## 3.12 Cortex XSOAR

**Type:** Security orchestration, case management and automated response.

**Where it is better:** mature playbooks, conditions, scripts, loops, third-party integrations, incident handling and automation across security products.

**Gap exposed:** KAVACH's response orchestrator is conceptually similar but far less mature. Therefore the claim “automated security response” is not novel by itself.

**KAVACH opportunity:** make the FCVM/financial-communication evidence the unique decision input, while allowing existing SOAR systems to execute downstream controls.

**Evidence:** PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://docs-cortex.paloaltonetworks.com/

---

## 3.13 Splunk SOAR

**Type:** Security orchestration and automated response / case management.

**Where it is better:** mature playbook automation, integration ecosystem and SOC workflow tooling.

**Gap exposed:** KAVACH should avoid positioning generic automation as its novelty.

**KAVACH opportunity:** publish KAVACH as a specialized financial-risk verification service that can feed Splunk SOAR.

**Evidence:** PRIMARY PRODUCT DOCUMENTATION.

**Site:** https://help.splunk.com/en/splunk-soar

---

## 3.14 Darktrace RESPOND

**Type:** Autonomous response across network, email, cloud and endpoint contexts.

**Where it is better:** established autonomous-response infrastructure and real-time control across multiple enterprise layers.

**Gap exposed:** KAVACH must prove that its response logic is genuinely financial-action-aware and not merely another generic autonomous SOC engine.

**Evidence:** VENDOR.

**Site:** https://www.darktrace.com/

---

## 3.15 MISP

**Type:** Open-source threat-intelligence collection, correlation and sharing platform.

**Where it is better:** mature machine-readable threat-intelligence events, indicator correlation, sharing and ecosystem interoperability.

**Gap exposed:** KAVACH needs an explicit IOC data model and external intelligence feed strategy instead of a home-grown collection of domains/IPs/hashes.

**KAVACH opportunity:** ingest/emit MISP-compatible events and use the IOC layer as evidence for FCVM and response.

**Evidence:** PRIMARY open-source project.

**Site:** https://www.misp-project.org/

---

## 3.16 OpenCTI

**Type:** Cyber-threat intelligence platform / knowledge graph.

**Where it is better:** formal threat-intelligence entity relationships, observables, knowledge graphing and analyst workflows.

**Gap exposed:** KAVACH's evidence graph is financially focused but not yet a mature cyber-threat-intelligence knowledge base.

**KAVACH opportunity:** integrate OpenCTI/MISP rather than trying to become a general threat-intelligence platform.

**Evidence:** PRIMARY project documentation.

**Site:** https://docs.opencti.io/latest/

---

## 3.17 AbuseIPDB

**Type:** IP reputation / abuse reporting API.

**Where it is better:** broad crowdsourced malicious-IP intelligence and simple machine-readable reputation checks.

**Gap exposed:** KAVACH needs external reputation signals for network indicators and should expose their source and confidence rather than presenting a home-grown C2 verdict.

**Evidence:** PRIMARY service documentation.

**Site:** https://www.abuseipdb.com/

---

## 3.18 Microsoft Entra ID + FIDO2 / passkeys

**Type:** Identity, phishing-resistant authentication, passkeys, WebAuthn.

**Where it is better:** cryptographic identity and enterprise directory integration are already solved at a much higher maturity level.

**Gap exposed:** KAVACH should **not** become an identity provider. Its trusted-channel verification should invoke enterprise IdP/authentication APIs.

**Evidence:** PRIMARY Microsoft documentation.

**Site:** https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-passkeys-fido2

---

## 3.19 Okta WebAuthn / Passkeys

**Type:** Enterprise identity and phishing-resistant authentication.

**Where it is better:** enterprise identity lifecycle, WebAuthn/passkey infrastructure and authentication policy.

**Gap exposed:** trusted-channel verification requires real IdP integration, enrollment, policy and recovery paths.

**Evidence:** PRIMARY product documentation.

**Site:** https://developer.okta.com/docs/guides/authenticators-web-authn/main/

---

# 4. RESEARCH PROJECTS / DATASETS / TECHNICAL BASELINES

This section separates **scientific research** from commercial products. These systems may be “better than KAVACH” at a narrow research problem, but that is not the same as being a better product.

## 4.1 AV-Deepfake1M / AV-Deepfake1M++

**Type:** Large-scale audio-video deepfake dataset / benchmark.

**Why it matters:** multimodal audio-video manipulation at scale is much closer to KAVACH's voice/video problem than single-modality datasets.

**What it has that KAVACH lacks:** large-scale labelled multimodal training/evaluation data and explicit manipulation diversity.

**KAVACH gap:** a financial communication dataset linking media to sender identity, transaction intent, beneficiary change and authorization state does not already exist at comparable scale. Building a synthetic/authorized benchmark is therefore a major research requirement.

**Site/project:** https://github.com/AV-Deepfake/AV-Deepfake1M

**Evidence:** PRIMARY research/project repository; exact benchmark version should be checked before use.

---

## 4.2 ASVspoof 5

**Type:** speech anti-spoofing benchmark/challenge.

**Why it matters:** KAVACH's voice layer depends on surviving degraded real-world conditions, spoof attacks and adversarial manipulation.

**What it has that KAVACH lacks:** carefully defined anti-spoof evaluation protocols, diverse speech conditions and benchmark infrastructure. The research corpus emphasizes performance/calibration degradation under difficult conditions.

**KAVACH gap:** no proprietary benchmark exists yet for Indian enterprise telephony, call-center routing, WhatsApp-like re-encoding, multilingual/Hinglish, and financial intent.

**Site:** https://www.asvspoof.org/

**Primary paper/reference:** https://arxiv.org/abs/2601.03944

**Evidence:** PRIMARY.

---

## 4.3 DeepFakeBench

**Type:** standardized deepfake benchmark/framework.

**What it has that KAVACH lacks:** common evaluation protocols, baseline implementations and multi-dataset comparisons.

**Gap exposed:** KAVACH must produce reproducible evaluation rather than relying on individual detector claims.

**Site:** https://github.com/SCLBD/DeepfakeBench

**Evidence:** PRIMARY project.

---

## 4.4 FakeAVCeleb

**Type:** audio-video deepfake dataset.

**What it has that KAVACH lacks:** paired synthetic audio/video examples and a ready benchmark for multimodal mismatch.

**Gap exposed:** KAVACH needs rights-safe, financially contextualized examples that go beyond celebrity-style media.

**Site:** https://github.com/DASH-Lab/FakeAVCeleb

**Evidence:** PRIMARY project.

---

## 4.5 FaceForensics++

**Type:** facial manipulation dataset and evaluation baseline.

**What it has that KAVACH lacks:** well-established controlled benchmark for manipulated facial video.

**Gap exposed:** KAVACH's real-world robustness must include compression, re-encoding and open-world generators instead of depending on in-domain benchmark accuracy.

**Site:** https://github.com/ondyari/FaceForensics

**Evidence:** PRIMARY project.

---

## 4.6 Celeb-DF / Celeb-DF variants

**Type:** challenging deepfake video benchmark.

**What it has that KAVACH lacks:** evaluation conditions designed to be more visually realistic than early manipulation datasets.

**Gap exposed:** KAVACH still needs domain-shift testing from public media datasets to enterprise communications.

**Site:** https://github.com/yuezunli/celeb-deepfakeforensics

**Evidence:** PRIMARY project.

---

## 4.7 M2TR

**Type:** multimodal-transformer / deepfake detection research.

**What it contributes:** a research baseline for multimodal/transformer-style forensic reasoning and manipulation traces.

**Gap exposed:** KAVACH should benchmark its FCVM against strong modern multimodal detectors, not only classic CNN baselines.

**Project:** https://github.com/CHELSEA234/M2TR

**Evidence:** PRIMARY project; paper metadata should be checked from the repository/publication page before citation in the pitch.

---

## 4.8 LipForensics / “Lips Don't Lie”

**Type:** robust lip-based video forensic research.

**What it contributes:** forensic information from mouth/lip dynamics that can complement generic frame-level detectors.

**Where better:** research-specific robustness and spatial-temporal cues for manipulated talking-head video.

**KAVACH gap:** KAVACH needs a reproducible video subsystem and systematic benchmark of lip dynamics under compression/screen recapture.

**Project:** https://github.com/ahaliassos/LipForensics

**Paper reference:** DOI 10.1109/CVPR46437.2021.00500

**Evidence:** PRIMARY.

---

# 5. RESEARCH PAPERS CLOSEST TO KAVACH'S TECHNICAL PROBLEM

## 5.1 “AASIST: Audio Anti-Spoofing Using Integrated Spectro-Temporal Graph Attention Networks”

**Venue:** IEEE/ACM TASLP, 2022.

**Why it matters:** strong audio anti-spoofing foundation for the voice layer.

**What it has that KAVACH lacks:** a peer-reviewed, reproducible anti-spoofing method with benchmark evaluation.

**KAVACH gap:** an FCVM cannot rely on AASIST alone; KAVACH must characterize out-of-domain and financial-channel performance.

**DOI:** 10.1109/TASLP.2022.3168128

**Project:** https://github.com/mrinmoyim/AASIST

---

## 5.2 “End-to-End Anti-Spoofing with RawNet2”

**Venue:** ICASSP, 2021.

**What it contributes:** raw-waveform anti-spoofing baseline.

**KAVACH gap:** ensemble diversity and robustness to telephony/audio transforms remain necessary.

**DOI:** 10.1109/ICASSP39728.2021.9413977

**Project:** https://github.com/eurecom-asp/rawnet2

---

## 5.3 “ECAPA-TDNN: Emphasized Channel Attention, Propagation and Aggregation in TDNN Based Speaker Verification”

**Venue:** Interspeech, 2020.

**What it contributes:** speaker-verification identity baseline.

**Important limitation for KAVACH:** speaker identity is not authorization. A perfect ECAPA match cannot prove that the speaker is authorized to request a payment.

**Reference:** https://www.isca-archive.org/interspeech_2020/desplanques20_interspeech.html

---

## 5.4 ASVspoof 5 research / evaluation papers

**Contribution:** formal anti-spoof evaluation using difficult speech conditions, spoofing/deepfake attacks, calibration and cost-sensitive evaluation.

**Why better than KAVACH:** it has a scientific benchmark and standardized scoring protocol that KAVACH still lacks.

**KAVACH gap:** build a financial-context benchmark with both audio authenticity and transaction/authorization labels.

**Reference:** https://arxiv.org/abs/2601.03944

---

## 5.5 AV-LMMDetect — Leveraging Large Multimodal Models for Audio-Video Deepfake Detection

**Type:** 2026 research / multimodal large-model approach.

**Why it matters:** directly probes whether large multimodal models can reason over audio and video together for deepfake detection.

**What it has that KAVACH lacks:** a contemporary multimodal-model baseline with modern foundation-model reasoning.

**KAVACH gap:** compare FCVM against a strong AV foundation-model baseline; otherwise “multimodal” remains a vague architectural word rather than an evaluated capability.

**Reference:** https://arxiv.org/abs/2604.24890

**Evidence:** PRIMARY research paper/preprint; verify final publication status before claiming peer review.

---

## 5.6 “Divide and Conquer: Multimodal Video Deepfake Detection via Cross-Modal Fusion and Localization”

**Type:** contemporary multimodal video deepfake research.

**Why it matters:** cross-modal fusion and localization are directly relevant to KAVACH's audio/video consistency layer.

**What it has that KAVACH lacks:** explicit cross-modal localization research, allowing models to point to where inconsistencies occur rather than merely assigning a global score.

**KAVACH gap:** FCVM needs segment-level evidence and localization to make analyst outputs defensible.

**Reference:** https://arxiv.org/abs/2602.23393

**Evidence:** PRIMARY research/preprint; verify final status.

---

## 5.7 “Verifying Provenance of Digital Media: Why the C2PA Specifications Fall Short”

**Type:** 2026 technical/security critique of provenance assumptions.

**Why it matters:** this directly challenges an architectural assumption in many authenticity systems: that cryptographic provenance alone solves verification.

**What it contributes:** a security-oriented critique of limitations in current provenance goals/specification assumptions.

**KAVACH gap:** provenance must be one evidence source, not a truth oracle. KAVACH needs a threat model for stripping, re-encoding, malformed manifests, compromised capture chains, and provenance gaps.

**Reference:** https://arxiv.org/abs/2602.00209

**Evidence:** PRIMARY research/preprint; verify publication status before formal citation.

---

## 5.8 “MEADE: Towards a Malicious Email Attachment Detection Engine”

**Venue:** IEEE conference paper, 2018.

**Why it matters:** it is extremely close to the KAVACH ZIP/email threat surface. The cited research describes large-scale malicious/benign attachment data including ZIP archives and Office documents.

**What it has that KAVACH lacks:** a dedicated scientific treatment of malicious attachment detection and a benchmark-oriented attachment dataset.

**KAVACH gap:** financial-context + deepfake + malware correlation still needs a benchmark; KAVACH should compare against dedicated attachment detectors.

**DOI:** 10.1109/THS.2018.8574202

**Reference:** https://ieeexplore.ieee.org/document/8574202

**Evidence:** PRIMARY.

---

## 5.9 “Email Forensics Using Machine and Deep Learning Techniques for Cybercrime Detection”

**Venue:** IEEE conference, 2025.

**Why it matters:** directly relevant to email forensic extraction/classification.

**KAVACH gap:** KAVACH needs to validate sender/header/intent features against modern BEC attacks, and needs to quantify how email forensics improves financial-action verification beyond generic phishing detection.

**DOI:** 10.1109/CISES66934.2025.11265002

**Reference:** https://ieeexplore.ieee.org/abstract/document/11265002

**Evidence:** PRIMARY.

---

## 5.10 “Lips Don't Lie: A Generalisable and Robust Approach to Face Forgery Detection”

**Venue:** CVPR, 2021.

**Why it matters:** robust talking-head evidence can complement face-level artifact detectors.

**KAVACH gap:** segment-level temporal evidence and compression robustness need empirical evaluation.

**DOI:** 10.1109/CVPR46437.2021.00500

---

## 5.11 “Face X-Ray for More General Face Forgery Detection”

**Venue:** CVPR, 2020.

**What it contributes:** generalization from manipulation boundaries rather than one specific generator.

**KAVACH gap:** KAVACH needs open-world / unseen-generator testing rather than training and testing on the same manipulation family.

---

## 5.12 “Thinking in Frequency: Face Forgery Detection by Mining Frequency-Aware Clues”

**Venue:** ECCV, 2020.

**What it contributes:** frequency-domain forensic features.

**KAVACH gap:** frequency clues can be damaged by recompression and analog-hole transformations; they should remain complementary rather than authoritative.

---

## 5.13 “Detecting Deepfakes with Self-Blended Images”

**Venue:** CVPR, 2022.

**What it contributes:** synthetic training construction to improve generalization.

**KAVACH gap:** a similar strategy could be useful for generating controlled financial-communication examples, but its utility must be tested on real enterprise communication transformations.

---

# 6. INCIDENTS AND THREAT-INTELLIGENCE CASES RELEVANT TO KAVACH

These are not “products,” but they are important evidence for the exact problem KAVACH is trying to solve.

## 6.1 Arup — 2024 deepfake video-conference fraud

**Attack pattern:** spear-phishing email → secret transaction lure → multi-person video call → executive impersonation using deepfake audio/video → multiple transfers.

**Why relevant:** demonstrates that social corroboration and familiar faces/voices can defeat human verification even without a traditional network breach.

**KAVACH lesson:** cross-modal identity + financial context + transaction hold must occur before irreversible payment action.

**Sources:**
- Financial Times: https://www.ft.com/content/b977e8d4-664c-4ae4-8a8b-eb93bdf785ea
- Related incident reporting in the KAVACH research corpus.

**Evidence status:** widely reported incident; maintain source-specific wording for exact loss figure.

---

## 6.2 Ferrari — 2024 CEO voice impersonation

**Attack pattern:** impersonation via WhatsApp and cloned voice to pressure an executive into a high-value transaction.

**Why relevant:** the attack was disrupted by an out-of-band verification question.

**KAVACH lesson:** trusted-channel verification is not just a nice feature; it can be the recovery control when media identity is uncertain.

**Source:** https://news.bloomberglaw.com/daily-labor-report/ferrari-narrowly-dodges-deepfake-scam-simulating-deal-hungry-ceo

**Evidence:** secondary/incident reporting; corroborate before using numeric claims.

---

## 6.3 WPP — 2024 CEO impersonation using fake WhatsApp + Teams

**Attack pattern:** fake WhatsApp account → Teams interaction → AI voice cloning and impersonation → solicitation of money/PII.

**Why relevant:** multi-channel social engineering defeats assumptions that a “video call” is inherently trustworthy.

**Sources:**
- Guardian: https://www.theguardian.com/technology/article/2024/may/10/ceo-wpp-deepfake-scam
- OECD.AI incident: https://oecd.ai/en/incidents/2024-05-10-e24d

**Evidence:** SECONDARY + institutional incident registry.

---

## 6.4 Fideuram / Intesa Sanpaolo — 2026 AI-messaging impersonation scam

**Attack pattern:** executive impersonation through messaging/voice cloning with a high-value financial objective.

**Why relevant:** contemporary European example of AI-enabled executive impersonation at a major financial institution.

**Source:** Reuters, 25 September 2026: https://www.reuters.com/legal/government/ai-messaging-scam-costs-italys-top-bank-intesa-millions-sources-say-2026-09-25/

**Evidence:** PRIMARY-REPORTING / REPUTABLE NEWS; exact recovered/unrecovered totals should be cited precisely as Reuters reported them.

---

## 6.5 SEBI “Boss Scam” — 17 July 2026

**Attack pattern:** impersonation of senior executives using communication channels including email and messaging, with deepfake voice/video among the described methods.

**Why relevant:** this is direct Indian regulatory recognition of executive-impersonation risk for regulated entities and listed companies.

**Official source:** https://www.sebi.gov.in/media-and-notifications/press-releases/jul-2026/caution-to-regulated-entities-and-listed-companies-boss-scam_102919.html?outputType=chromeless

**Evidence:** PRIMARY REGULATORY.

---

## 6.6 RBI / Indian deepfake investment-video warnings

**Why relevant:** demonstrates the broader Indian financial-fraud problem involving synthetic voices/video and trusted-person impersonation.

**Primary RBI source:** the KAVACH corpus cites RBI warnings around deepfake investment content. For production/legal citation, use the current RBI publication rather than secondary summaries.

**Site:** https://www.rbi.org.in/

**Evidence:** PRIMARY regulatory institution; exact notice/URL should be verified for the final deck.

---

## 6.7 INTERPOL Global Financial Fraud Threat Assessment 2026

**Why relevant:** provides an authoritative global threat context for AI-enhanced financial fraud and the growing intersection of organized cybercrime, fraud and automation.

**Important finding:** INTERPOL's 2026 assessment states that AI-enhanced fraud is substantially more profitable than traditional approaches and describes increasingly automated fraud campaigns.

**Official source:** https://www.interpol.int/News-and-Events/News/2026/INTERPOL-report-warns-of-increasingly-sophisticated-global-financial-fraud-threat

**Evidence:** PRIMARY INTERNATIONAL ORGANIZATION. citeturn189739search7

---

## 6.8 FBI Business Email Compromise

**Why relevant:** BEC remains a foundational threat model for KAVACH because malicious ZIPs, invoices, impersonation and payment instructions often appear in the same workflow.

**Official source:** https://www.fbi.gov/how-we-help-you/common-frauds-and-scams/business-email-compromise

**Evidence:** PRIMARY GOVERNMENT.

---

# 7. STANDARDS, SECURITY CONTROL REFERENCES AND PROVENANCE

## 7.1 C2PA

**Use in KAVACH:** provenance evidence for images/video/documents where credentials exist.

**What is better than KAVACH:** C2PA is an established provenance framework rather than a KAVACH invention.

**KAVACH gap:** the system needs a nuanced trust policy because provenance can be absent after normal transport transformations; provenance does not establish factual truth; and recent research questions some security assumptions.

**Current spec:** https://spec.c2pa.org/

**Current ecosystem:** https://c2pa.org/

**Evidence:** PRIMARY standard.

---

## 7.2 Adobe Content Credentials

**Use:** practical content-credential inspection and ecosystem implementation.

**Where better:** real product/ecosystem reach and durable-provenance mechanisms.

**KAVACH gap:** C2PA should be integrated as one signal; KAVACH must characterize what happens when credentials are absent/stripped and avoid binary “missing = fake” decisions.

**Site:** https://contentauthenticity.adobe.com/

**Evidence:** PRIMARY/VENDOR.

---

## 7.3 MITRE ATT&CK — Network Traffic Filtering / M1037

**Use:** reference for blocking unauthorized outbound traffic and C2 communication.

**What it exposes:** geo-blocking is only one possible egress-control tactic and can be circumvented. Indicator-based and policy-based network controls are more fundamental.

**KAVACH gap:** implement real firewall/DNS/SWG/EDR connectors and document blast radius, exclusions and rollback.

**Official source:** https://attack.mitre.org/mitigations/M1037/

**Evidence:** PRIMARY. citeturn189739search3

---

## 7.4 Microsoft Defender automatic attack disruption

**Use:** reference architecture for automated containment.

**Where better:** existing telemetry and mature endpoint/network/user containment actions.

**KAVACH implication:** KAVACH should orchestrate, not reimplement, endpoint isolation and user/session actions.

**Official documentation:** https://learn.microsoft.com/en-us/defender-xdr/automatic-attack-disruption

---

# 8. WHAT KAVACH STILL LACKS — HONEST GAP AUDIT

This is the section the team should treat as a **pre-build and pre-pitch risk register**.

## 8.1 The FCVM is still a hypothesis, not a proven technical advantage

KAVACH currently has the strongest conceptual opportunity in the FCVM, but there is no demonstrated evidence yet that an event-level financial communication model materially outperforms:

1. individual media detectors;
2. conventional score fusion;
3. a strong multimodal deepfake model;
4. a mature transaction-fraud system with contextual features.

**Required experiment:** construct a controlled benchmark with identical media and different financial contexts. Compare media-only, simple score-fusion and FCVM-style models using precision, recall, calibration, false-positive cost and financial-action decision quality.

**Priority:** CRITICAL.

---

## 8.2 KAVACH does not yet have the financial multimodal dataset needed to train/test FCVM

Existing deepfake datasets mostly provide media labels, not:

- sender identity;
- sender authority;
- beneficiary history;
- amount;
- approval state;
- channel history;
- financial intent;
- attack stage;
- malware evidence;
- eventual financial outcome.

**Required solution:** synthetic + public + consented benchmark that joins media payloads to mock financial workflow states. Avoid real confidential financial data.

**Priority:** CRITICAL.

---

## 8.3 Production email analytics are far behind Abnormal/Proofpoint

KAVACH has the conceptual email layer but not their:

- relationship graphs;
- behavioral baselines;
- mailbox-scale telemetry;
- mature remediation;
- enterprise mail-flow deployment;
- false-positive tuning at scale.

**Response:** integrate with existing email security where possible; focus KAVACH on the financial-action verification boundary.

**Priority:** HIGH.

---

## 8.4 ZIP malware analysis is currently architecture, not mature capability

KAVACH describes safe ZIP processing correctly but does not yet have the depth of OPSWAT, ANY.RUN, ReversingLabs-class systems or long-established sandbox ecosystems.

**Required:** static triage + safe archive extraction + optional external sandbox + malware intelligence + C2 evidence. The core host must never execute uploaded payloads.

**Priority:** CRITICAL.

---

## 8.5 Endpoint/C2 response is not actually available without integrations

“Isolate endpoint,” “revoke session,” “block C2,” and “disable user” require:

- EDR;
- IdP;
- firewall/DNS/SWG;
- SIEM/SOAR;
- IAM permissions;
- customer-specific policy.

**Required:** explicit connector architecture, API permissions, rollback, action logging and failure handling.

**Priority:** CRITICAL.

---

## 8.6 Autonomous response creates a new safety problem

Automatic blocking can be wrong. The system therefore needs:

- confidence thresholds;
- business-impact classes;
- allowlists/exclusions;
- idempotent actions;
- time-limited containment;
- rollback;
- human override;
- protected critical assets;
- audit logs;
- dry-run mode;
- simulation before policy activation.

Microsoft's own automatic device isolation documentation highlights scoping, time limits and exclusions because automated containment can cause business impact. citeturn189739search0turn189739search5

**Priority:** CRITICAL.

---

## 8.7 Geo-blocking alone is not sufficient for C2

A geographically unusual destination can be a useful signal, but it is not equivalent to maliciousness.

**Required response hierarchy:**

1. confirmed IOC/domain/IP/URL/hash block;
2. DNS/firewall/SWG/EDR enforcement;
3. session/endpoint containment;
4. optional regional egress restriction as defence-in-depth;
5. allowlists for legitimate business regions/services.

MITRE describes egress filtering and notes that network blocking can be circumvented by other adversary techniques. citeturn189739search3

**Priority:** HIGH.

---

## 8.8 FCVM must handle missing and conflicting evidence

A real event may contain:

- genuine voice;
- missing C2PA;
- legitimate PDF;
- compromised email account;
- new beneficiary;
- valid biometric match;
- invalid authorization.

KAVACH needs explicit reasoning for:

- missing evidence;
- contradictory signals;
- low-quality signals;
- stale identity references;
- out-of-distribution models.

**Priority:** CRITICAL.

---

## 8.9 Identity is not authorization

A perfectly verified CFO voice can still be:

- compromised;
- replayed;
- synthetically generated;
- used outside the person's authority;
- attached to a fraudulent workflow.

KAVACH must preserve this principle everywhere in the architecture.

**Priority:** CRITICAL.

---

## 8.10 KAVACH lacks enterprise-scale transaction-fraud telemetry

BioCatch, Featurespace and Feedzai show how far the financial-fraud side of the market has progressed.

KAVACH currently needs stronger access to:

- transaction history;
- device history;
- behavioral baselines;
- beneficiary age;
- user entitlements;
- transaction velocity;
- amount distributions;
- geographic patterns;
- account/session relationships;
- maker-checker state.

**Priority:** HIGH.

---

## 8.11 The communication-to-transaction causal link is difficult

Simply occurring near each other in time does not prove that a communication caused a transaction.

KAVACH needs strong correlation keys such as:

- case ID;
- payment/order ID;
- beneficiary ID;
- invoice ID;
- vendor ID;
- employee/requester ID;
- message ID;
- timestamp windows;
- workflow state transitions.

Otherwise the evidence graph risks creating false causal relationships.

**Priority:** CRITICAL.

---

## 8.12 India-specific language and channel robustness are unproven

Real Indian enterprise communication can include:

- English;
- Hindi;
- regional languages;
- Hinglish;
- code switching;
- accents;
- call-centre compression;
- WhatsApp-like re-encoding;
- low-quality forwarded recordings.

KAVACH needs explicit validation instead of assuming clean English recordings.

**Priority:** HIGH.

---

## 8.13 Provenance cannot be the truth layer

C2PA is useful evidence, but missing provenance can be caused by normal platform processing. Recent security research also challenges the assumption that provenance specifications alone solve authenticity.

**KAVACH requirement:** treat provenance as one signal inside FCVM, with channel-aware missingness handling.

**Priority:** HIGH.

---

## 8.14 Model governance and drift are not yet solved

KAVACH needs:

- model versioning;
- threshold versioning;
- calibration monitoring;
- drift detection;
- unseen-generator tests;
- champion/challenger evaluation;
- rollback;
- bias/accent/language evaluation;
- dataset lineage;
- detector provenance.

**Priority:** HIGH.

---

## 8.15 Evidence and legal defensibility remain incomplete

KAVACH currently has the correct direction: hashes, immutable originals, derived evidence, timestamps and audit history.

But it still needs:

- formal evidence package schema;
- chain-of-custody procedures;
- signer identity for analyst actions;
- retention policy;
- legal hold workflow;
- reproducibility of model outputs;
- versioned detector manifests;
- controlled export format.

**Priority:** HIGH.

---

## 8.16 Biometrics create their own security risk

Voice/face references are high-value assets. If the KAVACH database is compromised, attackers could potentially gain highly sensitive biometric information.

KAVACH therefore needs:

- data minimization;
- encrypted reference storage;
- template protection;
- separation of identity references from case data;
- strict tenant isolation;
- access logging;
- deletion/retention policies;
- explicit organizational consent.

**Priority:** CRITICAL.

---

## 8.17 Messaging-platform integration is still a hard product boundary

“Integrate with WhatsApp” is not a sufficient enterprise integration design.

KAVACH needs specific, authorized business interfaces or ingestion points and must define exactly what data an enterprise is legally/technically allowed to provide.

**Priority:** HIGH.

---

## 8.18 KAVACH currently lacks demonstrated latency/SLA evidence

The architecture proposes asynchronous heavy processing plus lightweight pre-transaction checks, which is sound.

But KAVACH still needs actual measurements for:

- ingestion;
- FFmpeg extraction;
- ASR;
- speaker verification;
- anti-spoofing;
- PDF triage;
- ZIP static scan;
- sandbox latency;
- FCVM inference;
- final decision;
- queueing under load.

**Priority:** HIGH.

---

## 8.19 KAVACH lacks independent benchmark evidence for the whole system

Individual components can have strong benchmark numbers while the system performs poorly in real-world mixtures.

KAVACH needs end-to-end evaluation under:

- recompression;
- screen recording;
- telephony;
- noise;
- codec changes;
- missing metadata;
- password-protected ZIPs;
- nested archives;
- malicious PDFs;
- new beneficiaries;
- legitimate high-value transactions;
- insider-like unusual but legitimate behavior.

**Priority:** CRITICAL.

---

## 8.20 Commercial positioning is still vulnerable to market overlap

Abnormal, Proofpoint, Reality Defender, Pindrop, BioCatch, Featurespace, Feedzai, Microsoft and SOAR vendors already cover portions of the KAVACH story.

Therefore KAVACH must **not** claim:

- “first AI cybersecurity platform”;
- “first multimodal detector”;
- “first autonomous response platform”;
- “first risk-scoring engine.”

The defensible position is narrower:

> **KAVACH is specifically designed to verify a high-risk financial communication as an authorization for a financial action by combining evidence that normally lives in separate security, identity, communication and fraud systems.**

**Priority:** CRITICAL.

---

# 9. COMPARATIVE ANSWER: WHAT IS ACTUALLY HARDER/BETTER ELSEWHERE?

| Capability | Strong existing examples | Why they are ahead of KAVACH | KAVACH response |
|---|---|---|---|
| Enterprise email/BEC | Abnormal, Proofpoint, FortiMail | production mailbox telemetry, behavioral graphs, remediation, scale | integrate / focus on financial-action boundary |
| Voice anti-spoof | Pindrop, AASIST ecosystem, Reality Defender | specialized data, telephony robustness, mature deployments | benchmark + use as evidence layer |
| Deepfake multimodal detection | Reality Defender, DeepFakeBench, modern AV research | specialized models, datasets, inference infrastructure | evaluate FCVM against strong baselines |
| Provenance | C2PA, Adobe, Truepic | mature cryptographic ecosystem | use as evidence, not truth |
| Malware/ZIP | OPSWAT, ANY.RUN, CAPE, ReversingLabs-class tooling | detonation, recursive archive handling, large AV/intel ecosystem | integrate, sandbox safely |
| Transaction fraud | BioCatch, Feedzai, Featurespace | huge financial telemetry and mature risk models | consume context; don't replace whole fraud stack |
| Endpoint containment | Microsoft Defender, CrowdStrike | actual endpoint sensors and response APIs | orchestrate integrations |
| SOAR | Cortex XSOAR, Splunk SOAR | mature playbooks and integration ecosystems | feed KAVACH decisions into existing SOAR |
| Threat intelligence | MISP, OpenCTI, AbuseIPDB | mature indicator ecosystems | integrate and expose provenance of indicators |
| Enterprise identity | Entra, Okta | cryptographic identity and lifecycle | invoke trusted-channel verification |
| Financial communication verification | fragmented ecosystem | no obvious single incumbent dominates every layer | **this is KAVACH's core opportunity, but FCVM must be experimentally validated** |

---

# 10. THE MOST IMPORTANT COMPETITIVE REALITY

After reviewing the relevant ecosystem, the following claims **should not** be used as KAVACH's innovation claim:

- “We use AI to detect deepfakes.”
- “We detect malicious ZIP files.”
- “We fuse multiple risk scores.”
- “We automate incident response.”
- “We create attack graphs.”
- “We block C2 servers.”
- “We use C2PA.”
- “We use biometric verification.”

All of those concepts already exist independently or in combinations.

The strongest unresolved product/technical proposition is:

> **Can an event-level Financial Communication Verification Model materially improve the correctness of financial-action verification by jointly reasoning over communication authenticity, identity, authorization, malware, provenance, intent and transaction context?**

That must be an experiment, not a slogan.

---

# 11. RECOMMENDED KAVACH TECHNICAL STRATEGY AFTER THIS COMPETITIVE REVIEW

## Own

- Financial Communication Verification Model (FCVM)
- financial-event schema
- communication-to-financial-action correlation
- context-aware evidence representation
- uncertainty/conflict handling
- decision explanation
- financial-action policy boundary
- case/evidence model
- KAVACH-specific benchmark

## Integrate

- email gateway
- EDR
- IdP / passkeys
- transaction/fraud engine
- threat intelligence
- malware sandbox
- C2/firewall/SWG
- SOAR
- enterprise document systems

## Do not rebuild unnecessarily

- full email gateway
- full antivirus engine
- world-class sandbox fleet
- enterprise identity provider
- complete transaction-fraud platform
- general-purpose SIEM/SOAR
- C2PA ecosystem

This is not weakness. It is sane system architecture.

---

# 12. SITE / PROJECT DIRECTORY

## Deepfake / authenticity

- Reality Defender — https://www.realitydefender.com/
- Pindrop — https://www.pindrop.com/
- Truepic — https://www.truepic.com/
- Sensity — https://sensity.ai/
- C2PA — https://c2pa.org/
- Adobe Content Credentials — https://contentauthenticity.adobe.com/
- HyperVerge — https://hyperverge.co/
- Signzy — https://www.signzy.com/
- IDfy — https://www.idfy.com/
- iProov — https://www.iproov.com/
- BioID — https://www.bioid.com/
- Veridas — https://veridas.com/
- DuckDuckGoose — https://duckduckgoose.ai/
- Attestiv — https://www.attestiv.com/
- Vastav AI — https://vastav.ai/

## Email / BEC / enterprise communication

- Abnormal AI — https://abnormal.ai/
- Proofpoint — https://www.proofpoint.com/us/solutions/bec-protection
- FortiMail — https://www.fortinet.com/products/email-security
- Microsoft Defender for Office 365 — https://learn.microsoft.com/defender-office-365/
- Darktrace — https://www.darktrace.com/

## Malware / ZIP / sandbox

- OPSWAT MetaDefender — https://www.opswat.com/products/metadefender/core
- ANY.RUN — https://any.run/
- CAPE Sandbox — https://github.com/kevoreilly/CAPEv2
- YARA — https://github.com/Yara-Rules/rules
- ClamAV — https://www.clamav.net/
- VirusTotal — https://www.virustotal.com/

## Financial fraud / behavioural risk

- BioCatch — https://www.biocatch.com/
- Featurespace — https://www.featurespace.com/
- Feedzai — https://www.feedzai.com/
- SEON — https://www.seon.io/

## Endpoint / response

- CrowdStrike — https://www.crowdstrike.com/
- Microsoft Defender for Endpoint — https://learn.microsoft.com/defender-endpoint/
- Cortex XSOAR — https://docs-cortex.paloaltonetworks.com/
- Splunk SOAR — https://help.splunk.com/en/splunk-soar
- Darktrace RESPOND — https://www.darktrace.com/

## Threat intelligence

- MISP — https://www.misp-project.org/
- OpenCTI — https://docs.opencti.io/latest/
- AbuseIPDB — https://www.abuseipdb.com/
- MITRE ATT&CK — https://attack.mitre.org/

## Identity / trusted channel

- Microsoft Entra / FIDO2 — https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-passkeys-fido2
- Okta WebAuthn — https://developer.okta.com/docs/guides/authenticators-web-authn/main/
- FIDO Alliance — https://fidoalliance.org/

## Research / benchmarks

- ASVspoof — https://www.asvspoof.org/
- ASVspoof 5 paper — https://arxiv.org/abs/2601.03944
- DeepFakeBench — https://github.com/SCLBD/DeepfakeBench
- FaceForensics++ — https://github.com/ondyari/FaceForensics
- Celeb-DF — https://github.com/yuezunli/celeb-deepfakeforensics
- FakeAVCeleb — https://github.com/DASH-Lab/FakeAVCeleb
- AV-Deepfake1M — https://github.com/AV-Deepfake/AV-Deepfake1M
- AASIST — https://github.com/mrinmoyim/AASIST
- RawNet2 — https://github.com/eurecom-asp/rawnet2
- LipForensics — https://github.com/ahaliassos/LipForensics
- M2TR — https://github.com/CHELSEA234/M2TR
- Whisper — https://github.com/openai/whisper
- c2patool — https://opensource.contentauthenticity.org/docs/c2patool/
- Didier Stevens PDF tools — https://blog.didierstevens.com/programs/pdf-tools/

---

# 13. PAPER / RESEARCH REFERENCE INDEX

| Research / paper | Main relevance to KAVACH | KAVACH gap exposed | Reference |
|---|---|---|---|
| MesoNet | Compact face forgery baseline | Modern open-world generalization | https://doi.org/10.1109/WIFS.2018.8630761 |
| Face X-Ray | General face forgery cues | Need unseen-generator testing | CVPR 2020; verify source before deck |
| Frequency-Aware Clues | Frequency-domain forensic evidence | Compression destroys clues | ECCV 2020 |
| RawNet2 | Raw-waveform spoof detection | Need telecom/channel robustness | https://doi.org/10.1109/ICASSP39728.2021.9413977 |
| LipForensics | Temporal/lip forensic cues | Need localized analyst evidence | https://doi.org/10.1109/CVPR46437.2021.00500 |
| Self-Blended Images | Generalization strategy | Need financial-domain validation | CVPR 2022 |
| AASIST | Audio anti-spoofing | Need domain shift and cost calibration | https://doi.org/10.1109/TASLP.2022.3168128 |
| DIRE | Diffusion-image detection | Image detector generalization | ICCV 2023 |
| De-Diffusion | Robust synthetic-image detection | Open-world generalization | CVPR 2024 |
| ASVspoof 5 | Modern speech spoof benchmark | Need financial telephony benchmark | https://arxiv.org/abs/2601.03944 |
| DeepFakeBench | Standardized benchmark framework | Need system-level benchmark | https://github.com/SCLBD/DeepfakeBench |
| AV-Deepfake1M | Large multimodal AV dataset | Need financial context labels | https://github.com/AV-Deepfake/AV-Deepfake1M |
| AV-LMMDetect | Modern AV multimodal model | Need FCVM comparison | https://arxiv.org/abs/2604.24890 |
| Divide and Conquer multimodal localization | Cross-modal localization | Need evidence segments | https://arxiv.org/abs/2602.23393 |
| MEADE | Malicious attachment detection | Need financial-context malware correlation | https://doi.org/10.1109/THS.2018.8574202 |
| Email Forensics Using ML/DL | Email security/forensics | Need modern BEC + financial-action validation | https://ieeexplore.ieee.org/abstract/document/11265002 |
| C2PA security critique | Provenance limitations | Need layered provenance policy | https://arxiv.org/abs/2602.00209 |

**Note:** The KAVACH master contains a much longer bibliography. This index intentionally highlights papers with a direct implication for the final implementation. The full bibliography should remain in `KAVACH.md` and source annexes to avoid redundancy.

---

# 14. KAVACH BUILD GAPS → ACTION TABLE

| Gap | What must happen | Build / Integrate / Research |
|---|---|---|
| FCVM has no empirical superiority evidence | Create controlled financial-context experiment | Research + Build |
| Financial multimodal dataset missing | Generate synthetic/consented event-level dataset | Build |
| Enterprise email behavior weak | Ingest from existing mail security / M365 gateway | Integrate |
| ZIP engine immature | Build safe static pipeline, integrate specialist sandbox | Both |
| EDR action unavailable | CrowdStrike/Defender connector | Integrate |
| C2 control unavailable | DNS/firewall/SWG/EDR connector | Integrate |
| Identity infrastructure missing | Entra/Okta/FIDO2 integration | Integrate |
| Transaction risk weak | Consume payment/fraud-engine context | Integrate |
| Cross-event causality weak | Strong correlation IDs + temporal graph | Build |
| Provenance incomplete | C2PA + channel-aware missingness | Build/Integrate |
| Explainability weak | Evidence segments + reason codes + lineage | Build |
| Autonomous response safety weak | allowlists + TTL + rollback + human override | Build |
| Biometrics create honeypot | protected templates + tenant isolation | Build |
| India language robustness weak | Hindi/Hinglish/regional test set | Research |
| Real-time SLA unknown | benchmark every pipeline stage | Research |
| Regulatory/evidence uncertainty | verify current primary sources | Research/Governance |
| Market differentiation vulnerable | validate FCVM against competitors/baselines | Research/Product |

---

# 15. FINAL STRATEGIC CONCLUSION

After removing marketing language and comparing KAVACH against actual adjacent systems, the picture is clear:

**KAVACH is not differentiated because it has AI detection, malware scanning, risk scoring or automated response.** Established products already do each of those things, often far better than a 48-hour prototype could.

The defensible opportunity is the **financial communication boundary**:

> A single business event contains a communication, a claimed identity, a requested financial action, attachments/media, authorization state, transaction context and potentially a cyber-compromise path. KAVACH should determine whether those pieces jointly justify trusting the requested financial action.

The next step is therefore not to add more detectors merely to make the architecture larger. It is to **prove FCVM**.

The strongest experimental design is:

```text
Same communication/media
        ↓
Different financial contexts
        ↓
Compare:

A. Media-only detector
B. Simple weighted signal fusion
C. Strong multimodal baseline
D. KAVACH FCVM
        ↓
Measure:
- precision / recall
- false positive cost
- false negative cost
- calibration
- robustness to compression/noise
- decision correctness for financial action
```

If FCVM demonstrably improves the correctness of the financial-action decision, **that is a genuine technical contribution**.

If it does not, then KAVACH remains a strong security-integration product concept but should not pretend that the model itself is novel.

That distinction should remain explicit in the product, the architecture, the technical paper-style explanation and the hackathon pitch.

---

# 16. SOURCES REFERENCED DIRECTLY IN THIS DELTA

### Official / primary product and standards sources

1. Microsoft Defender for Endpoint — device isolation and automatic attack disruption: https://learn.microsoft.com/defender-endpoint/respond-machine-alerts
2. Microsoft Defender for Endpoint — isolate machine API: https://learn.microsoft.com/en-us/defender-endpoint/api/isolate-machine
3. Microsoft Defender XDR — automatic attack disruption: https://learn.microsoft.com/en-us/defender-xdr/automatic-attack-disruption
4. MITRE ATT&CK M1037 — Filter Network Traffic: https://attack.mitre.org/mitigations/M1037/
5. SEBI — Boss Scam warning, 17 July 2026: https://www.sebi.gov.in/media-and-notifications/press-releases/jul-2026/caution-to-regulated-entities-and-listed-companies-boss-scam_102919.html?outputType=chromeless
6. INTERPOL — Global Financial Fraud Threat Assessment 2026: https://www.interpol.int/News-and-Events/News/2026/INTERPOL-report-warns-of-increasingly-sophisticated-global-financial-fraud-threat
7. FBI — Business Email Compromise: https://www.fbi.gov/how-we-help-you/common-frauds-and-scams/business-email-compromise
8. C2PA specification: https://spec.c2pa.org/
9. C2PA organization: https://c2pa.org/
10. Adobe Content Credentials: https://contentauthenticity.adobe.com/
11. ASVspoof: https://www.asvspoof.org/

### Commercial / technology landscape

12. Abnormal AI: https://abnormal.ai/
13. Proofpoint BEC: https://www.proofpoint.com/us/solutions/bec-protection
14. FortiMail: https://www.fortinet.com/products/email-security
15. OPSWAT MetaDefender: https://www.opswat.com/products/metadefender/core
16. ANY.RUN: https://any.run/
17. BioCatch: https://www.biocatch.com/
18. Featurespace: https://www.featurespace.com/
19. Feedzai: https://www.feedzai.com/
20. CrowdStrike: https://www.crowdstrike.com/
21. Cortex XSOAR: https://docs-cortex.paloaltonetworks.com/
22. Splunk SOAR: https://help.splunk.com/en/splunk-soar
23. MISP: https://www.misp-project.org/
24. OpenCTI: https://docs.opencti.io/latest/
25. AbuseIPDB: https://www.abuseipdb.com/
26. Microsoft Entra FIDO2/passkeys: https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-passkeys-fido2
27. Okta WebAuthn: https://developer.okta.com/docs/guides/authenticators-web-authn/main/

### Research / projects

28. ASVspoof 5: https://arxiv.org/abs/2601.03944
29. DeepFakeBench: https://github.com/SCLBD/DeepfakeBench
30. FaceForensics++: https://github.com/ondyari/FaceForensics
31. Celeb-DF: https://github.com/yuezunli/celeb-deepfakeforensics
32. FakeAVCeleb: https://github.com/DASH-Lab/FakeAVCeleb
33. AV-Deepfake1M: https://github.com/AV-Deepfake/AV-Deepfake1M
34. AASIST: https://github.com/mrinmoyim/AASIST
35. RawNet2: https://github.com/eurecom-asp/rawnet2
36. LipForensics: https://github.com/ahaliassos/LipForensics
37. M2TR: https://github.com/CHELSEA234/M2TR
38. Whisper: https://github.com/openai/whisper
39. CAPE Sandbox: https://github.com/kevoreilly/CAPEv2
40. YARA rules: https://github.com/Yara-Rules/rules
41. Didier Stevens PDF tools: https://blog.didierstevens.com/programs/pdf-tools/

### Incidents / case reporting

42. Arup / Financial Times: https://www.ft.com/content/b977e8d4-664c-4ae4-8a8b-eb93bdf785ea
43. Ferrari / Bloomberg Law: https://news.bloomberglaw.com/daily-labor-report/ferrari-narrowly-dodges-deepfake-scam-simulating-deal-hungry-ceo
44. WPP / Guardian: https://www.theguardian.com/technology/article/2024/may/10/ceo-wpp-deepfake-scam
45. WPP / OECD.AI: https://oecd.ai/en/incidents/2024-05-10-e24d
46. Fideuram/Intesa / Reuters, 25 September 2026: https://www.reuters.com/legal/government/ai-messaging-scam-costs-italys-top-bank-intesa-millions-sources-say-2026-09-25/

---

# 17. NOTES ON CLAIM VERIFICATION

The KAVACH source corpus contains a mixture of primary research, vendor claims, technical blogs, news reporting and representative/synthesized numbers. This file intentionally avoids turning every number in the corpus into a fact.

Before using a claim in the final hackathon deck, verify:

- exact paper title;
- author list;
- venue;
- DOI/URL;
- benchmark dataset version;
- exact metric and test split;
- whether a capability is GA, beta or experimental;
- vendor-reported versus independent validation;
- incident loss figure and status;
- legal/regulatory interpretation against primary text;
- current version/date for standards and products.

Keep these evidence states visible in internal research:

**VERIFIED → INDEPENDENTLY CORROBORATED → VENDOR-REPORTED → REPORTED BUT NOT INDEPENDENTLY VERIFIED → REPRESENTATIVE / ILLUSTRATIVE → UNSUPPORTED / EXCLUDED.**

---

# 18. FINAL KAVACH CHECK

Before freezing the product architecture, the team should be able to answer yes to all of the following:

- Is the primary financial event sharply defined?
- Is the FCVM experimentally distinguishable from simple risk scoring?
- Is every major detector a source of evidence rather than an unquestioned oracle?
- Can KAVACH safely process malicious ZIPs without executing them on the core host?
- Can KAVACH correlate communication evidence with a real or simulated financial event using reliable IDs?
- Can it handle missing/conflicting signals?
- Can it explain exactly why an action was held?
- Can automated response be scoped, audited, reversed and tested safely?
- Are endpoint, identity, network and SOAR actions explicitly defined as integrations rather than hand-wavy capabilities?
- Is the benchmark financial-context-aware?
- Are India-specific language/channel transformations tested?
- Are claims about competitors and incidents evidence-labelled?
- Is the product positioned as complementary to existing enterprise security stacks rather than pretending to replace them?

If any answer is no, that is a **build gap**, not a slide-design problem.

---

## Bottom line

The competitive landscape actually makes KAVACH's mission **more precise**, not less viable. Mature systems already dominate the individual layers. KAVACH should not beat them at email filtering, antivirus, sandboxing, endpoint detection, identity or payment fraud independently.

KAVACH should instead prove that it can **consume those signals, understand their relationship to a specific financial action, and make a better financial-communication verification decision than artifact-only or siloed systems.** The FCVM experiment is therefore the critical piece that determines whether KAVACH is merely a smart integration layer or a genuinely differentiated technical product.
