# Zenvio privacy policy

**Last updated 18 November 2026**

Zenvio is a game clipper for Windows. This policy explains what personal data Zenvio handles, where it goes, and your
rights. The short version:

- **Your clips, settings and logs stay on your PC.** We never receive them unless you choose to send part of a log
  with a problem report.
- **No account, no ads, no tracking, no analytics, no selling of data.**
- Zenvio goes online for only two things: **update checks** (to GitHub) and **problem reports you choose to send**
  (to our report server).

This policy goes with the [terms of use](TERMS.md).

## 1. Who is responsible for your data

The "controller" (the one responsible for your personal data under UK and EU data protection law) is **the Zenvio
developer**, an individual in the United Kingdom ("we", "us").

**Contact:** [iposbots@proton.me](mailto:iposbots@proton.me). Please use this address for any privacy question or
request. We don't have a data protection officer; we're too small to need one.

## 2. Data that stays on your PC

Zenvio stores these things **only on your own PC**. We never see them, and they're not sent anywhere:

| What | Where | Notes |
|---|---|---|
| Your clips | your clips folder (`Videos\Clips` unless you choose another) | Can include your screen, PC sound (including voice chat) and your microphone. |
| The rolling recording | `%LOCALAPPDATA%\Zenvio\buffer` | The last few minutes, overwritten as you play. Deleted when Zenvio closes; after a crash or power cut, deleted the next time Zenvio starts. |
| Settings, your own sounds, starred clips | `%APPDATA%\Zenvio` | |
| Logs | `%LOCALAPPDATA%\Zenvio\logs` | What Zenvio did and when: file paths (which include your Windows user name), audio device names, your graphics card model and which video encoder Zenvio used, which program was in front and whether it counted as a game, and clip file names. Never what you type, and never window titles. Limited in size. |
| Clip thumbnails and other working files | `%LOCALAPPDATA%\Zenvio` | Includes a list of large or full-screen programs Zenvio has seen, for the games list in Settings. |
| A random "PC number" | `%LOCALAPPDATA%\Zenvio\report-id.txt` | Made by Zenvio the first time you open the problem-report form. Not linked to you or your PC's hardware. |
| Your sent reports | `%LOCALAPPDATA%\Zenvio\sent-reports.json` | The reference and a secret "delete key" for each report you sent, so you can delete it later. |

Zenvio never collects your name, email address, location, contacts, keystrokes or game account details. It does not
read anything from inside your games.

You control all of this: change settings any time, delete clips in Zenvio, or delete the folders above (see "Stopping
using Zenvio" in the [terms](TERMS.md#14-stopping-using-zenvio)). Uninstalling Zenvio leaves these files in place so you
don't lose your clips by accident.

Because this data never leaves your PC, we are not the controller for it. Your own personal use of Zenvio is up to
you. If you share clips, data protection and recording laws may apply to you (see section 5 of the
[terms](TERMS.md#5-using-zenvio-responsibly)).

## 3. Update checks (GitHub)

About every 6 hours, and when you open the Zenvio window (never while recording), Zenvio asks GitHub whether a newer
version exists at [github.com/ipo461/zenvio-releases](https://github.com/ipo461/zenvio-releases), and downloads it if
there is one. Nothing installs until you click Update.

- **What is sent:** an ordinary web request for the list of releases and, if there's an update, the download. It does
  not include your clips, settings, logs or anything about you.
- **Who sees it:** **GitHub, Inc.** (a Microsoft company in the US) sees your internet address (IP address), the time,
  and basic technical details of the request, as for any website you visit. GitHub decides what it logs and how long
  it keeps it; see the
  [GitHub General Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
  We don't receive your IP address from GitHub. We can only see how many times each release was downloaded.
- **Turning it off:** switch off update checks in Zenvio's Settings.

**When you install Zenvio**, the installer downloads Microsoft's free .NET Desktop Runtime if your PC doesn't have it
yet. Microsoft then sees your IP address; see the [Microsoft Privacy Statement](https://privacy.microsoft.com/privacystatement).
The same goes for GitHub when you download Zenvio from the releases page.

## 4. Problem reports

This is the only time we receive data from Zenvio, and **only if you choose to send a report** (Settings → Report a
problem). Nothing is sent automatically. You see exactly what will be sent before you click Send.

### What a report contains

| Item | Example | Stored? |
|---|---|---|
| What you typed (up to 4,000 characters) | "Clip saved without sound" | Yes |
| Zenvio version | `0.7.1` | Yes |
| Windows version | `Windows 11 25H2 (build 26200.9974)` | Yes |
| Graphics card name | `NVIDIA GeForce RTX 3050` | Yes |
| Zenvio's logs: **only if you tick the box** | the last 200 lines of each of Zenvio's two logs | Yes, if you ticked it |
| Your random PC number | 32 random letters and digits | **No.** Only used for the "3 reports per hour" limit (below) |

The server also stores **the time** the report arrived, a random **report ID**, and a scrambled copy (hash) of the
report's delete key. It does **not** store your IP address or your PC number with the report.

**Logs are cleaned on your PC before you see the preview.** Zenvio replaces your Windows user name, PC name and user
folder, e-mail addresses, internet and network addresses (IP and MAC), Windows account IDs, names in device names
(like "Sam's headphones") and anything that looks like a password, key or token. Logs still show which games and
programs Zenvio noticed and when, and your clip file names. Tick **"Also hide game, app and clip names"** to remove those
too.

**There is no email field and no account.** Please don't type personal details (your real name, address, phone number,
passwords) into a report. Under 13, or under 16 in some EU countries? Ask a parent or guardian first.

### Why we use it, and the legal basis

Only to **find and fix problems in Zenvio**. Reports are never sold, shared with anyone for their own use, used for
ads, profiling or tracking, or used to train AI. We don't make any automated decisions about you.

The legal basis is **your consent** (UK GDPR and EU GDPR Article 6(1)(a)): you choose to send each report, and you can
withdraw your consent at any time by deleting it (below). Withdrawing doesn't affect anything done before.

### Stopping spam (your IP address)

To stop one person flooding the inbox, the server allows **3 reports per hour** from the same PC number and from the
same internet connection, and 300 a day in total. For this it keeps, for each report sent, a **scrambled version (keyed
hash)** of your IP address and of your PC number, with the time. These can't be turned back into your IP address
without our secret key. They're used only for the 1-hour limit, and are deleted when they're 2 hours old, at the
latest at the next daily clean-up. Cloudflare's own flood protection also counts requests per scrambled IP address
over 1 minute. The legal basis for this is our **legitimate interest** in keeping the report service working and free
of spam (Article 6(1)(f)).

### Where reports go: Cloudflare

Reports are sent over an encrypted connection (HTTPS) to Zenvio's report server, which runs on **Cloudflare**
(Cloudflare, Inc., USA). Cloudflare acts as our **processor**: it stores and handles reports only on our instructions,
under its Data Processing Addendum. The report database is stored in Cloudflare's **Western Europe** region. Like any
website host, Cloudflare's network sees your IP address while it carries the request, and the request may be handled
at the Cloudflare data centre nearest to you.

Because Cloudflare is a US company, your data may be accessed from the US. This is protected by Cloudflare's Data
Processing Addendum, which includes the EU Standard Contractual Clauses and the UK Addendum to them; Cloudflare is
also certified under the EU-US Data Privacy Framework and its UK Extension. See
[Cloudflare's privacy policy](https://www.cloudflare.com/privacypolicy/).

We have switched off Cloudflare's request logs for the report server, so it doesn't keep a log of who sent what.

### Who can read reports

Only the Zenvio developer, using a private key. Players can only send reports and delete their own.

### How long reports are kept

**Deleted automatically after 90 days** by a daily clean-up (and hidden from us as soon as they're 90 days old), or
earlier if you or we delete them.

Cloudflare's database keeps its own automatic restore history for a limited time (up to 30 days), so a deleted report
fully disappears from that history within 30 days of being deleted. We don't use that history to bring reports back.

### Deleting your report

After sending, you get a **reference** such as `3F9A-0C21-7B44`. To delete your report, go to **Report a problem →
"Your sent reports" → Delete**. No email or account needed; it's removed from the report database straight away.

Lost your PC, or deleted Zenvio's folders? Email [iposbots@proton.me](mailto:iposbots@proton.me) with the reference,
and we'll delete it. You can also ask on the public
[GitHub issues page](https://github.com/ipo461/zenvio-releases/issues), quoting **only** the reference, but that
page is public and needs a GitHub account (13+), so email is better.

## 5. If you email us

If you email us, we receive your email address, your message and anything you attach. We use them only to answer you
(legal basis: our legitimate interest in replying, or taking the steps you asked for). Our email is provided by
**Proton AG** in Switzerland (see [Proton's privacy policy](https://proton.me/legal/privacy)). We delete emails once
your question is dealt with, and at the latest after 12 months. If you asked us to delete a report or exercised another
right, we keep a short note (date, what was asked, what we did) for up to 2 years, to show we did it.

## 6. No tracking, ads or selling

Zenvio has no analytics, no tracking, no cookies, no advertising, and no third-party code that reports on you. We don't
sell or share personal data. Nobody else gets reports, except Cloudflare as our processor (section 4), or if the law
forces us to (for example a valid court order).

## 7. Children

Zenvio is meant for people aged **13 and over**, and anyone younger should only use it with a parent's or
guardian's permission (see the [terms](TERMS.md#6-age)). We've designed Zenvio to need as little personal data as
possible: no account, no email, nothing sent automatically, logs left out of reports unless ticked, and in-app deletion
that needs no account.

If you're under 13, or under 16 in some EU countries, please ask a parent or guardian before sending a problem report
or emailing us. If you're a parent and think your child has sent us personal data, email us with the report reference
if you have it, and we'll delete it.

## 8. Your rights

Under UK and EU data protection law you have the right to:

- **access** the personal data we hold about you, and get a copy;
- have it **corrected** if it's wrong;
- have it **deleted**;
- **restrict** or **object** to how we use it;
- **withdraw your consent** at any time (for reports: delete them);
- receive your data in a portable format.

To use any of these rights, email [iposbots@proton.me](mailto:iposbots@proton.me). It's free, and we'll answer within
one month. **Please include your report reference.** Reports aren't linked to a name, email or account, so without
the reference we usually can't tell which report is yours. We won't ask you for ID beyond what we need to find your
report.

**Complaints.** If you're unhappy with how we handle your data, please tell us first so we can put it right. You also
have the right to complain to a data protection authority:

- in the UK: the **Information Commissioner's Office (ICO)**, [ico.org.uk/make-a-complaint](https://ico.org.uk/make-a-complaint/),
  phone 0303 123 1113;
- in the EU or EEA: the data protection authority in your country (list at
  [edpb.europa.eu](https://www.edpb.europa.eu/about-edpb/about-edpb/members_en)).

## 9. How we keep reports safe

Reports travel over an encrypted connection (HTTPS only). The report server accepts only the exact fields listed
above, checks every report, and can't be read without our private key. Only scrambled versions of IP addresses and PC
numbers are kept, and only for a short time. No system is perfectly secure, so please don't put anything sensitive in a
report.

## 10. Summary: how long data is kept

| Data | Kept for |
|---|---|
| Clips, settings, logs on your PC | Until you delete them (stay after uninstalling; see the terms) |
| Problem report | 90 days, or until you delete it (plus up to 30 days in Cloudflare's restore history) |
| Scrambled IP address and PC number (spam limit) | 2 hours, at most until the next daily clean-up |
| Emails to us | Until dealt with, at most 12 months |
| Note of a deletion or rights request | Up to 2 years |
| GitHub's logs of update checks | Up to GitHub (see its privacy statement) |

## 11. Changes to this policy

If we change this policy, we'll update the date at the top and publish the new version on
[github.com/ipo461/zenvio-releases](https://github.com/ipo461/zenvio-releases). If a change matters for you (for
example, if Zenvio starts sending anything new), Zenvio will show you the change and ask you to agree to the terms
again before it sends anything new.

## 12. Contact

The Zenvio developer: **[iposbots@proton.me](mailto:iposbots@proton.me)**
