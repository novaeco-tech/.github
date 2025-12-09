# 🌍 NovaEco — Digital Public Infrastructure for the Circular Economy

**NovaEco** is the open‑source **Digital Public Infrastructure** for the circular economy. It connects individuals and siloed sectors to **foster innovation**, measure impact, and **collaborate** within a federated system-of-systems.

NovaEco is commercially supported by **[Circular Engineering Nova GmbH](https://circular.engineering/)**.

---

## 🚀 Key Entry Points

The ecosystem is anchored by **four core services** (hosted in the `novaeco` repository) that provide unified identity, orchestration, and access management:

- 📊 **[Mission Control](https://app.novaeco.tech)** — Unified dashboard and launchpad for all ecosystem application.
- 🔗 **[Gateway](https://api.novaeco.tech)** — Single public API entry point for all external traffic.
- 🔐 **[Identity](https://auth.novaeco.tech)** — Centralized SSO, MFA, and Trust Profile issuance service.
- 🌐 **[Docs](https://novaeco.tech)** — Public landing page and technical documentation hub.

---

## 🏗️ Architecture Overview

NovaEco follows a **Federated Monorepo model**. Each **Enabler** or **Sector** is a self-contained monorepo that groups its API, App, Website, and Tests together.

### 1. Horizontal Enabler Monorepos
Cross‑cutting foundational services consumed by all sectors:

- **[NovaBalance](https://github.com/novaeco-tech/novabalance)** — Environmental audit engine for carbon, water, and mass[.
- **[NovaEquity](https://github.com/novaeco-tech/novaequity)** — Social audit engine tracking fair wages and labor rights.
- **[NovaFin](https://github.com/novaeco-tech/novafin)** — Ledger for payments, staking, and ESG token settlements.
- **[NovaInfra](https://github.com/novaeco-tech/novainfra)** — Registry for IoT devices and fleet management command.
- **[NovaLogistics](https://github.com/novaeco-tech/novalogistics)** — Optimization engine for reverse logistics and circular transport.
- **[NovaMaterial](https://github.com/novaeco-tech/novamaterial)** — Engine for Digital Product Passports and material lineage.
- **[NovaMind](https://github.com/novaeco-tech/novamind)** — Shared AI models and inference engine for all sectors.
- **[NovaPolicy](https://github.com/novaeco-tech/novapolicy)** — Policy-as-Code engine for automated regulatory compliance checks.
- **[NovaSkills](https://github.com/novaeco-tech/novaskills)** — Verification system for human labor certifications and degrees.
- **[NovaTrade](https://github.com/novaeco-tech/novatrade)** — Marketplace for matching orders and discovering circular assets.

### 2. Vertical Sector Monorepos
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

We welcome contributors of all kinds. Start with our [Contribution Guide](../CONTRIBUTING.md) and [Code of Conduct](../CODE_OF_CONDUCT.md).

**Finding your way:**
1. Begin with [`novaeco`](https://github.com/novaeco-tech/novaeco) to understand the platform foundation.
2. Explore Enabler or Sector repos that match your interests.
3. Check out Product repos to see how everything comes together.
