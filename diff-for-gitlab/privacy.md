---
title: Privacy Policy
permalink: /diff-for-gitlab/privacy/
---

# Diff for GitLab — Privacy Policy

**Effective date:** 10 October 2026

This policy explains what the iOS app **Diff for GitLab™** ("the App") does with your data. It is an independent app, not affiliated, endorsed, sponsored, or approved with or by GitLab Inc. GITLAB is a trademark of GitLab Inc. in the United States and other countries and regions. The App is made and published by Dmytro Yantsybaiev, a software developer based in Kraków, Poland ("I", "me"), who is the data controller for the processing described here. Contact details are in section 12.

## Summary

- Your GitLab token is stored only in your device's Keychain and is sent only to the GitLab server you signed in to. It never reaches me.
- Your code, merge requests, pipelines and other GitLab content travel only between your device and your GitLab server. I have no access to them.
- Purchases are handled by Apple. I never see your payment details.
- The App sends nothing to me. It talks only to your GitLab server and to Apple. Legal pages you open from it, like this one, load from GitHub Pages (section 10).
- No advertising, no tracking across apps or websites, no selling or sharing of data with data brokers.

Data in section 1 is handled by the App on your device under your control; I never receive it. Emailing me is optional. A GitLab token is needed to use the App, but it never reaches me. I make no automated decisions or profiles about you.

| Processing | Legal basis | Who receives it | Kept for |
|---|---|---|---|
| Checking your subscription (section 4) | Performance of the contract, Art. 6(1)(b) | Apple (independent controller) | While the App is installed |
| Email you send me (section 6) | Legitimate interest in answering you, Art. 6(1)(f); performance of the contract, Art. 6(1)(b), when it concerns your subscription | Google (Gmail) | 24 months after the last message |
| Everything on your device (section 1) | Performance of the contract, Art. 6(1)(b), to provide the App you use; for other people's names and avatars, legitimate interest, Art. 6(1)(f) | No one but your GitLab server (section 2); never me | Token, accounts, cache and recent items: until you sign out (unused cache entries after 30 days). Other preferences: until you delete the App |
| Crash reports and usage statistics from Apple (section 5) | Legitimate interest in fixing faults, Art. 6(1)(f) | Me, via Apple | Until the fault is fixed |

## 1. Data stored on your device

Everything below stays on your device unless a later section says otherwise.

| Data | Where | Details |
|---|---|---|
| GitLab access token (personal access token or OAuth tokens) | iOS Keychain | Stored with the "accessible when unlocked, this device only" protection class. It is not synced to iCloud Keychain and is not restored to another device from a backup. Deleted when you sign out. |
| Account list | App preferences | For each account: username, GitLab server address, sign-in method and, for OAuth, the application identifier. Needed to show your accounts and switch between them. |
| Offline cache of GitLab responses | App cache folder | Responses from your GitLab server (for example merge request lists and diffs) so screens open instantly and work offline. Protected until the device is first unlocked after a restart, capped at 200 MB, entries unused for 30 days are deleted, and iOS may purge the folder when storage is low. Cleared when you sign out of the account. |
| Recent searches and recently viewed projects | App preferences | Kept per account, cleared when you sign out of that account. |
| Preferences | App preferences | Code text size, job-log timestamp setting, the last self-managed server address you entered, the state of home-screen sections, which tips you have already seen, and, for an account on an older GitLab server, that server's version so the App can show the simpler home screen. Per-account items are cleared when you sign out of that account. |

Deleting the App removes the cache and preferences. iOS does not guarantee that Keychain items are deleted together with an app, so sign out first, which deletes the token, or revoke the token in GitLab.

## 2. Data sent to your GitLab server

The App is a client for GitLab. Every request it makes goes to the GitLab server you signed in to, over HTTPS only, carrying your token so GitLab can act as you. That includes reading merge requests, diffs, pipelines, job logs, projects and files, and the actions you take by tapping a control, for example approving or removing your approval, merging or rebasing, commenting or resolving a thread, retrying, cancelling or running a pipeline or job, and starring a project.

- People's avatars are loaded only from your own GitLab server, never from Gravatar or any other third-party image service. Project avatars are not loaded at all.
- When you type a self-managed server address, the App sends requests without credentials to `/api/v4/user` on that address and, if needed, on the root of the same host, to confirm it is a GitLab server before asking for a token.
- The App refuses cookies from your GitLab server. Network responses are kept in memory only, never written to disk, and are discarded when you sign out or the App quits. The App's own offline cache (section 1) is the only copy kept on your device.
- When you open Search, the App asks iOS whether the clipboard holds a web link, without reading it, so it can offer a Paste button. The clipboard's contents are read only when you tap Paste, and are not kept.

What your GitLab server does with these requests is governed by GitLab Inc.'s privacy policy (for gitlab.com) or by the organisation that runs your self-managed instance; they are independent controllers of that data. I have no access to it.

## 3. Signing in with OAuth

If you choose "Sign in with GitLab", the App opens GitLab in a system web sign-in sheet provided by iOS. You sign in on GitLab's own pages; the App never sees your GitLab password. On your first sign-in to a server, and when you re-authorise an account, the sheet shares cookies with Safari, so GitLab may keep you signed in to its website in Safari; signing out of the App does not sign you out there. When you add another account on the same server, the sheet does not share them, so you can sign in as someone else. The App requests GitLab's `api` scope, and the tokens are exchanged directly between your device and your GitLab server using PKCE. No server of mine is involved at any point.

For gitlab.com, the OAuth application the App uses is registered under my GitLab account; this registration gives me no access to your account or tokens. For self-managed servers, the application is registered by your instance administrator. You can revoke the App's access at any time on GitLab's "Applications" or "Access Tokens" settings pages.

## 4. Purchases

Subscriptions are sold through Apple's in-app purchase system. Apple is an independent controller for the purchase and your Apple Account: it processes the payment and holds your payment details, name and account. From Apple the App receives only signed transaction information: the product, its status, renewal or expiry dates, and Apple's transaction identifiers, which do not identify you to me. Apple's privacy policy applies to the purchase itself. The App uses this information only on your device, to unlock its features; it is not sent to me. Apple gives me sales and subscription reports that do not identify you.

## 5. No tracking, no advertising

The App does not track you across other companies' apps or websites, does not show advertising, and does not sell or share your data with data brokers. It therefore does not ask for App Tracking Transparency permission, and its privacy manifest declares no tracking and no collected data.

Apple's privacy label for the App is **Data Not Collected**.

If you have turned on *Share With App Developers* in your device's privacy settings, Apple may give me crash reports and aggregated usage statistics for the App. This is Apple's feature, controlled in iOS settings, not by the App. Apple does not give me your identity with them. I use them to fix faults, on the basis of my legitimate interest (Art. 6(1)(f)), and keep them until the fault is fixed. You can stop them at any time by turning off *Share With App Developers*.

## 6. Email you send me

If you email me, I keep your address and message to answer you and to keep a record of the conversation. Mail is hosted by Google (Gmail), which acts as an independent controller under Google's Privacy Policy, and may be processed in the United States by Google LLC, which is certified under the EU–U.S. Data Privacy Framework and its UK Extension. I delete support threads 24 months after the last message, or later only if I need them to establish or defend a legal claim, and only until it is resolved. This is the only data through which I could identify you.

## 7. Security

- Only HTTPS server addresses are accepted. Certificates are validated by iOS; a self-managed server with a private certificate authority requires a configuration profile installed on the device.
- Tokens are protected by the iOS Keychain and are readable only while the device is unlocked.
- Cached GitLab data is protected by iOS file protection until the device is first unlocked after a restart.

No method of storage or transmission is completely secure. If you believe your token has been exposed, revoke it in GitLab.

## 8. Children

The App is a developer tool for people who hold a GitLab account and is not directed at children.

## 9. Your rights

Under the GDPR and similar laws you may have the right to access, correct or delete personal data, to object to or restrict processing, to data portability, and to complain to a supervisory authority.

The only personal data I hold that could identify you is email you send me (section 6). To exercise any of these rights for it, email me. Data that stays on your device never reaches me: you control it by signing out or deleting the App.

**Right to object.** Where I rely on legitimate interest (answering your email, or crash reports), you can object at any time by emailing me, and I will stop unless I have compelling legitimate grounds that override your interests, or need the data for a legal claim. You can also stop crash reports at any time by turning off *Share With App Developers*.

You may complain to the supervisory authority in the country where you live or work. For me, that is the President of the Personal Data Protection Office in Poland (Prezes Urzędu Ochrony Danych Osobowych, uodo.gov.pl).

Data held by your GitLab provider or by Apple is subject to their policies; please contact them for requests about that data.

## 10. Third parties

| Party | Role |
|---|---|
| GitLab Inc. (gitlab.com) or the operator of your self-managed instance | Independent controller: receives every request the App makes as you and governs your GitLab data |
| Apple Inc. | Independent controller for in-app purchases, subscriptions and your Apple Account; distributes the App |
| Google (Gmail; Google LLC in the United States) | Hosts my email, including email you send me (section 6) |
| GitHub Inc. | Hosts this page on GitHub Pages; GitHub may log visitor IP addresses under its own privacy statement |

I do not share your data with anyone else, except where the law requires it.

## 11. Changes

I may update this policy as the App changes. The current version is always at this address with its effective date.

## 12. Contact

Dmytro Yantsybaiev, Kraków, Poland  
Email: d.yantsybaiev@gmail.com

My full business details (address, telephone, NIP) are in the [Terms of Use](../terms/#14-contact).
