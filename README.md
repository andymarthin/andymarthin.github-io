## Blog Andy Marthin

Blog ini berisi catatan apa yang sedang saya pelajari dan opini


## Notes to self

To update (as explained in the [github docs](https://help.github.com/articles/using-jekyll-with-pages)): `bundle update`

To add a draft post: just drop a markdown file in `_drafts`

To preview locally: `jekyll serve --watch --baseurl `

To preview locally, with drafts: `jekyll serve --watch --drafts --baseurl `

Publish your draft using [jekyll compose](https://github.com/jekyll/jekyll-compose):
```sh
$ bundle exec jekyll publish _drafts/my-new-draft.md
# or specify a specific date on which to publish it
$ bundle exec jekyll publish _drafts/my-new-draft.md --date 2014-01-24
```

To publish: commit locally and `git push`
