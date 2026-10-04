---
title: QuickBooks Automation
description: >-
  Set up QuickBooks rules, recurring transactions, bank feeds and scripts so
  your books stay current with minutes of work each week.
category: Accounting
icon: gears
date: 2026-10-04
---

QuickBooks keeps most small organizations' books, but the default workflow -
typing every transaction by hand - quietly kills volunteer motivation. This
guide covers the built-in automation QuickBooks already offers, then the
scriptable extras for teams comfortable with a bit of code.

## Start with bank feeds

Connect your bank account to QuickBooks and let transactions flow in
automatically. This is the foundation; everything below builds on it.

1. **Banking → Link bank**, sign in with your bank credentials.
2. Choose to auto-import the last 90 days.
3. Set the connection's refresh to run automatically (QuickBooks Online does
   this by default).

Never accept a feed transaction without categorizing it - the point of
automation below is that you stop doing this one at a time.

## Rules: your first 80%

QuickBooks Rules let you say "if the description contains X, categorize as
Y." A few minutes of setup eliminates most manual categorization:

| Rule | Condition | Action |
| --- | --- | --- |
| Rent | Description contains landlord name | → Rent expense |
| Utilities | Description contains utility name | → Utilities |
| Hardware store | Description contains vendor | → Supplies |
| Salary | Description contains payroll service | → Payroll expense |

Write rules from the **Rules** tab under Banking: pick a real transaction,
tell QuickBooks how to categorize it, and check "Auto-accept." Keep
auto-accept off for anything ambiguous (e.g. checks).

## Recurring transactions

Anything that happens monthly belongs in **Settings → Recurring
transactions**:

- Rent, subscriptions and insurance → *Scheduled* bills.
- Recurring invoices to funders or program partners → *Scheduled* invoices.
- Retainer or monthly bookkeeping fees → *Reminder*.

Review the recurring list quarterly. Lapsed subscriptions that keep
generating invoices are a classic audit finding.

## Receipt capture

QuickBooks Online's receipt capture lets you photograph or email receipts
and have them matched to bank transactions automatically. Forward receipts
to a dedicated address (available on Plus and higher), or snap them in the
mobile app at the time of purchase - then the monthly reconciliation is a
review, not a data-entry session.

## Integrations worth turning on

- **Payment processors** (Stripe, Square, PayPal): official sync apps post
  donations and fees to QuickBooks automatically - no more re-keying
  donation batches.
- **Payroll** (Gusto, QuickBooks Payroll): journals post on each run.
- **Expense tools** (Hubdoc, Ramp): receipts arrive categorized.

Each integration replaces a recurring manual task; add one at a time and
verify the postings for a full month before trusting them.

## Scripting the rest

For teams comfortable with code, QuickBooks exposes a REST API that makes
bulk work trivial. Our
[community-tech-kit repository](https://github.com/goodfoundation/community-tech-kit)
includes starter scripts for common jobs:

- **Monthly category report** - pull all transactions, group by class, and
  email the board a one-pager.
- **Donation reconciliation** - match a Stripe payout report to QuickBooks
  deposits and flag anything unexplained.
- **Year-end export** - archive every transaction and attachment to a
  dated folder for the accountant or auditor.

> Automation should remove keystrokes, not oversight. Keep the monthly
> reconciliation and the two-person controls from our
> [accounting setup guide]({{ '/guides/accounting-setup-best-practices/' | relative_url }}) - the
> scripts above just feed them cleaner data.

## A weekly rhythm that fits in 15 minutes

1. **Monday (5 min):** accept auto-categorized bank feed items.
2. **Midweek (5 min):** photograph or forward any receipts from the week.
3. **Month end (5 min):** run the reconciliation, review the rules that
   fired, clear exceptions.

If any step regularly takes longer, it's a candidate for a new rule,
recurring transaction or script - tell us about it and we may add the
recipe here.