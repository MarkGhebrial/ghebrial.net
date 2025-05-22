+++
template = "page.html"
title = "mailroom"
+++

{% aside() %}
## Links
Repository: [GitHub](https://github.com/MarkGhebrial/mailroom)
{% end %}

# mailroom

**Self-hosted email for the masses**

Mailroom is an email server designed for simplicity and quick setup.
It's still a work in progress, but I intend to see it to production readiness.

Mailroom is written in Rust, using tokio as the async backend and sea-orm as the orm.

## Why?

I began working on mailroom because I wanted to learn how email works.
No amount of reading can replace learning by doing.

## Design Philosophy

The #1 design goal for mailroom is to be extremely simple to set up and administrate.
Going from registering a domain to hosting your own email server should take less than 20 minutes.

In scope features:

- **Automatic TLS certificate management.** The user should *never* need to worry about acquiring or renewing certificates unless they opt into more advanced configuration options. Additionally, TLS must be enabled by default.
- **Simple configuration.** Defaults should be sensible and work out of the box. No configuration changes required to get a fully functioning email server.

Out of scope features: (may come into scope as the project matures)

- **Web administration interface.** Designing a web-based interface for administrating mailroom would increase complexity and project scope beyond what I want to undertake.
- **Email client.** Mailroom is only an email server, *not* a client. To read and send emails through mailroom, users must use a separate email client such as Thunderbird.