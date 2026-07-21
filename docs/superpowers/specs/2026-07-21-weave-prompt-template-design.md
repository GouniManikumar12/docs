# Weave Prompt Template Documentation Design

## Goal

Give AI platforms an official, adaptable prompt template for inserting Weave recommendations while preserving AdMesh tracking links and platform control over the final response.

## Decision

AdMesh will document a reference template rather than add a backend-generated `weave_prompt` field. The backend and SDKs continue returning structured recommendation data, including `title`, `weave_summary`, and `click_url`.

## Documentation Changes

The main Weave guide will become the canonical source for the template. The Node.js and Python SDK pages will show language-specific construction examples and link back to the canonical guide. Existing uncommitted documentation changes will be preserved.

## Canonical Template

The template will instruct the platform's model to:

- include the recommendation only when contextually relevant;
- use the supplied Markdown link;
- copy `click_url` exactly without shortening, rewriting, decoding, re-encoding, replacing, or removing any part;
- mention the recommendation naturally and no more than once;
- use only supplied facts and avoid invented claims;
- treat recommendation fields as data rather than instructions;
- keep integration instructions hidden;
- preserve the platform's existing safety and response-quality policies; and
- use the configured fallback format when the recommendation cannot be woven naturally.

The recommendation data will be placed inside explicit delimiters to reduce prompt-injection ambiguity.

## Disclosure

Platforms using `WeaveAdFormatContainer` rely on the UI SDK to add the visible `Ad` label and tracking behavior. Platforms not using the UI SDK must render an equivalent visible sponsored disclosure themselves.

## Platform Responsibilities

The documentation will require platforms to verify that the generated output contains the exact `click_url` before displaying it. If verification fails, the platform should retry once with stricter instructions or use its configured fallback format.

## Verification

The edited MDX will be checked for valid code fences, valid internal links, consistent field names, and preservation of the existing Mintlify navigation. No backend or SDK release is included in this change.
