# 블로그

- 블로그 주소 : https://moto6.github.io/hugoblog/
- 블로그 제작기 : (작성중)
- engineering archive

# 글쓰기
```sh
hugo new posts/{{$title}}.md
hugo new posts/.md
```
```sh
hugo new projects/{{$title}}.md
hugo new projects/.md
```

```


hugo new site hugoblog && cd hugoblog
git init

# git submodule add https://github.com/<theme 경로>.git themes/<theme 이름>

git submodule add -f https://github.com/wjh18/hugo-liftoff.git themes/hugo-liftoff


## git submodule add -f https://github.com/binokochumolvarghese/lightbi-hugo themes/lightbi-hugo


# 대충 시도해본것들

## git submodule add https://github.com/CaiJimmy/hugo-theme-stack.git themes/hugo-theme-stack
### 다크모드가 좀 별로인듯..

## git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke && echo "theme = 'ananke'" >> hugo.toml
### 아 뭐랄까.. 너무 흑백흑백 하다랄까?? 뭔가 알록달록한 세상을 모르는 느낌이랄까?

## git submodule add https://github.com/lubang/hugo-hello-programmer-theme themes/hugo-hello-programmer-theme


# blog/public -> <username>.github.io 연결
# git submodule add -b main http://github.com/<username>/<username>.github.io.git public
$ git submodule add -b main -f https://github.com/moto6/blog.git public


# 글쓰기
hugo new posts/my-first-post.md
hugo new projects/test-project.md


# 로컬확인
hugo --config=hugo.toml server -D

```

```
# Simple workflow for deploying static content to GitHub Pages
name: Deploy static content to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
permissions:
  contents: read
  pages: write
  id-token: write

# Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
# However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  # Single deploy job since we're just deploying
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Setup Pages
        uses: actions/configure-pages@v3
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2
        with:
          # Upload entire repository
          path: '.'
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2

```
