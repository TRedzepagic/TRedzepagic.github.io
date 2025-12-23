# Blog Notes

Quick lookup for working on this Hugo site.

## Run locally (hot reload)

```
hugo server
```

Drafts are hidden by default. To preview drafts:

```
hugo server -D
```

## New posts

Create a new post under `content/posts/`:

```
hugo new posts/my-post.md
```

The new file starts with `draft = true`. Change it to `false` when ready to publish.

## New pages

Create a standalone page (for example `about.md`) under `content/`:

```
hugo new about.md
```

Add a menu entry in `hugo.toml` if you want it in the nav.

## Images

Option A: Static images
- Place images in `static/images/`.
- Reference them with `/images/filename.jpg`.

Markdown example:
```
![Alt text](/images/filename.jpg)
```

Option B: Page bundle (recommended for post-specific images)
- Create a folder: `content/posts/my-post/`
- Put `index.md` and your images in the same folder.

Markdown example:
```
![Alt text](image.jpg)
```

Theme image shortcode (optional):
```
{{< image src="image.jpg" alt="Alt text" position="center" >}}
```

## Videos

YouTube shortcode:
```
{{< youtube dQw4w9WgXcQ >}}
```

## Build

```
hugo --minify
```
