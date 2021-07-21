# anwens.net

## Add a Post

Create a new markdown file (e.g. "2021-07-19-hello-world.md") under `_posts`
directory. Note that the file name must follow naming convention
"YYYY-MM-DD-whatever-...md"

For Markdown syntax, please see: 

[https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)

This website uses Jekyll Sinai theme. For Sinai document, please see:

[https://aspirethemes.com/docs/sinai-jekyll](https://aspirethemes.com/docs/sinai-jekyll)

## Test Locally

Launch a Jekyll server if it's not already running:

```
bundle exec jekyll serve --livereload
```

Visit `http://localhost:4000` in the browser to see the rendered website.

## Publish

This website is hosted on gitlab, with a CI/CD pipeline set up to automatically
publish whenever there is an update to the main branch. The CI/CD pipeline is
configured by `.gitlab-ci.yml`

To publish the changes, simply commit and push the changes. For a quick guide
to git commands, please see [https://rogerdudler.github.io/git-guide/](https://rogerdudler.github.io/git-guide/)

```
# add any updated/new files
git add [_posts/..., images/...]

# commit the changes
git commit

# push to gitlab
git push
```

It might take a few minutes for the web site to update.

