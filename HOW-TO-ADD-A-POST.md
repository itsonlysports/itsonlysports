# How to add a new post

You don't need to install anything. You can do all of this in your web browser.

## The short version

1. Go to the `_posts` folder.
2. Make a new file named like this: **`2026-12-01-my-headline.md`**
   - The date first (year-month-day), then a short name with dashes instead of spaces.
   - It has to end in `.md`.
3. Copy everything from `_templates/new-post.md` into it.
4. Change the headline, sport, tags and summary at the top, then write your post below the second `---` line.
5. Save (on GitHub this button says **Commit changes**). The site updates on its own in a minute or two.

## The part at the top

Every post starts with a small block between two `---` lines. It tells the site about the post:

```
---
layout: post
title: "Why the Lions are for real"
sport: NFL
tags: [lions, detroit]
summary: "One or two sentences that show on the home page."
---
```

| Line | What it does |
|---|---|
| `layout: post` | Leave this alone. |
| `title` | Your headline. Keep the quote marks. |
| `sport` | Which sport section it goes in. Must match a name in the `sports:` list in `_config.yml` (NFL, NBA, MLB, NHL, College, Soccer, Other). |
| `tags` | Optional extra labels, like team or player names, inside square brackets with commas. |
| `summary` | The teaser shown on the home page and in link previews. |
| `dateline` | Optional. A city in capitals, like `MINNEAPOLIS`, shown at the start of the post the way newspapers do. Delete the line if you don't want one. |
| `image` | Optional. The photo for the post's card and the top of the post. Upload it to `assets/images` first, then put its path here. |
| `image_alt` | A few words describing the photo, for people using screen readers. |
| `image_credit` | Who took the photo and its license. Shows under the photo. |
| `series` | Optional. Puts the post in a series: `"The Leverage Play"`, `"Enjoy It Monday"`, `"Receipts"` or `"Previews"`. Spell it exactly like that. |
| `affiliate: true` | Add this if the post has affiliate links. It shows the required disclosure at the top of the post. |
| `featured: true` | Optional. Add this line to show the post as the big "Featured take" on the home page. Only one post should have it. |

## Writing tips

- A blank line starts a new paragraph.
- `## Heading` makes a section heading.
- `**bold**` makes **bold**. (This site doesn't use italics.)
- `> text` makes a short callout, styled like a small heading. Use sparingly.
- `- item` makes a bullet list. `1. item` makes a numbered list.
- `[link text](https://...)` makes a link.
- For a picture, upload it to `assets/images`, then write `![what it shows](/assets/images/file-name.jpg)`.

## Finding photos you're allowed to use

Use photos that are free to reuse, and always fill in `image_credit`:

- **Wikimedia Commons** (commons.wikimedia.org): lots of real game, player and stadium photos. Each photo page shows the license and how to credit it, for example `Photo: Jane Doe / Wikimedia Commons (CC BY-SA 4.0)`.
- **Unsplash** (unsplash.com) and **Pexels** (pexels.com): free stock photos of stadiums, fans and equipment. Credit is optional but polite: `Photo: Jane Doe / Unsplash`.
- **Team and league press photos** and **Getty/AP images are NOT free to use**, even if they're all over the internet. Skip those.

Wide photos work best (about 16:9, at least 1600 pixels wide).

## Updating Receipts

Your results live in one file: `_data/receipts.yml`. For each contest, copy one block, paste it at the top, and change the numbers. The page adds up the totals for you. Delete the three sample rows (`example: true`) once your first real result is in.

## Turning on the newsletter

1. Make a free account at buttondown.com.
2. In `_config.yml`, set `buttondown_username:` to your Buttondown username.
3. That's it. The "Opening soon" button becomes a working Subscribe button everywhere.

## Other things you might want to change

- **Site name, tagline, sports list:** edit `_config.yml`.
- **About page:** edit `about.md`.
- **Hide a post without deleting it:** add `published: false` to its top block. Drafts I write for you start this way. Delete the line to publish.
- **Disclaimers:** the footer and the Disclosures page (`disclosures/index.md`) already cover gambling, affiliate links, league affiliation and AI help.
- **Posts dated in the future** won't show until that date.
