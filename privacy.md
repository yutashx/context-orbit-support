---
title: Privacy policy
permalink: /privacy/
lang: en
translation_url: /ja/privacy/
---
# ContextOrbit privacy policy

Effective date: November 7, 2026

## What ContextOrbit does

ContextOrbit helps you keep selected health and fitness records on a server you control, so you can review and analyze them on your computer. It can also collect optional location observations and motion activity estimates you choose to include in your personal activity history.

You provide one compatible receiver and configure its address and access token. ContextOrbit does not provide a developer-operated cloud account or storage service. The developer does not automatically receive the records you send to your own receiver.

## Data you choose to collect

With your selection and the relevant system permissions, the app can read supported Apple Health records, location observations and visits, and motion activity estimates and available recent history.

Records can include values, units, times, source app/device metadata, original record identifiers, related recordings and changes or deletion events. Motion results are estimates, not confirmed facts about your activities. Availability varies by OS, device, records and permissions.

The app also stores the configuration, installation identifier, collection progress, permission-request history, transfer state and server-storage confirmations needed to operate reliably. Your receiver access token is stored in the iOS Keychain.

ContextOrbit does not collect your photo library. Reproductive/sexual-health and clinical health-record types are not collected. A permission request completing does not establish that every selected record is readable.

## Where records go

The app sends records to the receiver you configure. That receiver stores the original records. The developer does not host or manage your receiver or the records stored there. You choose and manage its environment, access controls, backups, retention, deletion and any downstream use or sharing of records. The separately published reference receiver is an implementation you may choose to run, not a developer-operated storage service.

The app does not include advertising, cross-app tracking or an integrated third-party AI service. Analysis on your PC is separate from the phone app. If you configure your server to share records with other tools or providers, review their handling of the data and authorize that sharing separately. Permission to read Health data is not permission for unrelated sharing.

Use HTTPS for normal operation. Private IPv4 HTTP, including Tailscale CGNAT addresses, is accepted without an extra app opt-in; public HTTP is rejected. HTTP itself does not encrypt health records or the receiver token. A private network address alone does not provide encryption; an encrypted tunnel you operate, such as a Tailscale tailnet, can protect that traffic.

## Phone retention

Records are stored on the phone before transfer. The app retains unconfirmed records until it validates the configured receiver's confirmation that the original records have been durably stored. A successful connection or HTTP response alone is not that confirmation.

The app does not automatically delete records from the phone. Records can remain on the phone and occupy storage even after server storage is confirmed. Removing a phone copy does not delete the original record on your receiver.

Unconfirmed records are not deleted because they are old, a source is turned off or paused, or a retry budget has been exhausted. Long offline periods and large historical imports can therefore use substantial phone storage.

The app also retains configuration, progress, identity and transfer metadata needed to avoid duplicate or skipped work. These are separate from the record copies themselves.

The app applies an iCloud Backup exclusion to its private storage directory and treats failure to apply it as a storage error. The receiver token is stored in the device-only Keychain and becomes accessible after the first unlock following a restart. ContextOrbit has no iCloud record-sync feature and does not control receiver backups.

Uninstalling the app or losing the device can remove unconfirmed phone data. ContextOrbit is not a substitute for receiver backups and does not promise recovery after device loss.

## Your controls

You can choose supported source types, pause collection and change system permissions. Turning a type off stops new collection and automatic sending for that type. An already-started request may finish. It does not delete existing pending records.

The explicit "Send all pending records" action includes pending records from types that are off. Pausing collection does not itself pause transfer.

You can revoke Health, Location and Motion access in iOS Settings. You manage removal of records already on your receiver, including any copies and backups. The published reference receiver has no automatic expiration or API for physically deleting stored originals. Deleting a record in Health does not automatically erase its previously stored original from the receiver; supported changes and deletions are recorded as events.

## Support and public pages

App documentation is hosted on GitHub Pages; app support uses GitHub Issues. Opening these pages sends an ordinary web request to GitHub and is subject to [GitHub's privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). It does not grant GitHub access to records stored inside this app. Posting an issue requires a GitHub account. Issues in a public repository and their attachments are publicly visible.

Do not post Health records, location history, access tokens, device identifiers, databases or unredacted diagnostic files in public issues. Information you choose to submit for support is separate from automatic app operation.

## Policy changes and contact

Contact the maintainer through the [ContextOrbit app issue tracker](https://github.com/yutashx/context-orbit-support/issues). Use it for questions about this policy as well as app support; never include personal records or credentials. See the [support page]({{ '/support/' | relative_url }}) for reporting guidance. Changes to collection or sharing require an updated explanation and any additional consent required for that change.

## Language

These documents are available in English and Japanese. The English version is authoritative. If the versions differ, the English version takes precedence.
