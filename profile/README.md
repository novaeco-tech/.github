# 🌍 NovaEco — Digital Public Infrastructure for the Circular Economy

**NovaEco** is an open-source, institutional-grade **Digital Public Infrastructure (DPI)** designed to break down data silos in the circular economy via a federated system-of-systems architecture. It connects individuals and siloed sectors to foster innovation, measure impact, and collaborate.

NovaEco is commercially supported by **[Circular Engineering Nova GmbH](https://circular.engineering/)**.

---

## 🏗️ Architectural Migration
*Note: We are currently migrating from our legacy prototype to a high-performance, event-driven polyrepo architecture. Our Q2/Q3 2026 development sprint is focused strictly on the core orchestration infrastructure.*

### 🧱 Core Infrastructure (Active Development)
- **[Kernel](https://github.com/novaeco-tech/novaeco)** — System Legislature: Architecture specs (ADRs), Requirements, and Governance docs.
- **[Gateway](https://github.com/novaeco-tech/novaeco-gateway)** — Unified Ingress: Hybrid REST/gRPC proxy routing public traffic.
- **[Auth](https://github.com/novaeco-tech/novaeco-auth)** — Identity Verifier: High-speed internal token validation and RBAC.
- **[UI](https://github.com/novaeco-tech/novaeco-ui)** — User Interface: Launchpad and other shared UI elements once.
- **[Website](https://github.com/novaeco-tech/novaeco-website)** — Public Portal: Marketing landing page and user guide documentation.
- **[Sentinel](https://github.com/novaeco-tech/novaeco-sentinel)** — AIOps & Governance: CI/CD drift detection and live telemetry auditing.
- **[Backup](https://github.com/novaeco-tech/novaeco-backup)** — Backup & Recovery: Disaster recovery snapshots to cold storage.
- **[QA](https://github.com/novaeco-tech/novaeco-qa)** — Quality: Central quality assurance hub. Runs inter-enabler/sector/worker/product test suites.
- **[Releases](https://github.com/novaeco-tech/novaeco-releases)** — Release manifests: defining the artifacts for each stable ecosystem release.
- **[Operations](https://github.com/novaeco-tech/novaeco-operations)** — Infrastructure as Code: Terraform and Kubernetes deployment manifests.
- **[Runtime](https://github.com/novaeco-tech/novaeco-runtime)** — Base Images: Hardened Docker images (Python/Node) used by all service builds.
- **[DevTools](https://github.com/novaeco-tech/novaeco-devtools)** — Developer Tooling: CLI, standard base images, and workspace scripts.

---

## 🌐 The Broader Ecosystem (Domains & Sectors)
*The following repositories represent the specialized business logic, data models, and vertical domains that plug into the core NovaEco infrastructure.*

### 1. Horizontal Enablers
Cross‑cutting foundational services consumed by all sectors:
- **[NovaAdmin](https://github.com/novaeco-tech/novaadmin)** — Unified dashboard and launchpad for all ecosystem applications.
- **[NovaBalance](https://github.com/novaeco-tech/novabalance)** — Environmental audit engine for carbon, water, and mass.
- **[NovaEquity](https://github.com/novaeco-tech/novaequity)** — Social audit engine tracking fair wages and labor rights.
- **[NovaFin](https://github.com/novaeco-tech/novafin)** — Ledger for payments, staking, and ESG token settlements.
- **[NovaInfra](https://github.com/novaeco-tech/novainfra)** — Registry for IoT devices and fleet management command.
- **[NovaLogistics](https://github.com/novaeco-tech/novalogistics)** — Optimization engine for reverse logistics and circular transport.
- **[NovaMaterial](https://github.com/novaeco-tech/novamaterial)** — Engine for Digital Product Passports and material lineage.
- **[NovaMind](https://github.com/novaeco-tech/novamind)** — Shared AI models and inference engine for all sectors.
- **[NovaPolicy](https://github.com/novaeco-tech/novapolicy)** — Policy-as-Code engine for automated regulatory compliance checks.
- **[NovaSkills](https://github.com/novaeco-tech/novaskills)** — Verification system for human labor certifications and degrees.
- **[NovaTrade](https://github.com/novaeco-tech/novatrade)** — Marketplace for matching orders and discovering circular assets.

### 2. Vertical Sectors
Industry‑specific applications that consume Enablers:
- **[NovaAgro](https://github.com/novaeco-tech/novaagro)** — Management of regenerative agriculture and sustainable food systems.
- **[NovaAir](https://github.com/novaeco-tech/novaair)** — Air quality monitoring and carbon capture credit verification.
- **[NovaBuild](https://github.com/novaeco-tech/novabuild)** — Management of construction lifecycles and material banks.
- **[NovaChem](https://github.com/novaeco-tech/novachem)** — Chemical leasing models and hazardous material tracking.
- **[NovaEnergy](https://github.com/novaeco-tech/novaenergy)** — Renewable grid balancing and vehicle-to-grid energy coordination.
- **[NovaMake](https://github.com/novaeco-tech/novamake)** — Distributed manufacturing via 3D printing and CNC networks.
- **[NovaNature](https://github.com/novaeco-tech/novanature)** — Biodiversity monitoring and reforestation project management.
- **[NovaPack](https://github.com/novaeco-tech/novapack)** — Reusable packaging systems and deposit return schemes.
- **[NovaRecycle](https://github.com/novaeco-tech/novarecycle)** — Management of recycling centers and urban mining recovery.
- **[NovaRetail](https://github.com/novaeco-tech/novaretail)** — Product-as-a-Service management and consumer take-back schemes.
- **[NovaTronix](https://github.com/novaeco-tech/novatronix)** — E-waste management and electronics repair documentation.
- **[NovaTextile](https://github.com/novaeco-tech/novatextile)** — Circular fashion management and fiber-to-fiber recycling loops.
- **[NovaWater](https://github.com/novaeco-tech/novawater)** — Management of industrial water cycles and treatment systems.

### 3. Worker Repos
Decoupled, single‑purpose backend services for high-throughput tasks:
- **[novaair-worker-quality](https://github.com/novaeco-tech/novaair-worker-quality)** — Ingests and normalizes data from air quality sensors.
- **[novanature-worker-bioacoustics](https://github.com/novaeco-tech/novanature-worker-bioacoustics)** — Identifies species from audio streams using AI models.
- **[novainfra-worker-iot-ingest](https://github.com/novaeco-tech/novainfra-worker-iot-ingest)** — High-throughput processor for raw telemetry from sensors.
- **[novabalance-worker-lca-calculator](https://github.com/novaeco-tech/novabalance-worker-lca-calculator)** — Calculates real-time environmental impact from material BOMs.
- **[novamake-worker-slicer-check](https://github.com/novaeco-tech/novamake-worker-slicer-check)** — Verifies 3D model printability for manufacturing jobs.
- **[novafin-worker-trade-settlement](https://github.com/novaeco-tech/novafin-worker-trade-settlement)** — Asynchronously batches and commits transactions to the ledger.

### 4. Product Repos
Flagship applications combining multiple sectors:
- **[DurasAGV](https://github.com/novaeco-tech/product-duras-agv)** — Autonomous agricultural robot for regenerative farming tasks.
- **[NovaLab](https://github.com/novaeco-tech/product-nova-lab)** — Innovation engine for designing and launching circular projects.
- **[RetailLoop](https://github.com/novaeco-tech/product-retail-loop)** — E-commerce plugin for resale and product take-back.
- **[UrbanMiner](https://github.com/novaeco-tech/product-urban-miner)** — Dashboard for city councils to map municipal waste streams.

---

## 🤝 Contributing

We welcome contributors of all kinds. All core infrastructure is licensed under **Apache 2.0**. Start with our [Contribution Guide](../CONTRIBUTING.md) and [Code of Conduct](../CODE_OF_CONDUCT.md).

**Finding your way:**
1. Begin with [`novaeco`](https://github.com/novaeco-tech/novaeco) to understand the platform foundation and architectural definitions.
2. Explore the Core Infrastructure repos to understand the event-driven routing mesh.
3. Check out the Domain Enablers and Sectors to see how vertical business logic plugs into the ecosystem.
