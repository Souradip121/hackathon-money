---
title: 5 GitHub URL Hacks
---

# 5 GitHub URL hacks that feel illegal to know 🚨

All five are free and work on **public** repos. The examples use React's repo; swap in any repo you like.

## 1. github.com → deepwiki.com

Change `github.com` to `deepwiki.com` in a repo's URL and you get a full AI-written wiki of the codebase, and you can ask it questions.

- `https://github.com/facebook/react` → [`https://deepwiki.com/facebook/react`](https://deepwiki.com/facebook/react)
- Free for public repos. Great for understanding a library in 10 minutes before you build on it.

## 2. Press T on any repo

Open any repo on GitHub and press **T**. The file finder opens: type part of a file name and it searches every file by name instantly. (Press **?** on GitHub to see all keyboard shortcuts.)

## 3. Download just one folder

Need one folder, not the whole repo? Paste the folder's link into [download-directory.github.io](https://download-directory.github.io).

- Example: `https://github.com/facebook/react/tree/main/fixtures/dom`
- It downloads just that folder as a zip. If you hit GitHub's rate limit, the site lets you add a token.

## 4. star-history.com

Put a repo into [star-history.com](https://www.star-history.com) to see its GitHub stars over time. Compare libraries before you pick one: is it growing, or flattening out?

- Example: [star-history.com/#facebook/react&vuejs/vue&Date](https://www.star-history.com/#facebook/react&vuejs/vue&Date)

## 5. Any file in a public repo → a free CDN link

Use jsDelivr's `/gh/` path:

```
https://cdn.jsdelivr.net/gh/<user>/<repo>@<version>/<path-to-file>
```

- Example: [`https://cdn.jsdelivr.net/gh/facebook/react/README.md`](https://cdn.jsdelivr.net/gh/facebook/react/README.md)
- Drop `github.com` **and** the `/blob/main` part of the file's GitHub URL.
- Add `@<tag-or-branch>` to pin a version; without it you get the latest release or default branch.
- Public repos only; very large repos or files may not be served.

---

Last checked: 27 Oct 2026.

Follow [@souradip.sh](https://www.instagram.com/souradip.sh/) for hackathon tips every day.
