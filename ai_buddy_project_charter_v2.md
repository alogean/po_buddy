# AI Buddy — Project Charter

---

## 1. General Information

| Field | Value |
|-------|-------|
| **Project name** | AI Buddy — UZH Digital Study Companion |
| **Project code** | PRJ-AIB-2026 |
| **Version / date** | v2.0 — February 20, 2026 |
| **Charter author** | Antoine Logean (PM / Product Owner) |
| **Project sponsor** | UZH Digital Charter |
| **Project manager** | Antoine Logean — DSI, University of Zurich |
| **Prepared by** | Antoine Logean (Product Workstream Lead) |

---

## 2. Background and Justification

### 2.1 Background

The AI Buddy project was initiated as a direct response to the **DSI Strategy Lab 2023** position paper on *"AI in Education, Research, and Innovation"*, produced during a workshop on the Weissenstein (Solothurn) from August 20–22, 2023 by a consortium of 20 experts from UZH, ETH Zürich, industry, and government. Recommendation 1.2 of that paper explicitly called for:

> *"Es soll darauf hingearbeitet werden, dass jede:r Studierende einer Hochschule einen 'KI-Buddy' nutzen kann, der nicht nur der reinen Wissensvermittlung dient, sondern die Studierenden als Diskussions- und Sparringpartner durch das Studium begleitet."*
>
> ("Every student at a university should be able to use an 'AI Buddy' that not only serves to transmit knowledge but also accompanies them through their studies as a discussion and sparring partner.")

The paper identified three core functions for such an AI companion: (1) knowledge transmission through university resources, (2) personalized study plan advisory, and (3) peer networking. It recommended a participative, modular in-house development approach with concurrent resolution of legal and privacy questions.

**Organizational context:** Students at the University of Zurich face significant challenges navigating their academic journey. Information is scattered across multiple platforms (OLAT, Student Services, faculty websites, the VVZ course catalog) with no unified access point. Module planning is complex, administrative burden is high, and digital literacy support from lecturers is limited — despite 97% of students already using AI tools. A March 2024 survey of 926 UZH students revealed that 90% use ChatGPT and 77% use DeepL, yet only 14% receive AI skills training from UZH lecturers. The primary learning sources are online resources (89%) and peers (48%).

**Strategic alignment:** The project directly serves the UZH Digital Charter's AI in Education strategic objective. It is part of the DSI Strategic Projects portfolio and is designed from the ground up to comply with the Swiss Data Protection Act, GDPR, and UZH AI Principles (UZH Directing Principles for AI).

### 2.2 Justification / Business Case

**Student demand is validated:** 64.5% of 926 surveyed students indicated they would likely use an AI Buddy (Mean = 4.79/7). The most desired functions are editor/proofreading (78%), reference management (68.5%), course/content advising (65.8%), and time management (58.7%). Students with higher digital literacy show significantly higher adoption likelihood (F(2,542) = 30.5, p < 0.001).

**Key barrier is awareness, not rejection:** 38.9% of students were unaware of AI-related courses at UZH, and 54% were unfamiliar with UZH AI principles. This signals high upside potential once the tool is visible.

**Expected benefits:**

- **Student retention and success:** Centralized access to regulations, deadlines, and study planning reduces administrative friction and information gaps that contribute to student disorientation.
- **Operational efficiency:** Reduces repetitive queries to the Dekanat, study advisors, and student services by providing 24/7 self-service for common administrative questions.
- **Institutional innovation positioning:** Positions UZH as a leader in AI-assisted education within the Swiss and European university landscape.
- **Scalable model:** The "chatbot as a service" architecture enables expansion to all UZH faculties multiplying institutional value.
- **AI literacy through usage:** By interacting with AI Buddy, students organically develop AI competencies — directly addressing DSI Strategy Lab Recommendation 1.1.

---

## 3. Objectives and Expected Results

### 3.1 Project Objectives (SMART)

| ID | Objective | Target | Measurement | Timeline |
|----|-----------|--------|-------------|----------|
| OBJ-1 | Deploy AI Buddy 2.0 for the full WWF Faculty | Zero critical (P0/P1) bugs at release | Release metrics, QA gate checklist | February 15, 2026 |
| OBJ-2 | Achieve student adoption of >50% of WWF students | >50% registered users within first semester | Registration analytics via Entra ID | By June 2026 |
| OBJ-3 | Attain response accuracy >90% on validated queries | >90% correct answers (>80% human agreement) | DeepEval automated pipeline + human validation | At release and ongoing |
| OBJ-4 | Maintain full Swiss privacy compliance | Zero data breaches, GDPR audit passed | Privacy audit, consent mechanism validation | Continuous |
| OBJ-5 | Establish a scalable faculty expansion model | 2–4 week onboarding cycle for new faculties | Onboarding Playbook validated on first expansion | March 2026+ |

### 3.2 Key Deliverables

| Deliverable | Target Date | Acceptance Criteria |
|-------------|-------------|---------------------|
| **AI Buddy 2.0 Production Release** | February 23, 2026 | All Cat 1–3 tests passed, Dekanat QC approved, zero P0/P1 bugs |
| **WWF Data Source Catalog** | February 1, 2026 | Complete course catalog for all 4 WWF departments (DF, DBA, ECON, IFI) |
| **Ground Truth Catalog** | February 20, 2026 | 90+ validated Q&A pairs across 3 test categories |
| **Automated Testing Framework** | February 20, 2026 | DeepEval operational |
| **Testing Playbook** | February 27, 2026 | Documented test process, bug classification schema, and procedures |
| **Onboarding Playbook** | February 27 | Faculty expansion process documented and ready for first use |
| **Communication Plan** | February 2026 | Multi-channel launch strategy across 4 institutional carriers, 4 channels |

### 3.3 Success Metrics

| KPI | Target | Method |
|-----|--------|--------|
| Adoption Rate | >50% of WWF students | Registration analytics |
| API Response Latency (P95) | <2 seconds | Performance monitoring |
| Net Promoter Score (NPS) | >50 | Post-usage surveys |
| Student Awareness | >80% of WWF students | Pre-launch surveys |
| Response Accuracy | >90% correct | DeepEval + human validation |
| System Availability | >99% uptime | Infrastructure monitoring |

**DeepEval Evaluation Weights:**

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Correctness | 40% | Factual response vs. Ground Truth |
| Completeness | 25% | All key points present |
| Relevance | 20% | Answers the question asked |
| Helpfulness | 15% | Actionable, clear next steps |

---

## 4. Scope

### 4.1 In-Scope (AI Buddy 2.0 — Q1 2026)

**Content Coverage:** Full WWF Faculty — Banking & Finance, Business Administration, Economics, and Informatics — for all Bachelor and Master programs (excluding MSc UZH ETH in Quantitative Finance).

**Functional features:**

- **(F_1) Course Information Hub:** Display courses from processed VVZ export with official descriptions, ECTS credits, dependencies (Knowledge Graph), lecture/tutorial schedules, exam dates. Basic search/filtering by name, keyword, and time slots.
- **(F_2) Study Regulation & Process Guidance:** RAG-based Q&A on study regulations (PDFs/text) for all 4 WWF departments. Automated ingestion pipeline for selected UZH websites. Content includes FAQs, process descriptions (module booking, enrollment), IT info, exam periods/rules, health/support services, campus building info. Curated links to official UZH pages for critical deadlines.
- **(F_3) University Service & Resource Locator:** RAG-based Q&A using scraped web data for IT/support services, health/counseling, tutoring/mentoring programs, campus maps/building directories, and primary student associations (Fachvereine) for Economics and Informatics.

**Non-functional features:**

- **(NF_1) Data Sources Management:** VVZ export → cleaning → parsing → validation → Knowledge Graph. Manual enrichment with topics/competencies (AI-assisted). PDFs + automated web scraping pipeline.
- **(NF_2) Privacy & Security:** UZH data privacy guidelines compliance, minimal PII collection, user consent mechanism, data management UI, Microsoft Entra ID authentication, input sanitization, dependency scanning, secure configuration.

**Optional / Stretch:**

- **(F_4) Advanced Agent Capabilities:** Agentic memory (Mem0), artifact generation (Markdown/HTML summaries), generic MCP integrations, simple visualization.

### 4.2 Out-of-Scope (Until post-release)

- Expansion beyond WWF Faculty (planned for v3.0)
- Learning content creation and tutoring functions
- OLAT integration
- Advanced analytics and automated data ingestion
- Personalized study plan generation (planned for v3.0, September 2026)
- Student Information System (SIS) integration
- Calendar export (.ics)
- ASVZ integration
- MCP: Mensa
- Enhanced PII removal via LLM Guard (planned for v3.0)
- Local LLMs for sensitive query categorization (planned for v3.0)

---

## 5. Stakeholders and Roles

### 5.1 Stakeholder Register

| Name | Role | Organization | Interest | Influence | Engagement |
|------|------|--------------|----------|-----------|------------|
| Prof. Dr. Abraham Bernstein | Executive Sponsor / DSI Director | DSI | High | High | Supportive |
| Dr. Alexandra Jansky | Educational Development Lead | Lehrstelle | High | High | Supportive |
| Prof. Dr. Claudia Witt | DSI Director | DSI | High | High | Supportive |
| Prof. Dr. Titus Mangham-Neupert | DSI Director | DSI | High | High | Supportive |
| Michelle Stärke | Steering Board Member / Studivers | Digital Charter | High | Medium | Supportive |
| WWF Dekanat (Harald C. Gall) | Faculty Administration | WWF | High | Medium | Supportive |
| Susanne Bürchler | ZI Portfolio Manager | ZI | Medium | Medium | Neutral |
| Priska Feichter | Head of Social Media | UZH Communications | Medium | Medium | Supportive |
| Ruben Kranendonk | Communication | UZH.ai | Medium | Medium | Supportive |
| Gil | Data Protection Advisor | UZH Legal | Medium | High | Neutral |
| Roger Gfroerer | Career Services | UZH | Low | Low | Interested |
| WWF Students | End Users | WWF | High | Low | Varies |
| WWF Lecturers | Content Stakeholders | WWF | Medium | Medium | Neutral |

### 5.2 Roles and Responsibilities

| Role | Name | Responsibility |
|------|------|----------------|
| **Executive Sponsor** | UZH Digital Charter Michelle Staerke | Strategic direction, funding authority, escalation decisions, release approval (Accountable) |
| **PM / Product Owner** | Antoine Logean | Day-to-day management, stakeholder alignment, product decisions, communication, compliance, testing coordination |
| **Tech Lead KlickerUZH** | Roland Schläfli | Technical architecture, dev team leadership, ZI coordination, infrastructure, DevOps |
| **Tech Lead AI Buddy** | Michael Wechner | Development support, technical decisions |
| **Content Lead** | Johanna Braun | WWF faculty relations, data source catalog, expert agents, quality testing, Dekanat coordination |
| **PostDoc Researcher** | Oriane Camille Iris Pierrès | AI Buddy vision, branding, student requirement engineering, usability studies |
| **User Testing / Studivers** | Michelle Stärke | Usability studies, tester framework management, steering board member |

### 5.3 RACI Matrix

| Deliverable / Decision | Sponsor (Michelle) | PM/PO (Antoine) | Tech Lead (Roli) | Content Lead (Johanna) | Research (Oriane) | ZI |
|------------------------|:-------------------:|:----------------:|:-----------------:|:---------------------:|:-----------------:|:---:|
| Project Charter Approval | A | R | C | C | I | I |
| Technical Architecture | I | A | R | C | I | C |
| Data Source Catalog | I | A | C | R | I | I |
| WWF Content Accuracy | A | I | I | R | C | I |
| Testing Strategy | I | A | R | R | C | I |
| Release Decision | A | R | C | C | I | C |
| Communication Strategy | I | R | I | R | I | I |
| Faculty Expansion | A | R | C | R | I | C |
| Privacy Compliance | A | R | C | I | I | C |

*R = Responsible | A = Accountable | C = Consulted | I = Informed*

---

## 6. Project Organization

### 6.1 Organizational Structure

**Steering Committee** — Quarterly meetings (March, June, September, December):

| Member | Role |
|--------|------|
| Prof. Dr. Abraham Bernstein | Chair / Executive Sponsor |
| Prof. Dr. Claudia Witt | DSI Director |
| Prof. Dr. Titus Mangham-Neupert | DSI Director |
| Dr. Alexandra Jansky | Educational Development Lead |
| Michelle Stärke | Digital Charter |
| Prof. Dr. Markus Christen | DSI |


**Three-Workstream Model:**

**1. Development Workstream (Lead: Roland Schläfli)**
- AI Platform development, Data Platform, Infrastructure & Deployment
- Technical stakeholder coordination (ZI, etc.)

| Team Member | FTE % |
|-------------|-------|
| Roland (Roli) | 20% |
| Max | 30% |
| Patrick | 10% |
| Antonio | 10% |
| Alex Achotian | 40% |
| Lena Fiedor | 40% |

**2. Content Workstream (Lead: Johanna Braun)**
- Data Source Catalog management, prompt / expert agent design, quality testing
- Stakeholders: Dekanat, WWF, subject-specific experts

| Team Member | FTE % |
|-------------|-------|
| Johanna Braun | 10% |
| Semester Assistant | 30% |

**3. Product Workstream (Lead: Antoine Logean)**
- Communication strategy & execution, data analysis & bug tracking, compliance, testing / usability, evaluations
- Stakeholders: Steering Board, sponsors

| Team Member | FTE % |
|-------------|-------|
| Antoine Logean | 100% |
| Michael Wechner | TBD% |
| Oriane Pierrès | 10% |
| Michelle Stärke | TBD% |

**Agile Cadence:**
- Sprint duration: 3 weeks (extended from 2 weeks based on team learning)
- AI Buddy Days: Full team review/demo at each sprint iteration
- Sprint Review + Retrospective at end of each sprint

**Decision Authority Matrix:**

| Decision Type | Authority Level | Response Time |
|---------------|-----------------|---------------|
| Scope changes requiring additional resources | Steering Committee | Next quarterly meeting |
| Budget variance > 10% | Project Sponsor | 3 business days |
| Schedule changes < 2 weeks | Project Manager | 24 hours |
| Technical architecture decisions | Tech Lead + PM | 48 hours |
| Content accuracy / regulations | Content Lead + Faculty | 1 week |
| Resource allocation within team | Project Manager | 24 hours |
| External communication | PM with DSI approval | 48 hours |

### 6.2 Required Resources

**Human resources:** ~3.5 FTE total across three workstreams (see breakdown above).

**Infrastructure:**

| Component | Provider | Notes |
|-----------|----------|-------|
| Azure Kubernetes Service (AKS) | Microsoft Azure | Zedi-Cloud (Swiss-hosted) |
| Azure OpenAI | Microsoft Azure | Primary LLM inference |
| Vertex AI | Google Cloud | Secondary LLM provider |
| Neo4j | Self-hosted on AKS | Knowledge Graph |
| Milvus | Self-hosted on AKS | Vector Store |
| Langfuse | Self-hosted | Observability |
| GitLab CI | UZH Infrastructure | CI/CD pipeline |

**Technology stack summary:**
- Frontend: LibreChat (customized) + Microsoft Entra ID (SSO)
- Backend: Python / FastAPI on AKS
- Pipeline orchestration: Haystack
- Agentic memory: Mem0 + Neo4j
- RAG: Hybrid search with optimized chunking and contextual embeddings
- Local LLM: Qwen 3 on AKS (privacy-sensitive tasks)
- Infrastructure as Code: Pulumi (TypeScript/Python) + Terraform
- Data pipelines: Custom VVZ processing (P0), Firecrawl web scraping (P0), Docling PDF extraction (P1)

### 6.3 Budget Estimate

**Funding sources:**
- **Primary:** DSI (Digital Society Initiative) budget
- **Secondary:** UZH Digital Charter funding

**Constraints:**
- Communication activities limited to ~4 hours/week
- Infrastructure costs are covered within the DSI and ZI cloud allocation (Zedi-Cloud)
- No dedicated external vendor budget; all development is in-house

---

## 7. Schedule and Milestones

| Field | Value |
|-------|-------|
| **Planned start date** | March 2025 |
| **Planned end date (v2.0)** | February 23, 2026 |
| **Current phase** | AI Buddy 2.0 — Post-Release (launched February 23, 2026) |

### 7.1 Key Milestones

| ID | Milestone | Target Date | Gate / Checkpoint |
|----|-----------|-------------|-------------------|
| M-0 | Project Kickoff | March 2025 | Charter Approved |
| M-1 | AI Buddy 1.0 Pilot Release | September 2025 | Finance & Informatics programs deployed |
| M-2 | MVP Validation Complete | December 2025 | OEC-Dekanat QC Passed |
| M-3 | Testing Infrastructure Ready | January 12, 2026 | DeepEval + Ground Truth operational |
| M-4 | Category 1–3 Testing Complete | January 31, 2026 | >85% pass rate, 0 P0/P1 bugs |
| M-5 | UAT Complete | February 7, 2026 | Student validation passed |
| M-6 | Release Readiness (Go/No-Go) | February 10, 2026 | Go/No-Go decision by Sponsor |
| **M-7** | **WWF 2.0 Deployment** | **February 23, 2026** | **Production Ready** |
| M-8 | Faculty Expansion Start | March 2026+ | Onboarding Playbook Ready |
| M-9 | AI Buddy 3.0 Release | September 2026 | New faculties + personalized study plans |
| M-10 | ZI Ecosystem Integration | 2026 (TBD) | Integration specifications complete |

### 7.2 Phase Overview

| Phase | Start | End | Key Activities | Exit Criteria |
|-------|-------|-----|----------------|---------------|
| **AI Buddy 1.0** | Mar 2025 | Sep 2025 | Pilot with Finance & Informatics, 1st/3rd semester students | Pilot deployed |
| **AI Buddy 2.0 Dev** | Sep 2025 | Feb 2026 | WWF scope extension, testing, bug fixes | All tests passed |
| **Release Readiness** | Jan 2026 | Feb 15, 2026 | Category 1–3 testing, bug burn-down, UAT | Release approved |
| **Post-Release** | Mar 2026+ | Ongoing | Faculty onboarding, feature enhancements, v3.0 development | Continuous |

### 7.3 Testing Plan (40 days pre-release)

| Phase | Period | Duration | Focus |
|-------|--------|----------|-------|
| Phase 1 | Jan 6–12 | 7 days | Test infrastructure & preparation |
| Phase 2 | Jan 13–26 | 14 days | Functional & content tests (Cat 1–3) |
| Phase 3 | Jan 27 – Feb 2 | 7 days | User Acceptance Testing (UAT) |
| Phase 4 | Feb 3–9 | 7 days | Bug fixing & regression |
| Phase 5 | Feb 10–14 | 5 days | Release readiness & go-live |

---

## 8. Risks, Assumptions and Constraints

### 8.1 Identified Risks

| ID | Risk | Prob. | Impact | Score | Mitigation Strategy | Owner |
|----|------|-------|--------|-------|---------------------|-------|
| R-01 | GDPR compliance for chat history | High | Very High | 20 | Legal review in progress, privacy-by-design architecture, user consent UI | Antoine + Gil |
| R-02 | API latency >5s for course search | High | High | 15 | Performance optimization, caching strategies, infrastructure scaling | Roli |
| R-03 | Low student awareness at launch | High | High | 15 | Multi-channel communication strategy (4 institutional carriers × 4 channels) | Antoine + Johanna |
| R-04 | Scope expectations mismatch | Medium | High | 12 | Clear messaging: AI Buddy is for admin navigation, not learning content creation | Antoine |
| R-05 | VVZ data quality & processing complexity | Medium | High | 12 | Early data exploration, schema definition, contingency plans for partial data | Roli |
| R-06 | RAG performance sub-optimal | Medium | Medium | 9 | DeepEval testing, iterative tuning, confidence signaling to users | Dev Team |
| R-07 | Cloud LLM access / cost escalation | Low | High | 8 | Engage ZI for institutional agreements, develop local fallback (Qwen 3 on AKS) | Roli |
| R-08 | Ambitious scope for timeline | Medium | Medium | 9 | Strict MVP definition, agile re-evaluation, scope moratorium until release | Antoine |
| R-09 | Privacy in persistent memory | Medium | High | 12 | Privacy-by-design, consent UI, session-only fallback if persistent storage cannot be secured | Roli + Antoine |
| R-10 | DevOps reimplementation by ZI | Low | Medium | 6 | Coordinate early with ZI, document architecture decisions for handover | Roli |
| R-11 | AI competency scarcity (talent) | Medium | Medium | 9 | Internship program, university collaboration, knowledge documentation | Antoine |

### 8.2 Assumptions

| ID | Assumption | Impact if False |
|----|-----------|-----------------|
| A-01 | VVZ data export will be available and processable | Core features delayed |
| A-02 | Microsoft Entra ID will support required auth flows | Alternative auth needed |
| A-03 | Azure OpenAI service remains available and cost-stable | Need to switch to local LLMs |
| A-04 | WWF Dekanat will approve content for all 4 departments | Partial deployment only |
| A-05 | Student adoption interest (~64.5%) will translate to actual usage | Lower impact/value |
| A-06 | Legal review of GDPR compliance will conclude before release | Chat history feature delayed |
| A-07 | 2–4 week onboarding timeline is realistic for new faculties | Slower expansion |

### 8.3 Constraints

| ID | Constraint | Impact |
|----|-----------|--------|
| C-01 | **Scope Moratorium:** No scope extension until mid-February 2026 | All resources focused on release |
| C-02 | **Regulatory:** Swiss Data Protection Act + GDPR compliance mandatory | Architecture constraints, mandatory legal review |
| C-03 | **Timeline:** Release must align with spring semester start (Feb 15) | Fixed, non-negotiable deadline |
| C-04 | **Infrastructure:** Swiss-hosted (Zedi-Cloud) required | Limits provider choices |
| C-05 | **Resource:** Communication activities limited to ~4h/week | Requires high-efficiency comms strategy |
| C-06 | **Content:** Outdated source information managed but flagged back to source | AI Buddy is not responsible for source content accuracy |

### 8.4 Dependencies

| ID | Dependency | Type | Owner |
|----|-----------|------|-------|
| D-01 | VVZ data pipeline functional | Technical | Roli |
| D-02 | Azure AD / Entra ID integration | Technical | Roli + ZI |
| D-03 | WWF content approval (all 4 departments) | Content | Johanna |
| D-04 | Legal review completion (GDPR chat history) | Regulatory | Antoine + Gil |
| D-05 | ZI portfolio registration | Organizational | Michelle + Antoine |
| D-06 | Staging environment stability (48h+) | Technical | Roli |
| D-07 | Dekanat quality control sign-off | Quality | Johanna |

---

## 10. Appendices

### 10.1 Reference Documents

| Document | Location | Status |
|----------|----------|--------|
| DSI Strategy Lab 2023 Position Paper | [DSI Website](https://www.dsi.uzh.ch/de/research/projects/strategy-lab.html) | Published |
| Student Survey Results (N=926, March 2024) | DSI / Project Files | Completed |
| Design Challenge Documentation | Project SharePoint | Active |
| Technical Architecture (MCP, Haystack) | GitLab | Active |
| PO Copilot Configuration | [GitHub](https://github.com/alogean/po_buddy) | Active |
| Testing Playbook | ClickUp | In Development |
| Onboarding Playbook | ClickUp | Planned |
| Communication Roadmap | SharePoint | Active |

### 10.2 DSI Strategy Lab 2023 — Recommendations Addressed

| Recommendation | AI Buddy Implementation |
|----------------|------------------------|
| 1.1 KI-Kompetenzen für alle Studierende | AI Buddy teaches AI literacy through daily usage |
| 1.2 KI-Buddies für alle Studierende | Core mission of the project |
| 1.3 Neustrukturierung universitärer Lernräume | AI Buddy supports hybrid learning models |
| 2.1 KI-harte Fähigkeiten prüfen | Informs content strategy (admin focus, not replacing learning) |
| 2.2 Individualisierung der Lehre | Personalized study plan advisory (v3.0) |
| 3.1 KI als kritische Forschungsinfrastruktur | Swiss-hosted, privacy-first infrastructure |

### 10.3 Key Learnings from AI Buddy 1.0 Pilot

1. **Expectation Mismatch:** Students often seek broader learning content support rather than just administrative guidance — this informs more targeted communication about AI Buddy's specific functions.
2. **Evaluation Approach:** Combining automatic evaluation (LLM-as-Judge) with human validation provides the most effective QA — >80% agreement at significantly lower cost.
3. **Faculty Coordination:** Successful implementation depends on early engagement of institute representatives; 2–4 week onboarding timelines are realistic when properly supported.
4. **Technical Architecture:** Modular, Swiss-hosted solutions prioritizing data privacy are essential for university adoption and stakeholder confidence.
5. **Awareness Gap:** The biggest barrier to adoption is not rejection but **awareness** — marketing and faculty communication need strengthening.
6. **Team Structure:** The 3-workstream model (Dev/Content/Product) with clear RACI improves coordination compared to less structured approaches.

### 10.4 Faculty Expansion Pipeline (Post-Release)

| Code | Faculty | Dekanat | Application Status |
|------|---------|---------|-------------------|
| **WWF** | Business, Economics & Informatics | Harald C. Gall | **Current (2.0)** |
| VSF | Vetsuisse Faculty | Thomas Lutz | Applied (~450 students) |
| TRF | Theology & Religion | Stefan Krauter | Applied (~80 students) |
| PhF | Arts and Social Sciences | Peter Finke | Interested |
| MeF | Medicine | Christian Stockmann | Not applied |
| RWF | Law | Felix Bommer | Not applied |
| MNF | Science | Thierry Hennet | Not applied |

**Onboarding model (2–4 weeks per faculty):**

| Phase | Duration | Activities |
|-------|----------|------------|
| Phase 1: Engagement | Week 1 | Contact faculty representatives, define scope, gather resource lists |
| Phase 2: Data Ingestion | Week 1–2 | Ingest study regulations, web content, course data |
| Phase 3: Testing | Week 2–3 | Faculty-specific QA with subject-matter experts |
| Phase 4: Communication | Week 3–4 | Student-facing announcements, launch coordination |

### 10.5 Product Ecosystem

AI Buddy is part of a broader product ecosystem sharing the same infrastructure:

| Product | Target Audience | Description |
|---------|-----------------|-------------|
| **AI Buddy** | Students | Main study companion (current focus) |
| **Clicker** | Students (tutorials) | Tutorial chatbot based on course content |
| **Education AI** | Lecturers | AI assistant for lecturers |

All products use a common codebase and MCP-based services architecture, designed to be generic and well-documented for potential open-source release.

### 10.6 Glossary

| Term | Definition |
|------|------------|
| AI Buddy | AI-powered conversational study companion for UZH students |
| AKS | Azure Kubernetes Service — container orchestration platform |
| DeepEval | Automated evaluation framework for LLM quality |
| DSI | Digital Society Initiative — UZH competence center for digital transformation |
| Entra ID | Microsoft Azure Active Directory (authentication) |
| Haystack | Open-source framework for building LLM pipelines |
| KG | Knowledge Graph — structured data representation (Neo4j) |
| Langfuse | Open-source LLM observability platform |
| LLM | Large Language Model |
| MCP | Model Context Protocol — standard interface for AI agent tools |
| Mem0 | Agentic memory framework for persistent user context |
| Milvus | Open-source vector database for similarity search |
| NPS | Net Promoter Score — customer loyalty metric (-100 to +100) |
| OLAT | Online Learning and Training — UZH learning management system |
| RAG | Retrieval-Augmented Generation — AI technique combining search with generation |
| TRL | Technology Readiness Level |
| UAT | User Acceptance Testing |
| VVZ | Vorlesungsverzeichnis — UZH official course catalog |
| WWF | Wirtschaftswissenschaftliche Fakultät — Faculty of Business, Economics and Informatics |
| Zedi-Cloud | Swiss-hosted cloud infrastructure used by UZH |
| ZI | Zentrale Informatik — UZH Central IT Services |

---

### Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | March 2025 | Antoine Logean | Initial draft |
| 0.2 | September 2025 | Antoine Logean | Updated with team restructuring (3 workstreams) |
| 1.0 | January 6, 2026 | Antoine Logean | Comprehensive charter for WWF 2.0 release |
| 2.0 | February 7, 2026 | Antoine Logean | Full consolidation with all project knowledge |
| **2.1** | **February 16, 2026** | **Antoine Logean** | **Charter template format — post-release edition** |

---

> **Project Vision:**
> *"AI Buddy: Your personalized UZH study companion — intelligent, ethical, Swiss. Ensuring that every student at the University of Zurich can have an AI Buddy who not only serves to impart knowledge but also accompanies them through their studies as a discussion and sparring partner."*
