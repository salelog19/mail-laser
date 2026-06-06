# CHANGELOG (MailLaser)


<a name="v3.0.5"></a>
## [v3.0.5](https://github.com/Govcraft/mail-laser/compare/v3.0.4...v3.0.5)

> 2026-06-07


<a name="v3.0.4"></a>
## [v3.0.4](https://github.com/Govcraft/mail-laser/compare/v3.0.3...v3.0.4)

> 2026-06-07


<a name="v3.0.3"></a>
## v3.0.3

> 2026-06-07

### Bug Fixes

* **build:** correctly include config tests from separate file
* **build:** correct Dockerfile syntax and certificate placement
* **ci:** separate full changelog from release notes
* **ci:** use correct git-chglog argument for existing tags
* **ci:** ensure release-notes.md exists before generation
* **ci:** handle empty release notes and pass body via output
* **config:** change default SMTP port to 2525 to avoid permission errors
* **deps:** remove stale package-lock.json and update npm dependencies
* **deps:** resolve Dependabot security vulnerabilities
* **docker:** ensure application runs correctly in Docker container
* **docker:** actually rebuild main crate after src copy
* **docs:** route Markdoc links through next/link so basePath applies
* **smtp:** correctly handle non-TLS sessions and sender address parsing
* **smtp:** correct DATA phase handling and loop termination
* **test:** prevent parallel execution interference in config tests
* **webhook:** update hyper client to 1.x API

### Code Refactoring

* migrate to acton-reactive actor model with resilience and comprehensive tests
* improve config loading robustness and cleanup Dockerfile
* rename project to mail_laser
* **ci:** simplify release notes handling
* **health:** Migrate health check server from Axum to Hyper

### Features

* add optional header prefix passthrough to webhook payload
* **auth:** add attachment pass-through with Cedar-based authorization
* **build:** add static musl Docker build using rustls
* **ci:** add workflow to build and publish Docker image to GHCR on tag
* **config:** add info logging for loaded configuration values
* **dmarc:** add SPF+DKIM+DMARC validation for inbound SMTP
* **error-handling:** improve panic logging and enable unwinding
* **health:** add basic HTTP health check endpoint
* **parser:** handle multipart emails and generate text body using mailparse
* **parser:** use Content-Type for HTML detection and include HTML body
* **parser:** include HTML body in webhook payload and strip for text body
* **smtp:** add STARTTLS support using rustls
* **smtp:** extract sender name from Reply-To header
* **smtp:** bound unknown-RCPT per session and close v3 test gaps
* **webhook:** allow plain HTTP for loopback webhook URLs
* **webhook:** add HMAC-SHA256 request signing for outbound webhooks
* **webhook:** use dynamic user-agent from Cargo manifest

