# Re:VIEW Scaffold

Scaffold Boilerplate for [Re:VIEW](https://github.com/kmuto/review) and [docker-review](https://github.com/vvakame/docker-review).

## Requirements

- docker

## Setup

```
$ git clone git@github.com:kokuyouwind/review-scaffold.git
$ git remote rm origin
$ git remote add origin (your-repo-url)
```

option: You can use [CircleCI](https://circleci.com/) for autobuild pdf and use [textlint](https://github.com/textlint/textlint), [reviewdog](https://github.com/haya14busa/reviewdog).

- Setup Your Project
- If you use [reviewdog](https://github.com/haya14busa/reviewdog)
  - Set `REVIEWDOG_GITHUB_API_TOKEN` Environment Variable
  - Select "only PullRequest build"
- If you use dropbox upload(master branch only)
  - create access token from [Dropbox Developer](https://www.dropbox.com/developers)
  - Set `DROPBOX_TOKEN` Environment Variable

## HowToUse

Run commands at project root.

- `./bin/pdf` for create pdf.
  - creates `dists/book.pdf`
- `./bin/epub` for create epub.
  - creates `dists/book.epub`
- `./bin/html` for create html pages.
  - creates `docs/*.html`
  - [GitHub Pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/) Available
    - set `master branch /docs folder` for GitHub Pages source
    - ex. https://kokuyouwind.github.io/review-scaffold/
- `./bin/lint` for check textlint.

## EditorSetting

- Use: VSCode
- Extentions: yet another Re:VIEW extension
- GraphTool:
  - gnuplot
    - http://mashiroyuya.hatenablog.com/entry/installgnuplot
  - graphviz
    - https://dev.classmethod.jp/tool/graphviz-beginner/
  - aafigure
    - http://ftparmy.com/198478-aafigure.html
    - ↑ python setup.py install
  - blockdiag
    - pip install blockdiag
