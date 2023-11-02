# Editing the Software Page

All information shown on the Software page is present in the folder `/content/software`. Each programme is represented by a single markdown file.

## Software Files

### Filenames
The convention for naming the files is to use the name of the programme in lowercase letters, replacing spaces iwth underscores (`_`).

### Page Variables
Much of what you see on the software page is determined by the [page variables](https://gohugo.io/variables/page/) in each member's file. The markdown text after the [frontmatter](https://gohugo.io/content-management/front-matter/) is one or two sentences describing the programme.

|Variable|Description|Example|
|--------|-----------|-------|
|`title`|Name of the software.|`"RAPPPID"`|
|`links.github`|Link to the GitHub repository, if one exists.|`"https://github.com/jszym/rapppid"`|
|`links.paper`|Link to the publication to which the programme belongs, if one exists. Best to use DOI links.|`"https://doi.org/10.1093/bioinformatics/btac429"`|
|`links.data`|Link to the relevant data repository, if one exists. Best to use links to data repositories like [Zenodo](https://zenodo.org).|`"https://zenodo.org/record/6709790"`|

### Example
```
+++
title = 'RAPPPID'

[links]
    github = "https://github.com/jszym/rapppid"
    paper = "https://academic.oup.com/bioinformatics/article-abstract/38/16/3958/6623405"
    data = "https://zenodo.org/record/6709790"
+++

**R**egularised **A**utomatic **P**rediction of **P**rotein-**P**rotein **I**nteractions using **D**eep Learning 
```
