---
title: Support
permalink: /support/
lang: en
translation_url: /ja/support/
---
# ContextOrbit support

> Prepared for publication. App release and public-site verification are still pending.

## Requirements

ContextOrbit is for users who operate their own compatible receiver. It is not a hosted storage subscription. You need a supported iPhone, the source permissions you choose to grant, and a receiver reachable from that phone. The current app requires iOS 26 or later.

Start with the [receiver instructions](https://github.com/yutashx/context-orbit-server#requirements-and-install). Use HTTPS for normal operation; an encrypted tunnel you operate, such as a Tailscale tailnet, can protect private HTTP. Private IPv4/CGNAT HTTP is accepted by the app without an extra opt-in; public HTTP is rejected. HTTP itself is unencrypted. The receiver must remain available when you want transfer to proceed. The phone can retain records while it is unavailable, but large imports and long offline periods need sufficient free space.

Receiver hosting and backups are not included in the app purchase. Read the receiver prerequisite before purchasing. There is no developer cloud, app account or integrated AI.

## First setup

1. Install and configure your own receiver, including authentication and durable storage.
2. Enter its URL and token in the app. Confirm that its server identity matches the receiver you intended.
3. Select the Health, Location and Motion sources you want. Selection and system permission are separate decisions. Vision prescriptions use a separate per-object picker.
4. Allow collection and check transfer status. Connection success is not proof that records have been saved. "Saved to server" means the app validated the receiver's durable-storage result.

The app does not include a shared public destination. The [reference receiver](https://github.com/yutashx/context-orbit-server) is software you may choose to run in your own environment. The developer does not host or operate it for you, manage stored records or determine their downstream use. You manage its access controls, backups, retention, deletion and any sharing with other services. The reference implementation has no automatic expiration or API for physically deleting stored originals.

## Common situations

### Records are waiting to send

Check that your receiver is running and reachable from the iPhone, not only from the computer running it. A loopback listener is only reachable on its own computer. Offline periods are normal; iOS determines when background work can run.

Types that are off keep their pending records without automatic sending. Re-enable the relevant type or explicitly use "Send all pending records" if you intend to send all pending types. This action includes off types. Collection pause is separate from transfer.

### The receiver needs an update

Check the app and receiver release compatibility instructions. Restarting a new process does not replace a different old process serving the phone's configured URL. Verify the actual listener and run one intended receiver service. Do not initialize a new store, rotate the identity or delete the phone's buffer to fix a version mismatch.

Follow the [receiver backup, restore and upgrade procedure](https://github.com/yutashx/context-orbit-server#backups-restore-and-upgrades). Preserve its identity, credentials and original records. Test a restore on a separate private path before relying on it. Never run init-store over an existing store or change identity to work around an error.

### No Health records appear

Check the selected types, permissions, available records and whether the source is available on your device and OS. An empty read does not prove permission was denied. The app cannot promise data for every supported type or data that HealthKit does not make available.

### Phone storage is growing

Historical records can occupy gigabytes even without photos or videos. Pending records must remain until their receiver-save confirmation is validated. Automatic cleanup is currently disabled, so records can remain on the phone even after server storage is confirmed. Free other storage rather than deleting the app or its pending records. Receiver retention is separate.

### Background work is delayed

Check source permissions and normal iOS settings. Background delivery, motion history availability and network execution are limited by iOS. The app does not guarantee continuous collection or immediate upload on reconnection.

## Reporting an issue

For app questions, bug reports and feature requests, [open an issue in ContextOrbit support](https://github.com/yutashx/context-orbit-support/issues). A GitHub account is required to post. Public issues and attachments can be read by anyone; do not use them to send confidential information. Include app/iOS/receiver versions, visible status and a redacted description of the failed action. A diagnostic reference can locate a failure without posting the underlying record.

For a bug in the reference receiver itself, use the [receiver issue tracker](https://github.com/yutashx/context-orbit-server/issues). Support covers the app and the published reference implementation; it does not include operating your server, administering stored data or managing downstream tools. For a suspected security issue, describe only the general concern and request a private reporting route; do not disclose exploit details, records or credentials in a public issue.

Never post access tokens, Health records, precise locations, device identifiers, personal screenshots, databases or raw logs. Review attachments before submitting them.

## Health information

ContextOrbit transfers records for your own storage, review and analysis. It does not provide medical advice, diagnose conditions or recommend treatment. Do not use it for emergency monitoring or assume missing records mean no activity or event occurred.

Read the [privacy policy]({{ '/privacy/' | relative_url }}) for collection, transfer and retention boundaries.

## Language

These documents are available in English and Japanese. The English version is authoritative. If the versions differ, the English version takes precedence.
