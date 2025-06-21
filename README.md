使用Jekyll  从 0 到 1 构建一个网站  并发布到 githubpage

# prepare environment
https://www.ruby-lang.org/en/downloads/

```shell

# for  install ruby
# https://github.com/rbenv/rbenv
brew install rbenv
rbenv install 3.2.2

rbenv global 3.2.2   # set the default Ruby version for this machine
# or:
rbenv local 3.2.2    # set the Ruby version for this directory

gem install bundler
gem install  jekyll
```


# start to build jekyll site

```shell
jekyll new my-awesome-site

cd my-awesome-site

bundle exec jekyll serve

```