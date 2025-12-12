# 👋 Welcome to the NovaEco!

Thank you for your interest in contributing to the open-source operating system for a circular economy! We are thrilled to have you here.

Whether you're a developer, designer, policy expert, or just passionate about sustainability, your contributions are welcome and valued. This document is the "getting started" guide for our entire ecosystem.

First, please read our **[Code of Conduct](./CODE_OF_CONDUCT.md)**. We are committed to maintaining an open, welcoming, and respectful community for all.

## 🗺️ How Our Organization is Structured

Our organization uses a **Federated Monorepo model** to group related code, making it easier to develop and test features atomically.

1.  **`novaeco`**: **The Core Monorepo.** This is the "heart" that runs the entire system. It contains our central `/api` (Gateway), `/auth` (Identity), and `/website` (Docs).
2.  **Horizontal Enabler Monorepos** (e.g., `novaadmin`, `novahub`, `novafin`, `novabalance`): **The Foundational Services.** These are the cross-cutting, shared services (like finance, or auditing) that all sectors consume.
3.  **Vertical Sector Monorepos** (e.g., `novaagro`, `novawater`, `novabuild`): **The Industry Applications.** These are the end-user-facing applications for a specific market, which are built by *consuming* the enablers.
4.  **Decoupled Workers** (e.g., `novaair-worker-quality`): **Backend Services.** These are separate, single-purpose repos for background tasks, developed and deployed independently.
5.  **Central Governance** (e.g., `ecosystem-qa`, `ecosystem-releases`): Repos that manage testing *between* repositories and define our official releases.
6.  **Products** (e.g., `product-duras-agv`): Standalone "flagship" product monorepos that consume services from multiple **Enablers** and **Sectors**.

You can read a full description of every repository on our [**Organization README**](https://github.com/novaeco-tech).

## 🚀 How to Get Started

### 1. See the Big Picture

To understand our vision and where we're headed, start with our high-level planning tools:

  * **Ecosystem Development Roadmap:** Our main [**project board**](https://github.com/orgs/novaeco-tech/projects/1) tracks major, cross-ecosystem initiatives and high-level features.
  * **Ecosystem Discussions:** For brainstorming, Q&A, and early-stage idea refinement, join our [discussions](https://github.com/orgs/novaeco-tech/discussions/).

### 2. Find Your First Contribution

Want to dive in? We've made it easy to find a place to start.

1.  **Start with Documentation:** The easiest way to contribute is to help with our docs. Find a typo, a confusing sentence, or suggest a new guide.
      * **Go to the docs directory:** [**`novaeco/website`**](https://github.com/novaeco-tech/novaeco/tree/main/website)

2.  **Find a Beginner-Friendly Task:** We tag simple, well-scoped tasks just for new contributors.
    * **Browse `good first issues`:** [**Find all `good first issue 🌱` tasks**](https://github.com/search?q=org%3Anovaeco-tech+is%3Aopen+is%3Aissue+label%3A%22good+first+issue+%F0%9F%8C%B1%22)
    * **Check the Ecosystem Development Roadmap:** [**View the `Good First Issues 🌱` Roadmap**](https://github.com/orgs/novaeco-tech/projects/1/views/6)

3.  **Help Where It's Wanted:** Look for tasks the core team has specifically requested help on.
      * **Browse `help wanted` issues:** [**Find all `help wanted 🤝` tasks**](https://github.com/search?q=org%3Anovaeco-tech+is%3Aopen+is%3Aissue+label%3A%22help+wanted+%F0%9F%A4%9D%22)

4.  **Pick Up a "Ready" Task:** Once you're more comfortable, you can grab any task that's fully scoped and ready to be built.
      * **View the "Ready" column:** [table](https://github.com/orgs/novaeco-tech/projects/1/views/4)

-----

## 🏷️ How We Use Issues & Labels

We use issues, labels, and project boards to manage all work. Understanding them is key to contributing.

### Issue Types (GitHub standard)

Across the ecosystem, we use the standard GitHub Issue Type values (selected when creating an issue or PR):

  * **Task**
  * **Bug**
  * **Feature**

Set the correct **Type** when creating an issue so items can be filtered and mapped to Projects automatically.

### Label Set

We maintain a small, consistent set of organization-wide labels.

| Label | Purpose |
| :--- | :--- |
| **`good first issue 🌱`** | Simple, well-scoped tasks ideal for newcomers. |
| **`help wanted 🤝`** | Open for contribution: maintainers welcome external help. |
| **`blocked ⛔`** | Work cannot proceed due to external dependency. |
| **`hotfix 🔥`** | Urgent fix required for production stability. |
| **`needs design 🖌️`** | Requires UX/UI design input. |
| **`needs dev 💻`** | Requires coding or engineering expertise. |
| **`needs docs 📝`** | Requires technical writing or documentation updates. |
| **`needs expert-input 🎯`** | Needs input from a subject matter expert. |
| **`needs legal 📜`** | Requires legal or compliance review. |
| **`needs pm 📊`** | Requires product management input for scope/clarity. |

### Filter by your skills using labels (How to Contribute by Role)

Filter issues and the roadmap by the labels that describe the skills or input required. This helps you quickly find work that matches your strengths.

  * **`needs dev 💻`** — Requires coding or engineering expertise.
  * **`needs docs 📝`** — Requires technical writing or documentation updates.
  * **`needs design 🖌️`** — Needs UX/UI or visual design input.
  * **`needs expert-input 🎯`** — Needs subject-matter expertise (e.g., in a **Vertical Sector** like `novaagro` or a **Horizontal Enabler** like `novafin`).
  * **`needs legal 📜`** — Requires legal or compliance review (e.g., for **Enablers** like `novapolicy` or `novafin`).
  * **`needs pm 📊`** — Requires product management input for scope, acceptance criteria, or prioritization.

-----

## ⚙️ Our Contribution Workflow

### 1. How Triage Works

Our workflow is managed using the [project board](https://github.com/orgs/novaeco-tech/projects/1/).

  * **Triage:** The inbox for new issues. Maintainers review, add labels from the official set, set **Type**, **Priority**, and **Difficulty**, and move the item to the `Ready` column.
  * **Ready:** Fully scoped and prioritized issues ready for contributors to pick up. **This is the main column to find work.**
  * **In Progress:** Issues that have been assigned and are actively being worked on.
  * **In Review:** Issues with an open Pull Request awaiting review.
  * **Done:** Pull Requests have been merged and the work is complete.

### 2. Code Contribution Steps

We follow a standard "fork-and-pull" Git workflow.

1.  **Find an Issue:** Find an issue in the **`Ready`** column of our [project board](https://github.com/orgs/novaeco-tech/projects/1) that you want to work on.
2.  **Claim it:** Comment on the issue to say you want it. A maintainer will assign it to you and move it to **`In Progress`**.
3.  **Fork:** Fork the specific monorepo (e.g., `novahub` or `novaeco`) to your personal GitHub account.
4.  **Create a Branch:** Create a new branch with a descriptive name. We recommend:
      * `feat/your-feature-name` (for new features)
      * `fix/bug-description` (for bug fixes)
      * `docs/topic-you-are-updating` (for documentation)
5.  **Code & Commit:** Make your changes. Write clear, atomic commits. We strongly recommend [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) (e.g., `feat: add user login button`, `docs: fix typo in README`).
6.  **Test:**
      * Run the local tests for the component(s) you changed (e.g., `npm test` in the `novahub/api` directory).
      * Run the **intra-enabler/intra-sector integration tests** at the root of the monorepo (e.g., `npm test:integration` in the `novahub` repo's root).
      * If your change affects other *repositories* (like `novahub` and `novaair-worker-quality`), please describe the scenario in your Pull Request. The core team will run it against our central **`ecosystem-qa`** test suite.
7.  **Submit a Pull Request (PR):**
      * Push your branch to your fork.
      * Open a Pull Request from your branch to the `main` branch of the `novaeco-tech` repository.
      * **Link your PR to the issue** (e.g., "Closes #123"). This will automatically move the issue to the **`In Review`** column.
      * Fill out the PR template with a clear description of *what* you did and *why*.
8.  **Review:** A core team member will review your code, provide feedback, and merge it when it's ready.

-----

## 📖 Our Development Standards

  * **API Design:** Our internal services use **gRPC/Protobuf** for high performance and upgradability. Our public-facing API (in the **`novaeco`** repo) translates these into **REST/JSON** for ease of use.
  * **Versioning:** We use a hybrid model:
      * **SemVer (e.g., `v1.2.0`)** for all individual release artifacts (our `.tar.gz` packages).
      * **CalVer (e.g., `v2025.11.0`)** for our high-level "Ecosystem Release" (a "meta-package" of tested, compatible SemVer artifacts).
  * **Code Style:** Most of our projects use `Prettier` and `ESLint` (for JS/TS) or equivalent linters. Please check the local `README.md` and `package.json` of the component you're working in.
  * **Tooling:** We use the internal **`novaeco` CLI** to manage workspaces and releases.
      * **Install:** `pip install "git+https://github.com/novaeco-tech/ecosystem-devtools.git@main#subdirectory=novaeco-cli"`
      * **Bootstrap:** Run `novaeco init` to clone all repos and set up your VS Code workspace.

### Label & Project Hygiene (For Maintainers)

  * We run an org-wide label sync from `.github/labels.json`. Do not rename official labels locally; open an issue in this repo to discuss changes.
  * Project custom fields (Status, Priority, Difficulty) are authoritative for the roadmap and are set by maintainers during triage.

## 🛡️ Security Vulnerability Reporting

Please **do not** report security vulnerabilities on the public issue tracker. If you find a security issue, please send a private email to **`security@novaeco.tech`**.

## 💬 Get in Touch

  * **General Questions:** Use our **[discussions board](https://github.com/orgs/novaeco-tech/discussions)**.
  * **Specific Bugs/Features:** Use the **Issues** tab on the specific repository.
  * **Corporate/Legal:** [contact@novaeco.tech](mailto:contact@novaeco.tech)

Thank you for helping us build the future of the circular economy!