# Awesome SMS Infrastructure

A curated list of SMS/A2P messaging providers, open-source gateways, specs, datasets,
and testing tools. General-purpose — usable whether or not you ever touch SMSRoute.

## Contributing

PRs welcome. Criteria: entries must be factual and verifiable (a working link, a real
repo/spec), one neutral line per entry, alphabetical within each section, no affiliate
links, no self-promotion beyond a single factual line.

## Contents

- [Providers & APIs](#providers--apis)
- [Open-source gateways & tools](#open-source-gateways--tools)
- [Specs & standards](#specs--standards)
- [Datasets](#datasets)
- [Testing & debugging tools](#testing--debugging-tools)

## Providers & APIs

Commercial SMS/A2P sending APIs, alphabetical. One neutral line each — not a ranking.

- **[AWS End User Messaging](https://aws.amazon.com/end-user-messaging/)** — Amazon's SMS/voice/push messaging service, part of AWS, billed through an AWS account.
- **[MessageBird / Bird](https://bird.com/)** — Omnichannel messaging platform (SMS, WhatsApp, email) with a REST API and account-based billing.
- **[Plivo](https://www.plivo.com/)** — Voice and SMS API platform with account-based billing and carrier-direct routes in some regions.
- **[Sinch](https://www.sinch.com/)** — Global CPaaS provider (SMS, voice, verification) built partly on its own acquired carrier network.
- **[SMSRoute](https://smsroute.cc/)** — Web-based outbound SMS sending, 149 countries, email-only signup (no ID documents), per-message pricing, crypto payment (BTC/ETH/USDT/XMR/LTC/SOL).
- **[Telnyx](https://telnyx.com/)** — Carrier-grade SMS/voice API provider operating its own private IP network.
- **[Textbelt](https://textbelt.com/)** — Simple single-endpoint SMS API, free tier plus paid quota, no account dashboard required.
- **[Twilio](https://www.twilio.com/)** — Large CPaaS provider; SMS/voice/video APIs, account-based billing, extensive carrier compliance tooling (10DLC, etc.).
- **[Vonage](https://www.vonage.com/)** (formerly Nexmo) — CPaaS provider offering SMS, voice, and verification APIs with account-based billing.

## Open-source gateways & tools

- **[Kannel](https://www.kannel.org/)** — long-running open-source WAP/SMS gateway; developed via its own CVS repo and mailing list, no canonical GitHub mirror.
- **[Jasmin](https://github.com/jookies/jasmin)** — open-source SMPP-based SMS gateway written in Python.
- **[Gammu](https://github.com/gammu/gammu)** — command-line utility and library for working with mobile phones/modems, including SMS send/receive.
- **[SMS Gateway for Android (capcom6)](https://github.com/capcom6/android-sms-gateway)** — Android app that exposes local or cloud-relayed SMS send/receive as an API, with a companion [server](https://github.com/android-sms-gateway/server) component.
- **[playSMS](https://github.com/playsms/playsms)** — web front-end for SMS gateways/bulk SMS with plugin support for multiple backends.

## Specs & standards

- **GSM 03.38** — character set / alphabet and SMS text-encoding standard (7-bit default alphabet, extension table).
- **SMPP 3.4 / 5.0** — Short Message Peer-to-Peer protocol, the standard binding used between gateways/aggregators and carriers/SMSCs.
- **[E.164](https://www.itu.int/rec/T-REC-E.164/)** — ITU-T recommendation for international phone-number numbering (the format SMS destination numbers should be validated against).
- **[RFC 5724](https://www.rfc-editor.org/rfc/rfc5724)** — defines the `sms:` URI scheme for pre-filling a message/recipient from a link.

## Datasets

- **[smsroute-open-datasets](https://github.com/SMSRoute-cc/smsroute-open-datasets)** — dated JSON snapshots of published SMS pricing and sender-ID/registration rules.
- **[SMSRoute open data API](https://smsroute-cc.github.io/api/v1/)** — the live version of the same data (`prices.json` / `countries.json` / `coverage.json`).
- **[libphonenumber](https://github.com/google/libphonenumber)** — Google's phone-number metadata + parsing/formatting/validation library; the closest thing to an open dataset of real-world numbering-plan formats.

## Testing & debugging tools

- **[SMSRoute free tools](https://smsroute-cc.github.io/tools/)** — deliverability pre-flight linter, sender-ID rules-by-country lookup, opt-out footer generator, anonymity threat-model matrix, crypto top-up fee comparator. Static, client-side, nothing sent to a server.
- **[node-smpp](https://github.com/farhadi/node-smpp)** — SMPP client/server implementation in Node.js, useful for standing up a local SMPP test server.
- **[OpenSmpp](https://github.com/OpenSmpp/opensmpp)** — Java library implementing SMPP, for building/testing ESMEs.
- **[twilio-cli](https://github.com/twilio/twilio-cli)** — Twilio's official CLI; useful for scripting test sends and inspecting delivery logs against a Twilio account.

## License

MIT — see [LICENSE](LICENSE).

## Related: Sender-ID Regulations Dataset
Verified alphanumeric sender-ID rules, registration regimes and charset classes for 40 countries (JSON/CSV, CC-BY-4.0): [sms-sender-id-regulations](https://github.com/SMSRoute-cc/sms-sender-id-regulations)
