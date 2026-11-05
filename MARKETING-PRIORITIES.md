# AI Data Plane marketing priorities

November 5, 2026

Start with three projects: a reliable first tutorial, a practical search comparison, and a memory example with a clear reason to use it. These priorities follow the [audit findings](full-audit/FINDINGS.md); the suggested owners still need team agreement.

| Priority | Work to produce | Who it helps | Suggested owner |
|---|---|---|---|
| 1 | Repair Catalog and Python examples; replace mislabeled Hyperscale lookups with actual nearest-neighbor queries. Run the examples before filming. | Developers trying the product | Docs and SDK maintainers |
| 2 | A start-to-finish guide: choose components, set up keys, run a query, inspect the answer and clean up. Show required and optional services and who pays for each. | New evaluators | Technical Marketing and DevRel |
| 3 | Keyword, vector and hybrid search on the same data. Explain index choices and show mandatory filters working in each retrieval path. | Search developers | Search DevRel and integration maintainers |
| 4 | A support assistant that retrieves current orders and searches policy documents. Show how a changed record affects its answer. | Application developers and architects | DevRel and Solutions Engineering |
| 5 | A memory decision guide and demo: later recall, changed preferences, temporary exceptions and deletion. Compare with a saved profile. | Agent developers | Memory PM and DevRel |
| 6 | A repeatable memory cost study, including a workload where memory adds little value. Report quality, latency and all costs. | Architects and buyers | Performance Engineering and Memory PM |
| 7 | An SDK guide showing versions, index support, filter syntax, credentials and support contacts. Include separate MCP and app environments where needed. | Developers and platform teams | SDK and integration maintainers |
| 8 | A troubleshooting demo connecting tool versions, permissions and traces. Include a denied request and failed log write. | Platform and security reviewers | MCP/Catalog maintainers and Technical Marketing |
| 9 | Operating guides for source changes, credential renewal, model configuration and cache errors. Show recovery and its costs. | Teams preparing deployment | AI Services PM and DevRel |
| 10 | Consistent article templates, review checks and maintenance ownership. Link each video to its tested guide and code revision. | Content contributors | Technical Marketing and Docs tooling |

Start item 10 alongside item 1. The order reflects setup blockers and dependencies, not a measured revenue ranking.

## What counts as finished

For every package, a developer unfamiliar with the example should be able to follow the guide, obtain the expected result, inspect a failure case and clean up. Record the versions and results. The video should use the same code, not a separate demonstration that readers cannot reproduce.

For benchmarks, publish the dataset, configuration, raw results and costs. Keep token reduction separate from total savings. Our managed-memory cost and quality tests remain unrun.

## How the priorities map to the audit

1: G01, G31–32, G35. 2: G07, G17, G26, G36. 3: G02, G15–16, G33–34. 4: G30. 5: G09, G11, G35. 6: G08–09. 7: G33–37, G39. 8: G10, G38, G41. 9: G06, G24–25, G27, G42. 10: G12–13, G45.

[Summary](full-audit/README.md) · [Articles and videos](full-audit/CONTENT-REVIEW.md) · [Benchmark plan](full-audit/PROOF-PLAN.md) · [Content templates](content-system/README.md)
