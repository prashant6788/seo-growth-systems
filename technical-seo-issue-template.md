# 🔧 Technical SEO Issue Template

### From SEO Finding → Developer Action → Validation

Use this template to document technical SEO issues in a way that makes them clear, actionable and verifiable.

It can be used for:

**GitHub Issues · Jira · ClickUp · Asana · Linear · Trello · Internal SEO Audits**

The objective is simple:

> A technical SEO recommendation should explain the problem, its impact, the required action and how the fix will be validated.

---

# 📋 Issue Information

| Field | Details |
|---|---|
| Website | |
| Issue Title | |
| Date Identified | |
| Identified By | |
| Environment | Production / Staging |
| Priority | Critical / High / Medium / Low |
| Status | Open / In Progress / Ready for Validation / Closed |
| Assigned To | |
| Target Date | |

---

# 1. Issue Summary

### What is the problem?

```text
Describe the issue clearly in 1–3 sentences.
```

### Example

```text
A group of important product pages contains canonical tags
pointing to different URLs.

This may prevent the intended product URLs from being treated
as the preferred canonical versions.
```

---

# 2. Affected URLs

### Example URLs

```text
https://example.com/page-1
https://example.com/page-2
https://example.com/page-3
```

### Estimated Scale

```text
Number of affected URLs:
```

### URL Pattern

```text
Example:

/products/*
/category/*
/locations/*
```

If the issue affects a large number of URLs, provide representative examples rather than listing thousands of URLs directly in the issue.

---

# 3. Issue Category

Select the most relevant category.

- [ ] Crawling
- [ ] Indexation
- [ ] Robots.txt
- [ ] XML Sitemap
- [ ] Canonicalization
- [ ] Redirects
- [ ] HTTP Status Codes
- [ ] Site Architecture
- [ ] Internal Linking
- [ ] JavaScript SEO
- [ ] Core Web Vitals / Performance
- [ ] Structured Data
- [ ] Mobile
- [ ] International SEO
- [ ] Pagination
- [ ] Duplicate Content
- [ ] Migration
- [ ] HTTPS / Security
- [ ] Other

---

# 4. Evidence

Document how the issue was identified.

### Evidence Source

- [ ] Google Search Console
- [ ] Crawl
- [ ] Browser Inspection
- [ ] Server Logs
- [ ] Page Source
- [ ] Lighthouse / PageSpeed
- [ ] Structured Data Validator
- [ ] Analytics
- [ ] Manual Testing
- [ ] Other

### Evidence

```text
Add the relevant observation, screenshot reference,
crawl data, response header, HTML example or other evidence.
```

---

# 5. Current Behavior

Explain what happens currently.

```text
Example:

The page:

https://example.com/product-a

currently contains:

<link rel="canonical" href="https://example.com/category-a/">

The product URL is intended to be independently indexable.
```

---

# 6. Expected Behavior

Explain what should happen after implementation.

```text
Example:

The product page should contain a self-referencing canonical:

<link rel="canonical" href="https://example.com/product-a">
```

Avoid vague instructions such as:

```text
Fix canonical tags.
```

The expected result should be clear enough for implementation and QA.

---

# 7. SEO Impact

### Potential Impact

- [ ] Crawling
- [ ] Indexation
- [ ] Search visibility
- [ ] Internal authority flow
- [ ] Duplicate URL handling
- [ ] Structured data eligibility
- [ ] User experience
- [ ] Page performance
- [ ] Conversion
- [ ] Reporting / measurement

### Explanation

```text
Explain why this issue matters.

Avoid claiming traffic or ranking improvements that cannot
reasonably be predicted.
```

---

# 8. Priority

## 🔴 Critical

Use when the issue can severely prevent important sections of the website from being crawled, indexed or accessed correctly.

Examples:

- Production site accidentally blocked
- Important sections set to noindex
- Major migration failure
- Critical redirect failure
- Important pages returning server errors

---

## 🟠 High

Significant issue affecting important pages or templates.

Examples:

- Incorrect canonicals at scale
- Major internal-linking problems
- Important structured data implementation errors
- Significant performance problems
- Large indexation inconsistencies

---

## 🟡 Medium

Meaningful optimization that should be addressed but is not immediately blocking core search functionality.

---

## 🟢 Low

Minor optimization, cleanup or technical refinement.

---

# 9. Recommended Solution

### Recommended Action

```text
Describe the recommended implementation.

Be specific about:

• what should change
• where it should change
• which URLs/templates are affected
• what should remain unchanged
```

---

# 10. Implementation Notes

### Developer Notes

```text
Add implementation details here.
```

### Important Constraints

```text
Example:

Do not apply this rule to filtered category URLs.

Do not change existing redirects.

Test on staging before production deployment.
```

---

# 11. Example Implementation

Where useful, provide a simplified example.

### Before

```html
<link rel="canonical" href="https://example.com/category/">
```

### After

```html
<link rel="canonical" href="https://example.com/product/">
```

> Examples should demonstrate the expected outcome. They should not be treated as production-ready code without reviewing the website's actual implementation.

---

# 12. Dependencies

Does implementation depend on another team or task?

- [ ] Developer
- [ ] CMS
- [ ] DevOps
- [ ] Content Team
- [ ] Analytics
- [ ] Design
- [ ] Hosting
- [ ] Third-Party Platform
- [ ] No Dependency

### Dependency Notes

```text

```

---

# 13. Risk Assessment

### Implementation Risk

```text
Low / Medium / High
```

### What could go wrong?

```text

```

### Rollback Required?

```text
Yes / No
```

### Rollback Approach

```text

```

---

# 14. Testing Before Deployment

Before releasing the change:

- [ ] Test on staging where available
- [ ] Test representative URLs
- [ ] Confirm intended HTML/output
- [ ] Check HTTP responses
- [ ] Check crawlability
- [ ] Check indexability
- [ ] Check canonical behavior
- [ ] Check internal links
- [ ] Validate structured data where relevant
- [ ] Test mobile behavior
- [ ] Check for unintended template-wide changes

---

# 15. Post-Deployment Validation

Implementation is not complete until the outcome is validated.

### Validation Checklist

- [ ] Production deployment confirmed
- [ ] Representative URLs checked
- [ ] Source HTML verified
- [ ] HTTP status verified
- [ ] Crawl test completed
- [ ] Indexability checked
- [ ] Canonical checked
- [ ] Structured data validated where relevant
- [ ] Internal links checked
- [ ] No unexpected side effects identified

---

# 16. Search Console Validation

Where relevant:

- [ ] URL Inspection reviewed
- [ ] Sitemap status reviewed
- [ ] Indexing report reviewed
- [ ] Core Web Vitals reviewed
- [ ] Enhancement reports reviewed

### Observation

```text

```

> Search Console data may take time to reflect technical changes. Deployment validation and search-engine processing should be treated as separate stages.

---

# 17. Validation Evidence

### Before Fix

```text
Observation:
```

### After Fix

```text
Observation:
```

### Validated By

```text

```

### Validation Date

```text

```

---

# 18. Success Criteria

Define success **before implementation**.

Example:

```text
PASS when:

1. All tested product pages contain the intended canonical.
2. Canonicals return HTTP 200.
3. No unintended category pages are affected.
4. A fresh crawl confirms the expected implementation.
```

### Success Criteria

- [ ]  
- [ ]  
- [ ]  
- [ ]  

---

# 19. Final Status

```text
[ ] Open

[ ] In Progress

[ ] Ready for Validation

[ ] Validation Failed

[ ] Closed
```

### Final Notes

```text

```

---

# ⚡ Quick Version

For smaller issues, use this shortened format:

```text
TITLE:

PRIORITY:
Critical / High / Medium / Low

ISSUE:
What is wrong?

AFFECTED URLS:
Which pages/templates are affected?

EVIDENCE:
How was the problem identified?

SEO IMPACT:
Why does it matter?

RECOMMENDED FIX:
What needs to change?

EXPECTED RESULT:
What should happen after implementation?

VALIDATION:
How will we confirm the fix worked?
```

---

# 🧪 Example Technical SEO Issue

## Incorrect Canonical on Product Pages

**Priority:** High

### Issue

A group of independently indexable product pages contains canonical tags pointing to their parent category.

### Example

```text
Page:
https://example.com/products/product-a

Current canonical:
https://example.com/category-a/

Expected canonical:
https://example.com/products/product-a
```

### Potential Impact

The implementation may send conflicting canonicalization signals and make it harder for search engines to determine the intended preferred URL.

### Recommended Action

Update the product-page template so independently indexable product pages output the intended canonical URL.

### Validation

After deployment:

1. Crawl representative product URLs.
2. Verify canonical tags in rendered/source HTML as appropriate.
3. Confirm canonical destinations return HTTP 200.
4. Confirm category templates were not unintentionally changed.
5. Monitor relevant Search Console signals over time.

### Success

```text
PASS when all tested product pages output
the intended canonical without introducing
unexpected changes elsewhere.
```

---

# 🔗 Related Resources

- [Technical SEO Audit Framework](technical-seo-audit-framework.md)
- [SEO Audit Worksheet](seo-audit-worksheet.md)
- [SEO Growth Framework](seo-growth-framework.md)
- [SEO Reporting Framework](seo-reporting-framework.md)
- [Monthly SEO Reporting Template](monthly-seo-reporting-template.md)

---

## About

This template is part of **[SEO Growth Systems](README.md)**, an open knowledge repository maintained by **[Prashant Rajput](https://github.com/prashant6788)**, Founder of [Touchstone Infotech](https://www.touchstoneinfotech.com/).

The repository focuses on practical systems for **SEO, GEO, AI Search Visibility and search-to-revenue measurement**.

---

## License

This resource is licensed under the repository's **Creative Commons Attribution 4.0 International (CC BY 4.0) License**.

See [LICENSE](LICENSE) for details.
