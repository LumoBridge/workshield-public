## 🎥 WorkShield Product Overview

WorkShield is a neutral documentation and evidence-preservation platform designed to help users record workplace events accurately and consistently over time.
<p align="center">
  <img src="https://github.com/Vey-Digital/workshield/raw/main/images/stat2.png" width="90%">
</p>
### What changed
- Adds server-side access context route and tests
- Hardens admin-protected layout and dashboard gating
- Updates service-role usage guard (passing)
- Adds security/regression documentation and checklists

### Why
- Ensure internal admin/tester access works without Stripe
- Prevent entitlement leaks to non-internal users
- Lock in CI guardrails before merging to main

### Safety checks
- Service role usage guard passes
- Admin bypass is server-only and env-controlled
- Non-internal users cannot bypass subscription

