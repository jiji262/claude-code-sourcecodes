# Claude Code Sourcecodes

Independent research mirror reconstructed from publicly distributed Claude Code artifacts.

[English](./README.md) | [简体中文](./README.zh-CN.md)

> [!IMPORTANT]
> This repository is unofficial. It is not affiliated with, endorsed by, or maintained by Anthropic.
>
> The materials here were derived from publicly distributed artifacts, primarily the public npm package [`@anthropic-ai/claude-code`](https://www.npmjs.com/package/@anthropic-ai/claude-code) (`2.1.88`), its bundled source map (`cli.js.map`), and public community discussion about those artifacts.
>
> No private repository access, leaked credentials, or other non-public source materials were used to assemble this snapshot.

> [!CAUTION]
> Copyright, trademarks, and all other rights remain with their respective owners.
>
> This repository is provided for research, interoperability analysis, education, and archival reference. It should not be treated as an official upstream source or as legal advice that redistribution is permitted in every jurisdiction.
>
> Before using, copying, redistributing, or building on top of these materials, review the applicable laws, license terms, and internal compliance requirements in your own environment.

## What This Repository Is

This repository is a research-oriented reconstruction of the publicly shipped Claude Code package contents. It exists to help readers inspect how the published package was assembled and what source-level information was embedded in its public source map.

It is not a claim that this tree matches Anthropic's internal development repository one-to-one. File boundaries, paths, generated outputs, and build context may differ from the original private source tree.

## Provenance

The current snapshot is grounded in public distribution channels:

- Public npm package: [`@anthropic-ai/claude-code@2.1.88`](https://www.npmjs.com/package/@anthropic-ai/claude-code)
- Public package metadata: [`package/package.json`](./package/package.json)
- Public bundled source map: [`package/cli.js.map`](./package/cli.js.map)
- Extraction helper included in this repo: [`extract-sources.js`](./extract-sources.js)

Verified from the bundled source map in this repository:

- Version: `2.1.88`
- Embedded source entries: `4,756`
- Entries with `sourcesContent`: `4,756`

## Repository Layout

- [`package/`](./package/) contains the unpacked public npm package payload
- [`src/`](./src/) contains the reconstructed source snapshot used for inspection
- [`extract-sources.js`](./extract-sources.js) shows the basic extraction approach from `sourcesContent`
- [`claude-code-2.1.88.tgz`](./claude-code-2.1.88.tgz) preserves the original public tarball snapshot used in this workspace

## Reconstruction Method

At a high level, the reconstruction path is straightforward:

1. Obtain the public npm tarball for the target Claude Code release.
2. Read the bundled `cli.js.map` file included in that public package.
3. Extract files from the source map's `sourcesContent` entries.
4. Write the recovered contents into a readable source tree for analysis.

That means the repository is based on artifacts already distributed through public channels, not on privileged access to a private development system.

## Scope and Non-Goals

This repository is useful for:

- Studying the structure of the public package
- Comparing published versions
- Inspecting bundled source-map contents
- Researching interoperability and packaging behavior

This repository is not intended to:

- Replace the official Claude Code distribution
- Imply any sponsorship, approval, or partnership with Anthropic
- Encourage misuse of trademarks, branding, or copyrighted material
- Guarantee that the reconstructed tree is complete, buildable, or identical to the original internal repository

## Rights and Compliance Notes

- Repository-level rights notice: [`LICENSE.md`](./LICENSE.md)
- The package payload includes [`package/LICENSE.md`](./package/LICENSE.md), which states that the original software is subject to Anthropic's legal agreements.
- Official product, legal, and compliance information should be taken from Anthropic's own properties, not from this mirror.
- If you are a rights holder and believe a specific file or section should be removed or narrowed, contact the repository maintainer through the hosting platform.

Official references:

- [Claude Code product page](https://claude.com/product/claude-code)
- [Claude Code documentation](https://code.claude.com/docs/en/overview)
- [Anthropic legal and compliance](https://code.claude.com/docs/en/legal-and-compliance)

## Practical Reading Notes

If you use this repository, treat it as a public-artifact research snapshot:

- Prefer citing the original public package version when discussing findings
- Double-check behavior against the official distributed binary or docs
- Avoid presenting this tree as official source code
- Keep redistribution and downstream publication decisions within your own legal review process
