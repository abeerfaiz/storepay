# StorePay

A retail payments and point-of-sale platform built with .NET 10 and Clean Architecture.

## What it does

A till opens a transaction, takes payment by cash, card or gift card, then completes or voids the sale. Money is stored in pence, card payments sit behind a payment provider interface, and every payment request is idempotent so a customer is never charged twice.

## Tech stack

.NET 10, C#, ASP.NET Core, EF Core, SQL Server 2022 (Docker), xUnit, Serilog, GitHub Actions

## Architecture

Four projects plus tests, with dependencies pointing inward only:

- `StorePay.Domain`: business rules, references nothing
- `StorePay.Application`: use cases and interfaces
- `StorePay.Infrastructure`: database and payment providers
- `StorePay.Api`: HTTP entry point and startup wiring
- `StorePay.Tests`: automated tests

## Roadmap

Built monolith first, as 8 finished monthly modules:

1. Tender API that never double-charges
2. Reconciliation and loss prevention
3. Event pipeline and refund saga
4. Multi-tenancy
5. Two tills, one gift card (concurrency)
6. Live store dashboard
7. Retiring VB.NET with the Strangler Fig
8. AI explanations of reconciliation reports

Status: Module 1, week 1.
