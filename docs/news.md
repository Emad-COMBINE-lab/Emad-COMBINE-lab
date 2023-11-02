# News

News posts should announce things like new manuscripts, members, awards, and talks.

Each post has its own file in the `/contents/news/` folder.

## News Post Files

### Filenames
It's a good idea to name the posts according to the scheme `{YYYY}{MM}{DD}_{SLUG}` where `{SLUG}` is a one or two word description of the news article, in all lower case, with spaces replaced with underscores (`_`).

### Page Variables
There are a couple of standard [page variables](https://gohugo.io/variables/page/) to change.

|Variable|Description|Example|
|--------|-----------|-------|
|`title`|The title of the post. This will appear in the headline.|`"COMBINE goes to ISMB '23"`|
|`date`|The date that this post is published. In YYYY-MM-DD format.|`"2023-07-02"`|
|`description`|A short description of the post. This is shown on the page that lists all news items, and give people an idea of what the post entails.|`"Read about the three talk we gave at the Intelligent Systems for Molecular Biology conference!"`|