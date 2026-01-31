# Mintlify Starter Kit

Use the starter kit to get your docs deployed and ready to customize.

Click the green **Use this template** button at the top of this repo to copy the Mintlify starter kit. The starter kit contains examples with

- Guide pages
- Navigation
- Customizations
- API reference pages
- Use of popular components

**[Follow the full quickstart guide](https://starter.mintlify.com/quickstart)**

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Install our GitHub app from your [dashboard](https://dashboard.mintlify.com/settings/organization/github-app) to propagate changes from your repo to your deployment. Changes are deployed to production automatically after pushing to the default branch.

## Choosing an AdMesh integration path

AdMesh supports two distinct integration styles depending on how your platform renders sponsored content. Most customers only need the standard SDK integration, while the Weave tooling remains optional for advanced, custom LLM pipelines.

### Weave Ad Format (custom LLM integration)
- Use **`admesh-weave-node`** only when you operate your own LLM stack and must embed AdMesh links directly into AI-generated responses.
- The weave-node package runs server-side, calls the AIP server for recommendations, and formats the results as inline links so the LLM can stitch them into the final answer.
- Because it plugs into your LLM response pipeline, you must manage the streaming lifecycle and embedding logic manually.

### Tail/Product Format (standard integration)
- For the standard tail or product recommendation layouts, integrate straight with the AIP server through the **`admesh-ui-sdk`** (this SDK is required for all integrations).
- The UI SDK already handles platform requests, auction parsing, CPX → CPC → CPA tracking, and rendering of creatives or fallback recommendations—no weave-node service is necessary.
- See the `admesh-ui-sdk` codebase for concrete examples of the direct AIP communication patterns and how the SDK encapsulates them.

## Need help?

### Troubleshooting

- If your dev environment isn't running: Run `mint update` to ensure you have the most recent version of the CLI.
- If a page loads as a 404: Make sure you are running in a folder with a valid `docs.json`.

### Resources
- [Mintlify documentation](https://mintlify.com/docs)
- [Mintlify community](https://mintlify.com/community)
