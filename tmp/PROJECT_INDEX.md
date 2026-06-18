# Project Index: ai-service-skill

> **Target Audience**: Overseas developer community (English-first)  
> **Internal Codename**: `ai-service-skill` / TRTC AI Customer Service Skill  
> **Generated**: 2026-06-18  
> **Total Tracked Files**: ~171 (text files: `.py`, `.md`, `.yaml`, `.sh`, `.js`, `.css`, `.html`, `.json`, `.j2`, `.tpl`, `.txt`, `.example`)

---

## Purpose

This Skill packages **Tencent Cloud TRTC Conversational AI** capabilities into a plug-and-play AI agent that helps developers (even zero-code users) rapidly build a voice-centric AI customer service system. It supports two paths:
- **Quick Experience (Path A)**: A ready-made voice agent UI + ticket dashboard
- **Integration (Path B)**: Backend APIs for existing projects

---

## Directory Structure Overview

```
ai-service-skill/
├── SKILL.md                    # ★ Main entry point / SOP for Coding Agent (932 lines)
├── README.md                   # Public-facing README
├── start.sh                    # Bootstrap script (dep install + service start)
│
├── capabilities/               # Pluggable service capabilities
│   ├── conversation-core/      # Core voice agent skeleton (TRTC)
│   ├── knowledge-base/         # FAQ / RAG knowledge retrieval
│   ├── human-handoff/          # Escalation to human agent + ticket mgmt
│   ├── session-summary/        # Conversation summarization
│   ├── tool-calling/           # Function/tool calling integration
│   └── digital-human/          # Digital human (placeholder)
│
├── scenarios/                  # End-user scenarios (UI + config)
│   ├── customer-service/       # Path A: Demo UI (voice agent + admin board)
│   └── custom-builder/         # Path B: Capability selection wizard
│
├── auto_adapters/              # Tech stack auto-adapters
│   ├── frontend-spa/           # React / Vue / Angular component templates
│   ├── python-backend/         # Flask / FastAPI / Django templates
│   ├── node-backend/           # Express / Fastify / Koa templates
│   ├── java-backend/           # SpringBoot / Quarkus templates
│   └── integration_templates/  # Generic REST API / frontend/backend guides
│
├── scripts/                    # AI-invoked tool scripts
│   ├── add-capability.py       # Capability assembly
│   ├── setup-credentials.py    # Interactive credential config
│   ├── verify-credentials.py   # Credential validation (3 keys)
│   ├── contract-adapt.py       # Interface contract adaptation
│   ├── detect-stack.py         # Tech stack detection
│   ├── post-install-patch.py   # Post-install patching
│   └── lib/                    # Reusable modules (12 files)
│
├── references/                 # Reference specs
│   └── business-contract-spec.md
│
└── tests/                      # Test suite (10 files)
```

---

## Detailed File Inventory

### Legend
- `[ZH]` = Contains Chinese characters → needs English translation
- `[EN]` = Already English only → no changes needed
- **Bold** = High-priority files (user-facing or large)

---

### ROOT LEVEL (3 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`SKILL.md`** | Markdown (SOP) | `[ZH]` | ⭐⭐⭐ |
| **`README.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| **`start.sh`** | Shell script | `[ZH]` | ⭐⭐ |

---

### references/ (1 file)

| File | Type | Status | Priority |
|------|------|--------|----------|
| `references/business-contract-spec.md` | Markdown | `[ZH]` | ⭐⭐ |

---

### scripts/ (18 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`scripts/add-capability.py`** | Python | `[ZH]` | ⭐⭐⭐ |
| **`scripts/contract-adapt.py`** | Python | `[ZH]` | ⭐⭐ |
| **`scripts/detect-stack.py`** | Python | `[ZH]` | ⭐⭐ |
| **`scripts/post-install-patch.py`** | Python | `[ZH]` | ⭐⭐ |
| **`scripts/setup-credentials.py`** | Python | `[ZH]` | ⭐⭐⭐ |
| **`scripts/verify-credentials.py`** | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/__init__.py` | Python | `[ZH]` | ⭐ |
| `scripts/lib/adapter_codegen.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/arbitrator.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/contract_resolver.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/credential_validators.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/curl_parser.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/degrader.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/injector.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/manifest_resolver.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/openapi_parser.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/stack_detector.py` | Python | `[ZH]` | ⭐⭐ |
| `scripts/lib/tokens_compile.py` | Python | `[ZH]` | ⭐⭐ |

---

### tests/ (10 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| `tests/__init__.py` | Python | `[ZH]` | ⭐ |
| `tests/test_arbitrator.py` | Python | `[ZH]` | ⭐ |
| `tests/test_capability_overlay.py` | Python | `[ZH]` | ⭐ |
| `tests/test_contract_resolver.py` | Python | `[ZH]` | ⭐ |
| `tests/test_handoff_ports.py` | Python | `[ZH]` | ⭐ |
| `tests/test_kb_ports.py` | Python | `[ZH]` | ⭐ |
| `tests/test_manifest_resolver.py` | Python | `[ZH]` | ⭐ |
| `tests/test_recipe_assembly.py` | Python | `[ZH]` | ⭐ |
| `tests/test_stack_and_degrader.py` | Python | `[ZH]` | ⭐ |
| `tests/test_verify_credentials.py` | Python | `[ZH]` | ⭐ |

---

### capabilities/conversation-core/ (21 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`capabilities/conversation-core/.env.example`** | Config | `[ZH]` | ⭐⭐ |
| **`capabilities/conversation-core/INTEGRATION.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| **`capabilities/conversation-core/INTERFACE_ADAPT.md`** | Markdown | `[ZH]` | ⭐⭐ |
| **`capabilities/conversation-core/QUICK_START.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| `capabilities/conversation-core/requirements.txt` | Config | `[EN]` | — |
| **`capabilities/conversation-core/manifest.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |
| `capabilities/conversation-core/src/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/conversation-core/src/_capability_loader.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/agent.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/credentials.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/health.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/log_filter.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/modality.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/server.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/trtc_client.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/src/usersig.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/tests/__init__.py` | Python | `[EN]` | — |
| `capabilities/conversation-core/tests/test_skeleton.py` | Python | `[ZH]` | ⭐ |
| `capabilities/conversation-core/web-demo/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/web-demo/app.js` | JavaScript | `[ZH]` | ⭐⭐ |
| `capabilities/conversation-core/web-demo/index.html` | HTML | `[EN]` | — |
| `capabilities/conversation-core/web-demo/styles.css` | CSS | `[EN]` | — |

---

### capabilities/knowledge-base/ (18 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`capabilities/knowledge-base/INTERFACE_ADAPT.md`** | Markdown | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| **`capabilities/knowledge-base/manifest.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |
| `capabilities/knowledge-base/data/faq.json` | JSON Data | `[EN]` | — |
| `capabilities/knowledge-base/src/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/knowledge-base/src/retriever.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/router.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/adapters/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/knowledge-base/src/adapters/default_rest.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/adapters/factory.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/adapters/local_json.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/adapters/mock.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/core/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/knowledge-base/src/core/models.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/core/scoring.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/core/service.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/knowledge-base/src/ports/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/knowledge-base/src/ports/kb_client.py` | Python | `[ZH]` | ⭐⭐ |

---

### capabilities/human-handoff/ (19 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`capabilities/human-handoff/INTERFACE_ADAPT.md`** | Markdown | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| **`capabilities/human-handoff/manifest.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |
| `capabilities/human-handoff/src/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/human-handoff/src/queue.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/router.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/summary_link.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/trigger.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/adapters/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/human-handoff/src/adapters/default_rest.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/adapters/factory.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/adapters/local_queue.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/adapters/mock.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/core/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/human-handoff/src/core/intent_detector.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/core/models.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/core/service.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/human-handoff/src/ports/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/human-handoff/src/ports/handoff_client.py` | Python | `[ZH]` | ⭐⭐ |

---

### capabilities/session-summary/ (14 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`capabilities/session-summary/INTERFACE_ADAPT.md`** | Markdown | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| **`capabilities/session-summary/manifest.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |
| `capabilities/session-summary/data/test_session.json` | JSON | `[ZH]` | ⭐ |
| `capabilities/session-summary/src/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/session-summary/src/recorder.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/router.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/summarizer.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/adapters/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/session-summary/src/adapters/base.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/adapters/default_rest.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/adapters/factory.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/adapters/local_json.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/session-summary/src/adapters/mock.py` | Python | `[ZH]` | ⭐⭐ |

---

### capabilities/tool-calling/ (10 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`capabilities/tool-calling/INTERFACE_ADAPT.md`** | Markdown | `[ZH]` | ⭐⭐ |
| `capabilities/tool-calling/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| **`capabilities/tool-calling/manifest.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |
| `capabilities/tool-calling/data/tools.yaml` | YAML Config | `[ZH]` | ⭐⭐ |
| `capabilities/tool-calling/examples/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/tool-calling/examples/local_tools.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/tool-calling/src/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/tool-calling/src/dispatcher.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/tool-calling/src/registry.py` | Python | `[ZH]` | ⭐⭐ |
| `capabilities/tool-calling/src/router.py` | Python | `[ZH]` | ⭐⭐ |

---

### capabilities/digital-human/ (3 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| `capabilities/digital-human/README.md` | Markdown | `[ZH]` | ⭐ |
| `capabilities/digital-human/manifest.yaml` | YAML Config | `[ZH]` | ⭐⭐ |
| `capabilities/digital-human/src/__init__.py` | Python | `[ZH]` | ⭐ |
| `capabilities/digital-human/src/router.py` | Python | `[ZH]` | ⭐⭐ |

---

### capabilities/__init__.py (1 file)

| File | Type | Status | Priority |
|------|------|--------|----------|
| `capabilities/__init__.py` | Python | `[ZH]` | ⭐ |

---

### scenarios/customer-service/ (13 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`scenarios/customer-service/README.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| **`scenarios/customer-service/recipe.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |
| **`scenarios/customer-service/system-prompt.template.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| `scenarios/customer-service/sample-data/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| **`scenarios/customer-service/sample-data/faq-sample.json`** | JSON Data | `[ZH]` | ⭐⭐⭐ |
| `scenarios/customer-service/ui/design-system/DESIGN_GUIDELINES.md` | Markdown | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/voice-customer-service/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/voice-customer-service/app.js` | JavaScript | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/voice-customer-service/tokens.css` | CSS | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/voice-customer-service/data.js` | JavaScript | `[EN]` | — |
| `scenarios/customer-service/ui/voice-customer-service/index.html` | HTML | `[EN]` | — |
| `scenarios/customer-service/ui/voice-customer-service/mock-shop.json` | JSON | `[EN]` | — |
| `scenarios/customer-service/ui/voice-customer-service/styles.css` | CSS | `[EN]` | — |
| `scenarios/customer-service/ui/widget-floating/agent-link.js` | JavaScript | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/widget-floating/app.js` | JavaScript | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/widget-floating/index.html` | HTML | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/widget-floating/styles.css` | CSS | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/widget-floating/tokens.css` | CSS | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/admin-board/app.js` | JavaScript | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/admin-board/index.html` | HTML | `[EN]` | — |
| `scenarios/customer-service/ui/admin-board/styles.css` | CSS | `[ZH]` | ⭐⭐ |
| `scenarios/customer-service/ui/admin-board/tokens.css` | CSS | `[ZH]` | ⭐⭐ |

---

### scenarios/custom-builder/ (7 files)

| File | Type | Status | Priority |
|------|------|--------|----------|
| **`scenarios/custom-builder/README.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| `scenarios/custom-builder/output-templates/recipe.yaml.j2` | Jinja Template | `[ZH]` | ⭐⭐ |
| **`scenarios/custom-builder/prompts/q1-business-scenario.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| **`scenarios/custom-builder/prompts/q2-io-modality.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| **`scenarios/custom-builder/prompts/q3-ui-form.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |
| **`scenarios/custom-builder/prompts/q4-capabilities.md`** | Markdown | `[ZH]` | ⭐⭐⭐ |

---

### auto_adapters/ (24 files)

#### Root + README

| File | Type | Status | Priority |
|------|------|--------|----------|
| `auto_adapters/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| **`auto_adapters/manifest.yaml`** | YAML Config | `[ZH]` | ⭐⭐⭐ |

#### frontend-spa/

| File | Type | Status | Priority |
|------|------|--------|----------|
| `auto_adapters/frontend-spa/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| `auto_adapters/frontend-spa/manifest.yaml` | YAML Config | `[ZH]` | ⭐⭐ |
| `auto_adapters/frontend-spa/angular/voice-agent.component.ts.tpl` | TypeScript TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/frontend-spa/react/VoiceAgent.tsx.tpl` | TSX TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/frontend-spa/vue/VoiceAgent.vue.tpl` | Vue TPL | `[ZH]` | ⭐⭐ |

#### python-backend/

| File | Type | Status | Priority |
|------|------|--------|----------|
| `auto_adapters/python-backend/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| `auto_adapters/python-backend/manifest.yaml` | YAML Config | `[ZH]` | ⭐⭐ |
| `auto_adapters/python-backend/django.py.tpl` | Python TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/python-backend/fastapi.py.tpl` | Python TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/python-backend/flask.py.tpl` | Python TPL | `[ZH]` | ⭐⭐ |

#### node-backend/

| File | Type | Status | Priority |
|------|------|--------|----------|
| `auto_adapters/node-backend/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| `auto_adapters/node-backend/manifest.yaml` | YAML Config | `[ZH]` | ⭐⭐ |
| `auto_adapters/node-backend/express.js.tpl` | JavaScript TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/node-backend/fastify.js.tpl` | JavaScript TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/node-backend/koa.js.tpl` | JavaScript TPL | `[ZH]` | ⭐⭐ |

#### java-backend/

| File | Type | Status | Priority |
|------|------|--------|----------|
| `auto_adapters/java-backend/README.md` | Markdown | `[ZH]` | ⭐⭐ |
| `auto_adapters/java-backend/manifest.yaml` | YAML Config | `[ZH]` | ⭐⭐ |
| `auto_adapters/java-backend/quarkus/VoiceAgentFilter.java.tpl` | Java TPL | `[ZH]` | ⭐⭐ |
| `auto_adapters/java-backend/springboot/VoiceAgentFilter.java.tpl` | Java TPL | `[ZH]` | ⭐⭐ |

#### integration_templates/

| File | Type | Status | Priority |
|------|------|--------|----------|
| `auto_adapters/integration_templates/generic-backend.md` | Markdown | `[ZH]` | ⭐⭐ |
| `auto_adapters/integration_templates/generic-frontend.md` | Markdown | `[ZH]` | ⭐⭐ |
| `auto_adapters/integration_templates/generic-rest-api.md` | Markdown | `[ZH]` | ⭐⭐ |

---

## Summary Statistics

| Category | Total | With Chinese [ZH] | Already English [EN] |
|----------|------:|------------------:|---------------------:|
| Root-level files | 3 | 3 | 0 |
| `references/` | 1 | 1 | 0 |
| `scripts/` (top) | 6 | 6 | 0 |
| `scripts/lib/` | 12 | 12 | 0 |
| `tests/` | 10 | 10 | 0 |
| `capabilities/` (root) | 1 | 1 | 0 |
| `capabilities/conversation-core/` | 21 | 17 | 4 |
| `capabilities/knowledge-base/` | 18 | 17 | 1 |
| `capabilities/human-handoff/` | 19 | 19 | 0 |
| `capabilities/session-summary/` | 14 | 14 | 0 |
| `capabilities/tool-calling/` | 10 | 10 | 0 |
| `capabilities/digital-human/` | 4 | 4 | 0 |
| `scenarios/customer-service/` | 22 | 17 | 5 |
| `scenarios/custom-builder/` | 7 | 7 | 0 |
| `auto_adapters/` | 24 | 24 | 0 |
| **TOTAL** | **~171** | **~161** | **10** |

---

## Translation Priority Groups

### Batch 1: TOP Priority (⭐⭐⭐) — User-facing core docs & SOP
Files that define the Skill's public interface and user experience.
- `SKILL.md` (932 lines)
- `README.md`
- `scenarios/customer-service/README.md`
- `scenarios/custom-builder/README.md`
- `capabilities/conversation-core/INTEGRATION.md`
- `capabilities/conversation-core/QUICK_START.md`
- All `manifest.yaml` files under `capabilities/*/`
- `scenarios/customer-service/recipe.yaml`
- `scenarios/customer-service/system-prompt.template.md`
- `scenarios/customer-service/sample-data/faq-sample.json`
- All `prompts/q*.md` under `scenarios/custom-builder/prompts/`
- `auto_adapters/manifest.yaml`
- `scripts/add-capability.py`
- `scripts/setup-credentials.py`

### Batch 2: HIGH Priority (⭐⭐) — Integration docs, adapters, key scripts
Important infrastructure and integration surface.
- `capabilities/*/INTERFACE_ADAPT.md` (all 5 capability modules)
- `capabilities/*/README.md` (all 5 capability modules)
- `auto_adapters/*/README.md` (all adapter READMEs)
- `auto_adapters/*/*.tpl` (all 11 code templates)
- `auto_adapters/integration_templates/*.md` (3 files)
- `references/business-contract-spec.md`
- `start.sh`
- All `scripts/lib/*.py` (12 files)
- `scripts/verify-credentials.py`, `contract-adapt.py`, `detect-stack.py`, `post-install-patch.py`
- All `capabilities/*/src/*.py` (all capability source files)
- UI markdown: `scenarios/customer-service/sample-data/README.md`, `DESIGN_GUIDELINES.md`, `voice-customer-service/README.md`

### Batch 3: MEDIUM Priority (⭐⭐) — UI frontend code
User-facing frontend with Chinese strings in the UI.
- `scenarios/customer-service/ui/voice-customer-service/app.js`
- `scenarios/customer-service/ui/voice-customer-service/tokens.css`
- `scenarios/customer-service/ui/widget-floating/*` (5 files)
- `scenarios/customer-service/ui/admin-board/app.js`, `styles.css`, `tokens.css`
- `capabilities/conversation-core/web-demo/app.js`, `README.md`

### Batch 4: LOW Priority (⭐) — Tests, `__init__.py`, minor internals
Low exposure, smaller changes.
- All `tests/*.py` (10 files)
- All `__init__.py` files (many small files)
- `capabilities/conversation-core/.env.example`
- `capabilities/conversation-core/tests/test_skeleton.py`

### No Changes Needed (already EN)
- 10 files are already English-only and require no changes.

---

## Notes

1. **How to use this index**: Start with Batch 1, then proceed through Batches 2-4. Each batch can be processed as a separate conversation session.
2. **Translation guidelines**: 
   - Docstrings, comments → translate to English
   - User-facing strings (print/log/UI) → translate to English
   - Variable names, function names → keep as-is
   - Technical terms (TRTC, LLM, SDK) → keep as-is
   - Path references, URLs → keep as-is
3. **Edge cases**: Template files (`.tpl`, `.j2`) contain embedded Chinese comments that must be translated without breaking template syntax.
4. **JSON data files**: `faq-sample.json` contains Chinese Q&A pairs — these are "sample data" and can either be translated or replaced with English samples.
