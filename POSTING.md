# How to write & publish a post

A quick reference for the folder layout and workflow on this blog.

## Folder layout

```
_drafts/                            # work-in-progress posts (no date prefix)
  my-next-post.md
_posts/                             # published posts (must have date prefix)
  YYYY-MM-DD-my-post.md
assets/img/posts/                   # one folder per post for its images
  YYYY-MM-DD-my-post/
    cover.jpg
    diagram.png
```

Convention: the image folder name matches the post's filename (without the `.md`).
That way every post and its images stay paired and easy to find.

## 1. Start a draft

Create a markdown file under `_drafts/` (no date prefix needed):

```text
_drafts/my-next-post.md
```

Use this front-matter template:

```yaml
---
title: A short, punchy title
description: One-sentence summary used for SEO and the post listing
author: twoshedzz
categories: [Blogging]            # one primary category, optionally [Parent, Child]
tags: [tag-one, tag-two]          # any number, lowercase preferred
pin: false                         # true to pin to home page
math: false
mermaid: false
image:
  path: /assets/img/posts/my-next-post/cover.jpg
  alt: Description of the cover image for accessibility
---

Your post content goes here. Use `## Heading` for sections — Chirpy auto-builds the TOC.
```

Drop any images for the post into a matching folder:

```text
assets/img/posts/my-next-post/cover.jpg
```

Reference inline images in the body with the same path:

```markdown
![Alt text](/assets/img/posts/my-next-post/diagram.png)
```

## 2. Preview locally

```bash
bundle exec jekyll serve --drafts --livereload
```

Open <http://127.0.0.1:4000>. The `--drafts` flag includes anything in `_drafts/`
and treats its file modification time as the post date for previewing.

## 3. Publish

When you're happy with the draft:

1. Rename the file with today's date prefix and move it to `_posts/`:

   ```bash
   mv _drafts/my-next-post.md _posts/2026-05-10-my-next-post.md
   ```

2. Rename the image folder to match (so the pair stays in sync):

   ```bash
   mv assets/img/posts/my-next-post assets/img/posts/2026-05-10-my-next-post
   ```

3. Update the `image.path:` in the front matter to the new folder path.
4. Add a `date:` field if you want a specific publish time, e.g.
   `date: 2026-05-10 09:00:00 +0100`. Otherwise Jekyll uses midnight of the date
   in the filename.
5. Commit & push — GitHub Pages will build and deploy automatically.

```bash
git add _posts/2026-05-10-my-next-post.md assets/img/posts/2026-05-10-my-next-post
git commit -m "Add post: my next post"
git push
```

## Tips

- Permalinks come from the post **title** (slugified) per `_config.yml`, e.g.
  `/posts/my-next-post/`. The filename is just for sorting/dating.
- Keep cover images reasonably sized (Chirpy will display them full width).
  The existing `coastal-reflection.jpg` is ~640 KB, which is a good upper bound.
- For wide screenshots, a 16:9 or 3:2 cover image looks best in the post card.
- Use `pin: true` sparingly — only one or two posts pinned at a time keeps the
  home page tidy.
