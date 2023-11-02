# Website Configuration

This repository uses [Hugo](https://gohugo.io/) to build the website. There are a few configurable settings that you can read about on the [official Hugo documentation](https://gohugo.io/getting-started/configuration/).

There are, however a couple of custom settings that I will outline here.

The website configuration file is defined using [TOML](https://toml.io/en/).

## Custom Settings
The template I wrote for this website has some custom features specific to the COMBINE lab website. Here's how to use them.

|Parameter|Description|Example|
|---------|-----------|-------|
|`params.recruiting`|This displays a banner at the top of the front page that announces that the lab is currently recruiting students, and links to the URL you define. A good idea is to create a post in the news section, and link to it. You can comment this line out when not recruiting.|`'/news/recruiting/'`|
|`params.password`|This setting prompts the visitor for a password upon viewing pages. Without the correct password, the page will appear blank. This is just to allow the website to be private when prototyping. **NOTE**: the prompt is easily by-passed and the contents of the website **should never be presumed to be private**. You can comment this line out when not needed.|`'test123'`|
