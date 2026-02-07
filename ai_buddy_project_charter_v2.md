# AI Buddy — Project Charter

**Project:** AI Buddy — UZH Digital Study Companion
**Project Code:** PRJ-AIB-2026
**Organization:** University of Zurich — Digital Society Initiative (DSI)
**Project Manager / Product Owner:** Antoine Logean
**Project Sponsor:** Prof. Dr. Abraham Bernstein
**Version:** 2.0 — February 7, 2026
**Status:** Active — Release Readiness Phase

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Objectives & KPIs](#2-objectives--kpis)
3. [Scope](#3-scope)
4. [Key Features](#4-key-features)
5. [Stakeholder Register](#5-stakeholder-register)
6. [Governance Structure](#6-governance-structure)
7. [High-Level Schedule](#7-high-level-schedule)
8. [Budget & Resources](#8-budget--resources)
9. [Technical Architecture](#9-technical-architecture)
10. [Risk Assessment](#10-risk-assessment)
11. [Assumptions, Constraints & Dependencies](#11-assumptions-constraints--dependencies)
12. [Quality Management](#12-quality-management)
13. [Communication Plan](#13-communication-plan)
14. [Change Control](#14-change-control)
15. [Appendices](#15-appendices)

---

## 1. Project Overview

### 1.1 Basic Information

| Field | Value |
|-------|-------|
| **Project Name** | AI Buddy — UZH Digital Study Companion |
| **Project Code** | PRJ-AIB-2026 |
| **Project Type** | Strategic Innovation |
| **Delivery Approach** | Agile (Hybrid) — 3-week sprint cycles |
| **Priority Level** | Critical |
| **Start Date** | March 2025 |
| **Current Phase** | AI Buddy 2.0 — Release Readiness |
| **Target Release Date** | February 15, 2026 |
| **Technology Readiness Level** | TRL 7 |

### 1.2 Strategic Context

AI Buddy is a direct implementation of the **DSI Strategy Lab 2023** recommendations, which stated:

> "Es soll darauf hingearbeitet werden, dass jede:r Studierende einer Hochschule einen 'KI-Buddy' nutzen kann, der nicht nur der reinen Wissensvermittlung dient, sondern die Studierenden als Diskussions- und Sparringpartner durch das Studium begleitet."

The project aligns with:

- **UZH Digital Charter** — AI in Education strategic objective
- **DSI Strategic Projects** portfolio
- **Swiss Data Protection Act** and **GDPR** regulatory requirements
- **UZH AI Principles** (UZH Directing Principles for AI)

### 1.3 Business Problem

Students at the University of Zurich face significant challenges navigating their academic journey:

- **Information Overload:** Multiple scattered sources (OLAT, Student Services, faculty websites, VVZ catalog) with no unified access point
- **Complex Module Planning:** Difficulty selecting appropriate modules based on interests, career goals, prerequisites, and schedule conflicts
- **Administrative Burden:** Time-consuming semester planning, deadline tracking, and exam registration processes
- **Social Isolation:** Limited tools to connect with peers for study groups and mentoring
- **Digital Literacy Gap:** 97% of students use AI tools (90% ChatGPT, 77% DeepL), but only 14% learn AI skills from UZH lecturers — the primary sources are online resources (89%) and peers (48%)

### 1.4 Project Vision

AI Buddy is an AI-powered conversational assistant designed to support Bachelor and Master students throughout their university journey. It serves as a trusted discussion partner and study planning assistant providing:

1. **Knowledge Transmission:** Access to educational resources from the university catalog, courses, and literature
2. **Study Plan Advisory:** Personalized guidance on curriculum planning based on individual academic goals
3. **Administrative Support:** Deadlines, exam information, regulations, and process guidance
4. **University Service Locator:** IT services, health/counseling, tutoring, campus maps, student associations

### 1.5 Student Research Evidence (N=926, March 2024)

A survey of 926 UZH students conducted in March 2024 provided foundational evidence:

| Finding | Data |
|---------|------|
| Students with AI tool experience | 97% |
| ChatGPT users (past 6 months) | 90% |
| DeepL users (past 6 months) | 77% |
| Likely to use AI Buddy | **64.5%** (Mean = 4.79/7) |
| Editor/Proofreader function desired | 78.0% |
| Reference & Literature Manager | 68.5% |
| Course/Content Advisor | 65.8% |
| Time Management Support | 58.7% |
| Peer Networking | 33.6% |
| Discussion Partner | 31.2% |

**Key Student Concerns:**

| Concern | Frequency |
|---------|-----------|
| Data protection | 508 mentions |
| Privacy | 124 mentions |
| Security | 49 mentions |

**Information students would share with AI Buddy:**

| Data Type | Willingness |
|-----------|-------------|
| Academic schedule | 80.0% |
| Learning preferences | 71.0% |
| Academic interest and career goals | 69.4% |
| Study materials | 67.6% |
| Academic records | 52.5% |
| Personal schedule | 34.6% |
| Browsing history | 12.2% |
| Trace data | 8.7% |

**Digital Literacy & Adoption:**

- Students with higher digital literacy levels show significantly higher likelihood to use AI Buddy (F(2,542) = 30.5, p < 0.001)
- 54% of students are not familiar with UZH AI principles
- 38.9% were not aware of AI-related courses at UZH
- Biggest barrier to adoption is **awareness** (not rejection)

### 1.6 Core Values

1. **Student-Centered:** Designed around real student needs and pain points
2. **Privacy-First:** Swiss data standards, GDPR compliance, student data sovereignty
3. **Supportive, Not Prescriptive:** Empowers without creating dependency
4. **Transparent & Trustworthy:** Clear about capabilities and limitations
5. **Open Architecture:** Reduces vendor lock-in, enables innovation and inter-university collaboration

---

## 2. Objectives & KPIs

### 2.1 SMART Objectives

| ID | Objective | Target | Measurement |
|----|-----------|--------|-------------|
| OBJ-1 | Deploy AI Buddy 2.0 for full WWF Faculty | February 15, 2026 — zero critical bugs | Release metrics |
| OBJ-2 | Student adoption >50% of WWF students | Registration analytics | User data |
| OBJ-3 | Response accuracy >90% | LLM-as-Judge (>80% human agreement) | DeepEval pipeline |
| OBJ-4 | Swiss privacy compliance | Zero breaches | GDPR audit |
| OBJ-5 | Scalable expansion model | 2-4 week faculty onboarding cycle | Process validation |

### 2.2 Key Performance Indicators

| KPI | Target | Method |
|-----|--------|--------|
| Adoption Rate | >50% of WWF students | Registration analytics |
| Task Completion Rate | >80% | Langfuse tracing |
| API Response Latency | <2 seconds (P95) | Performance monitoring |
| Net Promoter Score (NPS) | >50 | Post-usage surveys |
| Student Awareness | >80% of WWF students | Pre-launch surveys |
| Response Accuracy | >90% correct | DeepEval + human validation |
| System Availability | >99% uptime | Infrastructure monitoring |

### 2.3 DeepEval Evaluation Criteria

| Criterion | Weight | Description |
|-----------|--------|-------------|
| Correctness | 40% | Factual response vs. Ground Truth |
| Completeness | 25% | All key points present |
| Relevance | 20% | Answers the question asked |
| Helpfulness | 15% | Actionable, clear next steps |

---

## 3. Scope

### 3.1 In-Scope (AI Buddy 2.0 — Q1 2026)

- VVZ filtering/search and course information display
- WWF study regulations Q&A (all 4 departments)
- Deadlines, exam information, and process guidance
- UZH Services information (IT, health, campus, ASVZ)
- Study plan display and course recommendations
- Automated testing framework (DeepEval + Langfuse)
- Data ingestion pipelines (VVZ, web scraping, PDFs)
- **Content Coverage:** Full WWF Faculty — Banking & Finance, Business Administration, Economics, Informatics (BA + MA)

### 3.2 Out-of-Scope (Until mid-February 2026)

- Expansion beyond WWF Faculty
- Learning content and tutoring functions
- OLAT integration
- Advanced analytics and automated data ingestion
- Personalized study plan generation (v3.0)
- Student information system (SIS) integration
- Calendar export (.ics)
- ASVZ integration

### 3.3 Key Deliverables

| Deliverable | Target Date | Acceptance Criteria |
|-------------|-------------|---------------------|
| AI Buddy 2.0 Production Release | February 15, 2026 | All Cat 1-3 tests passed, Dekanat QC approved, zero P0/P1 bugs |
| WWF Data Source Catalog | February 1, 2026 | Complete course catalog for all 4 departments |
| Ground Truth Catalog | January 31, 2026 | 90+ validated Q&A pairs across 3 categories |
| Testing Playbook | January 31, 2026 | Documented test process and procedures |
| Onboarding Playbook | March 2026 | Faculty expansion process documented |
| Communication Plan | February 2026 | Multi-channel launch strategy executed |

---

## 4. Key Features

### 4.1 Functional Features (AI Buddy 2.0)

**(F_1) Course Information Hub**
- Display relevant courses based on processed VVZ export
- For each course: official description, ECTS credits, dependencies (from Knowledge Graph), lecture/tutorial schedule, exam date
- Basic search/filtering capabilities (name, keyword)
- Enhanced filtering by time slots (e.g., "Monday morning")

**(F_2) Study Regulation & Process Guidance**
- RAG-based Q&A on study regulations (PDFs/text) for full WWF Faculty
- Automated ingestion pipeline for selected UZH websites
- Periodic data refresh capability
- Content includes: FAQs, process descriptions (module booking, enrollment), IT info, exam periods/rules, health/support services, campus building info
- Curated links to official UZH pages for critical deadlines

**(F_3) University Service & Resource Locator**
- RAG-based Q&A using scraped web data for:
  - IT and support services (OLAT, VPN, Mail)
  - Health and counseling services
  - Official tutoring and mentoring programs
  - Campus maps and building directories (MCP: Rooms / uniability API)
  - Primary student associations (Fachvereine) for Economics and Informatics

### 4.2 Non-Functional Features

**(NF_1) Data Sources Management**
- Course Data: VVZ export → cleaning, parsing, validation → Knowledge Graph
- Manual enrichment with topics/competencies (AI-assisted)
- Regulations/Process/Support: PDFs + automated web scraping pipeline

**(NF_2) Privacy & Security**
- UZH data privacy guidelines compliance
- Minimal PII collection and storage
- User consent mechanism for personalized data
- User interface for viewing/managing stored data
- Microsoft Entra ID authentication
- Input sanitization, dependency scanning, secure configuration

### 4.3 Optional / Stretch (AI Buddy 2.0)

**(F_4) Advanced Agent Capabilities**
- Agentic memory (Mem0) for session context recall
- Artifact generation (formatted Markdown/HTML summaries)
- Generic MCP integrations (events, thesis topics, jobs)
- Simple visualization capabilities

### 4.4 Planned for AI Buddy 3.0 (September 2026)

- **(F_5)** Support for new faculties/study programs
- **(F_4)** Personalized Study Plan Proposal generation
  - Study plan based on user inputs, regulations, course catalog, and KG dependencies
  - Validation against core requirements
  - Schedule and exam overlap detection
  - User-managed "completed courses" tracking
  - MCP: Mensa, MCP: ASVZ
- **(NF_2)** Enhanced PII removal (LLM Guard)
- Local LLMs for sensitive query categorization

---

## 5. Stakeholder Register

### 5.1 Key Stakeholders

| Name | Role | Organization | Interest | Influence | Engagement |
|------|------|--------------|----------|-----------|------------|
| Prof. Dr. Abraham Bernstein | Executive Sponsor / DSI Director | DSI | High | High | Supportive |
| Dr. Alexandra Jansky | Educational Development Lead | Lehrstelle | High | High | Supportive |
| Prof. Dr. Claudia Witt | DSI Director | DSI | High | High | Supportive |
| Prof. Dr. Titus Mangham-Neupert | DSI Director | DSI | High | High | Supportive |
| Michelle Stärke | Steering Board Member / Studivers | Digital Charter | High | Medium | Supportive |
| WWF Dekanat | Faculty Administration | WWF | High | Medium | Supportive |
| Susanne Bürchler | ZI Portfolio Manager | ZI | Medium | Medium | Neutral |
| Priska Feichter | Head of Social Media | UZH Communications | Medium | Medium | Supportive |
| Ruben Kranendonk | Communication | UZH.ai | Medium | Medium | Supportive |
| Gil | Data Protection Advisor | UZH Legal | Medium | High | Neutral |
| Roger Gfroerer | Career Services | UZH | Low | Low | Interested |
| WWF Students | End Users | WWF | High | Low | Varies |
| WWF Lecturers | Content Stakeholders | WWF | Medium | Medium | Neutral |

### 5.2 Faculty Contacts for Expansion

| Code | Faculty | Expansion Priority | Contacts |
|------|---------|-------------------|----------|
| WWF | Business, Economics & Informatics | **Current (2.0)** | Johanna Braun (Content Lead) |
| PhF | Arts and Social Sciences | Post-2.0 | AL, MS, JB, RS |
| MNF | Science | Post-2.0 | TBD |
| RWF | Law | Post-2.0 | TBD |
| MeF | Medicine | Post-2.0 | TBD |
| ThF/TRF | Theology and Study of Religion | Post-2.0 | TBD |
| VSF | Vetsuisse Faculty | Post-2.0 | TBD |

| Faculty | Fakultät | Dekanat | Application | Institute | Studienprogramm | Ansprechperson | Anzahl |
|--------|----------|---------|-------------|-----------|----------------|---------------|--------|
| WWF | Wirtschaftswissenschaftliche Fakultät | Harald C. Gall | yes |  |  |  |  |
| VSF | Vetsuisse-Fakultät | Thomas Lutz | yes |  | Bachelor/Master Veterinärmedizin | Rutz Stefanie | 450 |
| TRF | Theologische und Religionswissenschaftlichen Fakultät | Stefan Krauter | yes |  | Bachelor of Theology UZH | Cahn Barbara | 80 |
| PhF | Philosophischen Fakultät | Peter Finke | (yes) | Kommunikationswissenschaft | BA KoWi Major<br>BA KoWi Minor<br>MA KoWi Major<br>MA KoWi Minor<br>MA Strat.Komm. Major<br>MA Internet & Society Mono |  |  |
| PhF | Philosophischen Fakultät | Peter Finke | (yes) | Historisches Seminar |  |  |  |
| MEF | Medizinische Fakultät | Christian Stockmann / Dominik Schaer | no |  |  |  |  |
| RWF | Rechtswissenschaftliche Fakultät | Felix Bommer | no |  |  |  |  |
| MNF | Mathematisch-naturwissenschaftliche Fakultät | Thierry Hennet | no |  |  |  |  |

### 5.3 RACI Matrix

| Deliverable / Decision | Sponsor (Bernstein) | PM/PO (Antoine) | Tech Lead (Roli) | Content Lead (Johanna) | Research (Oriane) | ZI |
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

## 6. Governance Structure

### 6.1 Project Organization

| Role | Name | Department | Responsibility |
|------|------|------------|----------------|
| **Executive Sponsor** | Prof. Dr. Abraham Bernstein | DSI | Strategic direction, funding authority, escalation decisions |
| **PM / Product Owner** | Antoine Logean | DSI | Day-to-day management, stakeholder alignment, product decisions, communication, compliance |
| **Tech Lead / Solution Architect** | Roland Schläfli (Roli) | DSI | Technical architecture, dev team leadership, ZI coordination, infrastructure |
| **Tech Lead** | Michael | DSI | Development support, technical decisions |
| **Content Lead** | Johanna Braun | WWF | WWF faculty relations, data source catalog, expert agents, quality testing |
| **PostDoc AI Buddy Research** | Oriane Camille Iris Pierrès | DSI | AI Buddy vision, branding, student requirement engineering, usability studies |
| **User Testing / Studivers** | Michelle Stärke | Digital Charter | Usability studies, tester framework management, steering board member |

### 6.2 Workstream Structure

**Development Workstream (Lead: Roland)**
- Technical stakeholders (ZI, etc.)
- AI Platform development
- Data Platform
- Infrastructure & Deployment

| Team Member | FTE % |
|-------------|-------|
| Roland (Roli) | 20% |
| Max | 30% |
| Patrick | 10% |
| Antonio | 10% |
| Alex Achotian | 40% |
| Lena Fiedor | 40% |

**Content Workstream (Lead: Johanna)**
- Stakeholders: Dekanat, WWF, subject-specific stakeholders
- Data Source Catalog management
- Prompts / Expert agents design
- Quality Testing

| Team Member | FTE % |
|-------------|-------|
| Johanna Braun | 10% |
| Semester Assistant | 30% |

**Product Workstream (Lead: Antoine)**
- Stakeholders: Steering Board, sponsors
- Communication strategy & execution
- Data Analysis & Bug tracking
- Compliance & Data Protection
- Testing / Usability
- Evaluations

| Team Member | FTE % |
|-------------|-------|
| Antoine Logean | 100% |
| Michael | TBD% |
| Oriane | 10% |
| Michelle | TBD% |

### 6.3 Steering Committee

| Member | Email | Role |
|--------|-------|------|
| Prof. Dr. Abraham Bernstein | bernstein@ifi.uzh.ch | Chair / Executive Sponsor |
| Prof. Dr. Claudia Witt | claudia.witt@uzh.ch | DSI Director |
| Prof. Dr. Titus Mangham-Neupert | titus.neupert@physik.uzh.ch | DSI Director |
| Dr. Alexandra Jansky | alexandra.jansky@uzh.ch | Educational Development Lead |
| Michelle Stärke | — | Digital Charter / Studivers |

**Meeting Cadence:** Quarterly (March, June, September, December)

### 6.4 Decision Authority Matrix

| Decision Type | Authority Level | Response Time |
|---------------|-----------------|---------------|
| Scope changes requiring additional resources | Steering Committee | Next meeting |
| Budget variance > 10% | Project Sponsor | 3 business days |
| Schedule changes < 2 weeks | Project Manager | 24 hours |
| Technical architecture decisions | Tech Lead + PM | 48 hours |
| Content accuracy / regulations | Content Lead + Faculty | 1 week |
| Resource allocation within team | Project Manager | 24 hours |
| External communication | PM with DSI approval | 48 hours |

---

## 7. High-Level Schedule

### 7.1 Key Milestones

| ID | Milestone | Target Date | Gate/Checkpoint |
|----|-----------|-------------|-----------------|
| M-0 | Project Kickoff | March 2025 | Charter Approved |
| M-1 | AI Buddy 1.0 Pilot Release | September 2025 | Finance & Informatics programs deployed |
| M-2 | MVP Validation Complete | December 2025 | OEC-Dekanat QC Passed |
| M-3 | Testing Infrastructure Ready | January 12, 2026 | DeepEval + Ground Truth operational |
| M-4 | Category 1-3 Testing Complete | January 31, 2026 | >85% pass rate, 0 P0/P1 bugs |
| M-5 | UAT Complete | February 7, 2026 | Student validation passed |
| M-6 | Release Readiness | February 10, 2026 | Go/No-Go decision |
| **M-7** | **WWF 2.0 Deployment** | **February 15, 2026** | **Production Ready** |
| M-8 | Faculty Expansion Start | March 2026+ | Onboarding Playbook Ready |
| M-9 | AI Buddy 3.0 Release | September 2026 | New faculties + personalized study plans |
| M-10 | ZI Ecosystem Integration | 2026 (TBD) | Integration specifications complete |

### 7.2 Phase Overview

| Phase | Start | End | Key Activities | Exit Criteria |
|-------|-------|-----|----------------|---------------|
| **AI Buddy 1.0** | Mar 2025 | Sep 2025 | Pilot with Finance & Informatics, 1st/3rd semester students | Pilot deployed |
| **AI Buddy 2.0 Dev** | Sep 2025 | Feb 2026 | WWF scope extension, testing, bug fixes | All tests passed |
| **Release Readiness** | Jan 2026 | Feb 15, 2026 | Category 1-3 testing, bug burn-down, UAT | Release approved |
| **Post-Release** | Mar 2026+ | Ongoing | Faculty onboarding, feature enhancements, v3.0 development | Continuous |

### 7.3 5-Phase Testing Plan (40 days to release)

| Phase | Period | Duration | Focus |
|-------|--------|----------|-------|
| Phase 1 | Jan 6-12 | 7 days | Test infrastructure & preparation |
| Phase 2 | Jan 13-26 | 14 days | Functional & content tests (Cat 1-3) |
| Phase 3 | Jan 27 - Feb 2 | 7 days | User Acceptance Testing (UAT) |
| Phase 4 | Feb 3-9 | 7 days | Bug fixing & regression |
| Phase 5 | Feb 10-14 | 5 days | Release readiness & go-live |

### 7.4 Sprint Cadence

- **Sprint Duration:** 3 weeks (extended from 2 weeks based on team learning)
- **AI Buddy Days:** Full team review/demo at each iteration
- **Current Sprint:** Sprint 22 (January 13 — February 10, 2026)
- **Sprint Status:** 89 total tasks, 55 remaining open

---

## 8. Budget & Resources

### 8.1 Team Resource Allocation

| Workstream | Lead | Total FTE | Members |
|------------|------|-----------|---------|
| Development | Roland | ~1.5 FTE | Roli (20%), Max (30%), Patrick (10%), Antonio (10%), Alex (40%), Lena (40%) |
| Content | Johanna | ~0.4 FTE | Johanna (10%), Sem. Assistant (30%) |
| Product | Antoine | ~1.6 FTE | Antoine (100%), Michael (TBD), Oriane (10%), Michelle (TBD) |
| **Total** | | **~3.5 FTE** | |

### 8.2 Infrastructure Costs

| Component | Provider | Notes |
|-----------|----------|-------|
| Azure Kubernetes Service (AKS) | Microsoft Azure | Zedi-Cloud (Swiss-hosted) |
| Azure OpenAI | Microsoft Azure | Primary LLM inference |
| Vertex AI | Google Cloud | Secondary LLM provider |
| Neo4j | Self-hosted on AKS | Knowledge Graph |
| Milvus | Self-hosted on AKS | Vector Store |
| Langfuse | Self-hosted | Observability |
| GitLab CI | UZH Infrastructure | CI/CD pipeline |

### 8.3 Funding Sources

- **Primary:** DSI (Digital Society Initiative) budget
- **Secondary:** UZH Digital Charter funding
- **Constraint:** Communication activities limited to ~4 hours/week

---

## 9. Technical Architecture

### 9.1 System Overview

AI Buddy uses a **multi-agent modular architecture** with specialized LLM agents for different functions, connected through the **Model Context Protocol (MCP)**.

### 9.2 Technology Stack

**Frontend & Authentication**

| Component | Technology | Details |
|-----------|------------|---------|
| UI Platform | LibreChat | Customized for study plan display |
| Authentication | Microsoft Entra ID (Azure AD) | UZH single sign-on |

**Backend & Infrastructure**

| Component | Technology | Details |
|-----------|------------|---------|
| Framework | Python / FastAPI | RESTful API backend |
| Container Orchestration | Azure Kubernetes Service (AKS) | Zedi-Cloud (Swiss-hosted) |
| Pipeline Orchestration | Haystack | Pipelines and agents |
| Agentic Memory | Mem0 + Neo4j | Persistent user preferences |
| Vector Store | Milvus | Self-hosted on AKS |
| CI/CD | GitLab CI | Automated testing and deployment |
| IaC | Pulumi + Terraform | Infrastructure as Code (TypeScript/Python) |

**Core AI Capabilities**

| Capability | Technology | Details |
|------------|------------|---------|
| Primary LLMs | Azure OpenAI, Vertex AI | Main inference engines |
| Local LLM | Qwen 3 on AKS | Privacy-sensitive tasks |
| RAG | Hybrid search | Optimized chunking, contextual embeddings |
| Knowledge Graph | Neo4j | Courses, requirements, programs modeling |
| Agent Logic | Tool calling | Routes between RAG, KG, or Memory |

**Data Pipelines**

| Pipeline | Tool | Purpose | Priority |
|----------|------|---------|----------|
| VVZ Processing | Custom | Automated cleaning/parsing of course catalog | P0 |
| Web Scraping | Firecrawl | UZH site ingestion | P0 |
| Document Processing | Docling | PDF-to-Markdown extraction | P1 |

**Observability & Evaluation**

| Component | Technology | Features |
|-----------|------------|----------|
| Tracing & Feedback | Langfuse | Deep integration, performance monitoring |
| Automated Evaluation | DeepEval | Quality pipelines, regression testing |

### 9.3 Product Ecosystem

AI Buddy is part of a broader product ecosystem sharing the same infrastructure:

| Product | Target Audience | Description |
|---------|-----------------|-------------|
| **AI Buddy** | Students | Main study companion (current focus) |
| **Clicker** | Students (tutorials) | Tutorial chatbot based on course content |
| **Education AI** | Lecturers | AI assistant for lecturers |

All products use a common codebase and MCP-based services architecture, designed to be generic and well-documented for potential open-source release.

### 9.4 MCP Tools Architecture

| MCP Tool | Function | Status |
|----------|----------|--------|
| RAG (Content Experts) | Web content retrieval via Milvus | Active |
| Neo4j Course Catalog | Graph database of course information | Active |
| Rooms / Uniability API | Campus and room information | Planned |
| Web Index | Web search capability | In development |

### 9.5 DevOps Approach

- **Containerization:** Docker containers orchestrated by Kubernetes on Azure
- **Three-environment architecture:** dev / test / prod
- **CI/CD:** GitLab CI with automated testing and deployment
- **Infrastructure as Code:** Pulumi (TypeScript/Python) + Terraform
- **Monitoring:** Langfuse for tracing + alerting infrastructure

### 9.6 Performance Requirements

| Metric | Target |
|--------|--------|
| Simple query response | <10 seconds |
| Complex query response | <15 seconds |
| P95 latency (production target) | <2 seconds |
| Concurrent users | ≥10% of target student population |
| Primary language | German |
| Secondary language | English |

---

## 10. Risk Assessment

### 10.1 Active Risk Register

| ID | Risk | Probability | Impact | Score | Mitigation | Owner |
|----|------|-------------|--------|-------|------------|-------|
| R-01 | GDPR compliance for chat history | High | Very High | 20 | Legal review in progress, privacy-by-design, consent UI | Antoine + Gil |
| R-02 | API latency >5s for course search | High | High | 15 | Performance optimization, caching strategies | Roli |
| R-03 | Low student awareness at launch | High | High | 15 | Multi-channel communication strategy (4 carriers, 4 channels) | Antoine + Johanna |
| R-04 | Scope expectations mismatch | Medium | High | 12 | Clear messaging on tool purpose (admin not learning content) | Antoine |
| R-05 | VVZ data quality & processing | Medium | High | 12 | Early data exploration, schema definition, contingency plans | Roli |
| R-06 | RAG performance sub-optimal | Medium | Medium | 9 | DeepEval testing, iterative tuning, confidence signaling | Dev Team |
| R-07 | Cloud LLM access/cost escalation | Low | High | 8 | Engage ZI, develop local fallback (Qwen 3) | Roli |
| R-08 | Ambitious scope for timeline | Medium | Medium | 9 | Strict MVP, agile re-evaluation, scope moratorium | Antoine |
| R-09 | Privacy in persistent memory | Medium | High | 12 | Privacy-by-design, consent UI, session-only fallback | Roli + Antoine |
| R-10 | DevOps reimplementation by ZI | Low | Medium | 6 | Coordinate early with ZI, document architecture | Roli |
| R-11 | KI competency scarcity (talent) | Medium | Medium | 9 | Internship program, university collaboration | Antoine |

### 10.2 Bug Classification (from 82 Staging Bugs Analysis)

| L1 Bug Type | Count | Percentage |
|-------------|-------|------------|
| Inaccurate Answer | 33 | 40.2% |
| Incomplete Answer | 19 | 23.2% |
| Tool Unavailable | 15 | 18.3% |
| Missing Knowledge | 6 | 7.3% |
| Tool Crash | 6 | 7.3% |
| UX/Formatting | 3 | 3.7% |

| L2 Topic Domain | Count | Top Issues |
|-----------------|-------|------------|
| Exams/Assessment | 15 | Inaccurate exam info |
| Mobility/Exchange | 13 | Missing exchange data |
| Course Planning/Booking | 12 | Wrong course details |
| Module Recognition/Credits | 8 | Credit calculation errors |
| Student Associations | 6 | Outdated links |
| Instructors/Staff | 6 | Wrong contact info |
| Student Finance | 6 | Incomplete fee info |
| Thesis/Graduation | 5 | Missing thesis requirements |

---

## 11. Assumptions, Constraints & Dependencies

### 11.1 Assumptions

| ID | Assumption | Impact if False |
|----|-----------|-----------------|
| A-01 | VVZ data export will be available and processable | Core features delayed |
| A-02 | Microsoft Entra ID will support required auth flows | Alternative auth needed |
| A-03 | Azure OpenAI service remains available and cost-stable | Need to switch to local LLMs |
| A-04 | WWF Dekanat will approve content for all 4 departments | Partial deployment only |
| A-05 | Student adoption interest (~64.5%) will translate to actual usage | Lower impact/value |
| A-06 | Legal review of GDPR compliance will conclude before release | Chat history feature delayed |
| A-07 | 2-4 week onboarding timeline is realistic for new faculties | Slower expansion |

### 11.2 Constraints

| ID | Constraint | Impact |
|----|-----------|--------|
| C-01 | **Scope Moratorium:** No scope extension until mid-February 2026 | All resources focused on release |
| C-02 | **Regulatory:** Swiss Data Protection Act + GDPR compliance mandatory | Architecture constraints |
| C-03 | **Timeline:** Release must align with spring semester start (Feb 15) | Fixed deadline |
| C-04 | **Infrastructure:** Swiss-hosted (Zedi-Cloud) required | Provider limitations |
| C-05 | **Resource:** Communication activities limited to ~4h/week | Requires efficiency |
| C-06 | **Content:** Outdated source information managed but flagged back to source | Not responsible for source content |

### 11.3 Dependencies

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

## 12. Quality Management

### 12.1 Quality Objectives

| Dimension | Target | Method |
|-----------|--------|--------|
| Response Accuracy | >90% | LLM-as-Judge + human validation |
| Response Performance | <2s (P95) | Langfuse monitoring |
| System Availability | >99% uptime | Infrastructure monitoring |
| User Satisfaction | NPS >50 | Post-usage surveys |
| Content Coverage | 100% WWF departments | Data catalog completeness |

### 12.2 Test Categories

| Category | Scope | # Q&A Target | Owner |
|----------|-------|--------------|-------|
| Cat 1: Functional | VVZ search, filters, course details | 20 | Dev Team |
| Cat 2: Faculty-Specific (DF) | Banking & Finance regulations | 15 | Johanna |
| Cat 2: Faculty-Specific (DBA) | Business Administration regulations | 15 | Johanna |
| Cat 2: Faculty-Specific (ECON) | Economics regulations | 15 | Johanna |
| Cat 2: Faculty-Specific (IFI) | Informatics regulations | 15 | Johanna |
| Cat 3: UZH Services | IT, Health, Campus, ASVZ | 10 | Johanna |
| **Total** | | **90** | |

### 12.3 Ground Truth Format

```
ID: GT-[CAT]-[DEPT]-[###]
Question (DE): [Realistic student question]
Expected Answer: [Mandatory key points in response]
Source: [Official URL]
Validated by: [Name]
```

### 12.4 Standard Test Workflow

```
List functionalities → Generate test questions → Execute tests → Evaluate quality
  ├─ Pass → Add to Ground Truth catalog
  └─ Fail → Create ClickUp bug with classification:
             L1: Bug Type (Inaccurate/Incomplete/Tool Unavailable/etc.)
             L2: Topic Domain (Exams/Mobility/Course Planning/etc.)
```

### 12.5 Problem Diagnosis Framework

| Root Cause Type | Description | Responsible |
|-----------------|-------------|-------------|
| RAG | Wrong documents retrieved | Dev Team (pipeline) |
| KG | Knowledge Graph incomplete/incorrect | Dev Team (Neo4j) |
| Prompt | Agent prompt formulation issue | Dev Team (prompts) |
| Content | Missing/outdated content | Johanna (catalog) |
| Perf | Latency exceeding targets | Dev Team (infra) |

### 12.6 Quality Gate Checklist (Phase 2 Exit — January 31)

| # | Criterion | Target |
|---|-----------|--------|
| 1 | Questions tested | 90/90 (100%) |
| 2 | DeepEval score | >85% |
| 3 | P0/P1 bugs open | 0 |
| 4 | Latency P95 | <5s |
| 5 | All fixes validated by retest | Yes |
| 6 | Staging stable | 48h+ continuous |

---

## 13. Communication Plan

### 13.1 Target Audiences

| Audience | Message Focus | Primary Channels |
|----------|---------------|------------------|
| **UZH Employees** | Strategic innovation, support for student guidance | Newsletter (UZH Inside), SharePoint |
| **Students** | Practical benefits, ease of use, privacy assurance | LinkedIn, Webpage, Social Media |

### 13.2 Institutional Carriers

| Institution | Role | Communication Focus |
|-------------|------|---------------------|
| **UZH** | Strategic Leadership | Official positioning, credibility |
| **DSI** | Operational | Technical development, community building |
| **UZH.ai** | AI Expertise | Scientific foundation, thought leadership |
| **WWF** | Faculty Validation | Pedagogical integration, practical application |

### 13.3 Communication Channels

| Channel | Type | Target Audience | Content Focus | Effort/Week |
|---------|------|-----------------|---------------|-------------|
| Newsletter (UZH Inside) | Internal | UZH Employees | Updates, milestones, training | ~1h |
| SharePoint | Internal | UZH Employees | Documentation, FAQ, resources | ~1h |
| LinkedIn | External | Professional community | Thought leadership, success stories | ~1h |
| Webpage | External | Students + public | Product info, testimonials, demo | ~1h |

### 13.4 Communication Matrix

| Communication | Audience | Frequency | Channel | Owner |
|---------------|----------|-----------|---------|-------|
| Steering Committee Update | Steering Board | Quarterly | Meeting + slides | Antoine |
| Sprint Review / AI Buddy Day | Project Team | Every 3 weeks | In-person/hybrid | Antoine + Roli |
| Newsletter Update | UZH Employees | Bi-weekly | UZH Inside | Antoine |
| Social Media Posts | Students | Weekly | LinkedIn, Instagram | Johanna + Priska |
| Faculty Update | WWF Lecturers | As needed | Email / Meeting | Johanna |
| Tester Communication | Beta Users | As needed | Email | Antoine + Johanna |
| Dekanat Coordination | WWF Dekanat | Bi-weekly | Email | Johanna |

### 13.5 Stakeholder Communication Roadmap

| Stakeholder | Owner | Channel | Status |
|-------------|-------|---------|--------|
| WWF Dekanat | Johanna | Email | Done |
| Digital Strategy Board (DiSB) | Michelle | Email | Done |
| AI Buddy Steering Board | Antoine | Email | Done |
| UZH Direction | Michelle | Email | In progress |
| UZH Employees | Antoine (via Priska) | Newsletter | Planned |
| Other UZH Faculties | TBD | Newsletter | Planned |
| SIB | Antoine | Email | Planned |
| ZI | Michelle | Email | Planned |
| Lehrstelle | Alexandra | Email | Planned |
| Testers | Antoine / Johanna | Email | Planned |
| WWF Students | Johanna | Social Media | Planned |
| WWF Lecturers | Johanna | Email / Faculty meeting | In coordination |

### 13.6 Escalation Path

| Level | Issue Type | Escalate To | Response Time |
|-------|------------|-------------|---------------|
| L1 | Operational issues, bugs | Project Manager | 24 hours |
| L2 | Resource conflicts, scope changes | Project Sponsor | 48 hours |
| L3 | Strategic, compliance, major blockers | Steering Committee | Next meeting |

---

## 14. Change Control

### 14.1 Change Control Process

1. Submit Change Request via ClickUp
2. PM logs CR and performs initial assessment
3. Impact analysis (scope, schedule, cost, quality, risk)
4. Approval based on authority thresholds
5. Communicate decision to stakeholders
6. Update project documents and baselines if approved

### 14.2 Change Authority Thresholds

| Change Size | Authority | Response Time |
|-------------|-----------|---------------|
| Minor (< 8 hours, no budget impact) | Project Manager | 24 hours |
| Medium (8-40 hours or < 10% budget) | Project Sponsor | 3 business days |
| Major (> 40 hours or > 10% budget) | Steering Committee | Next meeting |

### 14.3 Current Change Moratorium

**⚠ CONSTRAINT:** No scope extension until mid-February 2026. All resources are focused exclusively on WWF 2.0 release readiness.

---

## 15. Appendices

### 15.1 Related Documents

| Document | Location | Status |
|----------|----------|--------|
| DSI Strategy Lab 2023 Position Paper | DSI Website | Published |
| Student Survey Results (N=926) | DSI / Project Files | Completed |
| Design Challenge Documentation | Project SharePoint | Active |
| Technical Architecture (MCP, Haystack) | GitLab | Active |
| PO Copilot Configuration | GitHub (alogean/po_buddy) | Active |
| Testing Playbook | ClickUp | In Development |
| Onboarding Playbook | ClickUp | Planned |
| Communication Roadmap | SharePoint | Active |

### 15.2 Research & Innovation Themes

The AI Buddy project generates research opportunities across multiple dimensions:

**Architecture & System Design**
- Optimal multi-agent topologies and their impact on performance
- Scalable event-driven communication protocols between LLM agents
- Context management across specialized agents

**Knowledge Management**
- Domain-specific RAG optimization for higher education
- Dynamic knowledge update mechanisms
- Structured vs. unstructured information source integration

**AI Didactics & Learning Support**
- Personalization mechanisms for individual learning paths
- Metacognitive support through AI
- Long-term learning companionship strategies

**Human-AI Interaction**
- Conversational strategies for educational contexts
- Affective components and emotional state recognition
- Cultural sensitivity and multilingual support

**Privacy & Ethics**
- Privacy-preserving learning architectures
- Federated learning for personalized education
- Transparency and explainability of agent decisions
- Bias identification in educational chatbots

**Evaluation & Quality**
- LLM-as-Judge methodologies (>80% agreement with human evaluation)
- Automated vs. human quality assurance approaches
- Student satisfaction and learning outcome measurement

### 15.3 DSI Strategy Lab 2023 — Key Recommendations Addressed

| Recommendation | AI Buddy Implementation |
|----------------|------------------------|
| 1.1 KI-Kompetenzen für alle Studierende | AI Buddy teaches AI literacy through usage |
| 1.2 KI-Buddies für alle Studierende | Core mission of the project |
| 1.3 Neustrukturierung universitärer Lernräume | AI Buddy supports hybrid learning models |
| 2.1 KI-harte Fähigkeiten prüfen | Informs content strategy (admin focus, not replacing learning) |
| 2.2 Individualisierung der Lehre | Personalized study plan advisory (v3.0) |
| 3.1 KI als kritische Forschungsinfrastruktur | Swiss-hosted, privacy-first infrastructure |

### 15.4 Key Learnings from AI Buddy 1.0 Pilot

1. **Expectation Mismatch:** Students often seek broader learning content support rather than just administrative guidance — this informs more targeted communication about AI Buddy's specific functions
2. **Evaluation Approach:** Combining automatic evaluation (LLM-as-Judge) with human validation provides the most effective QA — >80% agreement at significantly lower cost
3. **Faculty Coordination:** Successful implementation depends on early engagement of institute representatives; 2-4 week onboarding timelines are realistic when properly supported
4. **Technical Architecture:** Modular, Swiss-hosted solutions prioritizing data privacy are essential for university adoption and stakeholder confidence
5. **Awareness Gap:** The biggest barrier to adoption is not rejection but **awareness** — marketing and faculty communication need strengthening
6. **Team Structure:** 3-workstream model (Dev/Content/Product) with clear RACI improves coordination compared to less structured approaches

### 15.5 Faculty Onboarding Model (Post-Release)

For expansion to new faculties, a "chatbot as a service" model with standardized onboarding:

| Phase | Duration | Activities |
|-------|----------|------------|
| Phase 1: Engagement | Week 1 | Contact faculty representatives, define scope, gather resource lists |
| Phase 2: Data Ingestion | Week 1-2 | Ingest study regulations, web content, course data |
| Phase 3: Testing | Week 2-3 | Faculty-specific QA with subject-matter experts |
| Phase 4: Communication | Week 3-4 | Student-facing announcements, launch coordination |

### 15.6 Glossary

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

### 15.7 Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | March 2025 | Antoine Logean | Initial draft |
| 0.2 | September 2025 | Antoine Logean | Updated with team restructuring (3 workstreams) |
| 1.0 | January 6, 2026 | Antoine Logean | Comprehensive charter for WWF 2.0 release |
| **2.0** | **February 7, 2026** | **Antoine Logean** | **Full consolidation with all project knowledge** |

---

*— End of Document —*

> **Project Vision:**
> *"AI Buddy: Your personalized UZH study companion — intelligent, ethical, Swiss.
> Ensuring that every student at the University of Zurich can have an AI Buddy who not only serves to impart knowledge but also accompanies them through their studies as a discussion and sparring partner."*
