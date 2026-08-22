# Getaround (getaround)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Getaround was a peer-to-peer and connected car-sharing marketplace (merged with France's Drivy in 2019) that let owners list personal or fleet vehicles fitted with Getaround Connect - a BLE/telematics smart-lock kit - for keyless, app-based rental. Getaround historically ran a documented Owner API and webhook program for fleet-management partners (CarSync, FleetWire, Invers Fleet Hawk) plus a native Connect Blueforce BLE SDK for lock/unlock.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/getaround/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/getaround/refs/heads/main/apis.yml)

## Operating Status (as of 2026-07-03)

Getaround is winding down and this entry documents a **discontinued/unreachable** API, not a live one:

- **U.S. shutdown (Feb 2025):** Getaround abruptly shut down U.S. car-sharing operations, including its HyreCar subsidiary (which it had bought out of HyreCar's own bankruptcy in 2024).
- **European sale (Apr 30, 2026):** Getaround's European car-sharing business was sold to Denmark's GoMore ApS for roughly EUR 31.5 million cash plus a non-interest-bearing note, forming a combined pan-European peer-to-peer carsharing network (5M+ users, 11 countries) led by GoMore's founder as Group CEO.
- **Dissolution (Jun 2026 onward):** Getaround Inc.'s (Nasdaq: GETR) board voted on June 5, 2026 to pursue formal Delaware dissolution and liquidation. A stockholder vote is scheduled for a Special Meeting on July 29, 2026. Liabilities are expected to exceed assets, so no distribution to common stockholders is anticipated.
- **API infrastructure:** `api.getaround.com` no longer resolves (DNS failure), the `getaround.tech` developer/tech blog now redirects to a jobs page, and the `getaround.com/docs/api/owner/v1` reference page now renders with no documentation body. The consumer-facing `fr.getaround.com` site remains live under the new GoMore-led ownership, but no evidence of an active public developer/API program under that ownership was found as of this review.

Given this, the API described below is reconstructed from partner-integration write-ups (Kitts, apitracker.io, Getaround's own "open marketplace" blog post) rather than a live specification, and its endpoints are marked as modeled, not confirmed-live.

## Tags

- Car Sharing
- Mobility
- Connected Car
- Fleet Management
- Peer to Peer
- Discontinued

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### Getaround Owner API

Historical partner/owner REST API used by fleet-management integrators (CarSync, FleetWire, Kitts) to sync bookings onto external calendars, block vehicle availability, generate invoices for professional owners, and receive event webhooks. Access required completing a "Getaround charter" with an account manager to receive an API key and register webhook URLs.

- **Human URL:** [https://getaround.com/docs/api/owner/v1](https://getaround.com/docs/api/owner/v1)
- **Endpoints modeled:** true (no live spec was reachable; api.getaround.com is offline)

#### Tags

- Bookings
- Vehicles
- Fleet
- Discontinued

#### Properties

- [Documentation](https://getaround.com/docs/api/owner/v1)
- [API Reference](https://api.getaround.com/docs-interactive)

### Getaround Connect Blueforce SDK

Native iOS (Objective-C) SDK for the Getaround Connect smart-lock hardware fitted to shared vehicles - discovers nearby Connect devices over Bluetooth LE and issues lock/unlock commands via `BlueforceConnectionManager`. This is a Bluetooth device SDK, not an HTTP API; it is listed here because it is Getaround's only publicly documented Connect integration surface.

- **Human URL:** [https://github.com/Getaround/Blueforce](https://github.com/Getaround/Blueforce)
- **Endpoints modeled:** true (Bluetooth device protocol, not HTTP)

#### Tags

- Connect
- Telematics
- Bluetooth LE
- Discontinued

#### Properties

- [Source Code](https://github.com/Getaround/Blueforce)

## Common Properties

- [GitHub Organization](https://github.com/Getaround)
- [LinkedIn](https://www.linkedin.com/company/getaround)
- [Website](https://getaround.com)
- [Documentation](https://getaround.com/docs/api/owner/v1)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
