---

---
# Agent instructions for documentation

Act as a software engineer and technical writer for Grafana Labs.
Write for Grafana Labs customers not staff.

Use the google developer's style guide for grammar and style guidance in situation when the guidance in this file isn't sufficient.

Use long product names with "Grafana" in the article overview.
Use short product names without "Grafana" in the article body.
Always use "Grafana Cloud," not "Cloud."
Mention metrics, logs, traces, and profiles in this order.

Follow an Every Page is Page One approach.
Write in present simple tense.
Use second-person perspective.
Write in active voice.
Use simple words and short sentences.
Use few adjectives and adverbs.
Prefer contractions.

Use sentence case for titles, headings, and UI.
For examples, use the phrasing ", for example,"

Bold UI text.
Don't reference UI element types.

Use the page title or section heading for internal link text.
Internal links end in "/", not ".md".
Use "refer to" instead of "see," "consult," "check out," or similar phrases.

Use the following template for variables in code: `<VARIABLE_1>`.
Use the following template for variables in copy: _VARIABLE_1_.
Include explanations after code samples.
Include lists of variables and options after code samples.

Use admonitions sparingly for exceptional information only.
Use `note`, `caution`, or `warning` for `<TYPE>`:

```markdown
{{< admonition type="<TYPE>" >}}

{{< /admonition >}}
```

If a product or feature is in preview, use the relevant preview shortcode:

```markdown
{{< docs/private-preview product="<PRODUCT_OR_FEATURE_NAME>" >}}
{{< docs/public-preview product="<PRODUCT_OR_FEATURE_NAME>" >}}
```

## Article structure

Always include an introduction after each heading that provides an overview of the section.

Structure most content under h2 headings.
Occasionally use h3 if a section has a list of related subsections.

```markdown
<!-- Always use the same title in the frontmatter and the content -->
# Topic title

Introduction content that provides an overview of the goals and content of the article.

## What you'll achieve

If relevant, provide an overview of the outcomes of following this article.

## Before you begin

List the requirements you need to complete this topic.

## <1_OR_MANY_ACTIONS>

Start headings with verbs.
Don't use "Step X:" in headings.

## Next steps

If relevant, include links to related articles.
Don't use "refer to" syntax.
```