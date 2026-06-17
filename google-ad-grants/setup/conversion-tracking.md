# Conversion Tracking Setup

Don't skip this. Without conversion tracking:
- You're capped at a $2 max CPC bid (ads rarely win competitive auctions)
- You can't use smart bidding (Maximize Conversions, Target CPA)
- You risk a "no valid conversions" compliance flag
- You have no idea if your ads are actually working

The conversion to track is a **program inquiry** — a contact form submission, a signup button click, or an "apply" page visit.

---

## Option A: GA4 → Google Ads (Recommended)

This is the cleanest path. Set up GA4 on your site first, then import conversions into Google Ads. You only need to add one tag to your site and it handles everything.

### Step 1 — Create a GA4 property

1. Go to [analytics.google.com](https://analytics.google.com)
2. Create a new property for your nonprofit's website
3. Go through the setup wizard — choose "Web" as the platform
4. Get your **Measurement ID** (format: G-XXXXXXXXXX)

### Step 2 — Add the GA4 tag to your site

Paste this immediately after the `<head>` tag on every page (or in your site's global head section):

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

Replace `G-XXXXXXXXXX` with your actual Measurement ID.

**For Base44 sites:** Add this to the `<head>` section of index.html via the Code tab.

### Step 3 — Define a conversion event in GA4

1. In GA4 → Admin → Events, find or create a `form_submit` event (GA4 tracks this automatically for most forms)
2. Mark it as a conversion: toggle the "Mark as conversion" switch

### Step 4 — Link GA4 to Google Ads

1. In Google Ads → Tools → Linked accounts → Google Analytics
2. Link your GA4 property
3. Import the conversion events from GA4 into Google Ads

### Step 5 — Enable smart bidding

Once conversions are flowing (give it 1–2 weeks of data):
- Switch campaign bidding from Maximize Clicks to **Maximize Conversions**
- This lifts the $2 CPC cap and lets Google optimize for actual inquiries

---

## Option B: Google Ads native conversion tracking

If you can't set up GA4, you can create conversion actions directly in Google Ads:

1. Google Ads → Goals → Conversions → New conversion action → Website
2. Choose "Submit lead form" or "Page visit" (for a thank-you page after form submit)
3. Get the tag snippet and add it to your site
4. For a thank-you page conversion: set the conversion page URL as the trigger

This works but is less flexible than GA4 for long-term analytics.

---

## Verifying it works

After adding the tag, use the **Google Tag Assistant** Chrome extension to confirm the tag is firing correctly. Allow 24–48 hours for conversion data to start appearing in Google Ads.
