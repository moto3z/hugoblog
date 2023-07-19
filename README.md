go

```


hugo new site hugoblog && cd hugoblog
git init




# git submodule add https://github.com/<theme 경로>.git themes/<theme 이름>
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke && echo "theme = 'ananke'" >> hugo.toml

# 안씀 $ git submodule add https://github.com/CaiJimmy/hugo-theme-stack.git themes/hugo-theme-stack



# blog/public -> <username>.github.io 연결
# git submodule add -b main http://github.com/<username>/<username>.github.io.git public
$ git submodule add -b main https://github.com/motrink/blog.git public


# 글쓰기
hugo new posts/my-first-post.md

# 로컬확인
hugo --config=hugo.toml server -D

```
