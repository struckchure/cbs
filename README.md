# 🏦 Core Banking System

A secure and modular core banking system built entirely in Go. Designed for high-performance financial operations like customer onboarding, transaction processing, and ledger management — all with strong type safety, concurrency, and auditability in mind.

## ✨ Features

- 🔐 **User & Role Management** — Admins, Tellers, Customers, and Auditors
- 🏦 **Account Management** — Multi-currency support, account statuses
- 💸 **Transaction Engine** — Real-time transfers with balance checks
- 📚 **Double-Entry Ledger** — Accurate financial accounting and reconciliation
- ⏱ **Scheduled Transfers** — Future and recurring payments
- 📊 **Dashboards & Reports** — Web UI built with Go + Templ
- 📡 **API Layer** — RESTful APIs for external integration

---

## 🧱 Tech Stack

| Layer        | Technology       |
|--------------|------------------|
| Language     | Go (Golang)      |
| ORM          | [Entgo](https://entgo.io) |
| Frontend     | [Templ](https://templ.guide) |
| DB           | PostgreSQL       |
| Messaging    | Redis (for pub/sub and async jobs) |
| Auth         | JWT / OAuth2     |
| DevOps       | Docker, Taskfile, CI/CD-ready |
| Serverless Functions | [OpenFaaS](https://openfaas.com) |

---

## ⚙️ Setup

### Prerequisites

- Go 1.22+
- PostgreSQL
- Docker (for local DB/dev setup)
- [Templ CLI](https://templ.guide/):  
```bash
  go install github.com/a-h/templ/cmd/templ@latest
````

* [Task](https://taskfile.dev/):

```bash
brew install go-task/tap/go-task # macOS  
choco install go-task            # Windows  
```

### Clone & Run

```bash
git clone https://github.com/struckchure/cbs.git
cd core-banking-system

cp .env.example .env

task dev
```

### Database Migrations

```bash
task migrate:up     # Apply migrations
task migrate:down   # Rollback
task ent:generate   # Regenerate Ent code
```

---

## 📘 Documentation

* [📄 API Reference](docs/api.md)
* [🧾 Ledger Architecture](docs/ledger.md)
* [🔐 Security Model](docs/security.md)
* [🧠 Ent Schema Guide](docs/ent.md)
* [🎨 Templ Component Library](docs/frontend.md)

---

## 🔒 Security Practices

* Passwords hashed using Argon2id
* JWT-based auth with expiry and refresh
* CSRF protection (for forms)
* Role-based access control
* Immutable ledger writes with audit logs

---

## 🛣 Roadmap

* [ ] Agent banking support
* [ ] Loan origination engine
* [ ] FX transfers & multi-currency support
* [ ] SMS/email notifications
* [ ] Mobile-ready frontend (Templ + Tailwind)

---

## 🤝 Contributing

This project is open to collaboration. Please see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📄 License

[MIT Non-Commercial License](LICENSE)
