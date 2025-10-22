# AdMesh Platforms Documentation Update

## Summary

Successfully updated the AdMesh Mintlify documentation for platforms to reflect correct integration terminology and structure.

---

## Changes Made

### 1. Renamed "Inline Recommendations" to "Weave Ad Format"

**File Created**: `admesh-mintlify-docs/platforms/weave-ad-format.mdx`

- ✅ Updated title from "Inline Recommendations" to "Weave Ad Format"
- ✅ Updated description to: "How to weave AdMesh recommendations naturally into your AI or LLM responses"
- ✅ Changed all prompt instructions from "=== INLINE RECOMMENDATIONS ===" to "=== WEAVE RECOMMENDATIONS ==="
- ✅ Updated instruction text from "Weave these naturally" to "Integrate these naturally"
- ✅ Maintained all `[Ad]` label requirements and formatting guidelines
- ✅ Kept all code examples (TypeScript, React, Kotlin, Dart, Swift, React Native)
- ✅ Preserved all transparency requirements and tracking instructions

### 2. Created "Choose Your Integration" Guide

**File Created**: `admesh-mintlify-docs/platforms/choose-integration.mdx`

- ✅ Comparison table between Weave Ad Format and Citation & Product Format
- ✅ Quick decision guide for choosing the right format
- ✅ Example scenarios for different platform types
- ✅ Flow diagram showing both integration paths
- ✅ Recommendation summary with links to both formats

### 3. Created "Citation & Product Format" Guide

**File Created**: `admesh-mintlify-docs/platforms/citation-format.mdx`

- ✅ Complete SDK integration guide
- ✅ 3-step integration instructions
- ✅ Supported formats (Citation, Product Cards, Ecommerce)
- ✅ Customization options (theme, event handlers)
- ✅ Automatic tracking explanation
- ✅ Best practices and troubleshooting

### 4. Updated Platform Overview

**File Modified**: `admesh-mintlify-docs/platforms/overview.mdx`

- ✅ Added "Choose Your Integration" section with format comparison
- ✅ Updated integration flow table with 6 steps (added "Choose Format")
- ✅ Added separate flow diagrams for both formats
- ✅ Updated links to new documentation pages
- ✅ Improved clarity and structure

### 5. Updated Navigation Configuration

**File Modified**: `admesh-mintlify-docs/docs.json`

- ✅ Added "choose-integration" to "For Platforms" group
- ✅ Renamed "inline-recommendations" to "weave-ad-format"
- ✅ Added "citation-format" to navigation
- ✅ Updated page order for logical flow:
  1. overview
  2. choose-integration
  3. create-session
  4. get-recommendations
  5. weave-ad-format
  6. citation-format
  7. fire-exposure-pixel
  8. close-session

---

## Documentation Structure

### For Platforms Navigation

```
📁 For Platforms
├── 📄 Overview
│   └── Platform overview with integration flow table
├── 📄 Choosing Your Integration
│   └── Comparison between Weave Ad Format and Citation & Product Format
├── 📄 Create Session
│   └── Session creation guide
├── 📄 Get Recommendations
│   └── Recommendations fetching guide
├── 📄 Weave Ad Format
│   └── Weave integration guide (renamed from inline-recommendations)
├── 📄 Citation & Product Format
│   └── Citation & Product Format SDK guide
├── 📄 Fire Exposure Pixel
│   └── Exposure tracking guide
└── 📄 Close Session
    └── Session closure guide
```

---

## Terminology Updates

### Before
- "Inline Recommendations" → Now "Weave Ad Format"
- "=== INLINE RECOMMENDATIONS ===" → Now "=== WEAVE RECOMMENDATIONS ==="
- "Weave these naturally" → Now "Integrate these naturally"

### After
- ✅ Consistent use of "Weave Ad Format" for API-based custom rendering
- ✅ Consistent use of "Citation & Product Format" for SDK-based automatic rendering
- ✅ Clear distinction between the two integration approaches

---

## Maintained Consistency

✅ All code examples preserved exactly as provided  
✅ All `[Ad]` label requirements intact  
✅ All transparency guidelines maintained  
✅ All tracking instructions preserved  
✅ All formatting guidelines kept  
✅ All best practices documented  

---

## Key Features

### Weave Ad Format
- API-based integration
- Full control over UI and placement
- Perfect for LLM-based conversational ads
- Manual pixel firing
- Custom rendering

### Citation & Product Format
- SDK-based integration
- Automatic rendering
- Built-in tracking
- Transparency labels auto-included
- Multiple format support (citation, product cards, ecommerce)

---

## Navigation Flow

Users can now:

1. **Start at Overview** - Understand platform integration options
2. **Choose Integration** - Decide between Weave or Citation & Product Format
3. **Create Session** - Initialize a new session
4. **Get Recommendations** - Fetch ads for a query
5. **Integrate** - Use either Weave or Citation & Product Format
6. **Track** - Fire exposure pixels
7. **Close** - End the session

---

## Files Created

1. ✅ `admesh-mintlify-docs/platforms/weave-ad-format.mdx` (300 lines)
2. ✅ `admesh-mintlify-docs/platforms/choose-integration.mdx` (150 lines)
3. ✅ `admesh-mintlify-docs/platforms/citation-format.mdx` (200 lines)

## Files Modified

1. ✅ `admesh-mintlify-docs/platforms/overview.mdx` - Updated structure and flow
2. ✅ `admesh-mintlify-docs/docs.json` - Updated navigation

## Files Preserved

- ✅ `admesh-mintlify-docs/platforms/create-session.mdx` - No changes
- ✅ `admesh-mintlify-docs/platforms/get-recommendations.mdx` - No changes
- ✅ `admesh-mintlify-docs/platforms/fire-exposure-pixel.mdx` - No changes
- ✅ `admesh-mintlify-docs/platforms/close-session.mdx` - No changes

---

## Status

✅ **COMPLETE**

All documentation has been updated with:
- Correct terminology (Weave Ad Format, Citation & Product Format)
- Complete integration guides for both formats
- Clear comparison and decision framework
- Updated navigation structure
- Maintained consistency across all files

---

## Next Steps

1. Review the updated documentation
2. Test navigation flow in Mintlify
3. Verify all links work correctly
4. Update any external references to "inline-recommendations"
5. Deploy updated documentation

---

**Date**: 2025-10-21  
**Status**: Complete  
**Files Created**: 3  
**Files Modified**: 2  
**Files Preserved**: 4

