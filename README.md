# keys-service

The public key directory. Every device publishes its identity key and a stock of one-time MLS key packages here. When someone starts a conversation or adds a member, they claim one key package per device, and each package is handed out exactly once.

Key changes are written to an append-only log built as a Merkle tree, so a client can check that the server is showing everyone the same keys.

Built with .NET 10 and PostgreSQL.

Owner: Tibor Koderman. Status: planned.

## Where this fits

This is one of the repositories of [Pretty Good Pigeon](https://github.com/rso-ekipa13), an end-to-end encrypted messenger built by ekipa 13 for the Cloud Computing course at UL FRI (2026/27). The architecture, plan and decisions live in [docs](https://github.com/rso-ekipa13/docs).

`main` only changes through pull requests; day-to-day work goes to `dev`.
