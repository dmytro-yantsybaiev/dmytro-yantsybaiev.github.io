---
title: Privacy Policy
permalink: /diff-for-gitlab/privacy/
---

# Diff for GitLab — Privacy Policy

**Effective date:** 6 October 2026

This policy explains what the iOS app **Diff for GitLab** ("the App") does with your data. The App is made and published by Dmytro Yantsybaiev, a software developer based in Kraków, Poland ("I", "me"), who is the data controller for the processing described here. Contact details are in section 13.

## Summary

- Your GitLab token is stored only in your device's Keychain and is sent only to the GitLab server you signed in to. It never reaches me.
- Your code, merge requests, pipelines and other GitLab content travel only between your device and your GitLab server. I have no access to them.
- Purchases are handled by Apple. I never see your payment details.
- The App sends a small set of **usage events that are not linked to your identity** to PostHog, hosted in the European Union, to see how the introductory screens and the purchase flow perform. **You can turn this off in the App at any time.** It is on by default, so the first events are sent during the introductory screens, before you reach the switch.
- No advertising, no tracking across apps or websites, no selling or sharing of data with data brokers.

For data that stays on your device, I set the rules but never receive it. My obligations as controller arise only for the usage events in section 5 and for email you send me (section 7).

| Processing | Legal basis | Who receives it | Kept for |
|---|---|---|---|
| Usage events and A/B test variants (section 5) | Legitimate interest, GDPR Art. 6(1)(f); you can object with the switch | PostHog Inc. (processor, EU Cloud) | Up to 12 months |
| Checking your subscription (section 4) | Performance of the contract, Art. 6(1)(b) | Apple (independent controller) | While the App is installed |
| Email you send me (section 7) | Legitimate interest in answering you, or the contract if you subscribe | Google (Gmail) | 24 months after the last message |
| Everything on your device (section 1) | Not received by me | Nobody | Until you sign out or delete the App |

## 1. Data stored on your device

Everything below stays on your device unless a later section says otherwise.

| Data | Where | Details |
|---|---|---|
| GitLab access token (personal access token or OAuth tokens) | iOS Keychain | Stored with the "accessible when unlocked, this device only" protection class. It is not synced to iCloud Keychain and is not restored to another device from a backup. Deleted when you sign out. |
| Account list | App preferences | For each account: username, GitLab server address, sign-in method and, for OAuth, the application identifier. Needed to show your accounts and switch between them. |
| Offline cache of GitLab responses | App cache folder | Responses from your GitLab server (for example merge request lists and diffs) so screens open instantly and work offline. Protected until the device is first unlocked after a restart, capped at 200 MB, entries unused for 30 days are deleted, and iOS may purge the folder when storage is low. Cleared when you sign out of the account. |
| Recent searches and recently viewed projects | App preferences | Kept per account, cleared when you sign out of that account. |
| Preferences | App preferences | Code text size, job-log timestamp setting, the last self-managed server address you entered, the state of home-screen sections, and your choice about usage analytics. |
| Analytics identifier and queued events | App support folder | A random identifier generated on your device by the analytics SDK (section 5). It is not Apple's advertising identifier and is not linked to your Apple Account or GitLab account. Discarded when you turn analytics off; not created while it is off. |

Deleting the App removes the cache, preferences and analytics data. iOS does not guarantee that Keychain items are deleted together with an app, so sign out first, which deletes the token, or revoke the token in GitLab.

## 2. Data sent to your GitLab server

The App is a client for GitLab. Every request it makes goes to the GitLab server you signed in to, over HTTPS only, carrying your token so GitLab can act as you. That includes reading merge requests, diffs, pipelines, job logs, projects and files, and the actions you take by tapping a control, for example approving or removing your approval, merging or rebasing, commenting or resolving a thread, retrying, cancelling or running a pipeline or job, and starring a project.

- The App never performs a write action on GitLab without you tapping the control for it.
- People's avatars are loaded only from your own GitLab server, never from Gravatar or any other third-party image service. Project avatars are not loaded at all.
- When you type a self-managed server address, the App makes one request without credentials to that server's `/api/v4/user` endpoint to confirm it is a GitLab server before asking for a token.

What your GitLab server does with these requests is governed by GitLab Inc.'s privacy policy (for gitlab.com) or by the organisation that runs your self-managed instance; they are independent controllers of that data. I have no access to it.

## 3. Signing in with OAuth

If you choose "Sign in with GitLab", the App opens GitLab in a system web sign-in sheet provided by iOS. You sign in on GitLab's own pages; the App never sees your GitLab password. The App requests GitLab's `api` scope, and the tokens are exchanged directly between your device and your GitLab server using PKCE. No server of mine is involved at any point.

For gitlab.com, the OAuth application the App uses is registered under my GitLab account; this registration gives me no access to your account or tokens. For self-managed servers, the application is registered by your instance administrator. You can revoke the App's access at any time on GitLab's "Applications" or "Access Tokens" settings pages.

## 4. Purchases

Subscriptions are sold through Apple's in-app purchase system. Apple is an independent controller for the purchase and your Apple Account: it processes the payment and holds your payment details, name and account. From Apple the App receives only signed transaction information: the product, its status, renewal or expiry dates, and Apple's transaction identifiers, which do not identify you to me. Apple's privacy policy applies to the purchase itself.

Whether a purchase, restore or offer-code redemption succeeded is also recorded in the usage events described in section 5, without any payment or identity details, unless you have turned analytics off.

## 5. Usage analytics

**Why.** To learn whether the introductory screens, the sign-in step and the purchase flow work, and to compare variants of those screens (A/B testing), in a product I sell.

**Legal basis.** I rely on legitimate interest (GDPR Art. 6(1)(f)). I have weighed this against your interests: the events are few, hold nothing that identifies you, are kept at most 12 months, and are never used for advertising or profiling. Where the law in your country requires consent for this kind of measurement, the switch described next is how you give or withdraw it.

**Your right to object, and your choice.** You may object to this processing at any time, for any reason, by turning off the **Share Anonymous Usage Data** switch. It is on the sign-in screen under *How Diff handles your sign-in*, and in the account menu (top right) once you are signed in. No email or justification is needed; it takes effect immediately. The switch is on by default, which means the first events (that the App was installed and opened, and which introductory screens were shown) are sent before you reach it. When the switch is off, the App does not contact PostHog at all: no events, no identifier, no A/B test lookups, and screens show their default variant. Turning it off discards the identifier; turning it back on creates a new one, unrelated to the old.

**Who processes it.** PostHog Inc., as my processor, on PostHog's EU Cloud, under PostHog's data processing agreement. PostHog Inc. is based in the United States; the events are stored in the European Union, and where PostHog staff outside the EEA need access, for example for support, PostHog relies on the EU Standard Contractual Clauses in that agreement. [OWNER: verify PostHog's current DPA and Data Privacy Framework status before publishing.]

**What these events are, legally.** They are grouped under a random identifier, so under the GDPR they count as personal data, even though I hold nothing that connects that identifier to you: no name, email, account, Apple ID or GitLab identity, and PostHog is set not to build person profiles. Events from one install are grouped together, so I can see that *an* install went through the flow, but nothing tells me whose.

**What is sent.**

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

Each event also carries technical properties added by the PostHog SDK: iOS version, device model, app version and build, interface language (language code only), screen size, whether the connection is Wi-Fi or cellular, a flag marking builds that use Apple's test purchases, and similar technical fields such as the SDK version and a session identifier. The full list is in PostHog's iOS SDK documentation.

**What is never sent.** Your token, username, email, GitLab server address, repository names, merge request or pipeline content, file contents, comments, or any text you type. Your IP address necessarily reaches PostHog's servers to deliver each request; the App asks PostHog not to derive a location from it, the PostHog project is set not to store it, and the App removes the device time zone from every event before it is sent. [OWNER: enable "Discard client IP data" in the PostHog project before publishing; this sentence states it as fact.]

**A/B tests.** To choose a variant of a screen, the App asks PostHog for feature flags using the same random identifier, and the variant you saw is attached to the events above. Assigning a variant is random and has no legal or similarly significant effect on you; there is no automated decision-making in the sense of GDPR Art. 22.

**Also off** in development and test builds and in automated screenshot runs.

**Retention.** Events are kept for up to 12 months and then deleted.

## 6. No tracking, no advertising

The App does not track you across other companies' apps or websites, does not show advertising, and does not sell or share your data with data brokers. It therefore does not ask for App Tracking Transparency permission, and its privacy manifest declares no tracking.

Apple's privacy label for the App lists **Product Interaction**, **Purchase History**, **Other Usage Data** and **Device ID** (the random analytics identifier), all collected for analytics, **not linked to your identity** and **not used for tracking**.

## 7. Email you send me

If you email me, I keep your address and message to answer you and to keep a record of the conversation. Mail is hosted by Google (Gmail), which may process it in the United States under Google's terms and the EU Standard Contractual Clauses. I delete support threads 24 months after the last message. This is the only data through which I could identify you.

## 8. Security

- Only HTTPS server addresses are accepted. Certificates are validated by iOS; a self-managed server with a private certificate authority requires a configuration profile installed on the device.
- Tokens are protected by the iOS Keychain and are readable only while the device is unlocked.
- Cached GitLab data is protected by iOS file protection until the device is first unlocked after a restart.

No method of storage or transmission is completely secure. If you believe your token has been exposed, revoke it in GitLab. If I learn of a breach affecting your data, I will notify the Polish supervisory authority within 72 hours and, where the law requires, you, through the App Store page or the App's release notes, since I hold no contact details for users.

## 9. Children

The App is a developer tool for people who hold a GitLab account and is not directed at children. I do not knowingly collect personal data from children under 16.

## 10. Your rights

Under the GDPR and similar laws you may have the right to access, correct or delete personal data, to object to or restrict processing, to data portability, and to complain to a supervisory authority.

For the usage events, I hold nothing that connects the random identifier to you. Under GDPR Art. 11 this means I generally cannot act on access, correction, deletion or portability requests unless you give me the identifier from your device. Turning the switch off is how you object to this processing; it takes effect immediately and discards the identifier. For anything else, email me and I will do what the data allows.

You may complain to the supervisory authority in the EU country where you live or work. For me, that is the President of the Personal Data Protection Office in Poland (Prezes Urzędu Ochrony Danych Osobowych, uodo.gov.pl).

Data held by your GitLab provider or by Apple is subject to their policies; please contact them for requests about that data.

## 11. Third parties

| Party | Role |
|---|---|
| GitLab Inc. (gitlab.com) or the operator of your self-managed instance | Independent controller: receives every request the App makes as you and governs your GitLab data |
| Apple Inc. | Independent controller for in-app purchases, subscriptions and your Apple Account; distributes the App |
| PostHog Inc. (EU Cloud) | Processor for the usage events in section 5, acting on my instructions, if you leave analytics on |
| Google (Gmail) | Processor for email you send me (section 7) |
| GitHub Inc. | Hosts this page on GitHub Pages; GitHub may log visitor IP addresses under its own privacy statement |

I do not share your data with anyone else.

## 12. Changes

I may update this policy as the App changes. The current version is always at this address with its effective date and a short list of what changed. Material changes are also mentioned in the App's release notes on the App Store.

## 13. Contact

Dmytro Yantsybaiev  
[OWNER: street and number]  
[OWNER: postal code] Kraków, Poland  
Email: d.yantsybaiev@gmail.com  
Telephone: [OWNER: number, or delete this line]
