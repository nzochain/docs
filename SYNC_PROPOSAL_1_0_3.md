# Proposta de sincronização docs.nzochain.com — 1.0.3

**Não publicar nesta fase.** Push para `main` neste repositório dispara deploy Mintlify (ver `README.md`).

## Estado

| Superfície | Estado |
|------------|--------|
| Repo local `docs-mintlify/` | Conteúdo alinhado (com patches 1.0.3) a `API_REFERENCE` / `PUBLIC_CAPABILITIES` |
| Live `https://docs.nzochain.com` | **Desatualizado** face ao local (ex.: Free `$0.01` / “não bloqueia”, “tempo real”, AI RiskScore, wallet-monitor/bulk como se live) |
| Publicação | Mintlify ligado ao GitHub; **requer push autorizado** (não feito) |

## Páginas a publicar (checklist)

Prioridade alta (divergência live confirmada via fetch):

1. `index.mdx` — remover “tempo real” no título live
2. `api/overview.mdx` — Free hard cap; teto 3×
3. `api/errors.mdx` — `RATE_LIMIT` / `HARD_CEILING` / `SCOPE_REQUIRED`
4. `api/webhooks.mdx` — só `revocation.completed`
5. `api/wallet-monitor.mdx` — deprecated 410
6. `api/bulk-scan.mdx` — not live
7. `api/v1.mdx`, `api/authentication.mdx`, `api/risk-scan.mdx`
8. `features/risk-score.mdx` — sem AI-Powered
9. `features/wallet-monitoring.mdx` — 6h opt-in
10. `pricing/enterprise.mdx`, `pricing/individual.mdx`
11. `how-it-works.mdx`, `introduction.mdx`, `faq.mdx`, `quickstart.mdx`
12. `networks/*`

## Como publicar (manual, autorizado)

```bash
cd docs-mintlify
mint dev   # preview local http://localhost:3000
# Review diffs; then authorized PR/push to the Mintlify-connected branch
```

**Não executar push/deploy nesta fase Product & Market Readiness 1.0.3.**

## Fonte de verdade cruzada

- Backend: `nzochain/nzochain-backend/docs/API_REFERENCE.md`, `PUBLIC_CAPABILITIES.md`, `WEBHOOKS.md`
- Portal Quickstart: `https://developers.nzochain.com/quickstart` (após login)
- Swagger: `https://api.nzochain.com/docs`
