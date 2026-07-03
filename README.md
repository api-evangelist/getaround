# Getaround (getaround)

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
