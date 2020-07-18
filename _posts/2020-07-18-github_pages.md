---
layout: post
title: GitHub博客搭建教程 
tags: github git jekyll
categories: productivity
---

# GitHub博客搭建教程
***
> 轻量级、一站式、便于迁移、免费的中小型博客主页搭建工具

## 1. Github Pages生成基本页面
- [*sign up*](github.com) -- chenbige50884@gmail.com
- *new repository*
- *repository name* -- geostrophic.github.io
- *settings&choose a theme* -- Architect
- *commit changes*
- *edit index.md*
## ~~2. 配置自定义域名&HTTPS~~
## 3. Git管理博客内容
```zsh
mkdir github
cd github
git clone https://github.com/geostrophic/geostrophic.github.io
cd geostrophic.github.io
git status
echo xx > index.md
git add -all
git commit -m "Push Again"
git fetch
git rb
git push -u origin master
git config user.email "chenbige50884@gmail.com"
git config user.name "geostrophic"
```
## 4. Jekyll生成博客页面
```zsh
brew install ruby
sudo gem install jekyll bundler
z ge
sudo jekyll new . --force
sudo bundle install
sudo bundle exec jekyll serve
#127.0.0.1:4000
aria2c -d Downloads -c https://github.com/bit-ranger/blog/archive/gh-pages.zip
unzip ~/downloads/blog-gh-pages.zip  
mv ~/downloads/blog-gh-pages/* ~/github/geostrophic.github.io 
sudo bundle lock --add-platform x86-mingw32 x64-mingw32 x86-mswin32 java
sudo gem install jekyll
sudo gem install jekyll-paginate
vi gemfile
#gem 'jekyll-paginate'
sudo bundle
sudo jekyll serve
rm index.markdown
#127.0.0.1:4000
#rake post title="x"

```
<br/>

***
<u>*&copy;2020/7/18 Chen Yuxin. All rights reserved*</u>