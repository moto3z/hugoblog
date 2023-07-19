go

```


hugo new site hugoblog && cd hugoblog
git init




# git submodule add https://github.com/<theme 경로>.git themes/<theme 이름>

git submodule add https://github.com/lubang/hugo-hello-programmer-theme themes/hugo-hello-programmer-theme

# 대충 시도해본것들
## git submodule add https://github.com/CaiJimmy/hugo-theme-stack.git themes/hugo-theme-stack
### 다크모드가 좀 별로인듯..
## git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke && echo "theme = 'ananke'" >> hugo.toml
### 아 뭐랄까.. 너무 흑백흑백 하다랄까?? 뭔가 알록달록한 세상을 모르는 느낌이랄까?


# blog/public -> <username>.github.io 연결
# git submodule add -b main http://github.com/<username>/<username>.github.io.git public
$ git submodule add -b main https://github.com/motrink/blog.git public


# 글쓰기
hugo new posts/my-first-post.md

# 로컬확인
hugo --config=hugo.toml server -D

```
