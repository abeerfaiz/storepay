# Roadmap

Monolith first, delivered as 8 finished monthly modules.

| Module | Weeks | Topic |
|---|---|---|
| 1 | 1–6 | Tender API that never double-charges: domain model, EF Core, idempotency, `IPaymentProvider`, Adyen test mode, web till (card states, cash keypad, receipt, refund), CI, Azure deploy, £20 budget alert |
| 2 | 7–10 | Reconciliation and loss prevention: till simulator (40 stores × 3 tills, 9 injected defects), end-of-day, cash-up, loss review |
| 3 | 13–18 | Event pipeline: outbox, MassTransit, refund Saga, OpenTelemetry trace, k6 load test, AKS (delete after demo) |
| 4 | 19–22 | Multi-tenancy: EF query filters, OAuth2 client credentials for tills, policy authorisation, isolation tests |
| 5 | 25–26 | Two tills, one gift card: concurrency, Redis locks, optimistic concurrency |
| 6 | 29–30 | Live store dashboard with SignalR; offline banner |
| 7 | 35–36 | Retiring VB.NET with the Strangler Fig and characterisation tests |
| 8 | 41–42 | AI that explains reconciliation reports: Azure OpenAI, Semantic Kernel, RAG |
