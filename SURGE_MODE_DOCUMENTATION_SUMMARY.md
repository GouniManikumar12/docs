# Surge Mode Documentation Update Summary

## Overview

Successfully added comprehensive documentation for AdMesh's Surge Mode feature to the Mintlify documentation. Surge Mode is an automatic optimization feature that keeps offers visible when budget runs low by adjusting pricing and temporarily disabling CPA tracking.

---

## What is Surge Mode?

**Trigger:** When remaining budget is greater than $0 but less than the CPA amount

**Activation:** Automatic, no configuration needed

**Key Changes:**
- CPX and CPC rates increase 3x
- CPA tracking is disabled
- Partial billing charges only available budget
- Offers continue to be shown instead of pausing

---

## Files Created

### 1. `admesh-mintlify-docs/advertisers/surge-mode.mdx` (188 lines)

**Purpose:** Comprehensive guide to understanding and managing Surge Mode

**Content Sections:**
- What is Surge Mode and trigger conditions
- How Surge Mode works with pricing adjustments
- Detailed example scenario showing activation
- When Surge Mode activates (automatic process)
- Impact on campaigns (what changes, what stays the same)
- Managing Surge Mode (prevention and response strategies)
- Billing during Surge Mode (partial billing explanation)
- FAQ with 5 common questions
- Related resources with links to related docs

**Key Features:**
- Clear pricing comparison table (Normal vs Surge Mode rates)
- Real-world example with budget progression
- Practical prevention strategies
- Partial billing examples
- Links to related documentation

---

## Files Updated

### 1. `admesh-mintlify-docs/docs.json`

**Change:** Added surge-mode page to navigation

**Location:** Campaign Management section under "For Advertisers"

**Before:**
```json
"pages": [
  "advertisers/create-offer",
  "advertisers/pricing",
  "advertisers/budgets-pacing",
  "advertisers/conversion-tracking"
]
```

**After:**
```json
"pages": [
  "advertisers/create-offer",
  "advertisers/pricing",
  "advertisers/budgets-pacing",
  "advertisers/surge-mode",
  "advertisers/conversion-tracking"
]
```

---

### 2. `admesh-mintlify-docs/advertisers/budgets-pacing.mdx`

**Change:** Added section explaining Surge Mode behavior

**New Section:** "What Happens When Budget Runs Low"

**Content:**
- Explains automatic Surge Mode activation
- Describes 3x rate multiplier
- Notes CPA tracking is disabled
- Links to full Surge Mode documentation

---

### 3. `admesh-mintlify-docs/advertisers/pricing.mdx`

**Change:** Added Surge Mode pricing section

**New Section:** "Surge Mode Pricing"

**Content:**
- Explains when Surge Mode activates
- Lists pricing changes (3x multiplier, CPA disabled)
- Describes continued delivery benefit
- Explains partial billing
- Links to full Surge Mode documentation

---

### 4. `admesh-mintlify-docs/faq/advertiser-faq.mdx`

**Change:** Added Surge Mode FAQ item

**New Accordion:** "What is Surge Mode?"

**Content:**
- Explains automatic activation
- Lists key behaviors in Surge Mode
- Describes how to avoid Surge Mode
- Links to full documentation

**Location:** Budget & Pacing section, after "What happens when I reach my budget limit?"

---

## Documentation Standards Applied

✅ **No emdashes** - All punctuation uses commas, periods, or regular hyphens
✅ **No duplicate headers** - Frontmatter title is the only header
✅ **Professional design** - Minimal, clean formatting with clear hierarchy
✅ **Concise explanations** - Clear, direct language without unnecessary verbosity
✅ **Proper linking** - Cross-references to related documentation
✅ **Consistent formatting** - Matches existing documentation style

---

## Key Information Documented

### Trigger Condition
- Remaining budget > $0 AND < CPA amount
- Automatic detection during recommendation generation

### Pricing Changes
- CPX: 3x multiplier (e.g., $0.002 → $0.006)
- CPC: 3x multiplier (e.g., $0.50 → $1.50)
- CPA: Disabled (set to $0)

### Billing Behavior
- Partial billing charges only available budget
- All transactions tracked with surge_mode flag
- Full audit trail in dashboard

### User Impact
- Offers continue to be shown
- Higher cost per engagement
- No conversion tracking
- Budget still respected

### Prevention Strategies
- Monitor remaining budget
- Increase budget before threshold
- Use even pacing
- Set daily limits

---

## Backend Implementation Reference

Documentation is based on implementation in:
- `admesh-protocol/api/routes/agent_recommendation.py` (lines 1476-1528)
- `admesh-protocol/api/utils/billing_finalization.py` (surge mode partial billing logic)
- `admesh-protocol/docs/COMPREHENSIVE_ATTRIBUTION_BUDGET_RESERVATION.md`

---

## Testing the Documentation

To verify the documentation locally:

```bash
cd admesh-mintlify-docs
npm install -g mint
mint dev
```

Then navigate to:
- `/advertisers/surge-mode` - Main documentation
- `/advertisers/budgets-pacing` - Updated with Surge Mode reference
- `/advertisers/pricing` - Updated with Surge Mode section
- `/faq/advertiser-faq` - Updated with Surge Mode FAQ

---

## Deployment

To deploy these changes:

```bash
cd admesh-mintlify-docs
mint deploy
```

Documentation will be live at: https://docs.useadmesh.com/advertisers/surge-mode

---

## Next Steps

1. Review documentation for accuracy
2. Test all links and cross-references
3. Deploy to production
4. Monitor for user feedback
5. Update as needed based on user questions

---

## Summary

The Surge Mode documentation is now comprehensive, accessible, and integrated throughout the advertiser documentation. Users can:
- Understand what Surge Mode is and when it activates
- See how pricing changes during Surge Mode
- Learn strategies to prevent or manage Surge Mode
- Find answers to common questions
- Access related documentation for context

