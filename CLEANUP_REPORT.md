# Cleanup Report

## Result

The original archive was 1,135,158,945 bytes. The cleaned source contains about 280 MB of files before ZIP compression.

## Removed from the deliverable

- `.git/`: local repository history and packed objects
- `_site/`: generated website output that duplicated source assets
- `.sass-cache/` and `.jekyll-cache/`: local build caches
- Template demo posts, drafts, talks, teaching pages, archive pages, sample comments, and publication generators
- Docker files and unused talk-map utilities
- Unused sample PDFs and slides
- 37 unreferenced images and document assets
- Unused portfolio/software detail pages and commented placeholder cards
- Disabled comment, analytics, feed, archive, pagination, gist, and emoji configuration

## Corrected while cleaning

- Removed local links to missing publication thumbnails
- Removed placeholder Fiber and `your-project` links
- Removed missing `paper.pdf` and placeholder repository buttons from the Bspline project page
- Removed the obsolete footer link to the deleted HTML sitemap page

## Validation

- Jekyll production build completed successfully
- 18 generated HTML pages were checked
- No missing local `href` or `src` references remained

The original archive was not modified.
