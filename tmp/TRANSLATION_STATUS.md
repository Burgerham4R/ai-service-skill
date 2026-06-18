# Translation Status & Remaining Work

> **Context for next session**. All `.py` capability source files under `capabilities/*/src/` are fully translated to English. 
> The remaining 51 files span various categories with different priority levels.

---

## ✅ Completed

| Category | Files | Notes |
|----------|------|-------|
| Capability source .py (all `src/` dirs) | ~60 | All docstrings/comments translated |
| Adapters (READMEs + .tpl templates + manifests) | ~20 | All translated |
| Integration templates | 3 | All translated |
| References | 1 (`business-contract-spec.md`) | Translated |
| INTERFACE_ADAPT.md (5 modules) | 5 | All translated |
| Capability READMEs (5 modules) | 5 | All translated |
| Root README.md | 1 | Translated |
| **`SKILL.md`** | 1 | The main SOP (932→931 lines). Fully translated to English. |

---

## 🔲 Remaining (0 files)

### Priority 2: Scripts (18 files) ✅ ALL DONE
All in `scripts/` and `scripts/lib/` — Chinese docstrings, comments, help text.
| File | Status |
|------|--------|
| `scripts/add-capability.py` | Already done ✅ |
| `scripts/setup-credentials.py` | Already done ✅ |
| `scripts/contract-adapt.py` | Translated ✅ |
| `scripts/detect-stack.py` | Translated ✅ |
| `scripts/post-install-patch.py` | Translated ✅ |
| `scripts/verify-credentials.py` | Translated ✅ |
| `scripts/lib/__init__.py` | Translated ✅ |
| `scripts/lib/adapter_codegen.py` | Translated ✅ |
| `scripts/lib/arbitrator.py` | Translated ✅ |
| `scripts/lib/contract_resolver.py` | Translated ✅ |
| `scripts/lib/credential_validators.py` | Translated ✅ |
| `scripts/lib/curl_parser.py` | Translated ✅ |
| `scripts/lib/degrader.py` | Translated ✅ |
| `scripts/lib/injector.py` | Translated ✅ |
| `scripts/lib/manifest_resolver.py` | Translated ✅ |
| `scripts/lib/openapi_parser.py` | Translated ✅ |
| `scripts/lib/stack_detector.py` | Translated ✅ |
| `scripts/lib/tokens_compile.py` | Translated ✅ |

### Priority 3: Tests (10 files) ✅ ALL DONE
| File | Status |
|------|--------|
| `tests/__init__.py` through `tests/test_verify_credentials.py` (10 files) | All docstrings/comments translated ✅ |

### Priority 4: UI Frontend Files (12 files) ✅ ALL DONE
Chinese strings in HTML/JS/CSS UI content — these are user-facing UI text.
| File | Status |
|------|--------|
| `scenarios/customer-service/ui/admin-board/app.js` | UI comments translated ✅ |
| `scenarios/customer-service/ui/admin-board/styles.css` | CSS comments translated ✅ |
| `scenarios/customer-service/ui/admin-board/tokens.css` | Header translated ✅ |
| `scenarios/customer-service/ui/voice-customer-service/app.js` | Header translated ✅ |
| `scenarios/customer-service/ui/voice-customer-service/README.md` | Full doc translated ✅ |
| `scenarios/customer-service/ui/voice-customer-service/tokens.css` | Header translated ✅ |
| `scenarios/customer-service/ui/widget-floating/index.html` | All UI text translated ✅ |
| `scenarios/customer-service/ui/widget-floating/app.js` | Comments + keywords translated ✅ |
| `scenarios/customer-service/ui/widget-floating/styles.css` | CSS comments translated ✅ |
| `scenarios/customer-service/ui/widget-floating/tokens.css` | Header translated ✅ |
| `scenarios/customer-service/ui/widget-floating/agent-link.js` | Header translated ✅ |
| `scenarios/customer-service/ui/design-system/DESIGN_GUIDELINES.md` | Full doc translated ✅ |
| `capabilities/conversation-core/web-demo/app.js` | Header translated ✅ |
| `capabilities/conversation-core/web-demo/README.md` | Full doc translated ✅ |

### Priority 5: Residual Traces ✅ ALL DONE
| File | Status |
|------|--------|
| `auto_adapters/frontend-spa/manifest.yaml` | Angular install_hint + comment translated ✅ |
| `capabilities/human-handoff/README.md` | Trigger keywords translated ✅ |
| `capabilities/human-handoff/manifest.yaml` | Trigger keyword defaults translated ✅ |
| `capabilities/session-summary/data/test_session.json` | Demo data translated ✅ |
| `capabilities/session-summary/manifest.yaml` | Inline comment translated ✅ |
| `capabilities/tool-calling/data/tools.yaml` | Header + descriptions translated ✅ |
| `scenarios/custom-builder/output-templates/recipe.yaml.j2` | All comments + default values translated ✅ |
| `scenarios/customer-service/sample-data/README.md` | Full doc translated ✅ |
| `scenarios/customer-service/system-prompt.template.md` | Keyword reference cleaned ✅ |

---

## Translation Approach That Worked Well

1. **`write_to_file` for large files**: Write the entire translated file when the file is 100% Chinese documentation.
2. **Targeted `replace_in_file` for code files**: Replace specific docstrings/comments while keeping code intact.
3. **Python bulk script for remaining traces**: The `tmp/translate_final.py` and `tmp/translate_final2.py` scripts show the approach — create exact-string replacement maps and apply them in bulk.

## 🎉 All Done! 

All 5 priority levels, approximately 152 files, have been fully translated to English.

## Bulk Scripts Available
- `tmp/translate_final.py` — Final bulk replacement patterns
- `tmp/translate_final2.py` — Second pass patterns  
- `tmp/final_pass.py` — Last pass (already executed, 0 .py files remaining in capabilities/src/)
