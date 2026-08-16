# ECC Subagents

68 Subagents aus [affaan-m/ECC](https://github.com/affaan-m/ECC) (v2.2.0, Commit `50743ce`, MIT-Lizenz),
installiert unter `.claude/agents/`.

Claude Code lädt jede `.md`-Datei in diesem Verzeichnis automatisch als Subagent, sobald du in
diesem Repository arbeitest. Prüfen mit `/agents`, aufrufen z. B. mit
„use the security-reviewer subagent to check this diff".

## Installation auf einem anderen Rechner

**Projektweit** (nur in diesem Repo aktiv) — bereits erledigt, nichts zu tun.

**Benutzerweit** (in allen Projekten aktiv):

```bash
cp .claude/agents/*.md ~/.claude/agents/
```

**Direkt aus ECC** (offizieller Installer, holt zusätzlich `AGENTS.md` und die
Antigravity-Skills):

```bash
git clone https://github.com/affaan-m/ECC.git
cd ECC && npm install
node scripts/install-apply.js --target claude --modules agents-core   # -> ~/.claude/
node scripts/install-apply.js --target claude-project --modules agents-core  # -> ./.claude/
```

`--dry-run` anhängen, um den Plan ohne Dateikopien zu sehen.

## Aktualisieren

```bash
git clone --depth 1 https://github.com/affaan-m/ECC.git /tmp/ecc
cp /tmp/ecc/agents/*.md .claude/agents/
```

## Enthaltene Agents

| Agent | Modell | Beschreibung |
|---|---|---|
| `a11y-architect` | sonnet | Accessibility Architect specializing in WCAG 2 |
| `agent-evaluator` | sonnet | Evaluates agent output against 5-axis quality rubric (accuracy, completeness, clarity, ... |
| `architect` | opus | Software architecture specialist for system design, scalability, and technical decision... |
| `build-error-resolver` | sonnet | Build and TypeScript error resolution specialist |
| `chief-of-staff` | sonnet | Personal communication chief of staff that triages email, Slack, LINE, and Messenger |
| `code-architect` | sonnet | Designs feature architectures by analyzing existing codebase patterns and conventions, ... |
| `code-explorer` | sonnet | Deeply analyzes existing codebase features by tracing execution paths, mapping architec... |
| `code-reviewer` | sonnet | Expert code review specialist |
| `code-simplifier` | sonnet | Simplifies and refines code for clarity, consistency, and maintainability while preserv... |
| `comment-analyzer` | haiku | Analyze code comments for accuracy, completeness, maintainability, and comment rot risk |
| `conversation-analyzer` | haiku | Use this agent when analyzing conversation transcripts to find behaviors worth preventi... |
| `cpp-build-resolver` | sonnet | C++ build, CMake, and compilation error resolution specialist |
| `cpp-reviewer` | sonnet | Expert C++ code reviewer specializing in memory safety, modern C++ idioms, concurrency,... |
| `csharp-reviewer` | sonnet | Expert C# code reviewer specializing in |
| `dart-build-resolver` | sonnet | Dart/Flutter build, analysis, and dependency error resolution specialist |
| `database-reviewer` | sonnet | PostgreSQL database specialist for query optimization, schema design, security, and per... |
| `django-build-resolver` | sonnet | Django/Python build, migration, and dependency error resolution specialist |
| `django-reviewer` | sonnet | Expert Django code reviewer specializing in ORM correctness, DRF patterns, migration sa... |
| `doc-updater` | haiku | Documentation and codemap specialist |
| `docs-lookup` | haiku | When the user asks how to use a library, framework, or API or needs up-to-date code exa... |
| `e2e-runner` | sonnet | End-to-end testing specialist using Vercel Agent Browser (preferred) with Playwright fa... |
| `fastapi-reviewer` | sonnet | Reviews FastAPI applications for async correctness, dependency injection, Pydantic sche... |
| `flutter-reviewer` | sonnet | Flutter and Dart code reviewer |
| `fsharp-reviewer` | sonnet | Expert F# code reviewer specializing in functional idioms, type safety, pattern matchin... |
| `gan-evaluator` | sonnet | GAN Harness — Evaluator agent |
| `gan-generator` | sonnet | GAN Harness — Generator agent |
| `gan-planner` | sonnet | GAN Harness — Planner agent |
| `go-build-resolver` | sonnet | Go build, vet, and compilation error resolution specialist |
| `go-reviewer` | sonnet | Expert Go code reviewer specializing in idiomatic Go, concurrency patterns, error handl... |
| `harmonyos-app-resolver` | sonnet | HarmonyOS application development expert specializing in ArkTS and ArkUI |
| `harness-optimizer` | sonnet | Analyze and improve the local agent harness configuration for reliability, cost, and th... |
| `healthcare-reviewer` | opus | Reviews healthcare application code for clinical safety, CDSS accuracy, PHI compliance,... |
| `homelab-architect` | sonnet | Designs home and small-lab network plans from hardware inventory, goals, and operator e... |
| `java-build-resolver` | sonnet | Java/Maven/Gradle build, compilation, and dependency error resolution specialist |
| `java-reviewer` | sonnet | Expert Java code reviewer for Spring Boot and Quarkus projects |
| `kotlin-build-resolver` | sonnet | Kotlin/Gradle build, compilation, and dependency error resolution specialist |
| `kotlin-reviewer` | sonnet | Kotlin and Android/KMP code reviewer |
| `loop-operator` | sonnet | Operate autonomous agent loops, monitor progress, and intervene safely when loops stall |
| `marketing-agent` | sonnet | Marketing strategist and copywriter for campaign planning, audience research, positioni... |
| `mle-reviewer` | sonnet | Production machine-learning engineering reviewer for data contracts, feature pipelines,... |
| `network-architect` | sonnet | Designs enterprise or multi-site network architecture from requirements, using existing... |
| `network-config-reviewer` | sonnet | Reviews router and switch configurations for security, correctness, stale references, r... |
| `network-troubleshooter` | sonnet | Diagnoses network connectivity, routing, DNS, interface, and policy symptoms with a rea... |
| `opensource-forker` | haiku | Fork any project for open-sourcing |
| `opensource-packager` | haiku | Generate complete open-source packaging for a sanitized project |
| `opensource-sanitizer` | sonnet | Verify an open-source fork is fully sanitized before release |
| `performance-optimizer` | sonnet | Performance analysis and optimization specialist |
| `php-reviewer` | sonnet | Expert PHP code reviewer specializing in PSR-12 compliance, PHP type system, Eloquent O... |
| `planner` | opus | Expert planning specialist for complex features and refactoring |
| `pr-test-analyzer` | sonnet | Review pull request test coverage quality and completeness, with emphasis on behavioral... |
| `python-reviewer` | sonnet | Expert Python code reviewer specializing in PEP 8 compliance, Pythonic idioms, type hin... |
| `pytorch-build-resolver` | sonnet | PyTorch runtime, CUDA, and training error resolution specialist |
| `rag-pipeline-reviewer` | sonnet | Reviews RAG (Retrieval-Augmented Generation) pipelines for retrieval quality, chunking ... |
| `react-build-resolver` | sonnet | Diagnose and fix React build failures across Vite, webpack, Next |
| `react-reviewer` | sonnet | Expert React/JSX code reviewer specializing in hook correctness, render performance, se... |
| `refactor-cleaner` | sonnet | Dead code cleanup and consolidation specialist |
| `rust-build-resolver` | sonnet | Rust build, compilation, and dependency error resolution specialist |
| `rust-reviewer` | sonnet | Expert Rust code reviewer specializing in ownership, lifetimes, error handling, unsafe ... |
| `security-reviewer` | sonnet | Security vulnerability detection and remediation specialist |
| `seo-specialist` | sonnet | SEO specialist for technical SEO audits, on-page optimization, structured data, Core We... |
| `silent-failure-hunter` | sonnet | Review code for silent failures, swallowed errors, bad fallbacks, and missing error pro... |
| `spec-miner` | opus | Extracts behavioral specs from existing codebases for OpenSpec |
| `swift-build-resolver` | sonnet | Swift/Xcode build, compilation, and dependency error resolution specialist |
| `swift-reviewer` | sonnet | Expert Swift code reviewer specializing in protocol-oriented design, value semantics, A... |
| `tdd-guide` | sonnet | Test-Driven Development specialist enforcing write-tests-first methodology |
| `type-design-analyzer` | sonnet | Analyze type design for encapsulation, invariant expression, usefulness, and enforcement |
| `typescript-reviewer` | sonnet | Expert TypeScript/JavaScript code reviewer specializing in type safety, async correctne... |
| `vue-reviewer` | sonnet | Expert Vue |

## Hinweise

- Die Agents sind reine Prompt-Definitionen (Markdown + YAML-Frontmatter). Sie führen beim
  Laden keinen Code aus; die erlaubten Tools stehen im `tools:`-Feld jeder Datei.
- `model: opus|sonnet|haiku` im Frontmatter steuert, welches Modell der Subagent nutzt.
- ECC bringt darüber hinaus 285 Skills, Hooks, Rules und Commands mit — hier bewusst **nicht**
  installiert, da nur die Agents angefragt waren.
