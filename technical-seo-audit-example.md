# Technical SEO Audit Example

### Sanitized Example: B2B SaaS Website

This example demonstrates how the **[Technical SEO Audit Framework](technical-seo-audit-framework.md)** can be applied to a real-world website.

All business names, URLs, metrics and identifiers in this example have been anonymized or modified.

The purpose is to demonstrate:

- How findings are structured
- How issues are prioritized
- How technical SEO recommendations are written
- How implementation can be validated
- How technical findings connect to business impact

---

## 1. Audit Context

| Field | Details |
|---|---|
| Business Type | B2B SaaS |
| Website Size | ~2,500 indexable URLs |
| Primary Market | English-speaking markets |
| Primary Objective | Increase qualified organic demo requests |
| Website Platform | JavaScript-based SaaS marketing site |
| Audit Scope | Technical SEO, indexation, architecture, rendering and performance |
| Audit Type | Full technical SEO audit |

---

## 2. Executive Summary

The website had a generally healthy technical foundation, but several structural issues were reducing crawl efficiency and weakening visibility for important commercial pages.

The most important findings were:

1. **Duplicate URL patterns were being crawled and indexed**
2. **Several high-value feature pages were weakly linked internally**
3. **Canonical tags were inconsistent across filtered URLs**
4. **JavaScript rendering delayed access to some important internal links**
5. **XML sitemaps included non-canonical URLs**
6. **Core Web Vitals were weak on product and feature templates**
7. **Structured data coverage was inconsistent**

The recommended priority was:

**Indexation Control → Internal Linking → Canonical Cleanup → Rendering → Performance → Structured Data**

---

## 3. Technical SEO Health Score

| Area | Score |
|---|---:|
| Crawlability | 8/10 |
| Indexability | 6/10 |
| Canonicalization | 6/10 |
| Site Architecture | 7/10 |
| Internal Linking | 5/10 |
| JavaScript / Rendering | 6/10 |
| Performance | 5/10 |
| Structured Data | 6/10 |
| XML Sitemaps | 6/10 |
| Monitoring | 7/10 |

### Overall Technical SEO Score

**62 / 100**

> This score is an internal audit framework for prioritization. It is not a search-engine ranking score.

---

# 4. Critical Findings

## Finding 1 — Duplicate Parameter URLs Were Indexable

### Priority

🔴 Critical

### Issue

The website generated multiple indexable parameter versions of category and resource pages.

Example pattern:

```text
/resources/
/resources/?sort=latest
/resources/?category=seo
/resources/?category=seo&sort=latest
```

Some parameter URLs:

- Returned HTTP 200
- Were crawlable
- Had self-referencing canonicals
- Appeared in internal links
- Were discovered by search engines

### Risk

This created unnecessary URL duplication and increased crawl activity across low-value variations.

Potential consequences included:

- Crawl inefficiency
- Duplicate indexation
- Diluted internal authority
- Inconsistent canonical selection
- Search-result fragmentation

### Recommendation

Define which parameter combinations should be:

```text
Indexable
Canonicalized
Noindexed
Blocked from internal discovery
```

Recommended approach:

```text
Canonical category page
↓
Useful SEO filter pages
↓
Index only when search demand exists

Low-value parameter combinations
↓
Canonicalize or noindex depending on purpose
```

### Validation

After implementation:

- Re-crawl parameter URLs
- Verify canonical behavior
- Confirm low-value URLs are not internally linked
- Monitor Search Console indexation
- Compare indexed URL count before/after

---

# 5. High-Priority Findings

## Finding 2 — Important Feature Pages Had Weak Internal Linking

### Priority

🟠 High

### Issue

Several commercial feature pages were only linked from deep product navigation.

Example architecture:

```text
Homepage
↓
Product
↓
Solutions
↓
Feature Group
↓
Feature Page
```

Some high-value feature pages had fewer than five internal links.

### Risk

Weak internal linking can reduce:

- Crawl discovery
- Internal authority
- Context
- Page prominence

### Recommendation

Add links from:

- Homepage sections
- Core product pages
- Relevant use-case pages
- Supporting blog content
- Documentation
- Comparison pages

### Example

```text
Core Product Page
      ↓
Feature Page
      ↑
Relevant Guide
      ↑
Use Case Page
```

### Validation

Use a fresh crawl to confirm:

- Internal link count increased
- Crawl depth improved
- Relevant anchor text was used
- No artificial sitewide overlinking was introduced

---

## Finding 3 — Canonical Tags Were Inconsistent

### Priority

🟠 High

### Issue

Some filtered and paginated pages used self-referencing canonical tags, while others pointed to the primary category page.

Example:

```text
/category/?filter=enterprise
```

Sometimes:

```html
<link rel="canonical" href="https://example.com/category/?filter=enterprise">
```

Other times:

```html
<link rel="canonical" href="https://example.com/category/">
```

### Risk

Inconsistent canonical rules can create conflicting signals.

### Recommendation

Define canonical behavior by page type.

Example:

```text
Primary Category
→ Self Canonical

SEO Landing Filter
→ Self Canonical

Low-Value Filter
→ Canonical to Category or Noindex

Pagination
→ Evaluate based on content/discovery requirements
```

### Validation

Test representative URLs from every template.

---

# 6. JavaScript & Rendering Findings

## Finding 4 — Internal Links Loaded Only After Client-Side Interaction

### Priority

🟠 High

### Issue

Some related-content links appeared only after JavaScript execution.

In raw HTML:

```text
No crawlable links present
```

After client-side rendering:

```text
Related links visible
```

### Risk

This increased reliance on rendering for URL discovery.

### Recommendation

Where practical, render important navigation and contextual links in server-delivered HTML.

Prefer:

```html
<a href="/feature/automation/">Automation</a>
```

instead of navigation that exists only after a client-side event.

### Validation

Compare:

```text
Raw HTML
vs
Rendered DOM
```

Confirm important destination URLs appear in accessible link elements.

---

# 7. XML Sitemap Findings

## Finding 5 — Sitemap Included Non-Canonical URLs

### Priority

🟠 High

### Issue

The XML sitemap included:

- Redirecting URLs
- Parameter URLs
- Non-canonical URLs

### Risk

Sitemap signals were inconsistent with canonical signals.

### Recommendation

Include only:

- HTTP 200 URLs
- Canonical URLs
- Indexable URLs
- Business-relevant pages

Exclude:

- Redirects
- 404s
- Noindex URLs
- Parameter duplicates
- Non-canonical URLs

### Validation

Rebuild sitemap and compare:

```text
Submitted URLs
vs
Canonical URLs
vs
Indexable URLs
```

---

# 8. Performance Findings

## Finding 6 — Product Templates Had Weak Core Web Vitals

### Priority

🟡 Medium–High

### Observation

Performance testing showed recurring issues on product and feature templates.

Common problems:

- Large hero images
- Heavy JavaScript bundles
- Third-party scripts
- Delayed interaction readiness
- Layout movement during component loading

### Recommendation

Prioritize template-level improvements rather than optimizing individual URLs.

Focus on:

- Hero image optimization
- Image sizing
- Lazy loading below the fold
- JavaScript reduction
- Third-party script review
- Layout stability
- Server response time

### Validation

Use both:

- Lab testing
- Field data where available

Do not rely on a single Lighthouse run.

---

# 9. Structured Data Findings

## Finding 7 — Schema Coverage Was Inconsistent

### Priority

🟡 Medium

### Issue

Some content templates contained structured data while similar templates did not.

Example:

```text
Blog Article → Article schema
Guide → No Article schema
Feature Page → No structured relationship
Breadcrumbs → Inconsistent
```

### Recommendation

Create template-level structured-data rules.

Potential types:

- Organization
- Article
- BreadcrumbList
- SoftwareApplication
- FAQ where valid and appropriate

### Important

Structured data should reflect visible page content and should not be used to make unsupported claims.

---

# 10. Indexation Findings

## Finding 8 — Low-Value Pages Consumed Index Coverage

### Priority

🟡 Medium

Observed indexable page groups included:

- Tag archives
- Search result pages
- Filter variations
- Old campaign landing pages
- Thin utility pages

### Recommendation

Classify each URL type.

```text
Should Rank?
      ↓
Yes → Index

No
↓
Does it need to exist?
      ↓
Yes → Noindex / Canonical / Crawl Control
No → Remove / 404 / 410
```

Avoid using one rule for every low-value URL.

---

# 11. Site Architecture Findings

## Finding 9 — Commercial Pages Were Too Deep

### Priority

🟡 Medium

Some commercial pages required four or five clicks from major entry points.

### Recommendation

Improve hierarchy:

```text
Homepage
↓
Product
↓
Feature / Use Case
```

rather than:

```text
Homepage
↓
Resources
↓
Category
↓
Subcategory
↓
Feature
```

for commercially important pages.

---

# 12. Technical SEO Priority Matrix

| Finding | Impact | Effort | Priority |
|---|---|---|---|
| Parameter Indexation | High | Medium | Critical |
| Weak Internal Linking | High | Low | High |
| Canonical Inconsistency | High | Medium | High |
| JS-Dependent Links | High | Medium | High |
| Sitemap Quality | Medium | Low | High |
| Core Web Vitals | Medium–High | High | Medium–High |
| Structured Data | Medium | Medium | Medium |
| Low-Value Indexation | Medium | Medium | Medium |
| Crawl Depth | Medium | Low | Medium |

---

# 13. Recommended 90-Day Implementation Plan

## Days 1–30

### Priority: Crawl & Indexation

- [ ] Define parameter URL rules
- [ ] Resolve canonical inconsistencies
- [ ] Clean XML sitemap
- [ ] Identify low-value indexable pages
- [ ] Fix critical crawl/indexation issues

---

## Days 31–60

### Priority: Architecture & Discovery

- [ ] Strengthen internal linking
- [ ] Reduce crawl depth
- [ ] Improve server-rendered links
- [ ] Review important commercial-page architecture
- [ ] Validate implementation with crawler

---

## Days 61–90

### Priority: Performance & Enhancement

- [ ] Improve Core Web Vitals
- [ ] Standardize structured data
- [ ] Monitor Search Console indexation
- [ ] Review crawl patterns
- [ ] Compare commercial-page visibility

---

# 14. Validation Plan

Each technical change should follow:

```text
Issue Identified
      ↓
Recommendation
      ↓
Development
      ↓
Staging Test
      ↓
Production Deployment
      ↓
Re-Crawl
      ↓
Search Console Monitoring
      ↓
Outcome Review
```

Implementation should not be considered complete until validated.

---

# 15. Expected Outcome

The audit does **not** guarantee ranking increases.

The expected technical outcomes are:

- Cleaner crawl paths
- More consistent canonical signals
- Better discovery of commercial pages
- Reduced low-value URL indexation
- Cleaner sitemap signals
- Improved page performance
- Stronger technical consistency

These improvements create a stronger foundation for content, authority and search visibility.

---

# 16. Example Technical Issue Ticket

## Product Pages Have Incorrect Canonicals

**Priority:** High

### Issue

A set of product pages outputs canonical URLs pointing to a parent category.

### Current

```html
<link rel="canonical" href="https://example.com/products/">
```

### Expected

```html
<link rel="canonical" href="https://example.com/products/product-a/">
```

### Impact

The implementation may create conflicting canonical signals for independently valuable product pages.

### Recommendation

Update the product-page template to output the intended canonical URL.

### Validation

- Crawl representative product URLs
- Inspect canonical output
- Verify canonical target returns HTTP 200
- Confirm unrelated templates remain unchanged

### Success Criteria

```text
PASS when all tested product pages output
the intended canonical URL and no unintended
template changes are introduced.
```

For implementation documentation, use the  
**[Technical SEO Issue Template](technical-seo-issue-template.md)**.

---

# 17. What This Example Demonstrates

This example shows that a technical SEO audit should not be:

> A list of crawler errors.

A useful audit should explain:

```text
What is wrong?
↓
Why does it matter?
↓
How important is it?
↓
What should change?
↓
How will the fix be validated?
```

That is the difference between **technical SEO reporting** and **technical SEO implementation planning**.

---

# Related Resources

- [Technical SEO Audit Framework](technical-seo-audit-framework.md)
- [Technical SEO Issue Template](technical-seo-issue-template.md)
- [SEO Audit Worksheet](seo-audit-worksheet.md)
- [SEO Growth Framework](seo-growth-framework.md)
- [SEO Reporting Framework](seo-reporting-framework.md)

---

## About This Example

This is a **sanitized educational example**.

The business name, domain, URL patterns, scores and implementation details have been generalized or modified to protect confidential information.

It should not be interpreted as a published audit of any identifiable company.

---

## About the Repository

This example is part of **[SEO Growth Systems](README.md)**, maintained by **[Prashant Rajput](https://github.com/prashant6788)**, Founder of [Touchstone Infotech](https://www.touchstoneinfotech.com/).

The repository focuses on practical systems for:

**SEO · GEO · AI Search Visibility · Technical SEO · Measurement**

---

## License

This resource is licensed under the repository's **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.

See [LICENSE](LICENSE) for details.
