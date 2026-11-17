# SFEDI Business Support Standards

The SFEDI Business Support Standards as open data, for use in your own apps, learning platforms, CRMs and mapping tools.

The Standards set out what business advisers, mentors and other business support professionals need to do and know. They are set by SFEDI, the standards setting body for business support, and evolved from the national standards SFEDI wrote between 2007 and 2010.

Read the Standards on the SFEDI website: https://www.sfedi.co.uk/standards

This is version 1.9 (November 2026).

## Files

| File | What it is |
|---|---|
| `sfedi-business-support-standards.json` | The full Standards as structured data |
| `sfedi-business-support-standards.schema.json` | A JSON Schema for the data |
| `SFEDI_Business_Support_Standards.md` | The Standards as a readable document. The JSON is generated from it |
| `CHANGELOG.md` | What changed in each version |
| `CITATION.cff` | How to cite the Standards |
| `LICENSE` | The licence (CC BY-ND 4.0) |

## What's in the data

- `about`: the name, publisher, licence and the credit line to use
- `framework`: the version, date, description and introductory sections
- `standards`: 44 Standards in four groups: Core (C1 to C8), Specialist (S1 to S27), Business Information (I1 to I4) and Introduction to Business Support (E1 to E5). Each has a code, title, summary, who it's for, what it evolved from, and its performance requirements ("What you need to show") and knowledge requirements ("What you need to know and understand")
- `behaviours`: the professional behaviours, B1 to B11
- `lineage`: how each unit of the earlier national standards maps to the current Standards
- `whatsNew`: what changed in this edition

There are 455 performance requirements and 418 knowledge requirements in this version.

## Codes are permanent

Every Standard and requirement has a code, for example C1, S3.4 or S3.K2. Codes are never renumbered or reused, with one exception before this repo existed, when version 1.6 renumbered the remaining C4 and C6 requirements once (see the CHANGELOG). So a mapping to S3.4 will always point at the same requirement. New requirements get the next number. The few codes withdrawn so far are listed in the CHANGELOG and will never be used again.

## Links to the SFEDI website

Every Standard, requirement and behaviour has a `url` that links to it on the SFEDI website. A requirement links to its place on its Standard's page, for example https://www.sfedi.co.uk/standards/s3-ai-and-digital-adoption#s3-4. Please link to these pages when you show the Standards in your app, so people can read them in full.

## Using the data

```js
const data = await fetch('https://raw.githubusercontent.com/SFEDI-Group/sfedi-business-support-standards/main/sfedi-business-support-standards.json').then((r) => r.json())

const requirements = data.standards.flatMap((s) => [...s.performanceRequirements, ...s.knowledgeRequirements])
const requirement = requirements.find((r) => r.code === 'S3.4')

console.log(requirement.text, requirement.url)
```

## Licence

The SFEDI Business Support Standards are © Small Firms Enterprise Development Initiative Limited and licensed under the Creative Commons Attribution-NoDerivatives 4.0 International licence (CC BY-ND 4.0): https://creativecommons.org/licenses/by-nd/4.0/

You can copy and share them for any purpose, including commercially, as long as you credit SFEDI. You can show all or part of them in your own app or website, in any format. You can quote them word for word, but you may not publish altered versions.

How to credit the Standards:

SFEDI Business Support Standards, version 1.9 (November 2026), © Small Firms Enterprise Development Initiative Limited, licensed under CC BY-ND 4.0.

The licence covers the Standards, not the SFEDI name or logo. SFEDI is a registered trade mark. Using the Standards does not mean SFEDI recognises you, your organisation or your programme. SFEDI recognises professionals through qualifications and Specialist Certification, and providers' programmes as SFEDI Specialist Programmes. Find out more at https://www.sfedi.co.uk

## Versions

Each version of the Standards is a tagged release of this repo. The latest version is always on the main branch and on the SFEDI website. Earlier versions stay available as releases.

## Using the Standards in your product

If you use the Standards in an app, a platform or a tool, we'd like to hear about it. Email the Business Support Team at support@sfedi.co.uk. You don't need to tell us, or ask, to use the data.

## Questions

SFEDI doesn't take pull requests to the Standards. For questions about the Standards or the data, email the Business Support Team at support@sfedi.co.uk.
