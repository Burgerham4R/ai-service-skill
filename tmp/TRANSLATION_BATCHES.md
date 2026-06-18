# Translation Batches Plan

> All files listed below contain Chinese text that needs to be translated to English.  
> Files are organized into 4 batches by priority. Process one batch at a time.

---

## Batch 1: Core Docs, SOP, User-Facing Configs (27 files)

High-impact, high-visibility files that define the Skill's public surface.

```text
SKILL.md
README.md
scenarios/customer-service/README.md
scenarios/custom-builder/README.md
capabilities/conversation-core/INTEGRATION.md
capabilities/conversation-core/QUICK_START.md
capabilities/conversation-core/manifest.yaml
capabilities/knowledge-base/manifest.yaml
capabilities/human-handoff/manifest.yaml
capabilities/session-summary/manifest.yaml
capabilities/tool-calling/manifest.yaml
capabilities/digital-human/manifest.yaml
scenarios/customer-service/recipe.yaml
scenarios/customer-service/system-prompt.template.md
scenarios/customer-service/sample-data/faq-sample.json
scenarios/custom-builder/prompts/q1-business-scenario.md
scenarios/custom-builder/prompts/q2-io-modality.md
scenarios/custom-builder/prompts/q3-ui-form.md
scenarios/custom-builder/prompts/q4-capabilities.md
auto_adapters/manifest.yaml
scripts/add-capability.py
scripts/setup-credentials.py
```

---

## Batch 2: Integration Docs, Adapters, Key Scripts (~55 files)

```text
# === Capability READMEs ===
capabilities/conversation-core/INTERFACE_ADAPT.md
capabilities/knowledge-base/INTERFACE_ADAPT.md
capabilities/knowledge-base/README.md
capabilities/human-handoff/INTERFACE_ADAPT.md
capabilities/human-handoff/README.md
capabilities/session-summary/INTERFACE_ADAPT.md
capabilities/session-summary/README.md
capabilities/tool-calling/INTERFACE_ADAPT.md
capabilities/tool-calling/README.md
capabilities/digital-human/README.md
capabilities/__init__.py

# === Adapter READMEs + Templates ===
auto_adapters/README.md
auto_adapters/frontend-spa/README.md
auto_adapters/frontend-spa/manifest.yaml
auto_adapters/frontend-spa/angular/voice-agent.component.ts.tpl
auto_adapters/frontend-spa/react/VoiceAgent.tsx.tpl
auto_adapters/frontend-spa/vue/VoiceAgent.vue.tpl
auto_adapters/python-backend/README.md
auto_adapters/python-backend/manifest.yaml
auto_adapters/python-backend/django.py.tpl
auto_adapters/python-backend/fastapi.py.tpl
auto_adapters/python-backend/flask.py.tpl
auto_adapters/node-backend/README.md
auto_adapters/node-backend/manifest.yaml
auto_adapters/node-backend/express.js.tpl
auto_adapters/node-backend/fastify.js.tpl
auto_adapters/node-backend/koa.js.tpl
auto_adapters/java-backend/README.md
auto_adapters/java-backend/manifest.yaml
auto_adapters/java-backend/quarkus/VoiceAgentFilter.java.tpl
auto_adapters/java-backend/springboot/VoiceAgentFilter.java.tpl
auto_adapters/integration_templates/generic-backend.md
auto_adapters/integration_templates/generic-frontend.md
auto_adapters/integration_templates/generic-rest-api.md

# === References ===
references/business-contract-spec.md

# === Scripts ===
start.sh
scripts/verify-credentials.py
scripts/contract-adapt.py
scripts/detect-stack.py
scripts/post-install-patch.py
scripts/lib/__init__.py
scripts/lib/adapter_codegen.py
scripts/lib/arbitrator.py
scripts/lib/contract_resolver.py
scripts/lib/credential_validators.py
scripts/lib/curl_parser.py
scripts/lib/degrader.py
scripts/lib/injector.py
scripts/lib/manifest_resolver.py
scripts/lib/openapi_parser.py
scripts/lib/stack_detector.py
scripts/lib/tokens_compile.py

# === Capability Source Files ===
capabilities/conversation-core/src/__init__.py
capabilities/conversation-core/src/_capability_loader.py
capabilities/conversation-core/src/agent.py
capabilities/conversation-core/src/credentials.py
capabilities/conversation-core/src/health.py
capabilities/conversation-core/src/log_filter.py
capabilities/conversation-core/src/modality.py
capabilities/conversation-core/src/server.py
capabilities/conversation-core/src/trtc_client.py
capabilities/conversation-core/src/usersig.py

capabilities/knowledge-base/src/__init__.py
capabilities/knowledge-base/src/retriever.py
capabilities/knowledge-base/src/router.py
capabilities/knowledge-base/src/adapters/__init__.py
capabilities/knowledge-base/src/adapters/default_rest.py
capabilities/knowledge-base/src/adapters/factory.py
capabilities/knowledge-base/src/adapters/local_json.py
capabilities/knowledge-base/src/adapters/mock.py
capabilities/knowledge-base/src/core/__init__.py
capabilities/knowledge-base/src/core/models.py
capabilities/knowledge-base/src/core/scoring.py
capabilities/knowledge-base/src/core/service.py
capabilities/knowledge-base/src/ports/__init__.py
capabilities/knowledge-base/src/ports/kb_client.py

capabilities/human-handoff/src/__init__.py
capabilities/human-handoff/src/queue.py
capabilities/human-handoff/src/router.py
capabilities/human-handoff/src/summary_link.py
capabilities/human-handoff/src/trigger.py
capabilities/human-handoff/src/adapters/__init__.py
capabilities/human-handoff/src/adapters/default_rest.py
capabilities/human-handoff/src/adapters/factory.py
capabilities/human-handoff/src/adapters/local_queue.py
capabilities/human-handoff/src/adapters/mock.py
capabilities/human-handoff/src/core/__init__.py
capabilities/human-handoff/src/core/intent_detector.py
capabilities/human-handoff/src/core/models.py
capabilities/human-handoff/src/core/service.py
capabilities/human-handoff/src/ports/__init__.py
capabilities/human-handoff/src/ports/handoff_client.py

capabilities/session-summary/src/__init__.py
capabilities/session-summary/src/recorder.py
capabilities/session-summary/src/router.py
capabilities/session-summary/src/summarizer.py
capabilities/session-summary/src/adapters/__init__.py
capabilities/session-summary/src/adapters/base.py
capabilities/session-summary/src/adapters/default_rest.py
capabilities/session-summary/src/adapters/factory.py
capabilities/session-summary/src/adapters/local_json.py
capabilities/session-summary/src/adapters/mock.py

capabilities/tool-calling/src/__init__.py
capabilities/tool-calling/src/dispatcher.py
capabilities/tool-calling/src/registry.py
capabilities/tool-calling/src/router.py
capabilities/tool-calling/data/tools.yaml
capabilities/tool-calling/examples/__init__.py
capabilities/tool-calling/examples/local_tools.py

capabilities/digital-human/src/__init__.py
capabilities/digital-human/src/router.py

# === Scenario config ===
scenarios/customer-service/sample-data/README.md
scenarios/customer-service/ui/design-system/DESIGN_GUIDELINES.md
scenarios/customer-service/ui/voice-customer-service/README.md
scenarios/custom-builder/output-templates/recipe.yaml.j2
```

---

## Batch 3: UI Frontend Code (~15 files)

```text
scenarios/customer-service/ui/voice-customer-service/app.js
scenarios/customer-service/ui/voice-customer-service/tokens.css
scenarios/customer-service/ui/widget-floating/agent-link.js
scenarios/customer-service/ui/widget-floating/app.js
scenarios/customer-service/ui/widget-floating/index.html
scenarios/customer-service/ui/widget-floating/styles.css
scenarios/customer-service/ui/widget-floating/tokens.css
scenarios/customer-service/ui/admin-board/app.js
scenarios/customer-service/ui/admin-board/styles.css
scenarios/customer-service/ui/admin-board/tokens.css
capabilities/conversation-core/web-demo/app.js
capabilities/conversation-core/web-demo/README.md
capabilities/conversation-core/.env.example
capabilities/session-summary/data/test_session.json
```

---

## Batch 4: Tests & Minor Utils (~25 files)

```text
tests/__init__.py
tests/test_arbitrator.py
tests/test_capability_overlay.py
tests/test_contract_resolver.py
tests/test_handoff_ports.py
tests/test_kb_ports.py
tests/test_manifest_resolver.py
tests/test_recipe_assembly.py
tests/test_stack_and_degrader.py
tests/test_verify_credentials.py
capabilities/conversation-core/tests/test_skeleton.py
```

Small `__init__.py` files scattered across capabilities (list in PROJECT_INDEX.md detail tables).

---

## Already English (10 files) — Skip

```text
capabilities/conversation-core/requirements.txt
capabilities/conversation-core/tests/__init__.py
capabilities/conversation-core/web-demo/index.html
capabilities/conversation-core/web-demo/styles.css
capabilities/knowledge-base/data/faq.json
scenarios/customer-service/ui/admin-board/index.html
scenarios/customer-service/ui/voice-customer-service/data.js
scenarios/customer-service/ui/voice-customer-service/index.html
scenarios/customer-service/ui/voice-customer-service/mock-shop.json
scenarios/customer-service/ui/voice-customer-service/styles.css
```

---

## Total

| Batch | Files | Description |
|-------|------:|-------------|
| Batch 1 | ~22 | Core docs, SOP, manifest YAMLs |
| Batch 2 | ~90 | Integration docs, adapters, scripts, capability sources |
| Batch 3 | ~15 | UI frontend (JS/CSS/HTML) |
| Batch 4 | ~25 | Tests, `__init__.py`, minor internals |
| **Total** | **~152** | Files requiring translation |
