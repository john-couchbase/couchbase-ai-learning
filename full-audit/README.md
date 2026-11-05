# AI Data Plane: findings and marketing priorities

Prepared for John Kupchanko and marketing leadership · November 5, 2026

Couchbase has useful documentation and demos across the AI Data Plane. The immediate work is to fix several starting examples, help developers choose the components they need, and make the performance claims easier to check.

The review contains **45 findings**. Some are reproduced example or package problems. Others are recommendations for content, documented limitations, or questions for engineering. The [findings register](FINDINGS.md) records those differences, along with evidence and suggested owners.

## Start with these three projects

**1. Make the first tutorial work.** Developers should be able to follow a short path from setup to a verified result. We found Catalog examples that disagree with package 1.1.5, two Python snippets that fail syntax checks, and nine SDK guides whose Hyperscale examples show a record lookup rather than a nearest-neighbor query. Fix and run those examples before recording them. Add a short guide explaining which services, keys and billing accounts each path needs. See G01, G07, G31, G32 and G35.

**2. Show how to choose and test search.** Use the same dataset and questions to compare keyword, vector and hybrid retrieval. Include exact identifiers, semantic questions and mandatory country or customer restrictions. An offline LangChain test showed that passing a Search-style filter to the Query adapter can leave the filter out of the generated SQL. The guide needs to show the correct syntax for each adapter and a failing case, not just a successful search. See G02, G15, G16, G33 and G34.

**3. Explain when memory earns its cost.** The Memory setup and developer guides already exist. Build on them with a support or personalization example that compares memory with recent conversation history and a saved profile. Show what happens when a person changes a preference or deletes it. Then measure answer quality and the full cost, including extraction and infrastructure. We have not tested the managed service, so we cannot yet recommend it on the strength of our own savings results. See G08, G09, G11 and G35.

Each project should produce a written guide, runnable code and a short video of that exact code revision. The [ten priorities](../MARKETING-PRIORITIES.md) cover the follow-on work, audiences and proposed owners.

## What the tests tell us

The earlier database labs demonstrated indexed queries, transactions, lexical search, vector retrieval and trace storage. They also exposed useful limits: an expensive query timed out, some vector settings lost recall, and trace recording did not automatically remove synthetic sensitive values.

Those results give us concrete demos to build. They do not establish production throughput, managed-memory savings or reliable autonomous tool selection. The [capability review](CAPABILITIES.md) separates live results from documentation and offline checks.

## Reuse the material we already have

Link the Memory quickstarts to the new decision guide. Extend the Ragas evaluation tutorial for search comparisons. Connect the Tracer and Tools/Prompts Hub guides to a demonstration of a changed tool and its recorded activity. Keep useful architecture videos and customer stories, with current setup links and clear recording dates.

The [content review](CONTENT-REVIEW.md) names the articles and video groups reviewed. Proposed additions are gaps in the reviewed learning path; we have not established that no equivalent asset exists elsewhere.

## Decisions for the team

- Choose owners for the first tutorial, search comparison and memory example.
- Ask Docs and SDK maintainers to confirm and repair the reproduced issues.
- Agree on a costed memory experiment before making new savings claims.
- Require each article, demo and video to name its owner, tested version and review date. Start this now, alongside the first tutorial repairs.

## Audit scope and confidence

The review covers the core AI Data Plane journey plus operational data, search, framework integrations, Operational Insights and edge boundaries. It combines the November 3–4 native labs with a November 5 documentation, package and content audit.

- Inventoried **all 71 unique pages linked by the official AI Data Plane documentation index**; each returned HTTP 200. Inventory and heading checks are broader than detailed line-by-line review.
- Compared **ten operational SDK entry points**. Nine vector guides were readable in Markdown; Kotlin was checked through HTML after the Markdown request failed. No claim of executing all language SDKs.
- Inspected metadata and Python interfaces from **seven versioned distributions**; imported LangChain separately; ran a dependency resolver and **ten offline adapter/Memory validation cases**. Spies replaced database/HTTP calls.
- Refreshed **12 selected video descriptions/metadata records**, alongside the earlier 30 visible channel cards. Videos were not watched end to end; this is a topic, freshness and navigation review, not a production-quality score.
- Reviewed selected technical articles, repositories, benchmark publications, customer evidence and prior lab reports. This is not a census of every company webpage or private enablement asset.

**Not established:** live managed-memory usefulness/cost; complete Catalog publishing; hosted-model generation/tool-selection accuracy; managed MCP deployment; cache/guardrail effectiveness; workflow recovery; all-language runtime parity; production failover or scale. This is a marketing and developer-experience audit, not a security certification or proof of production readiness.

No paid model call, cluster resume or paid deployment was made for this audit. The $30 cumulative cap remains in force; the historical invoice total and ongoing retained-resource charges have not been reconciled. See [method and evidence](METHOD.md).

[Findings and evidence](FINDINGS.md) · [SDK coverage](CAPABILITIES.md) · [Articles and videos](CONTENT-REVIEW.md) · [Benchmark plan](PROOF-PLAN.md) · [Review checks](EDITORIAL-REVIEW.md)
