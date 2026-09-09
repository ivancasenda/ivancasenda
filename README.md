# Ivan Casenda

Platform and backend engineer in Indonesia.

I build and run a multi-tenant Odoo SaaS. External paying clients, two years in production. I handle the architecture, the infrastructure, the application modules, CI, and on-call.

Most of the work is in private repos, so here's a rough idea of what's in them.

**tenantd** is a tenant-lifecycle control plane written in Python. An in-cluster agent claims work under a lease, heartbeats while it holds one, and submits each step back as it finishes. Resource fencing keeps two agents off the same tenant. The control plane itself never holds a general-purpose Kubernetes credential, which was the constraint I designed around first.

**The platform** is moving from Docker Compose to Kubernetes on Oracle OKE, while it's live. OpenTofu for production and staging, Argo CD, Helm, and CloudNativePG for Postgres, with backups I've restored from.

**Odoo** is where most of the application work goes. Custom modules for accounting, sales, inventory and POS, plus Indonesian e-Faktur (Coretax) compliance. Multiple Odoo majors run side by side, so tenants upgrade when they're ready rather than all at once.

Python, Kubernetes, PostgreSQL, OpenTofu, Argo CD, Helm, FastAPI, OpenTelemetry.

## Public work

**[semantic-search](https://github.com/ivancasenda/semantic-search)** — semantic search over Stack Overflow data. MiniLM embeddings indexed in Vertex AI Vector Search, FastAPI backend, Angular frontend, and a TFX pipeline that handles ingestion and refreshes the index.

**[invoicehub](https://github.com/ivancasenda/invoicehub)** — invoicing app. Spring Boot and Angular, PDFs via JasperReports.

**[motorist-behavior-ml](https://github.com/ivancasenda/motorist-behavior-ml)** — ResNet classifier that identifies what a driver is doing from an image.
