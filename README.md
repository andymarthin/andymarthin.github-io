![Build status](https://travis-ci.org/andymarthin/andymarthin.github.io.svg?branch=master)

![Built With Love](http://forthebadge.com/images/badges/built-with-love.svg)


## Blog Andy Marthin

Blog ini berisi catatan apa yang sedang saya pelajari dan opini


## Notes to self

To update (as explained in the [github docs](https://help.github.com/articles/using-jekyll-with-pages)): `bundle update`

To add a draft post: just drop a markdown file in `_drafts`

Create your new page using:

    $ bundle exec jekyll page "My New Page"

Create your new post using:

    $ bundle exec jekyll post "My New Post"

Create your new draft using:

    $ bundle exec jekyll draft "My new draft"

To preview locally: `jekyll serve --watch --baseurl `

To preview locally, with drafts: `jekyll serve --watch --drafts --baseurl `

Publish your draft using [jekyll compose](https://github.com/jekyll/jekyll-compose):
```sh
$ bundle exec jekyll publish _drafts/my-new-draft.md
# or specify a specific date on which to publish it
$ bundle exec jekyll publish _drafts/my-new-draft.md --date 2014-01-24
```

```shell
bundle exec htmlproofer ./_site --disable-external --assume-extension --allow-hash-href --check-html
```

To publish: commit locally and `git push`
