# Awesome-Workflow-Automation-Business-Process-Management

# Awesome Workflow Automation & Business Process Management

> A curated list of top Workflow Automation and Business Process Management (BPM) platforms — both SaaS/Hosted commercial solutions and open-source alternatives for process modeling, execution, and automation.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Zoho Flow](#zoho-flow)
  - [Zapier](#zapier)
  - [Make](#make)
  - [Workato](#workato)
  - [Nintex](#nintex)
  - [ProcessMaker](#processmaker)
  - [Kissflow](#kissflow)
  - [Camunda 8](#camunda-8)
  - [Pipefy](#pipefy)
  - [Appian](#appian)
- [Open-Source Software](#-open-source-software)
  - [Flowable](#flowable)
  - [CIB seven](#cib-seven)
  - [Operaton](#operaton)
  - [Apache jBPM (Apache KIE)](#apache-jbpm-apache-kie)
  - [m8flow](#m8flow)
  - [Bonita](#bonita)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Workflow Automation and BPM platforms. These are not open-source but are included as reference points for feature comparison.

### Zoho Flow
**Type:** No-code integration and workflow automation  
Zoho Flow connects 850+ applications with drag-and-drop workflow building, decision branches, custom variables, sub-flows, and outgoing webhooks [citation:12]. The 2026 release added Zia AI capabilities: natural language workflow creation, content generation/cleaning utilities, and agentic actions that can make context-based decisions during execution [citation:4]. Integrated within the broader Zoho ecosystem, making it accessible for organizations already using Zoho products.  
**Best for:** Teams in or near the Zoho ecosystem wanting no-code automation with emerging AI-assisted workflow capabilities.

### Zapier
**Type:** General-purpose automation platform  
Zapier connects 7,000+ apps with trigger-action workflows. Supports scheduled and webhook triggers, filters, and multi-step Zaps. The most widely adopted automation platform for non-technical users, with a massive integration library. Lacks native BPMN process modeling or human task management.

### Make
**Type:** Visual automation platform  
Make provides visual scenario building with scheduling, webhooks, and branching logic. Supports complex error handling and data transformation. Positioned between Zapier's simplicity and enterprise iPaaS complexity.

### Workato
**Type:** Enterprise automation with recipe-based workflows  
Workato provides enterprise-grade automation with recipes, triggers, and actions across 1,000+ connectors. Supports conditional logic, error handling, and approval workflows. Often used for cross-functional business processes in enterprise environments.

### Nintex
**Type:** Process automation and workflow platform  
Nintex offers workflow automation with forms, document generation, and process intelligence. Includes approval workflows with escalation and time-based reminders. Strong heritage in SharePoint-based workflows with cloud-native expansion.

### ProcessMaker
**Type:** BPM and workflow automation  
ProcessMaker is a low-code BPM platform with workflow design, form building, and process orchestration. Available as both cloud and self-hosted options. Focused on business-user-friendly process automation.

### Kissflow
**Type:** No-code workflow automation  
Kissflow provides no-code workflow and process automation with pre-built templates for approvals, procurement, and HR processes. Focused on simplicity for business users without technical backgrounds.

### Camunda 8
**Type:** Enterprise BPM with distributed orchestration  
Camunda 8 (built on the Zeebe engine) is a cloud-native platform designed for distributed service orchestration with horizontal scalability . Uses BPMN for process modeling with external workers for multi-language execution. **Key distinction:** Camunda 8 is not an upgrade from Camunda 7 — it is a different architecture requiring migration effort [citation:3]. The commercial platform has licensing costs for self-managed production deployments [citation:2].  
**Best for:** Organizations needing high-throughput, distributed service orchestration across microservices.

### Pipefy
**Type:** Workflow management with process templates  
Pipefy provides process management with pre-built workflow templates, SLA tracking, due date enforcement, and automated escalation. Focused on operations and service delivery workflows with a visual Kanban-style interface.

### Appian
**Type:** Low-code automation with process orchestration  
Appian's low-code platform includes workflow automation, process orchestration, and case management. Supports complex approval chains and process modeling with audit trails. Often used in regulated industries requiring compliance controls.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Workflow Automation and BPM platforms. All listed projects offer source code you can deploy on your own infrastructure.

### Flowable
**Stack:** Java | **License:** Apache 2.0  
A modern BPMN engine forked from Activiti, offering separate embeddable engines for BPMN 2.0, CMMN (case management), and DMN (decision management) [citation:9]. Clean modular architecture with Spring Boot starter, Docker/Kubernetes support, and a comprehensive REST API. The Flowable Modeler provides web-based modeling for BPMN, CMMN, DMN, and forms [citation:9]. **Trade-off:** Enterprise features like the Flowable Work UI require a commercial license; documentation for the modeler can be sparse [citation:9].  
**Best for:** Java development teams building cloud-native applications needing BPMN, case management, and decision logic in a single lightweight stack [citation:9]. For 90% of enterprise OA and approval scenarios, Flowable is considered sufficient and stable .

### CIB seven
**Stack:** Java | **License:** Apache 2.0  
A fork of Camunda Platform 7 created to provide a long-term open-source alternative after Camunda discontinued support for the Community Edition [citation:1]. 100% compatible with Camunda 7 — existing applications continue to operate without code changes as a drop-in replacement [citation:1]. Includes the core engine for BPMN, DMN, and CMMN, plus web applications for administration (Admin), task management (Tasklist), and operational monitoring (Cockpit) [citation:1][citation:5]. Fully on-premises deployable with Docker images and Helm charts available [citation:1].  
**Best for:** Organizations with existing Camunda 7 deployments seeking long-term open-source maintenance without migration to Camunda 8.

### Operaton
**Stack:** Java | **License:** Apache 2.0  
A community-driven fork of Camunda 7, positioned as a truly open-source BPM platform with no open-core model or single-vendor control [citation:10]. Evolved from the proven Camunda 7 codebase with over a decade of production use. Includes the process engine, REST API, and web apps (Cockpit, Tasklist, Admin). Supports H2, PostgreSQL, MySQL, MariaDB, Oracle, SQL Server, and DB2 [citation:10]. Offers an MCP server for AI integration and Keycloak plugin for identity management. Migration from Camunda 7 is supported via an OpenRewrite migration tool [citation:10].  
**Best for:** Organizations wanting Camunda 7 compatibility with community-driven governance and no vendor lock-in.

### Apache jBPM (Apache KIE)
**Stack:** Java | **License:** Apache 2.0  
Part of the Apache KIE (Knowledge Is Everything) project, combining jBPM/Kogito with Drools for business rules and DMN decisions [citation:2]. Supports BPMN process modeling with tight integration between processes and business rules. Backed by Red Hat and integrated with the JBoss/WildFly ecosystem. **Consideration:** jBPM 7 to 10 migration requires significant reimplementation; commercial support for jBPM 7 ends in 2027 [citation:11]. Configuration is complex with a steeper learning curve .  
**Best for:** Organizations in the Red Hat/JBoss ecosystem needing tight integration between BPMN processes and Drools business rules.

### m8flow
**Stack:** Python (SpiffWorkflow foundation) | **License:** Open Source  
A multi-tenant workflow orchestration platform implemented in Python, built on SpiffWorkflow [citation:6]. Supports BPMN 2.0 (pools, lanes, multi-instance tasks, sub-processes, timers, signals, messages, boundary events, loops) and DMN baseline implementation. Python-native workflows can run via Python code or JSON structures. Docker-based deployment with Keycloak, PostgreSQL, MinIO, Redis, and NATS components [citation:6]. Positioned as a modern Python-based alternative to Java-centric platforms like Camunda 7.  
**Best for:** Python-centric teams wanting a BPMN engine without adopting a Java stack.

### Bonita
**Stack:** Java | **License:** GPL-2.0 (Community)  
A complete BPM/DPA platform combining an engine, Studio (modeling), UI (task portal), and Runtime [citation:2]. Handles case management through its own patterns rather than the CMMN standard [citation:9]. The Community edition provides core BPM capabilities; commercial subscription adds support and advanced features.  
**Best for:** Business analysts wanting a complete, integrated BPM platform with a visual studio and task portal.

---

## 📊 Comparison at a Glance

| Software | License | Stack | BPMN | Human Tasks | Self-Hosted | Best For |
|----------|---------|-------|------|-------------|-------------|----------|
| **Zoho Flow** | Proprietary | Cloud | ❌ | ❌ | ❌ | Zoho ecosystem no-code automation |
| **Zapier** | Proprietary | Cloud | ❌ | ❌ | ❌ | General app-to-app automation |
| **Make** | Proprietary | Cloud | ❌ | ❌ | ❌ | Visual automation scenarios |
| **Workato** | Proprietary | Cloud | ❌ | Limited | ❌ | Enterprise recipe automation |
| **ProcessMaker** | Proprietary | Cloud | ✅ | ✅ | ✅ (core) | Low-code BPM |
| **Camunda 8** | Proprietary | Java/Zeebe | ✅ | ✅ | ✅ | Distributed orchestration |
| **Flowable** | Apache 2.0 | Java | ✅ | ✅ | ✅ | Java BPMN + CMMN + DMN |
| **CIB seven** | Apache 2.0 | Java | ✅ | ✅ | ✅ | Camunda 7 long-term OSS |
| **Operaton** | Apache 2.0 | Java | ✅ | ✅ | ✅ | Community Camunda 7 fork |
| **Apache jBPM** | Apache 2.0 | Java | ✅ | ✅ | ✅ | BPMN + Drools rules |
| **m8flow** | Open Source | Python | ✅ | ✅ | ✅ | Python BPMN engine |
| **Bonita** | GPL-2.0 | Java | ✅ | ✅ | ✅ | Complete BPM studio platform |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Workflow Automation or BPM platform that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source BPM ecosystem is Java-heavy; Python and other language options are emerging but limited.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
