# Contributor Runway

This guide defines how first-time contributors can land meaningful changes
quickly in `public-process`.

## Fast Start

### Content Map

- `_posts/` is the complete dated essay corpus.
- `essays/` is the curated long-form essay collection.
- Root Markdown files such as `index.md` and `about.md` are site pages.
- `data/` contains generated indexes and should not be edited by hand unless an
  issue explicitly asks for it.

### First Steps

1. Pick a scoped issue labeled `good first issue`, `documentation`, or
   `research`.
2. For local preview, install dependencies and run Jekyll:

   ```bash
   git clone https://github.com/YOUR_USERNAME/public-process.git
   cd public-process
   bundle install
   bundle exec jekyll serve
   ```

3. Before opening a PR, run the check that matches the change:

   - Docs-only change: preview the Markdown and self-review links.
   - Essay, layout, include, or config change:

     ```bash
     bundle exec jekyll build --strict_front_matter --future
     ```

## First Contribution Scope

A first contribution should:

- Touch a small, isolated surface area.
- Have clear acceptance criteria.
- Be testable with existing workflows.
- Avoid cross-repo architectural refactors.
- Avoid new organvm vocabulary unless it is defined in the same change.

## Review SLA Targets

- First maintainer response: within 3 business days.
- Review turnaround after requested changes: within 3 business days.
- Merge decision after final approval: within 2 business days.

## Required PR Evidence

- What changed and why.
- Validation output summary, or a note that the change was docs-only.
- Linked issue with acceptance criteria.

## Escalation

If blocked for more than 7 days without review, comment on the PR with the
current blocker and the smallest maintainer action needed.
