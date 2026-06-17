# Nonprofit Google Ad Grant Kit

A plug-and-play starter kit for marketers running Google Ad Grants for 501(c)(3) nonprofits.

Google gives verified nonprofits **$10,000/month in free Google Search ads**. Most nonprofits either don't know about it or set it up wrong and lose the grant. This repo documents everything — from activation to ongoing compliance — so you can launch fast and keep the grant running.

Built while setting up the grant for [Beach Cities Education Foundation (BCEF)](https://beachcitiesef.org), a South Bay LA nonprofit serving neurodivergent young adults.

---

## What's in here

```
nonprofit-google-ad-grant-kit/
├── README.md
├── setup/
│   ├── activation-guide.md       # Step-by-step: Goodstack → Google for Nonprofits → Ad Grants
│   └── conversion-tracking.md    # GA4 setup + linking to Google Ads
├── campaigns/
│   ├── campaign-template.md      # Generic structure any nonprofit can adapt
│   └── bcef-example.md           # BCEF's real campaigns as a working example
├── keywords/
│   ├── starter-keywords.md       # Keyword examples by nonprofit type
│   └── negative-keywords.md      # Universal negative keyword list
├── ad-copy/
│   └── rsa-templates.md          # Responsive search ad formulas (fill in the blanks)
└── compliance/
    └── checklist.md              # Monthly audit — what to check to keep the grant
```

---

## Who this is for

- Nonprofit marketing staff running Google Ads for the first time
- Freelance marketers or consultants onboarding a nonprofit client
- Anyone who wants to skip the trial-and-error and launch a compliant account on day one

---

## The two things that kill Ad Grant accounts

1. **CTR below 5%** — two consecutive months under 5% = automatic suspension
2. **No conversion tracking** — without it you're stuck at a $2 max CPC bid cap and can't use smart bidding

Set these up right from the start. Everything else is fixable.

---

## Quick start

1. Read `setup/activation-guide.md` — get the grant activated
2. Set up conversion tracking (`setup/conversion-tracking.md`) before building campaigns
3. Use `campaigns/campaign-template.md` to build your first campaign
4. Copy `keywords/negative-keywords.md` and apply it at the account level immediately
5. Run the monthly compliance check in `compliance/checklist.md`

---

## Contributing

PRs welcome. If you've run Ad Grants for a nonprofit and have keyword lists, ad copy, or compliance tips to add — open a PR or file an issue.

---

*Built by Cael Garriott. Not affiliated with Google.*
