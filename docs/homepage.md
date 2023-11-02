# Editing the Homepage

The files that control how the frontpage looks are in the folder `/content/homepage/`.

## Parts of the Homepage
The homepage is divided into three parts:
- The "jumbotron" which is the wide, top part of the homepage with the gray background. The contents of this part of the site is in `/content/homepage/jumbotron.md`.
- "Interest one" and "interest two", which are the two columns below the "Research Interests" heading. Interest one is on the left and two is on the right. The contents of these columns are `/content/homepage/interest_one.md` and `/content/homepage/interest_two.md`.

### `jumbotron.md`
The `title` page variable is the bolded headline of the jumbotron. The markdown contents of this file is responsible for the rest of the contents of the jumbotron.

### `interest_one.md` & `interest_two.md`
The `title` page variables are the names of the interests (these are the headlines that are navy and orange in colour). The `collaborators` page variable is a list of collaborators. This is a [TOML](https://toml.io/en/) list, but you can just use the same syntax as a python list of strings. `personnel` similarly lists lab members that work on this "interest". The rest of the file describes the interest.
