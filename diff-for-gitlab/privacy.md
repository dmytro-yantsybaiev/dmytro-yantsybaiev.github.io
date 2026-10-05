---
title: Privacy Policy
permalink: /diff-for-gitlab/privacy/
---

# Diff for GitLab — Privacy Policy

**Effective date:** 6 October 2026
**Last updated:** 6 October 2026

This policy explains what the iOS app **Diff for GitLab** ("the App") does with your data. The App is made by Dmytro Yantsybaiev, an individual developer based in Cracow, Poland ("I", "me"), who is the controller of any personal data described here. Contact: d.yantsybaiev@gmail.com.

## Summary

- Your GitLab token is stored only in your device's Keychain and is sent only to the GitLab server you signed in to. It never reaches me.
- Your code, merge requests, pipelines and other GitLab content travel only between your device and your GitLab server. I have no access to them.
- Purchases are handled by Apple. I never see your payment details.
- The App sends a small set of **anonymous usage events** to PostHog, hosted in the European Union, to see how the introductory screens and the purchase flow perform. These events contain no token, username, server address or GitLab content. **You can turn this off in the App at any time.**
- No advertising, no tracking across apps or websites, no selling or sharing of data with data brokers.

## 1. Data stored on your device

Everything below stays on your device unless a later section says otherwise. Deleting the App removes all of it.

| Data | Where | Details |
|---|---|---|
| GitLab access token (personal access token or OAuth tokens) | iOS Keychain | Stored with the "accessible when unlocked, this device only" protection class. It is not synced to iCloud Keychain and is not restored to another device from a backup. Removed when you sign out. |
| Account list | App preferences | For each account: username, GitLab server address, sign-in method and, for OAuth, the application identifier. Needed to show your accounts and switch between them. |
| Offline cache of GitLab responses | App cache folder | Responses from your GitLab server (for example merge request lists and diffs) so screens open instantly and work offline. Protected until the device is first unlocked after a restart, capped at 200 MB, entries unused for 30 days are deleted, and iOS may purge the folder when storage is low. Cleared when you sign out of the account. |
| Recent searches and recently viewed projects | App preferences | Kept per account, cleared when you sign out of that account. |
| Preferences | App preferences | Code text size, job-log timestamp setting, the last self-managed server address you entered, the state of home-screen sections, and your choice about usage analytics. |
| Anonymous analytics identifier and queued events | App support folder | A random identifier generated on your device by the analytics SDK (see section 6). It is not Apple's advertising identifier and is not linked to your Apple Account or GitLab account. Not created when analytics is turned off. |

## 2. Data sent to your GitLab server

The App is a client for GitLab. Every request it makes goes to the GitLab server you signed in to, over HTTPS only, carrying your token so GitLab can act as you. That includes reading merge requests, diffs, pipelines, job logs, projects and files, and the actions you take by tapping a control: approve, merge, comment, retry, cancel or run a pipeline job, star a project.

- The App never performs a write action on GitLab without you tapping the control for it.
- People's avatars are loaded only from your own GitLab server, never from Gravatar or any other third-party image service. Project avatars are not loaded at all.
- When you type a self-managed server address, the App makes one request without credentials to that server's `/api/v4/user` endpoint to confirm it is a GitLab server before asking for a token.

What your GitLab server does with these requests is governed by GitLab Inc.'s privacy policy (for gitlab.com) or by the organisation that runs your self-managed instance. I have no access to that data.

## 3. Signing in with OAuth

If you choose "Sign in with GitLab", the App opens GitLab in a system web sign-in sheet provided by iOS. You sign in on GitLab's own pages; the App never sees your GitLab password. The App requests GitLab's `api` permission, and the tokens are exchanged directly between your device and your GitLab server using PKCE. No server of mine is involved at any point.

For gitlab.com, the OAuth application the App uses is registered under my GitLab account; this registration gives me no access to your account or tokens. For self-managed servers, the application is registered by your instance administrator. You can revoke the App's access at any time on GitLab's "Applications" or "Access Tokens" settings pages.

## 4. Purchases

Subscriptions are sold through Apple's in-app purchase system. Apple processes the payment and holds your payment details, name and Apple Account. The App receives from Apple only signed transaction information: which product you bought, whether the subscription is active, and when it renews or ends. Apple's privacy policy applies to the purchase itself.

Whether a purchase, restore or offer-code redemption succeeded is also recorded in the anonymous analytics described in section 6, without any payment or identity details, unless you have turned analytics off.

## 5. No tracking, no advertising

The App does not track you across other companies' apps or websites, does not show advertising, and does not sell or share your data with data brokers. It therefore does not ask for App Tracking Transparency permission. Its privacy manifest declares no tracking.

## 6. Anonymous usage analytics

**Why.** To learn whether the introductory screens, the sign-in step and the purchase flow work, and to compare variants of those screens (A/B testing). This is my legitimate interest in improving a paid product. I believe it does not override your interests because the data cannot identify you, is minimal, and can be switched off at any time.

**Your choice.** Analytics is on by default. You can turn it off at any time with the **Share Anonymous Usage Data** switch, found on the sign-in screen under *How Diff handles your sign-in* and in the account menu (top right) once you are signed in. When it is off, the App does not contact PostHog at all: no events, no identifier, no A/B test lookups; screens show their default variant. Turning it back on starts analytics again under a new identifier.

**Who processes it.** PostHog Inc., using PostHog's EU Cloud with data stored in the European Union, under PostHog's data processing agreement.

**What is sent.** Events are sent under a random identifier created on your device when analytics first runs. No person profile is created on PostHog, so events cannot be looked up by who you are. The events are:

| Event | Properties |
|---|---|
| Application installed, updated, opened, backgrounded | App version and build (added by the SDK) |
| Onboarding screen shown | Which of the four introductory screens |
| Signed in | Method (OAuth or token); whether the server is gitlab.com or "self-managed". The address of a self-managed server is never sent. |
| Paywall opened | Which control opened it |
| Paywall failed to load | Reason category (offline, empty, other) |
| Plan selected | Yearly or weekly |
| Purchase started | Plan; whether a free trial was offered |
| Purchase finished | Plan; outcome (success, pending, cancelled, failed, unverified) |
| Restore finished | Where it was started; outcome |

Each event also carries technical properties added by the PostHog SDK: iOS version, device model, app version and build, interface language (language code only), screen size, whether the connection is Wi-Fi or cellular, and a flag marking development builds that use test purchases.

**What is never sent.** Your token, username, email, GitLab server address, repository names, merge request or pipeline content, file contents, comments, or any text you type. No location: the App asks PostHog not to derive a location from your IP address, the PostHog project is configured to discard client IP addresses, and the App removes the device time zone from every event before it is sent.

**A/B tests.** To choose a variant of a screen, the App asks PostHog for feature flags using the same random identifier. The variant you saw is attached to the events above.

**When it is off.** Besides your own switch, analytics is disabled in development builds, automated tests and screenshot runs.

**Retention.** Events are kept for 12 months and then deleted. The random identifier is deleted when you turn analytics off or delete the App; turning it on again or reinstalling creates a new one, unrelated to the old.

## 7. App Store privacy label

Apple's privacy label for the App, derived from the above, lists **Product Interaction**, **Purchase History**, **Other Usage Data** and **Device ID** (the random analytics identifier), all collected for analytics, **not linked to your identity** and **not used for tracking**.

## 8. Security

- Only HTTPS server addresses are accepted. Certificates are validated by iOS; a self-managed server with a private certificate authority requires a configuration profile installed on the device.
- Tokens are protected by the iOS Keychain and are readable only while the device is unlocked.
- Cached GitLab data is protected by iOS file protection until the device is first unlocked after a restart.

No method of storage or transmission is completely secure. If you believe your token has been exposed, revoke it in GitLab.

## 9. Children

The App is a developer tool for people who hold a GitLab account and is not directed at children. I do not knowingly collect personal data from children under 16.

## 10. Your rights

Depending on where you live, you may have rights under the GDPR, the UK GDPR, the CCPA or similar laws: to access, correct or delete personal data, to object to or restrict processing, to data portability, and to complain to a supervisory authority. In Poland the supervisory authority is the President of the Personal Data Protection Office (Prezes Urzędu Ochrony Danych Osobowych, uodo.gov.pl).

Because the only data I receive is anonymous analytics with no link to your identity, I am generally unable to find or delete the events of a specific person. You can stop further collection at any time with the switch described in section 6 or by deleting the App; both discard the random identifier. For anything else, contact me at the address below and I will help within the limits of what the data allows.

Data held by your GitLab provider or by Apple is subject to their policies; please contact them for requests about that data.

## 11. Third parties

| Party | Role |
|---|---|
| GitLab Inc. (gitlab.com) or the operator of your self-managed instance | Receives every request the App makes as you; governs your GitLab data |
| Apple Inc. | Processes in-app purchases and subscriptions; distributes the App |
| PostHog Inc. (EU Cloud) | Processes the anonymous usage events in section 6, if you leave analytics on |
| GitHub Inc. | Hosts this page on GitHub Pages; GitHub may log visitor IP addresses under its own privacy statement |

I do not transfer your data to anyone else.

## 12. Changes

I may update this policy as the App changes. The current version is always at this address with its effective date. If a change materially affects how data is used, I will announce it in the App or on the App Store page where reasonably possible.

## 13. Contact

Dmytro Yantsybaiev
Cracow, Poland
Email: d.yantsybaiev@gmail.com
