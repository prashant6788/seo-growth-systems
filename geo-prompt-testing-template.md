# 🤖 GEO / AI Search Prompt Testing Template

### A Practical Framework for Measuring Brand Visibility Across AI-Powered Discovery

Use this template to systematically test how a **brand, company, product, service or entity** appears across AI-powered search and answer systems.

This template is designed to help measure:

- Brand mentions
- Recommendation visibility
- Citation visibility
- Entity understanding
- Competitor visibility
- Factual accuracy
- Source patterns
- Prompt sensitivity
- Visibility changes over time

> AI-generated responses can vary by platform, model, location, personalization, retrieval behavior and time. Treat results as observations rather than fixed rankings.

---

# 📋 Test Information

| Field | Details |
|---|---|
| Brand / Entity | |
| Website | |
| Industry | |
| Primary Market | |
| Test Date | |
| Tester | |
| Primary Competitors | |
| Previous Test Date | |

---

# 1. Define the Testing Objective

Before running prompts, define what you want to measure.

### Primary Objective

```text
Example:

Measure whether the brand appears when users ask AI systems
for recommended providers within our service category.
```

### Business Topics

1.  
2.  
3.  
4.  
5.  

### Primary Competitors

1.  
2.  
3.  
4.  
5.  

---

# 2. Platforms to Test

Test the platforms relevant to your audience.

| Platform | Tested? | Date | Notes |
|---|---|---|---|
| ChatGPT | ⬜ | | |
| Google AI-powered search experiences | ⬜ | | |
| Gemini | ⬜ | | |
| Perplexity | ⬜ | | |
| Microsoft Copilot | ⬜ | | |
| Other | ⬜ | | |

Do not assume results from one AI system represent visibility across all systems.

---

# 3. Prompt Categories

A useful test set should contain different types of discovery prompts.

---

## Category A — Direct Brand Prompts

These test whether the AI system understands the brand/entity.

Examples:

```text
What does [Brand] do?

What services does [Brand] provide?

Who is [Brand]?

Is [Brand] a [business category]?

What is [Brand] known for?
```

### Results

| Prompt | Platform | Accurate? | Sources / Citations | Notes |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# 4. Category B — Category Discovery

These simulate users searching for providers without mentioning your brand.

Examples:

```text
What are some companies that provide [service]?

Who provides [service] in [location]?

What are good options for [service]?

Which companies specialize in [category]?

Who can help a business with [problem]?
```

### Results

| Prompt | Platform | Brand Mentioned? | Position / Context | Competitors Mentioned |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# 5. Category C — Recommendation Prompts

These test whether the brand appears when the user asks for recommendations.

Examples:

```text
Recommend companies for [service].

What are some reputable [service] providers?

Which [category] companies should I consider?

What are the best options for [problem]?

Recommend a company that can help with [specific requirement].
```

### Results

| Prompt | Platform | Brand Recommended? | Why? | Competitors |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

> A recommendation in one response does not establish a stable AI ranking.

---

# 6. Category D — Problem / Solution Prompts

These often represent high-value discovery behavior.

Examples:

```text
How can I solve [business problem]?

What type of company can help with [problem]?

How should a business implement [solution]?

What tools or services help with [problem]?

Who can help automate [workflow]?
```

### Results

| Prompt | Platform | Brand Visible? | Relevant? | Notes |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# 7. Category E — Comparison Prompts

Examples:

```text
[Brand] vs [Competitor]

Compare [Brand] and [Competitor].

What are alternatives to [Competitor]?

Which is better for [use case]: [Brand] or [Competitor]?
```

### Results

| Prompt | Platform | Brand Included? | Accurate? | Competitive Position |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# 8. Category F — Location-Based Prompts

Use these when geography affects the buying decision.

Examples:

```text
Best [service] companies in [city]

[service] provider near [location]

Who provides [service] in [country]?

Recommended [business category] in [city]
```

### Results

| Prompt | Platform | Brand Visible? | Location Accurate? | Competitors |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# 9. Category G — Expertise / Informational Prompts

These evaluate whether the brand's content or expertise becomes visible around important topics.

Examples:

```text
How does [topic] work?

What is the best approach to [topic]?

How should companies implement [topic]?

What should I consider when choosing [solution]?
```

### Results

| Prompt | Platform | Brand Mentioned? | Content Referenced? | Citation? |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |

---

# 10. Citation Analysis

When the platform displays sources, record them.

| Prompt | Platform | Brand Cited? | Your URL Cited? | Other Sources Cited |
|---|---|---|---|---|
| | | | | |
| | | | | |
| | | | | |
| | | | | |

### Frequently Cited Domains

| Domain | Citation Frequency | Type | Opportunity |
|---|---:|---|---|
| | | | |
| | | | |
| | | | |

This can help identify which sources appear to influence or support answers within the tested environment.

It should **not** be interpreted as proof that a particular domain is a universal LLM ranking factor.

---

# 11. Competitor Visibility

| Competitor | Mentions | Recommendations | Citations | Topics Associated |
|---|---:|---:|---:|---|
| | | | | |
| | | | | |
| | | | | |
| | | | | |

### Questions to Investigate

```text
Which competitors appear more frequently?

Which topics are competitors associated with?

Which external sources mention those competitors?

Do competitors have stronger entity clarity?

Do competitors publish more citation-worthy resources?

Are competitors mentioned by authoritative third-party sources?
```

---

# 12. Entity Accuracy

AI visibility has limited value if the information presented is inaccurate.

Check:

| Entity Attribute | Correct? | AI Response | Correct Information |
|---|---|---|---|
| Brand Name | ⬜ | | |
| Website | ⬜ | | |
| Business Category | ⬜ | | |
| Services | ⬜ | | |
| Location | ⬜ | | |
| Founder / Leadership | ⬜ | | |
| Products | ⬜ | | |
| Target Market | ⬜ | | |

### Accuracy Issues

1.  
2.  
3.  

---

# 13. Prompt Variation Testing

Small wording changes can produce different responses.

Test variations of the same underlying intent.

### Example

```text
Prompt 1:
Best SEO agencies for SaaS companies

Prompt 2:
Recommend SEO companies specializing in SaaS

Prompt 3:
Which agencies help SaaS companies grow organic traffic?

Prompt 4:
Who provides SaaS SEO services?

Prompt 5:
What companies specialize in SaaS organic growth?
```

### Variation Results

| Variation | Brand Visible? | Competitors | Citation | Observation |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |

This helps distinguish a repeatable visibility pattern from a single-response observation.

---

# 14. Core Prompt Set

Maintain a consistent group of prompts for repeated testing.

| ID | Prompt | Intent | Importance |
|---|---|---|---|
| P01 | | Brand | High |
| P02 | | Category | High |
| P03 | | Recommendation | High |
| P04 | | Problem / Solution | High |
| P05 | | Comparison | Medium |
| P06 | | Location | Medium |
| P07 | | Informational | Medium |
| P08 | | | |
| P09 | | | |
| P10 | | | |

Use the same core prompts during future measurement periods where practical.

---

# 15. Visibility Measurement

A simple internal scoring model can help compare tests over time.

### Suggested Observation Score

| Result | Score |
|---|---:|
| Not mentioned | 0 |
| Mentioned | 1 |
| Positively/relevantly included | 2 |
| Recommended | 3 |

Citation can be tracked separately.

### Example

```text
Total visibility points earned
÷
Maximum possible visibility points
×
100
```

### AI Visibility Observation Score

```text
________ / 100
```

> This is an internal benchmarking metric only. It is not an official score from any AI platform and should not be presented as an AI ranking score.

---

# 16. Citation Rate

```text
Prompts where the brand/site was cited
÷
Prompts where citations were available
×
100
```

### Citation Rate

```text
________ %
```

Track this separately from brand mentions and recommendations.

---

# 17. Recommendation Rate

```text
Prompts where the brand was recommended
÷
Relevant recommendation prompts tested
×
100
```

### Recommendation Rate

```text
________ %
```

---

# 18. Competitive Share of Mentions

For a defined test set:

```text
Brand mentions
÷
Total mentions across tracked brands
×
100
```

### Observed Share of Mentions

```text
________ %
```

This metric applies only to the defined prompt set and testing conditions.

---

# 19. Findings

## Strong Visibility

1.  
2.  
3.  

## Visibility Gaps

1.  
2.  
3.  

## Accuracy Problems

1.  
2.  
3.  

## Citation Opportunities

1.  
2.  
3.  

## Competitive Gaps

1.  
2.  
3.  

---

# 20. Recommended Actions

| Finding | Recommended Action | Priority | Owner |
|---|---|---|---|
| | | 🔴 High | |
| | | 🟠 Medium | |
| | | 🟢 Low | |
| | | | |
| | | | |

Potential actions may include:

- Improve entity clarity
- Strengthen service/product descriptions
- Improve factual consistency
- Create stronger topic resources
- Add original data or examples
- Improve structured information
- Strengthen relevant third-party authority
- Improve internal linking
- Update outdated information
- Build citation-worthy resources

---

# 21. Testing History

Repeated testing is more useful than treating one response as definitive.

| Test Date | Prompts Tested | Visibility Score | Citation Rate | Recommendation Rate |
|---|---:|---:|---:|---:|
| | | | | |
| | | | | |
| | | | | |
| | | | | |

---

# 22. Final Assessment

### Entity Understanding

```text
Strong / Moderate / Weak
```

### Category Visibility

```text
Strong / Moderate / Weak
```

### Recommendation Visibility

```text
Strong / Moderate / Weak
```

### Citation Visibility

```text
Strong / Moderate / Weak
```

### Competitive Visibility

```text
Strong / Moderate / Weak
```

### Information Accuracy

```text
Strong / Moderate / Weak
```

---

# ⚠️ Methodology Notes

AI-search testing has important limitations.

Results may change based on:

- Platform
- Model/version
- Retrieval availability
- Search integration
- Geography
- Language
- Prompt wording
- Conversation context
- Personalization
- Time
- Source availability

For stronger testing:

**Use multiple prompts → test multiple platforms → repeat over time → record citations → compare competitors → document conditions.**

Avoid claiming that a single test proves a stable ranking or universal AI-search behavior.

---

# 🔗 Related Resources

- [GEO / LLM Visibility Framework](geo-llm-visibility-framework.md)
- [AI Search Visibility Checklist](ai-search-visibility-checklist.md)
- [SEO Growth Framework](seo-growth-framework.md)
- [SEO Audit Worksheet](seo-audit-worksheet.md)
- [SEO Reporting Framework](seo-reporting-framework.md)

---

## About

This template is part of **[SEO Growth Systems](README.md)**, an open knowledge repository maintained by **[Prashant Rajput](https://github.com/prashant6788)**, Founder of [Touchstone Infotech](https://www.touchstoneinfotech.com/).

The repository explores practical approaches to **SEO, GEO, AI Search Visibility and search-to-revenue measurement**.

---

## License

This resource is licensed under the repository's **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.

See [LICENSE](LICENSE) for details.
