# Official sources and evidence register

Verified 14 September 2026. Facts, design assumptions and future validation are separate. Links point to original publishers. Source PDFs were read locally after download where browser extraction failed. No customer interviews or bank endorsements have been obtained.

## SIAP 2026: governing application material

1. [CBK announcement, 1 September 2026](https://www.cbk.gov.kw/en/cbk-news/announcements-and-press-releases/press-releases/2026/09/202609010800-cbk-launches-the-strategic-initiative-accelerator-program-at-the-innovation-hub). Application window: 1 September to 1 October 2026. No cutoff hour is stated. Applicant target: email before 1 October, preferably 28 September.
2. [Linked 2026 Strategic Initiative Accelerator Program brief](https://www.cbk.gov.kw/en/images/pr-iap-sep-2026-172217_v10_tcm10-172217.pdf), three pages. This supersedes the older 2024/2025 briefs for this application. Eligible: Kuwaiti individuals aged at least 18, without direct or indirect attachment to an existing fintech or financial institution. Idea must fit themes; teamwork, development commitment and receptiveness to mentoring are required. Individual applicants only.

Themes: data analytics/predictive modelling; AI; cybersecurity/digital trust/resilience; cryptography/secure technologies; digital transformation/emerging technologies. Haris selects **Cybersecurity, Digital Trust & Resilience**.

Exclusions include applications primarily seeking licensing or sandbox participation, electronic payments, wallets, payment gateways, open banking implementation, and existing commercial products requiring regulatory approval. Participation confers no regulatory approval, licence, sandbox admission, or commitment to adopt, implement or fund an initiative.

### Exact field coverage from pages 2–3

Send to **Accelerator@cbk.gov.kw**. Applicant information: Full Name; Nationality; Year of Birth; Email Address; Contact Number; Current Occupation; Academic & Professional Background. Background details: Educational Qualification; Field of Study; Professional Experience (if applicable); Technical Skills; Research Experience (if applicable). Proposal information: Selected Program Theme; Initiative Summary; Problem Statement; Innovative Aspects. Development stage choices: Idea, Concept, Prototype, Proof of Concept (PoC), Minimum Viable Product (MVP). No Civil ID, word limit, mandatory pitch deck or funding field appears in this 2026 brief. Supplementary material in this package supports the application, rather than representing extra official requirements.

## Other official material, distinct scope

3. [Wolooj framework](https://www.cbk.gov.kw/en/legislation-and-regulation/innovation-hub/innovation-framework): the separate regulatory sandbox journey includes pre-application, application, guidance, pilot and graduation. Its pre-application form and business plan go to innovationhub@cbk.gov.kw. Do not substitute that form/address for SIAP or imply SIAP selection advances its stages.
4. [CBK CORF landing page](https://www.cbk.gov.kw/en/supervision/cyber_operational_resilience_framework) and [389-page CORF v1.0, 3 December 2025](https://www.cbk.gov.kw/en/images/corf-170113_v10_tcm10-170113.pdf). Read the structure, applicability, baselines and relevant controls. CORF applies to CBK-regulated entities. Haris supplies a limited technical evidence example; it does not certify an entity or satisfy CORF as a whole. Precise control references and gaps: `cbk-control-map.md`.

## User and risk evidence

5. [NBK Annual Report 2025](https://www.nbk.com/dam/jcr%3A73b1509e-5280-4ef3-a29a-392c1b565299/nbk-annual-report-2025-e.pdf): describes Microsoft partnership for enterprise AI productivity adoption. Evidence that AI adoption is relevant locally, not proof of a Haris buyer, the proposed RM workflow, or inadequate existing safeguards.
6. [Boubyan Annual Report 2025](https://getapp.bankboubyan.com/media/filer_public/67/e2/67e2e79a-c6a0-40e1-aeeb-6c6fc73df37a/view_report.pdf): describes an AI assistant using Kuwaiti dialect. Supports local Arabic AI relevance; no Haris demand or customer relationship is inferred.
7. [Microsoft indirect prompt-injection defence guidance, updated March 2026](https://learn.microsoft.com/en-us/security/zero-trust/sfi/defend-indirect-prompt-injection): recommends layers, least privilege, information-flow restrictions and human review. Supports containment architecture; not a guarantee against all injection.
8. [OWASP prompt injection prevention](https://cheatsheetseries.owasp.org/cheatsheets/LLM_Prompt_Injection_Prevention_Cheat_Sheet.html) and [Excessive Agency, 2025 edition](https://genai.owasp.org/llmrisk/llm062025-excessive-agency/): untrusted content can steer models; excessive tool permissions/autonomy magnify harm. Use the named edition, not a claim about the current ranking.

## Alternatives, first-party capability documentation

9. [NVIDIA NeMo runtime security FAQ](https://docs.nvidia.com/nemo/guardrails/resources/runtime-security-faq) and [catalog](https://docs.nvidia.com/nemo/guardrails/configure-guardrails/guardrail-catalog): input/output/retrieval and tool rails, PII and evidence capabilities overlap substantially. Actual performance depends on configuration.
10. [Presidio overview](https://microsoft.github.io/presidio/), [entities](https://microsoft.github.io/presidio/supported_entities/): extensible local PII identification/anonymization, with explicit warning that automated recognition cannot find all sensitive information.
11. [LiteLLM guardrails](https://docs.litellm.ai/docs/proxy/guardrails/quick_start), [RBAC](https://docs.litellm.ai/docs/proxy/access_control): existing gateway integrations and access controls. Haris does not claim to invent either.


12. [Ollama chat API](https://docs.ollama.com/api/chat) and [Qwen2.5:0.5b model details](https://ollama.com/library/qwen2.5:0.5b): local inference route, model size and Apache 2.0 licence information. The actual downloaded model digest is recorded in `evidence/live-final/metrics.json`.

## Validation still needed

The RM case-preparation workflow, its frequency, cost, frustration, procurement owner, willingness to pay and alternatives in a target bank remain hypotheses. No interviews, incidents at named banks, savings, adoption numbers, market size or investment commitments are asserted. Sources establish relevance, controls and technical risk, not product-market fit.


# CORF control-to-evidence map

Source: [CBK CORF v1.0, 3 December 2025](https://www.cbk.gov.kw/en/images/corf-170113_v10_tcm10-170113.pdf). PDF page numbers below match printed page numbers. Mapping is engineering interpretation, not legal advice, a certification or a claim of complete compliance. The entity remains responsible for applicability and governance.

| CORF reference | Relevant expectation, paraphrased | Prototype evidence | Remaining bank implementation |
|---|---|---|---|
| Ch.4 5.6.1.4, p.247 | Need-to-know, least-privilege access | Server tenant/customer scope; model and tool allowlists; API isolation tests | Bank entitlement source, approval lifecycle, regular access reviews |
| Ch.4 5.6.1.6–7, p.247 | Separated duties and distinct identities | RM/reviewer separation; requester cannot approve; replay/concurrency tests | Bank IdP/MFA, joiner/mover/leaver process and privileged-access controls |
| Ch.4 5.6.1.9, p.247 | Protect authentication material | scrypt password hashes, random expiring sessions, HttpOnly cookie | TLS ingress, passwordless/MFA, enterprise credential custody; local HTTP is demo-only |
| Ch.4 5.11.1.3, p.255 | Protect data confidentiality, integrity and availability | Minimized case fields, synthetic PII redaction, scope isolation | Classification, encryption at rest, retention, validated PII coverage and availability |
| Ch.4 5.12.1.3–4, p.257 | Sufficient event metadata and tamper protection | Actor/time/source/action/outcome, policy version, English/Arabic reason, HMAC/hash chain | Protected SIEM/WORM storage, independent anchors, retention, time trust and operations |
| Ch.4 7.1.1.3/6, p.268 | Threat modelling and adequate security testing | Threat model, 48 fixed cases, negative authorization and browser tests | Independent penetration testing, representative data and release assurance |
| Ch.4 7.1.2.2, p.269 | Defences against AI adversarial attacks | Bounded injection checks plus tool/customer containment even for missed prompts | Stronger detectors, threat updates, red teaming, model-specific adversarial evaluation |
| Ch.4 7.1.2.3, p.269 | Protect training/inference data | No training or customer data ingestion; redaction before local inference | Privacy assessment, approved purpose, governance and bank-classified data protection |
| Ch.4 7.1.2.4–5, p.269 | Auditability and ongoing model evaluation | Decisions trace to policy/content digest; reproducible evaluation | Haris does not explain model reasoning or validate credit/fraud decisions; ongoing drift/reliability monitoring needed |
| Ch.4 6.1.1.2–4, p.265 | Significant IT third-party approval and due diligence | Dependency and founder limitations disclosed | Bank/vendor assessment and applicable CBK approval before engagement |
| Ch.4 7.1.1.2, p.268 | CBK approval process for regulated entities adopting emerging technology | Explicit deployment gate in regulatory case | Entity submits required risk/adoption information at least one month before go-live |
| Ch.4 7.2.1.2–3, p.270 | Cloud data/residency governance and approval | Prototype makes no cloud inference calls | Separate assessment and applicable approval if a future cloud service interacts with sensitive systems |

This application is an individual cybersecurity initiative for SIAP. It is not an application to operate a financial service or enter the regulatory sandbox. A future bank implementation may require approvals and controls independently of accelerator participation.
