# BA Context & Project Memory

## My Role
- **Name:** Mykola Fedorov (SoE eHealth / ДП «Електронне здоров'я»)
- **Position:** Senior Business Analyst — Medical Domain
- **Focus:** AI-powered BA tooling, Medical Data Exchange, Public Health Analytics

## Current Ecosystem
- **Workstation:** Windows 11 (Browser, Confluence, Google Workspace, Jira)
- **AI Workstation (Production):** Ubuntu 24.4 Server (OpenNCP repo, Clawdbot orchestration)
- **Sandbox:** Windows 10 VM (Ubuntu 24.4 WSL2) → *попередня локація навчання*
- **AI Orchestration:** Clawdbot (Telegram bot) + Claude Code CLI
- **Notes:** NotebookLM (21 нотатник по медичній аналітиці)

## Standards & Guidelines
- **Requirements:** Use standard User Story format (As a... I want... So that...).
- **Documentation:** Follow eHealth Ukraine internal standards for Confluence.
- **Language:** Work in Ukrainian for documentation, English for technical terms.
- **Requirement IDs:** REQ-XXX (functional), NFR-XXX (non-functional)
- **Priorities:** MoSCoW (Must / Should / Could / Won't Have)

## Active Projects

### 1. OpenNCP (EU HEALS) — Cross-border health data exchange
- **Platform:** OpenNCP v10.0.0 | UA National Connector (~6200 lines Java)
- **Partner:** Estonia (X-Road, test-gw.e-tervis.ee, community EE-EPR)
- **Status:** 3/4 flows ready | **2 blockers** (OAuth2 params from ЕСОЗ)
- **Standards:** FHIR R4, HL7 CDA L3, IHE XCPD/XCA/XDR, epSOS profiles
- **Terminology:** 7 JSON mapping tables, 356 records (ЕСОЗ ↔ SNOMED CT/ICD-10/ATC/EDQM)
- **Folder:** `~/projects/openncp-ukraine/` | Quick ref: `CLAUDE.md`

### 2. ПГЗ — Public Health Indicators Platform
- **Owner:** МОЗ Ukraine / ЦГЗ | **Admin:** ДП «Електронне здоров'я»
- **Funding:** USAID | **Legal basis:** Постанова КМУ № 506/2025
- **Standard:** HL7 FHIR v5.0.0 (Measure, MeasureReport, EvidenceVariable, Library)
- **Scope:** 39 data sources, 78 indicators (CVD-36, ONC-20, PMD-17, PREG-5)
- **Arch:** 7 modules (ДАНІ, КІ, КШ, КАТАЛ, ЗВІТ, КОР, КМ) | Protocol: Трембіта
- **Status:** Concept approved | TZ in development
- **Folder:** `~/projects/health-indicators/` | Quick ref: `CLAUDE.md`

### 3. AI Tooling for BA
- Building personal toolset: Claude Code + Clawdbot (Telegram) + NotebookLM
- Learning resource: `~/projects/claude-howto/` (v2.2.0, 100+ examples)
- Training course: `~/projects/docs/vscode-agent-research/` (11-13h, Ukrainian)

## Notes
This file serves as the core memory for Claude Code in this project directory.
For full project context — read the respective project's CLAUDE.md / CLAUDE-FULL.md.

---

## 🔐 Управління секретами (сервер Jinny-S7)

> **Правило:** Будь-які API-ключі та токени зберігаються **виключно** у  
> `~/.config/jinny-secrets/jinny.env` (chmod 600) — поза всіма git-репозиторіями.  
> Ніколи не додавати ключі у project `.env`, `.md` файли або JSON-конфіги.

**Деталі:** `/home/nkfed/Documents/jinny-s7-server-docs/SECRETS_CENTRAL_STORE_2026-05-09.md`
