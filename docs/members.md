# Editing the Members Page

All information shown on the members page is present in the folder `/content/members`. Each member is represented by a single markdown file.

## Order of Members 
Lab members are displayed according to the following algorithm.

- All postdoctoral fellows are shown first, sorted by the `name.last` variable in an alphabetical descending manner.

- All doctoral students are shown first, sorted by the `name.last` variable in an alphabetical descending manner.

- All masters students are shown first, sorted by the `name.last` variable in an alphabetical descending manner.

## Member Files

### Filenames
The convention for naming the files is `{SURNAME_NAME}_{GIVEN_NAME}.md`, but it isn't required. Names which don't conform to the western given/surname conventions can be written in whatever way is most practical. There is one exception to this, which is the `pi.md` file, which is Prof. Emad's file. This file is handled differently, and must not change its filename.

### Page Variables
Much of what you see on the members page is determined by the [page variables](https://gohugo.io/variables/page/) in each member's file. The markdown text after the [frontmatter](https://gohugo.io/content-management/front-matter/) is a blurb describing yourself. Alumni do not have blurbs visible.

The [page variables](https://gohugo.io/variables/page/) are, by convention, defined using [TOML](https://toml.io/en/).

|Variable|Description|Example|
|--------|-----------|-------|
|`title` |Member's full name. Western names should be written in the Given Middle Last name format.|`"Albert Einstein"`|
|`headless`|Must always be `true`.|`true`|
|`role`|Value must be `"current_student"` for current members of the lab and `"alumnus"` for alumni. Values other than these will result in unexpected behaviour.|`"current_student"`|
|`degree`|Value must be `"msc"` for Master's students, `"phd"` for Doctoral students, and `"pdf"` for Postdoctoral Fellows.|`"pdf"`|
|`email`|The value must be an email from which you would like to receive public professional correspondence, prepended with `"{{< email >}}` and appended with `{{</ email >}}"`. The `{{< email >}}` obfuscates your email and should help prevent spam.|`"{{< email >}}emc2@example.com{{</ email >}}"`|
|`avatar`|A path to an image file of you. The image should be 305 pixels wide and 150 pixels tall (or have the same aspect ratio). This variable is optional and can be omitted from the file if you haven't a photo. The files should be placed in the `/imgs/members/` folder. |`"/imgs/members/albert.jpg"`|
|`name.first`|The fragment of your name that you would like to appear first. For western names, this is your Given name.|`"Albert"`|
|`name.middle`|The fragment of your name that you would like to appear between the first and last fragments. For western names, this is your middle name. This variable is optional and can be omitted from the file in the event of not having a middle name.||
|`name.last`|The fragment of your name that you would like to appear after the first and middle fragments. For western names, this is your Surname name.|`"Einstein"`|
|`links.website`|The HTTP address to your personal website. This variable is optional and can be omitted from the file if it does not apply to you.|`"https://example.com/~einstein"`|
|`links.orcid`|A link to your [ORCID](https://orcid.org/) profile. This variable is optional and can be omitted from the file if it does not apply to you.|`"https://orcid.org/0000-0003-2125-060X"`|
|`links.linkedin`|A link to your [LinkedIn](https://www.linkedin.com/) profile. This variable is optional and can be omitted from the file if it does not apply to you.|`"https://linkedin.com/company/albert-einstein-institution"`|
|`links.twitter`|A link to your [Twitter](http://twitter.com) profile. This variable is optional and can be omitted from the file if it does not apply to you.|`"https://twitter.com/AlbertEinstein"`|
|`links.mastodon`|A link to your [Mastodon](https://joinmastodon.org/) profile. This variable is optional and can be omitted from the file if it does not apply to you.|`"https://mastodon.social/@Gargron"`|

## Example

Below is an example of file for Albert Einstein.

```
+++
title = 'Albert Einstein'
headless = true
role = "current_student"
degree = "pdf"
email = "{{< email >}}emc2@example.com{{</ email >}}"
avatar = "/imgs/members/albert.jpg"
[name]
    first = "Albert"
    last = "Einstein"
[links]
    website = "https://example.com/~einstein"
    orcid = "https://orcid.org/0000-0003-2125-060X"
    linkedin = "https://linkedin.com/company/albert-einstein-institution"
    twitter = "https://twitter.com/AlbertEinstein"
+++

Former patent-clerk trying to make inroads in the computation biology field. Main interest is in biophysical senescence and the phenomena of "black cells" which are hyper-dense cells which consume all macromolecules which approach its event horizon.
```