---
title: How Comment-to-DM Works
---

# How that DM reached you 🤖

You commented a word, and a DM arrived a couple of seconds later. Nobody typed it. Here's the whole path.

## The four steps

1. **You comment** a keyword on a reel ("API", "LINK", …).
2. **Instagram sends a webhook.** That's an HTTP request from Instagram to the creator's server. It says: *this account commented this text on this media.* The app has to subscribe to the account's `comments` field for this to happen.
3. **The server checks the word.** If the comment contains a keyword the creator set up for that reel, it's a match. (Good bots also ignore their own replies and check that the comment is on the right reel.)
4. **The server calls Instagram's messaging API** with a *private reply* to that comment. That's the DM in your inbox. A private reply is a one-time DM tied to your comment, and the business can only send it within a set window after the comment.

The round trip is usually about two seconds.

## Build one yourself

| | |
|---|---|
| 📘 Webhooks for Instagram | [developers.facebook.com/docs/instagram-platform/webhooks](https://developers.facebook.com/docs/instagram-platform/webhooks) |
| 💬 Private replies | [developers.facebook.com/docs/instagram-platform/private-replies](https://developers.facebook.com/docs/instagram-platform/private-replies) |
| 🔑 What you need | An Instagram professional account and a Meta app with the Instagram messaging and comments permissions (App Review for public use) |

A minimal server is a single HTTPS endpoint:

```text
GET  /webhook   → answer Meta's verification challenge (hub.challenge)
POST /webhook   → for each comment event:
                    if keyword in comment.text:
                        POST private reply (recipient: comment id, message: your text + link)
```

Watch out for:
- **Verify the signature** (`X-Hub-Signature-256`) so only Meta can call your endpoint.
- **Answer fast** (return 200 straight away) and do the work in the background.
- **Rate limits and the messaging window.** Instagram limits how many messages you can send and when.
- **Don't spam.** One reply per comment, and only to people who asked.

## Don't want to build it?

That's what reeldrop does: you pick the reel and the keyword, write the DM, and add a button. Over 1,000 creators use it.

---

Last checked: 31 Oct 2026. Meta changes API names and limits often, so check their docs before you build.

Follow [@souradip.sh](https://www.instagram.com/souradip.sh/) for hackathon tips every day.
